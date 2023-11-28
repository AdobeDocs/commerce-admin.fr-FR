---
title: '''[!DNL Inventory Management] Référence de ligne de commande"'
description: En savoir plus sur les commandes fournies par le [!DNL Inventory Management] pour gérer les données d’inventaire et les paramètres de configuration.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] Référence de ligne de commande

[!DNL Inventory Management] fournit des commandes pour gérer les données d’inventaire et les paramètres de configuration.

Ces commandes comprennent :

- Vérification et résolution des incohérences de réservation affectant la quantité vendable
- Ajout de géocodes pour l’algorithme Priorité de distance

## Résoudre les incohérences des réservations

Les réservations placent une quantité vendable en attente pour les SKU de produit par stock. Lorsque vous expédiez, ajoutez des produits, annulez ou remboursez une commande, les réservations de compensation vous permettent de les placer ou de les effacer.

[!DNL Inventory Management] fournit deux commandes pour vérifier et résoudre les incohérences de réservation :

- [`inventory:reservation:list-incohérences`](#list-inconsistencies-command)
- [`inventory:reservation:créer des compensations`](#create-compensations-command)

### Causes d’incohérences de réservation

[!DNL Inventory Management] génère des réservations pour les événements clés :

- Emplacement de la commande (réservation initiale)
- Envoi des commandes (réservation de compensation)
- Rembourser une commande ou émettre un avoir (réservation de compensation)
- Annulation de commande (réservation de compensation)

Des incohérences de réservation peuvent se produire dans les cas suivants :

- [!DNL Inventory Management] perd la réservation initiale et engage trop de compensations de réservation (surcompensant et entraînant des montants incohérents)
- [!DNL Inventory Management] place correctement la réservation initiale, mais perd les réservations compensatoires.

Vous pouvez manuellement vérifier et vérifier les réservations dans la variable `inventory_reservation` table.

Les configurations et événements suivants peuvent provoquer des incohérences de réservation :

- **Effectuez la mise à niveau vers la version 2.3.x avec des commandes qui ne sont pas à l’état final (Terminé, Annulé ou Fermé).** [!DNL Inventory Management] crée des réserves compensatoires pour ces commandes, mais elle n&#39;entre pas ou n&#39;a pas la réserve initiale qui déduise de la quantité vendable. Il est recommandé d’utiliser ces commandes après la mise à niveau vers Adobe Commerce ou Magento Open Source v2.3.x à partir de 2.1.x ou 2.2.x. Si vous avez des commandes en attente, les commandes mettent correctement à jour votre quantité vendable et les réservations pour les ventes et l’exécution des commandes.
- **Vous ne gérez pas le stock, puis modifiez ultérieurement cette configuration.** Vous pouvez commencer à utiliser la version 2.3.x avec **[!UICONTROL Manage Stock]** défini sur `No` dans la configuration. [!DNL Commerce] ne place pas de réservation lors des événements de placement et d’expédition de commande. Si vous activez le paramètre **[!UICONTROL Manage Stock]** et que certaines commandes sont créées, la qualité vendable serait corrompue avec une réservation de compensation lorsque vous traiterez et honorerez cette commande.
- **Vous réaffectez le stock d’un site web pendant que les commandes sont envoyées à ce site web.**. La réservation initiale porte sur le stock initial et toutes les réserves de compensation entrent dans le nouveau stock.
- **Le total de toutes les réserves peut ne pas se résoudre à `0`.** Toutes les réserves dans le cadre d’une commande dans un état final (Complète, Annulée, Fermée) doivent se résoudre à `0`, effacer toutes les quantités pouvant être vendues.

### Liste des incohérences, commande

La variable `list-inconsistencies` détecte et répertorie toutes les incohérences des réservations. Utilisez les options de commande pour vérifier uniquement les commandes terminées ou incomplètes, ou toutes.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Options de commande :

- `-c`, `--complete-orders` - Renvoie les incohérences des commandes terminées. Des réservations incorrectes peuvent toujours être suspendues pour les commandes terminées.
- `-i`, `--incomplete-orders` - Renvoie des incohérences pour les commandes incomplètes (partiellement expédiées, non expédiées). Les réservations incorrectes peuvent contenir trop ou pas assez de quantité vendue pour les commandes.
- `-b`, `--bunch-size` - Définit le nombre de commandes à charger simultanément.
- `-r`, `--raw` - Sortie brute.

Réponses utilisant `-r` return in `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` format :

- L’ID de commande indique la portée de l’incohérence.
- Le SKU indique que le produit est incohérent.
- Quantity définit le montant à renseigner pour la compensation de réservation.
- L’identifiant de stock définit la portée du stock, qui utilise les réserves pour calculer la quantité vendable.

Exemples:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Si aucun problème n’est détecté, ce message renvoie : Aucune incohérence de commande n’a été trouvée.

### Créer des compensations, commande

La variable `create-compensations` crée des réserves de compensation. En fonction du problème, de nouvelles réservations sont créées pour placer ou libérer une réserve sur la quantité vendable.

Pour créer des réservations, effectuez des compensations au format `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` par exemple `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Option de commande :

- `-r`, `--raw` - Renvoie la sortie brute.

Si le format de la requête est incorrect, le message suivant s’affiche :

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Lorsque la commande crée des réservations, elle affiche des messages indiquant les mises à jour par SKU, commande et stock.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Si le SKU d’une entrée de compensation inclut des espaces, placez le SKU entre guillemets.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Détecter les incohérences et créer des compensations

Vous pouvez détecter des incohérences et créer immédiatement des compensations en utilisant une barre verticale pour exécuter les deux `list-inconsistencies` et `create-compensations`. Utilisez la variable `-r` l’option de commande pour générer et envoyer les données brutes à `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Exemple de réponse :

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Une fois les mises à jour terminées, exécutez la commande list pour vérifier :

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

Vous pouvez également piloter les commandes pour détecter les incohérences et créer des compensations pour uniquement les incomplètes (`-i`) ou complete (`-c`) les commandes.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importer des géocodes

[!DNL Inventory Management] fournit la variable [Algorithme Priorité de distance](distance-priority-algorithm.md), qui permet de déterminer la meilleure option pour l’expédition d’une commande complète ou partielle. L’algorithme utilise des informations GPS ou des codes géographiques pour calculer la distance entre la source (un entrepôt ou un autre emplacement physique) de chaque article dans une commande et l’adresse de livraison. En fonction de ces résultats, l’algorithme recommande la source à utiliser pour expédier chaque élément dans la commande.

Le marchand sélectionne le fournisseur des données GPS ou géocode nécessaires au calcul des distances :

- **CARTE GOOGLE** uses [Plateforme Google Maps](https://mapsplatform.google.com/) services permettant de calculer la distance et l’heure entre l’adresse de destination de livraison et les emplacements sources. Cette option nécessite un plan de facturation Google et peut entraîner des frais via Google.

- **Calcul hors ligne** calcule la distance en utilisant les données téléchargées à partir de [geonames.org](https://www.geonames.org/) et importé dans Commerce à l’aide d’une commande . Cette option est gratuite.

Pour importer des géocodes pour le calcul hors ligne :

Saisissez la commande suivante avec une liste séparée par des espaces de [Codes de pays ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Par exemple :

```bash
bin/magento inventory-geonames:import us ca gb de
```

Le système télécharge et importe les données de géocode dans votre base de données, puis affiche le message.  `Importing <country code>: OK`.
