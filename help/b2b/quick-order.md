---
title: Commandes rapides
description: Découvrez la fonctionnalité de commande rapide et son activation pour vos clients.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Commandes rapides

La fonction _Commande rapide_ réduit le processus de commande à plusieurs clics pour les clients qui connaissent le nom ou le SKU du produit qu’ils souhaitent commander. Les commandes comportant plusieurs SKU peuvent être saisies manuellement ou importées dans le formulaire de commande rapide. La commande rapide peut être utilisée par les clients connectés à leurs comptes, ainsi que par les invités. Lorsque cette option est activée, le lien _Commande rapide_ s’affiche en haut de la page, en regard du nom du client.

![Lien de commande rapide](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Activation des commandes rapides pour votre boutique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans la section _[!UICONTROL General]_&#x200B;du panneau de gauche, choisissez **[!UICONTROL B2B Features]**.

1. Définissez **[!UICONTROL Enable Quick Order]** sur `Yes`.

   ![Activer l’ordre rapide](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur [Gestion du cache](../systems/cache-management.md) et actualisez les caches non valides.

## Workflows de commande rapide

Les clients peuvent spécifier des produits pour les commandes rapides à l’aide de l’une des méthodes suivantes.

### Méthode 1 : saisie de produits individuels

1. Le client clique sur le lien **[!UICONTROL Quick Order]** .

1. Sélection du produit par SKU ou nom du produit :

   Pour passer une **commande rapide par SKU**, le client effectue les opérations suivantes :

   - Entrez le **[!UICONTROL SKU]**.

   - Clics **[!UICONTROL Add to List]**.

     Le SKU apparaît dans la ligne de saisie, avec les détails du produit ci-dessous.

     ![Détails de commande rapide](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Pour passer une **commande rapide par nom de produit**, le client effectue les opérations suivantes :

   - Entrez les premiers caractères de **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >N’utilisez pas la clé _Entrée_ pour choisir le nom du produit.

   - Lorsque la liste des correspondances possibles apparaît, le client clique sur le produit qu’il souhaite commander.

     ![Cliquez pour choisir le nom du produit](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Entrez le **[!UICONTROL Qty]**.

1. En utilisant la ligne d’entrée suivante, répète ce processus autant de fois que nécessaire.

1. Clics **[!UICONTROL Add to Cart]**.

### Méthode 2 : saisissez plusieurs produits

1. Dans la zone **[!UICONTROL Enter Multiple SKUs]**, le client effectue l’une des opérations suivantes :

   - Saisie d’un SKU par ligne

   - Saisissez tous les SKU sur la même ligne, séparés par des virgules, et sans espaces.

     ![Entrer plusieurs SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Pour ajouter les produits à la liste, cliquez sur **[!UICONTROL Add to List]**.

1. Entrez le **[!UICONTROL Qty]** à classer pour chaque élément de la liste.

   ![Liste à commandes rapides](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si le produit dispose des options requises, le client est invité à les sélectionner. Ils peuvent attendre d’accéder au panier pour ajouter des options de produit.

   ![Choose Options](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Méthode 3 : téléchargement d’une liste de produits

1. Dans la section _[!UICONTROL Add from File]_, cliquez sur **[!UICONTROL Download Sample]**&#x200B;pour télécharger un modèle de commande.

   ![Ajouter à partir d’un fichier](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Ouvre le fichier téléchargé.

1. Utilise le modèle pour ajouter les SKU du produit à charger pour la liste de commandes rapides.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   ![SKU à télécharger](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Pour charger le fichier, cliquez sur **[!UICONTROL Choose]** et sélectionnez le fichier sur son système.

   Les éléments sont ajoutés à la liste Ordre rapide.

1. Une fois prêt, cliquez sur **[!UICONTROL Add to Cart]**.

Une fois que le client a créé la commande rapide, il peut procéder à l’extraction comme d’habitude.

![Ordre rapide](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
