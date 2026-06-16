---
title: Commandes rapides
description: Découvrez la fonctionnalité de commande rapide et comment l’activer pour vos clients.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# Commandes rapides

La fonction _Commande rapide_ réduit le processus de commande à plusieurs clics pour les clients qui connaissent le nom du produit ou le SKU des produits qu&#39;ils souhaitent commander. Les commandes comportant plusieurs SKU peuvent être saisies manuellement ou importées dans le formulaire de commande rapide. La commande rapide peut être utilisée par les clients qui sont connectés à leurs comptes et par les invités. Lorsqu’il est activé, le lien _Commande rapide_ s’affiche en haut de la page, en regard du nom du client.

![Lien de commande rapide](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Activer les commandes rapides pour votre boutique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans la section _[!UICONTROL General]_&#x200B;du panneau de gauche, choisissez **[!UICONTROL B2B Features]**.

1. Définissez **[!UICONTROL Enable Quick Order]** sur `Yes`.

   ![Activer la commande rapide](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur [Gestion du cache](../systems/cache-management.md) et actualisez tous les caches non valides.

## Workflows de commande rapides

Les clients peuvent spécifier des produits pour les commandes rapides en utilisant l&#39;une des méthodes suivantes.

### Méthode 1 : saisir des produits individuels

1. Le client clique sur le lien **[!UICONTROL Quick Order]**.

1. Sélectionne le produit par SKU ou nom de produit :

   Pour passer une **commande rapide par SKU**, le client effectue les opérations suivantes :

   - Entre dans le **[!UICONTROL SKU]**.

   - Effectue un clic sur **[!UICONTROL Add to List]**.

     Le SKU apparaît dans la ligne de saisie, avec les détails du produit ci-dessous.

     ![Détails de commande rapide](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Pour passer une **commande rapide par nom de produit**, le client effectue les opérations suivantes :

   - Entre les premiers caractères du **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >N&#39;utilisez pas la touche _Entrée_ pour choisir le nom du produit.

   - Lorsque la liste des correspondances possibles s’affiche, le client clique sur le produit qu’il souhaite commander.

     ![Cliquez pour choisir le nom du produit](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Entre dans le **[!UICONTROL Qty]**.

1. À l’aide de la ligne d’entrée suivante, répète ce processus autant de fois que nécessaire.

1. Effectue un clic sur **[!UICONTROL Add to Cart]**.

### Méthode 2 : saisir plusieurs produits

1. Dans la zone de **[!UICONTROL Enter Multiple SKUs]**, le client effectue l’une des opérations suivantes :

   - Saisit un SKU par ligne

   - Saisit tous les SKU sur la même ligne, séparés par des virgules et sans espaces.

     ![Saisie de plusieurs SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Pour ajouter les produits à la liste, cliquez sur **[!UICONTROL Add to List]**.

1. Permet d&#39;entrer les **[!UICONTROL Qty]** à classer pour chaque élément de la liste.

   ![Liste de commandes rapides](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si le produit comporte des options requises, le client est invité à choisir ces options. Il peut attendre d’atteindre le panier pour ajouter des options de produit.

   ![Choisir les options](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Méthode 3 : téléchargement d’une liste de produits

1. Dans la section _[!UICONTROL Add from File]_, cliquez sur **[!UICONTROL Download Sample]**&#x200B;pour télécharger un modèle de commande.

   ![Ajouter à partir du fichier](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Ouvre le fichier téléchargé.

1. Utilise le modèle pour ajouter les SKU de produit à charger pour la liste de commande rapide.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   ![&#x200B; SKU à charger &#x200B;](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Pour télécharger le fichier, cliquez sur **[!UICONTROL Choose]** et sélectionne le fichier sur leur système.

   Les articles sont ajoutés à la liste Commande rapide.

1. Lorsque vous êtes prêt, cliquez sur **[!UICONTROL Add to Cart]**.

Une fois la commande rapide créée, le client peut passer en caisse comme d’habitude.

![Commande rapide](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
