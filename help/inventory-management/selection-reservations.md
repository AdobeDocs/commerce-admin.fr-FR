---
title: Algorithmes et réservations Source
description: Découvrez l’algorithme de sélection Source et les systèmes de réservation qui s’exécutent en arrière-plan pour conserver vos quantités vendables à jour.
exl-id: dcd63322-fb4c-4448-b6e7-0c54350905d7
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '2179'
ht-degree: 0%

---

# Algorithmes et réservations Source

Le coeur de [!DNL Inventory Management] effectue le suivi de tous les produits disponibles, virtuellement et en main, dans vos entrepôts et magasins. L’algorithme de sélection et les systèmes de réservation de Source s’exécutent en arrière-plan, ce qui permet de conserver vos quantités vendables à jour, de ne pas subir de collisions et d’options d’expédition recommandées.

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation programmée du système [!DNL Inventory Management], reportez-vous à la [documentation destinée aux développeurs](https://developer.adobe.com/commerce/php/development/framework/inventory-management/).

## Algorithme de sélection Source

L’algorithme de sélection Source (SSA) analyse et détermine la meilleure correspondance pour les sources et l’expédition à l’aide de l’ordre de priorité des sources configurées dans un stock. Lors de l’envoi de commandes, l’algorithme fournit une liste recommandée de sources, de quantités disponibles et de montants à déduire selon l’algorithme sélectionné. [!DNL Inventory Management] fournit un algorithme de priorité et prend en charge les extensions pour les nouvelles options.

Avec plusieurs emplacements sources, des clients globaux et des opérateurs avec différentes options d’expédition et différents frais, connaître votre inventaire réel disponible et trouver la meilleure option d’expédition peut s’avérer difficile. SSA effectue le travail pour vous, depuis le suivi des quantités vendables des stocks de toutes les sources jusqu’au calcul et la recommandation des envois.

**Suivi de l’inventaire** - En utilisant des stocks et des sources, l’ASS vérifie le canal de vente des demandes de produits entrantes et détermine l’inventaire disponible :

- Calcule la quantité virtuelle agrégée de toutes les sources attribuées par stock : agrège Quantité - Seuil hors stock par source
- Enlève le montant du seuil d’rupture de stock à la quantité vendue afin de se protéger contre la vente excessive.
- Réserve les quantités d&#39;inventaire lors de l&#39;envoi de la commande, en les déduisant de l&#39;inventaire en stock lors du traitement des commandes et de l&#39;expédition
- Prend en charge les commandes avec des options améliorées de seuils négatifs

**Gérer les envois** - L’algorithme permet de traiter et d’envoyer des commandes. Vous pouvez exécuter l’algorithme pour obtenir des recommandations sur les meilleures sources d’expédition du produit ou remplacer les sélections sur :

- Livrez des envois partiels, n’envoyez que quelques produits provenant de lieux spécifiques et effectuez la commande complète ultérieurement.
- Livrez la commande entière à partir d’une source
- Ventilez les envois à plusieurs sources en différentes quantités, en conservant un stock équilibré dans tous les entrepôts et magasins.

SSA est extensible pour une prise en charge tierce et des algorithmes personnalisés pour recommander des envois rentables.

>[!NOTE]
>
>SSA fonctionne différemment pour les produits virtuels et téléchargeables, ce qui peut ne pas entraîner de frais d’expédition. Dans ce cas, le système exécute implicitement l’algorithme lorsqu’il crée des factures et utilise toujours les résultats suggérés. Vous ne pouvez pas ajuster ces résultats pour les produits virtuels et téléchargeables.

### Algorithme de priorité Source

Les stocks personnalisés comprennent une liste attribuée de sources à vendre et à expédier l’inventaire des produits disponibles via votre vitrine. L’algorithme de priorité Source utilise l’ordre des sources affectées dans le stock pour recommander des déductions de produit par source lors de la facturation et de l’expédition de la commande.

Lors de l’exécution, l’algorithme :

- Fonctionne par l’ordre configuré des sources au niveau du stock, en commençant par le haut
- Recommande une quantité à envoyer et une source par produit en fonction de la commande dans la liste, de la quantité disponible et de la quantité commandée.
- Continue la liste jusqu’à ce que la commande d’envoi soit remplie
- Ignore les sources désactivées si elles figurent dans la liste.

Pour configurer, affecter et commander des sources à un stock personnalisé. Voir [Hiérarchisation des sources pour un stock](stocks-prioritize-sources.md).

L’exemple suivant présente les sources mappées dans l’ordre, la quantité disponible, la source recommandée et le montant à déduire et à expédier. La source principale est un Drop Shipper au Royaume-Uni avec une quantité disponible de 240.

![Exemple de recommandations SSA pour un vélo tout terrain](assets/ssa-sources-example.png){width="600" zoomable="yes"}

### Algorithme de priorité des distances

L’algorithme de priorité des distances compare l’emplacement de l’adresse de destination de livraison aux emplacements sources afin de déterminer la source la plus proche pour accomplir les chargements. La distance peut être déterminée par la distance physique ou le temps passé d’un emplacement à un autre, à l’aide d’emplacements de base de données importés ou de directions Google (conduite, marche ou vélo).

Vous disposez de deux options pour calculer la distance et le temps afin de trouver la source la plus proche pour l’exécution de l’expédition :

- **Google MAP** - Utilise les services [Google Maps Platform][1] pour calculer la distance et l&#39;heure entre l&#39;adresse de destination d&#39;expédition et les emplacements source (adresse et coordonnées GPS). Cette option utilise la latitude et la longitude de la source. Une clé d’API Google est requise avec [l’API Geocoding][2] et l’ [ API Distance Matrix][3] activée. Cette option nécessite un plan de facturation Google et peut entraîner des frais via Google.

- **Calcul hors ligne** - Calcule la distance à l’aide des données de géocode téléchargées et importées pour déterminer la source la plus proche de l’adresse de destination de livraison. Cette option utilise les codes pays de l’adresse et de la source d’expédition. Pour configurer cette option, vous pouvez avoir besoin de l’aide du développeur pour télécharger et importer des géocodes à l’aide d’une ligne de commande.

Pour configurer, sélectionnez des configurations et effectuez d’autres étapes, telles que la clé de l’API Google ou le téléchargement des données d’expédition. Voir [Configuration de l’algorithme de priorité des distances](distance-priority-algorithm.md).

### Algorithmes personnalisés

[!DNL Commerce] prend en charge le développement personnalisé et les extensions pour ajouter d’autres algorithmes afin de prioriser les sources. Par exemple, vous pouvez avoir un algorithme de priorité basé sur la géographie et un autre basé sur les frais du stock ou un attribut du client. Lorsque le coût du stock change, votre mise en oeuvre peut facilement modifier les algorithmes pour garantir le coût le plus faible.

## Réservations

Au lieu de déduire ou d’ajouter immédiatement des quantités d’inventaire de produits, les réservations conservent des quantités d’inventaire jusqu’à l’envoi ou l’annulation des commandes. Les réservations fonctionnent entièrement en arrière-plan pour mettre automatiquement à jour votre quantité vendable au niveau du stock.

>[!NOTE]
>
>La fonctionnalité de réservation nécessite que le client de file d’attente de messages `inventory.reservations.updateSalabilityStatus` s’exécute en continu. Pour vérifier s’il est en cours d’exécution, utilisez la commande `bin/magento queue:consumers:list` . Si le consommateur de la file de messages n&#39;est pas répertorié, démarrez-le : `bin/magento queue:consumers:start inventory.reservations.updateSalabilityStatus`.

### Réservations des commandes

Les réservations sont conservées sur les quantités d&#39;inventaire déduites de la quantité vendable lors de la soumission d&#39;une commande. Les réservations sont au niveau du stock, en comptant les quantités jusqu&#39;à ce que la commande soit facturée et expédiée, annulée, etc. Lors de l’expédition de la commande, vous pouvez utiliser les recommandations SSA ou saisir manuellement les déductions de quantité par source. Une fois expédiées, les réservations sont automatiquement effacées et la quantité déduite. La quantité vendable est recalculée pour le stock avec une quantité mise à jour et les montants de réservation restants dans le système.

Le diagramme suivant permet de définir le processus de réservation lors d&#39;une commande et jusqu&#39;à l&#39;expédition.

![Réservations de la commande à la diffusion](assets/diagram-quantity.png){width="600" zoomable="yes"}

Un client envoie une commande. [!DNL Commerce] vérifie la quantité actuelle pouvant être vendue dans l’inventaire. Si un stock suffisant est disponible au niveau du stock, une réservation entre en place une suspension temporaire pour le SKU du produit (pour ce stock) et recalcule la quantité vendable.

Une fois la commande facturée, vous déterminez le produit à déduire et à expédier à partir de vos sources. L&#39;envoi est traité et envoyé d&#39;une ou plusieurs sources sélectionnées au client. Les quantités sont automatiquement déduites de la quantité de stock source et les réservations sont effacées. Pour obtenir des détails et des exemples complets, voir [À propos de l’état de la commande et des réservations](order-status.md).

## Calculs de réservation

Le système crée une réservation pour chaque produit lorsque les événements suivants se produisent :

- Un client ou un commerçant commande.
- Un client ou un commerçant annule entièrement ou partiellement une commande.
- Le marchand crée une cargaison pour un produit physique.
- Le marchand crée une facture pour un produit virtuel ou téléchargeable.
- Le commerçant émet un avis de crédit.

Les réservations sont des opérations d’ajout unique, comme un journal d’événements. Une valeur de quantité négative est affectée à la réservation initiale. Toutes les réservations créées ultérieurement lors du traitement de la commande sont des valeurs positives. Une fois la commande terminée, la somme de toutes les réservations pour le produit est de 0.

Avant que le système puisse émettre une réservation en réponse à une nouvelle commande, il détermine s’il existe suffisamment d’éléments pouvant être vendus pour répondre à la commande. Les quantités prises en compte dans le calcul sont les suivantes :

- **Quantité StockItem**. La quantité StockItem est la quantité agrégée de l’inventaire provenant de toutes les sources physiques du canal de ventes actuel. Prenons un exemple où la source Baltimore possède 20 unités de produit, la source Austin 25 unités du même produit et la source Reno 10. Lorsque toutes ces sources sont liées au stock A, le stockItem de ce produit est 55 (20 + 25 + 10). (Lorsque des articles sont expédiés, l’indexeur d’inventaire met à jour les quantités disponibles pour chaque source.)

- **Réservations en attente**. Le système totalise toutes les réserves initiales qui n&#39;ont pas été indemnisées. Ce nombre est toujours négatif. Si le client A a réservé dix articles et que le client B a réservé 5 articles, alors les réservations exceptionnelles pour le produit total -15.

Par conséquent, le marchand peut répondre à une commande entrante tant que le client commande moins de 40 (55 + -15) unités.

Lorsque vous terminez le traitement d’une commande (Terminé, Annulé, Fermé), toutes les réserves dans la portée de cette commande doivent être résolues sur `0`. Cela efface toutes les quantités pouvant être vendues.

>[!NOTE]
>
>Les paramètres d’arrière-plan (avec des seuils en rupture de stock) et de notification pour la quantité inférieure au seuil affectent également le calcul des quantités vendables, mais ils ne sont pas compris dans le cadre de cette rubrique. Pour plus d&#39;informations sur ces paramètres, voir [Configuration [!DNL Inventory Management]](./configuration.md).

## Objets de réservation

Une réservation contient les informations suivantes :

| Paramètre | Type de données | Description |
| --- | --- | --- |
| `reservation_id` | Entier | ID généré par le système |
| `stock_id` | Entier | ID du stock auquel le produit est affecté |
| `sku` | Chaîne | SKU du produit |
| `quantity` | Flottant | Le nombre d’éléments dans cette réservation |
| `metadata` | Chaîne | Type d’événement, type d’objet et ID d’objet pour cette réservation. Par exemple, `{"event_type":"order_placed","object_type":"order",| "object_id":"8"}` |

{style="table-layout:auto"}

Les métadonnées `event_type` peuvent avoir les valeurs suivantes :

- `order_placed`
- `order_canceled`
- `shipment_created`
- `creditmemo_created`
- `invoice_created`

Actuellement, le type d’objet de métadonnées doit être `order` et l’ID d’objet est l’ID de commande.

Dans les prochaines versions, il sera peut-être possible de créer une réservation lorsqu’un client ajoute un article à un panier. Chaque article peut être réservé pendant une durée fixe (15 minutes, par exemple), ce qui permet au client de réserver des articles tout en continuant à faire ses achats. Lorsque ce type de réservation est activé, les métadonnées peuvent contenir des types d’informations supplémentaires.

## Cycle de vie de la réservation

L’exemple suivant illustre la séquence des réservations générées pour une commande simple.

1. Le client effectue une commande pour 25 unités du produit `SKU-1`. La réservation contient les informations suivantes :

   ```text
   reservation_id = 1
   stock_id = 1
   sku = SKU-1
   quantity = -25
   event_type = order_placed
   ```

1. Le client envoie une facture pour 20 articles, annulant pour l&#39;essentiel 5 des unités commandées.

   ```text
   reservation_id = 2
   stock_id = 1
   sku = SKU-1
   quantity = 5
   event_type = order_canceled
   ```

1. Le marchand expédie les 20 unités achetées.

   ```text
   reservation_id = 3
   stock_id = 1
   sku = `SKU-1`
   quantity = 20
   event_type = shipment_created
   ```

Les trois valeurs `quantity` totalisent 0 (-25 + 5 + 20). Le système ne modifie aucune réservation existante.

## Suppression des réservations traitées

La tâche cron `inventory_cleanup_reservations` exécute des requêtes SQL pour effacer la table de la base de données de réservation. Par défaut, il s’exécute tous les jours à minuit, mais vous pouvez configurer les heures et la fréquence. La tâche cron exécute un script qui interroge la base de données afin de trouver des séquences de réservation complètes dans lesquelles la somme des valeurs de quantité est 0. Lorsque toutes les réservations pour un produit donné qui a été émis le même jour (ou à une autre heure configurée) ont été indemnisées, la tâche cron supprime toutes les réservations en même temps.

La tâche cron `inventory_reservations_cleanup` n’est pas la même que le consommateur de file d’attente de messages `inventory.reservations.cleanup`. Le consommateur supprime de manière asynchrone les réservations par SKU de produit après la suppression d’un produit, tandis que la tâche cron efface la table complète des réservations. Le consommateur est requis lorsque vous activez l’option de stock [**Synchroniser avec le catalogue**](../configuration-reference/catalog/inventory.md) dans la configuration du magasin. Voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_.

Souvent, toutes les réserves initiales produites en une seule journée ne peuvent être indemnisées ce même jour. Cette situation peut se produire lorsqu’un client passe une commande juste avant que la tâche cron ne commence ou effectue l’achat avec un mode de paiement hors ligne, tel qu’un transfert bancaire. Les séquences de réservation compensées restent dans la base de données jusqu’à ce qu’elles soient toutes indemnisées. Cette pratique n’interfère pas avec les calculs de réservation, car le total de chaque réservation est de 0.

>[!NOTE]
>
>Il existe des commandes d’interface de ligne de commande que vous pouvez utiliser pour détecter et gérer les incohérences de réservation (voir la [[!DNL Inventory Management] référence d’interface de ligne de commande](cli.md)).

### Mises à jour des réservations

Lorsque les modifications sont terminées dans les commandes et les quantités de produits, [!DNL Commerce] entre automatiquement les compensations de réservation. Vous n’avez pas besoin de renseigner des compensations par le biais de l’administrateur ou du code pour mettre à jour ou effacer ces retenues. Les réservations ne sont concernées que par les réservations entrées pour mettre une réserve sur une quantité ou pour effacer un montant de la retenue (qui compensent les réservations).

Voici comment ils fonctionnent :

- **Commande envoyée** - Lorsqu’une commande est envoyée pour plusieurs produits, une réservation entre pour ce montant. Par exemple, la commande de cinq sacs à dos à partir d’un site web américain entraîne la réservation de `-5` pour ce SKU et ce stock. La quantité vendable est réduite de 5.

- **Annulation de la commande** - Lorsqu’une commande est annulée (totale ou partielle), une réservation de compensation entre en vigueur pour effacer ce montant. Par exemple, l’annulation de trois packs sauvegarde une réservation de +3 pour ce SKU et ce stock, en vidant la suspension. La quantité vendable est augmentée de 3.

- **Commande expédiée** - Lorsqu’une commande est expédiée (partielle ou totale), une réservation de compensation entre en vigueur pour effacer ce montant. Par exemple, l’expédition de deux packs d’arrière-plan entre dans une réservation +2 pour ce SKU et ce stock, en effaçant la suspension. La quantité du produit est directement réduite de 2 pour l&#39;expédition. La quantité calculée pouvant être vendue est également mise à jour pour le montant réduit du stock, mais n&#39;est plus affectée par la réservation.

![ Mises à jour de réservation](assets/diagram-reservation.png){width="600" zoomable="yes"}

Toutes les réservations doivent faire l&#39;objet d&#39;une compensation lorsque les commandes sont réalisées, que les produits sont annulés, que des notes de crédit sont émises, etc. Si les compensations n&#39;effacent pas les réservations, vous pourriez avoir des quantités gardées en stase (non disponibles à la vente et jamais à la livraison).

>[!NOTE]
>
>Si vous souhaitez examiner les réservations, une série d’options de ligne de commande sont disponibles. Vous pouvez uniquement passer en revue les réservations via une interface de ligne de commande. L’utilisation de commandes de l’interface de ligne de commande peut nécessiter une aide du développeur. Voir [[!DNL Inventory Management] Référence de l’interface de ligne de commande](cli.md).

Si vous supprimez toutes les sources d’un produit pour un stock avec des commandes en attente, vous avez peut-être bloqué les réservations.

{{$include /help/_includes/unassign-source.md}}

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
