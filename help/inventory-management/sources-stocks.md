---
title: Stocks et sources
description: Découvrez les relations entre les produits, les sources et les stocks.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Stocks et sources

Gérez votre inventaire quel que soit l’emplacement de l’entrepôt, le type de produit, de service ou le canal de vente. Exécutez les commandes et expédiez les produits à partir de plusieurs entrepôts, magasins de briques et de mortiers, centres de distribution et abandonnez les commandes pour terminer les commandes en mettant l’accent sur un inventaire équilibré, les coûts de livraison, etc.

Ces descriptions incluent des produits, des sources et des stocks pour une société de vélos avec plusieurs sites Web et emplacements d’expédition aux États-Unis et en Europe.

## Sources

Les [sources](sources-manage.md) sont les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes ou où des services sont disponibles. Il peut s&#39;agir d&#39;entrepôts, de magasins en briques et de mortiers, de centres de distribution et d&#39;expéditeurs. [!DNL Commerce] utilise les quantités et les quantités vendables par stock et gère automatiquement les quantités d&#39;inventaire pour les produits gérés et les commandes. Si vous disposez d’une source, vous êtes considéré en mode _mono-source_. Si vous disposez de plusieurs sources, vous êtes considéré en mode _multi-source_.

Une source peut avoir la priorité dans le champ de stock d&#39;un entrepôt, mais pas nécessairement dans tous les entrepôts, car la source peut être réutilisée dans différents stocks. Le nombre de stocks et de sources ajoute à la complexité de la détermination du meilleur entrepôt ou magasin pour répondre à une commande. Par exemple, vous disposez peut-être d’un nombre limité de produits provenant de vos emplacements en briques et mortiers, avec un stock important dans vos entrepôts et services, dans des endroits clés, avec une disponibilité limitée.

Dans cet exemple, le marchand dispose d&#39;un vélo tout-terrain disponible pour l&#39;expédition à partir de magasins, d&#39;entrepôts et d&#39;un chargeur de débarquement.

![Exemple de diagramme de sources](assets/diagram-sources.png){width="600" zoomable="yes"}

## Stocks

[Stocks](stocks-manage.md) représente un inventaire virtuel agrégé de produits disponibles à la vente à vos canaux de vente (sites web). Chaque stock met en correspondance vos canaux de vente avec les sources des stocks disponibles et les quantités vendables. Selon la configuration de votre site, le stock peut être affecté à un ou plusieurs canaux et sources de vente.

Les Sales Channel représentent les entités qui vendent votre inventaire, notamment les sites web, les vues de magasins, les groupes de clients B2B, etc. Les canaux de vente ne peuvent être associés qu’à un seul stock. Un seul stock peut être affecté à chaque canal de vente, et un seul stock peut être affecté à plusieurs sites web. Grâce au stock, vous pouvez modifier la hiérarchisation des sources utilisées lors des commandes d’expédition et par l’ [algorithme de sélection Source](selection-reservations.md).

Vous commencez avec un stock par défaut affecté avec le Source par défaut et votre site web, mieux utilisé par les marchands à source unique. Seul le Source par défaut peut être affecté à ce stock. Les marchands multi-sources créent des stocks personnalisés pour les sources et les sites web personnalisés, si nécessaire.

![Diagramme par exemple stocks pour un magasin](assets/diagram-stock.png){width="600" zoomable="yes"}

## Quantités de produits

La quantité est le nombre de produits de votre inventaire actif qui peuvent être achetés. La quantité de produits augmente et diminue lorsque vous effectuez des envois ou que vous ajustez le stock. L’ajout de produits à un panier n’a aucune incidence sur ce montant. La quantité vendable suit la disponibilité du produit pour un canal de vente et utilise également cette valeur pour déterminer le stock disponible à acheter. Selon le nombre de vos sources, vous voyez et gérez la quantité de produits pour l’une des sources suivantes :

- **Quantity** - Pour les marchands à source unique, la colonne _[!UICONTROL Quantity]_&#x200B;et la valeur effectuent le suivi de la quantité de stock disponible.
- **Quantité par Source** - Pour les marchands multi-sources, la colonne _[!UICONTROL Quantity per Source]_&#x200B;et les valeurs effectuent le suivi de l’inventaire disponible par emplacement. Si vous ajoutez plusieurs sources, cette valeur remplace la quantité et répertorie chaque source et quantité affectée.

Les réservations effectuent le suivi des demandes de stock pour l’ensemble du processus d’achat : ajout de produits au panier, exécution du passage en caisse et gestion des remboursements. Pour les stocks et les stocks disponibles, les réservations réservent les montants de stock par commande via le processus de passage en caisse, soustrait de la quantité vendable. Les quotas sont convertis en déductions quantitatives lors de la facturation et de l’expédition de produits.

La quantité vendable calcule l&#39;inventaire virtuel des produits (ou leur disponibilité) à l&#39;aide de seuils configurés, de quantités réservées ou vendues et de quantités par source. Pour chaque stock, [!DNL Commerce] accède à toutes les sources attribuées et agrège les quantités de produits associées. Avec cette valeur de base, elle soustrait ensuite toutes les quantités de réservation et le seuil _[!UICONTROL Notify for Quantity Below]_.

![Calcul de la quantité vendable pour un stock](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Paramétrages du stock

Chaque produit, source et stock comprend plusieurs options à configurer pour votre magasin au niveau global, source, stock et produit. Pour obtenir la liste complète de ces options, reportez-vous à la section [Configuration d&#39;Inventory management](configuration.md).

Voici quelques options importantes à comprendre pour [!DNL Inventory Management] :

- **[!UICONTROL Out-of-Stock Threshold]** - Définit un montant à soustraire de votre Quantité vendable. Si vous activez l’option Commandes d’arrière-plan, cette valeur n’est pas déduite de la quantité vendable.
- **[!UICONTROL Backorders]** - Détermine si les produits peuvent être vendus au-delà d’un stock nul, ce qui permet d’économiser les commandes jusqu’au redémarrage. Lorsque les commandes en arrière-plan sont activées, la configuration de [!UICONTROL Out-of-Stock Threshold] est recommandée.

>[!NOTE]
>
>La valeur du seuil en rupture de stock prend en charge les montants négatifs et positifs. Si vous activez Commandes d’arrière-plan, définissez cette valeur sur une valeur négative pour le nombre maximal de produits pouvant être commandés en amont avant que le produit ne soit réellement considéré comme hors stock.

## Démo Inventory management

Regardez cette vidéo pour en savoir plus sur les sources et les stocks Inventory management :

>[!VIDEO](https://video.tv.adobe.com/v/3410196?quality=12&learn=on&captions=fre_fr)
