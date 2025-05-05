---
title: Référence de l’interface de ligne de commande [!DNL Inventory Management]
description: Découvrez les commandes fournies par le module  [!DNL Inventory Management]  pour gérer les données d’inventaire et les paramètres de configuration.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Référence de l’interface de ligne de commande [!DNL Inventory Management]

[!DNL Inventory Management] fournit des commandes pour gérer les données d’inventaire et les paramètres de configuration.

Ces commandes sont les suivantes :

- Vérification et résolution des incohérences de réservation affectant la quantité commercialisable
- Ajout de géocodes pour l&#39;algorithme Distance Priority

## Résoudre les incohérences des réservations

Les réservations placent un blocage de quantité vendable pour les SKU de produit par stock. Lorsque vous expédiez, ajoutez des produits, annulez ou remboursez une commande, les réservations de rémunération sont entrées pour placer ou effacer ces blocages.

[!DNL Inventory Management] fournit deux commandes pour vérifier et résoudre les incohérences de réservation :

- [`inventory:reservation:list-inconsistencies`](#list-inconsistencies-command)
- [`inventory:reservation:create-compensations`](#create-compensations-command)

### Causes des incohérences des réservations

[!DNL Inventory Management] génère des réservations pour les événements clés :

- Passation de commande (réservation initiale)
- Livraison de commande (réservation de rémunération)
- Commande de remboursement ou émission d&#39;un avoir (réservation de rémunération)
- Annulation de commande (réservation de rémunération)

Des incohérences de réservation peuvent se produire lorsque :

- [!DNL Inventory Management] perd la réservation initiale et enregistre un trop grand nombre de compensations (surcompensation et incohérence des montants)
- [!DNL Inventory Management] place correctement la réservation initiale, mais perd les réservations compensatoires.

Vous pouvez vérifier et vérifier manuellement les réservations dans la table `inventory_reservation`.

Les configurations et événements suivants peuvent entraîner des incohérences de réservation :

- **Mise à niveau vers la version 2.3.x avec les commandes non dans un état final (Terminé, Annulé ou Fermé).** [!DNL Inventory Management] crée des réservations compensatoires pour ces commandes, mais elle ne saisit pas ou ne possède pas la réservation initiale qui déduit de la quantité vendable. Il est recommandé d’utiliser ces commandes après la mise à niveau vers Adobe Commerce ou Magento Open Source v2.3.x à partir de la version 2.1.x ou 2.2.x. Si vous avez des commandes en attente, les commandes mettent correctement à jour votre quantité vendable et vos réservations pour les ventes et l&#39;exécution des commandes.
- **Vous ne gérez pas le stock, puis modifiez cette configuration par la suite.** Vous pouvez commencer à utiliser 2.3.x avec **[!UICONTROL Manage Stock]** défini sur `No` dans la configuration. [!DNL Commerce] n&#39;effectue pas de réservations lors des événements de placement de commande et d&#39;expédition. Si vous activez par la suite la configuration **[!UICONTROL Manage Stock]** et que certaines commandes sont créées, la Qté vendable est altérée avec réservation de rémunération lorsque vous traitez et exécutez cette commande.
- **Vous réaffectez les stocks d’un site web pendant que les commandes y sont envoyées**. La réservation initiale entre pour le stock initial et toutes les réservations de rémunération entrent pour le nouveau stock.
- **Le total de toutes les réserves peut ne pas se résoudre à `0`.** Toutes les réservations dans le cadre d&#39;une commande dans un état final (Terminé, Annulé, Fermé) doivent être résolues sur `0`, effaçant tous les blocages de quantité vendable.

### Commande Liste des incohérences

La commande `list-inconsistencies` détecte et répertorie toutes les incohérences de réservation. Utilisez les options de commande pour vérifier uniquement les commandes terminées ou incomplètes, ou toutes.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Options de commande :

- `-c`, `--complete-orders` - Renvoie les incohérences pour les commandes terminées. Les réservations incorrectes peuvent toujours être suspendues pour les commandes terminées.
- `-i`, `--incomplete-orders` - Renvoie les incohérences pour les commandes incomplètes (partiellement expédiées, non expédiées). Des réservations incorrectes peuvent contenir une quantité de vente trop importante ou insuffisante pour les commandes.
- `-b`, `--bunch-size` - Définit le nombre de commandes à charger simultanément.
- `-r`, `--raw` - Sortie brute.

Réponses utilisant `-r` retour au format `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` :

- L’ID de commande indique l’étendue de l’incohérence.
- Le SKU indique le produit avec l’incohérence.
- Quantité définit le montant à saisir pour la compensation de la réservation.
- L&#39;ID stock définit la portée du stock, qui utilise les réservations pour calculer la quantité vendable.

Exemples :

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Si aucun problème n’est identifié, ce message indique : Aucune incohérence de commande n’a été trouvée.

### Créer des compensations, commande

La commande `create-compensations` crée des réservations de rémunération. En fonction du problème, de nouvelles réservations sont créées pour placer ou lever un blocage sur la quantité à vendre.

Pour créer des réservations, fournissez des rémunérations en utilisant le format `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` tel que `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Option de commande :

- `-r`, `--raw` - Renvoie la sortie brute.

Si le format de la requête est incorrect, le message suivant s’affiche :

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Lorsque la commande crée des réservations, elle affiche des messages indiquant les mises à jour par SKU, commande et stock.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Si le SKU d&#39;une entrée de rémunération comprend des espaces, placez-le entre guillemets.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Détecter les incohérences et créer des compensations

Vous pouvez détecter des incohérences et créer immédiatement des compensations à l&#39;aide d&#39;une barre verticale pour exécuter les `list-inconsistencies` et les `create-compensations`. Utilisez l’option de commande `-r` pour générer et envoyer les données brutes à `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Exemple de réponse :

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Une fois les mises à jour terminées, exécutez la commande list pour vérifier :

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

Vous pouvez également diriger les commandes pour détecter les incohérences et créer des compensations pour les commandes incomplètes (`-i`) ou complètes (`-c`) uniquement.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importer des géocodes

[!DNL Inventory Management] fournit l&#39;algorithme [Distance Priority](distance-priority-algorithm.md), qui permet de déterminer la meilleure option pour expédier une commande complète ou partielle. L&#39;algorithme utilise des informations GPS ou des géocodes pour calculer la distance entre la source (un entrepôt ou autre emplacement physique) de chaque article dans une commande et l&#39;adresse d&#39;expédition. Sur la base de ces résultats, l’algorithme recommande la source à utiliser pour expédier chaque article dans la commande.

Le commerçant sélectionne le fournisseur des données GPS ou géocode nécessaires au calcul des distances :

- **Google MAP** utilise les services de [Google Maps Platform](https://mapsplatform.google.com/) pour calculer la distance et le temps entre l’adresse de destination d’expédition et les emplacements sources. Cette option nécessite un plan de facturation Google et peut entraîner des frais via Google.

- Le **Calcul hors ligne** calcule la distance à l’aide des données téléchargées à partir de [geonames.org](https://www.geonames.org/) et importées dans Commerce avec une commande . Cette option est gratuite.

Pour importer des géocodes pour le calcul hors ligne :

Saisissez la commande suivante avec une liste séparée par des espaces de [codes de pays ISO-3166 alpha-2](https://www.geonames.org/countries/) :

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Par exemple :

```bash
bin/magento inventory-geonames:import us ca gb de
```

Le système télécharge et importe les données de géocodes dans votre base de données, puis affiche le message `Importing <country code>: OK`.
