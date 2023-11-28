---
title: Gérer les commandes et les envois à partir du stock
description: En savoir plus sur les [!DNL Inventory Management] fonctionnalités et options pour gérer les quantités d’inventaire tout au long du processus d’expédition.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Gestion des commandes et des envois

[!DNL Inventory Management] comprend des fonctionnalités et options supplémentaires pour gérer les quantités d’inventaire par le biais du processus d’expédition. Au fur et à mesure que vous passez en revue et réalisez des envois, annulez les commandes et émettez des avis de crédit, la vente de produits et les quantités disponibles sont automatiquement mises à jour.

Ces informations incluent des détails spécifiques pour [!DNL Inventory Management]. Pour plus d’informations, voir [Commandes](../stores-purchase/orders.md){target="_blank"} dans la section _Guide d’expérience des ventes et des achats_.

## Commandes

[!DNL Commerce] prend en charge les commandes uniques et les commandes multi-adresses prêtes à l’emploi sans configurations supplémentaires. Lorsque les clients ou le personnel entrent des commandes, [!DNL Inventory Management] effectue le suivi de l’inventaire à l’aide de réservations pour la quantité vendable, en déduisant de la quantité de l’inventaire pour les produits facturés et expédiés.

### Commandes à plusieurs adresses

Pour les commandes à plusieurs adresses, une série de commandes uniques est générée, une pour chaque adresse de destination renseignée. Lors du passage en caisse, les clients sélectionnent chaque ensemble de produits associés par adresse lors du passage en caisse généré sous la forme de commandes uniques en fonction de l’adresse de destination. Chaque commande inclut les produits associés par adresse.

[!DNL Commerce] gère l’inventaire de ces commandes à plusieurs adresses exactement comme les commandes uniques. Il permet de recommander l’algorithme de sélection de la source ou de remplacer les données pendant l’expédition, les envois partiels, l’annulation des commandes et le refinancement avec les mises à jour du stock.

![Multi-adresses lors du passage en caisse](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Remboursement

Lorsque vous saisissez une [note de crédit](../stores-purchase/credit-memo-create.md){target="_blank"} pour effectuer un remboursement, vous pouvez renvoyer la quantité du produit à la source déduite. Les informations sur la commande incluent la source de l’inventaire qui a expédié le produit. Il est recommandé d’attribuer la quantité de produit renvoyée par le biais d’une note de crédit lors de la réception du produit renvoyé.

![Éléments à rembourser avec retour à la sélection Stock](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Annuler les commandes non expédiées

Si une commande n’a pas été expédiée et est annulée (en totalité ou partiellement), [!DNL Inventory Management] renvoie automatiquement le stock de produit à la quantité vendable. Jusqu&#39;à la facture et l&#39;expédition, les produits achetés sont réservés sur la quantité vendable, et non déduits de la quantité réelle. Au moment de la facturation et de l&#39;envoi de la commande, le système convertit la réservation en une déduction d&#39;inventaire.

En coulisses, [!DNL Inventory Management] saisit automatiquement une réservation de compensation supprimant la suspension sur la quantité de produit. La quantité est renvoyée à la quantité vendue virtuelle agrégée.

## Expéditions

Avec [!DNL Inventory Management] activée, vous pouvez envoyer des envois partiels ou complets depuis une ou plusieurs sources pour exécuter les commandes. Vous contrôlez votre inventaire sortant pour chaque commande, définissez les montants à déduire, envoyez une ou plusieurs cargaisons et effectuez un envoi en stock et en amont lorsque le stock est disponible. Pour chaque élément de ligne de la commande, saisissez un montant à déduire de la quantité source. Générez une expédition par source, car vous disposez d’un stock de stocks, jusqu’à ce que la commande entière soit satisfaite.

### Transferts partiels

Pour les marchands multisource, [!DNL Commerce] génère une expédition pour chaque source que vous sélectionnez. Le workflow général vous permet de sélectionner une source, de définir la quantité de produits à déduire pour respecter la commande et de passer à l’envoi. Une fois la commande terminée, créez des envois supplémentaires pour chaque source jusqu’à ce que vous ayez respecté la commande.

Les commerçants à source unique peuvent également envoyer des envois partiels pour soutenir les commandes en amont ou équilibrer l’inventaire au fur et à mesure que les commandes arrivent pour les articles les plus populaires.

### Algorithme de sélection de source et Recommendations

La variable [Algorithme de sélection de source](selection-reservations.md) (SSA) fournit des recommandations pour les envois complets et partiels. Vous pouvez accéder aux algorithmes de sélection de source lors de la création de factures d’expédition pour une commande. Sur la page Ship, exécutez à tout moment l’algorithme Priorité de la source ou Priorité de la distance pour déterminer les meilleures options pour faire correspondre les quantités commandées et les sources disponibles. Le système prend en charge l’expédition d’une commande complète à partir d’une source et la rupture de la commande en plusieurs envois partiels sur plusieurs sources. Vous pouvez accéder à ces options pour une exécution immédiate et des envois échelonnés afin d’envoyer des quantités moindres au fil du temps.

Pour terminer et envoyer une commande, elle doit avoir effectué le paiement et être facturée. Actuellement, vous pouvez réexécuter le contrat SSA pour les recommandations et l’envoyer à partir d’une ou de plusieurs sources, ou remplacer les recommandations du contrat SSA par des sources et des quantités définies manuellement pour satisfaire l’envoi.

- Il est recommandé de réexécuter le SSA pour examiner les recommandations pour chaque envoi.

- Si vous souhaitez modifier les sélections, vous pouvez remplacer les déductions à la source manuelles.

### Expéditions et réservations

À mesure que les envois se produisent, les réservations de produits sont vidées et la quantité de produits est déduite. La quantité disponible par stock est mise à jour en fonction des détails de l&#39;envoi. Par exemple, si vous envoyez des envois pour dix produits provenant de deux sources, les quantités pour ces sources déduisent 10 chacun. La Quantité vendable actualise automatiquement les stocks associés, fournissant aux clients et au personnel les dernières quantités de produits. Et les réserves sont claires, ne comptant plus sur la Quantité commercialisable.
