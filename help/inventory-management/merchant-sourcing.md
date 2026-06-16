---
title: Types d’approvisionnement des commerçants
description: Découvrez les deux types d’approvisionnement en fonction du nombre d’emplacements, ou sources, dans votre entreprise.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 486
ht-degree: 0%

---

# Types d’approvisionnement des commerçants

[!DNL Commerce] prend en charge le [!DNL Inventory Management] pour toutes les tailles d’entreprises, y compris un magasin unique avec un site web vers un réseau international de sites web, de magasins, d’entrepôts et d’expéditeurs. Tous les commerçants qui utilisent Adobe Commerce ou Magento Open Source se répartissent en deux types en fonction du nombre d’emplacements, ou de sources, dans votre entreprise.

- Les commerçants à source unique expédient les produits à partir d&#39;un seul endroit. Vous êtes considéré comme un marchand/mode à source unique jusqu’à ce que vous commenciez à ajouter des sources et des stocks personnalisés à votre installation.

- Les marchands multi-fournisseurs expédient des produits à partir de plusieurs emplacements tels que des magasins physiques, des entrepôts, des chargeurs automatiques et des centres de distribution. Après avoir ajouté des sources personnalisées par emplacement, vous devenez automatiquement un commerçant multi-source.

## Commerçants à source unique

Les commerçants à source unique ont un emplacement unique qui gère le stock disponible et exécute les commandes. En règle générale, vous disposez de plusieurs sites web (ou canaux de vente) vendant des produits du même catalogue, du même inventaire et du même emplacement.

Par exemple, vous disposez d’un site web ou d’une implémentation multisite avec des sites pour les États-Unis, l’Allemagne, la France et le Brésil qui extraient tous les produits d’un grand entrepôt. Cette source unique gère toutes les quantités en stock, les expéditions et les retours, quel que soit le canal de vente qui reçoit la commande.

Pour commencer :

- Configurez [paramètres globaux et de produit](configuration.md) pour l’inventaire de votre magasin, si nécessaire.

- Mettez à jour le Source par défaut](sources-manage.md) avec des informations sur votre emplacement d’inventaire unique. [Il n’est pas nécessaire de créer des sources supplémentaires.

- Mettez à jour le [ Stock par défaut ](stocks-manage.md). Assurez-vous que tous vos sites web sont sélectionnés comme canaux de vente. Lorsque vous ajoutez de nouveaux sites web, [!DNL Commerce] les ajoute automatiquement au Stock par défaut. Il n&#39;est pas nécessaire de créer des stocks supplémentaires.

>[!NOTE]
>
>Au fur et à mesure que votre entreprise se développe, ajoutez des sources et des stocks supplémentaires et mettez à jour votre configuration [!DNL Inventory Management] pour devenir un commerçant multi-sources. Voir [Développer et restructurer l’inventaire](expand-restructure.md) pour tous les détails.

## Marchands multi-sources

Les commerçants multi-sources ont un site web ou une implémentation multi-site et gèrent le stock disponible et exécutent les commandes à travers plusieurs emplacements.

Par exemple, vous disposez d’une implémentation multisite avec des sites web pour les États-Unis, l’Allemagne, la France et le Brésil. Votre entreprise comprend plusieurs entrepôts et magasins dans ces pays et des services de livraison directe qui gèrent tous les stocks et exécutent les commandes. Ces emplacements et sites web deviennent des sources et des stocks en [!DNL Commerce]. Vous pouvez créer un stock pour les Amériques et un autre pour l’Europe, en attribuant des sites web et des sources en fonction des paramètres régionaux et des emplacements. Les clients qui achètent sur chaque site web n’ont accès qu’aux stocks vendables provenant des sources attribuées.

Pour commencer :

- Configurez les paramètres globaux de l’inventaire de votre boutique selon vos besoins.

- Ajoutez [sources personnalisées](sources-add.md) pour vos emplacements de stock : entrepôts, magasins, centres de distribution et chargeurs.

- Ajoutez [stocks personnalisés](stocks-add.md) pour chaque région afin de mapper vos sites web à plusieurs sources. Réordonner les sources de chaque stock par priorité d&#39;emplacement, ce qui est utile pour exécuter vos commandes.

- Attribuez des sources aux produits, en ajoutant des quantités par emplacement.

- Effectuez d&#39;autres configurations par produit pour les seuils de quantité, les reliquats, etc.
