---
title: Types d'approvisionnement des marchés
description: Découvrez les deux types d’approvisionnement en fonction du nombre d’emplacements ou de sources dans votre entreprise.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Types d&#39;approvisionnement des marchés

[!DNL Commerce] prend [!DNL Inventory Management] pour toutes les tailles d’entreprises, y compris un seul magasin disposant d’un site web, à un réseau international de sites web, de magasins, d’entrepôts et d’expéditeurs. Tous les commerçants utilisant Adobe Commerce ou Magento Open Source sont classés en deux types en fonction du nombre d’emplacements ou de sources dans votre entreprise.

- Les marchands d’une seule source expédient les produits à partir d’un seul emplacement. Vous êtes considéré comme un mode/un marchand source unique jusqu’à ce que vous commenciez à ajouter des sources et des stocks personnalisés à votre installation.

- Les commerçants multi-sources expédient des produits de plus d’un emplacement, tels que des magasins en brique et des magasins, des entrepôts, des débardeurs et des centres de distribution. Après avoir ajouté des sources personnalisées par emplacement, vous devenez automatiquement un marchand multisource.

## Commerçants à source unique

Les marchands à source unique disposent d’un emplacement unique qui gère le stock disponible et exécute les commandes. En règle générale, plusieurs sites web (ou canaux de vente) vendent des produits du même catalogue, du même inventaire et du même emplacement.

Par exemple, vous disposez d’un site web ou d’une mise en oeuvre multi-site avec des sites pour les États-Unis, l’Allemagne, la France et le Brésil qui extraient tous des produits d’un grand entrepôt. Cette source unique gère l’ensemble des quantités d’inventaire, des envois et des retours, quel que soit le canal de vente qui reçoit la commande.

Pour commencer :

- Configurer [paramètres globaux et de produit](configuration.md) pour l’inventaire de votre magasin, si nécessaire.

- Mettez à jour le [Source par défaut](sources-manage.md) avec des informations sur votre emplacement de stock unique. La création de sources supplémentaires n’est pas requise.

- Mettez à jour le [Stock par défaut](stocks-manage.md). Assurez-vous que tous vos sites web sont sélectionnés comme canaux de vente. Lorsque vous ajoutez de nouveaux sites web, [!DNL Commerce] les ajoute automatiquement au stock par défaut. Il n&#39;est pas nécessaire de créer des stocks supplémentaires.

>[!NOTE]
>
>À mesure que votre entreprise se développe, ajoutez des sources et des stocks supplémentaires et mettez à jour vos [!DNL Inventory Management] pour devenir un site commercial multi-source. Voir [Agrandir et restructurer l’inventaire](expand-restructure.md) pour tous les détails.

## Marchands multisource

Les commerçants multi-sources disposent d’un site web ou d’une mise en oeuvre multi-site et gèrent l’inventaire disponible et le respect des commandes à travers plusieurs emplacements.

Par exemple, vous disposez d’une mise en oeuvre multi-site avec des sites web pour les États-Unis, l’Allemagne, la France et le Brésil. Votre entreprise comprend plusieurs entrepôts et magasins dans ces pays et abandonne les services des expéditeurs qui gèrent tous les stocks et exécutent les commandes. Ces emplacements et sites web deviennent des sources et des stocks dans [!DNL Commerce]. Vous pouvez créer un stock pour les Amériques et un autre pour l&#39;Europe, en attribuant des sites web et des sources en fonction des paramètres régionaux et des lieux. Les clients qui achètent chaque site web n’ont accès qu’aux stocks pouvant être vendus à partir des sources attribuées.

Pour commencer :

- Configurez les paramètres globaux pour l’inventaire de votre magasin, si nécessaire.

- Ajouter [sources personnalisées](sources-add.md) pour les emplacements de stock : entrepôts, magasins, centres de distribution et expéditeurs.

- Ajouter [stocks personnalisés](stocks-add.md) pour chaque région afin de mapper vos sites web avec plusieurs sources. Réorganisez les sources de chaque stock en priorité de localisation, ce qui s’avère utile lorsque vous effectuez vos commandes.

- Affectez des sources aux produits, en ajoutant des quantités par emplacement.

- Effectuez d’autres configurations par produit pour les seuils de quantité, les commandes en arrière-plan, etc.
