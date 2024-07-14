---
title: Classes fiscales
description: Découvrez comment configurer les classes de taxe utilisées pour les règles fiscales.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Classes fiscales

Les classes de taxe peuvent être attribuées aux clients, aux produits et aux frais d’expédition. Commerce analyse le panier de chaque client et calcule la taxe appropriée en fonction de la classe du client, de la classe des produits du panier et de la région. La région est déterminée par l’adresse de livraison, l’adresse de facturation ou l’origine de livraison du client. De nouvelles classes de taxe peuvent être créées lorsqu&#39;une [règle de taxe](tax-rules.md) est définie.

- **Client** : vous pouvez créer autant de classes d’impôts client que nécessaire et les affecter à des [groupes de clients](../customers/customer-groups.md). Par exemple, dans certaines juridictions, les transactions de gros ne sont pas taxées, mais les transactions de détail le sont. Vous pouvez associer des membres du groupe de clients de vente en gros à la classe de taxe de vente en gros.

- **Produit** - Les classes de produit sont utilisées dans les calculs pour déterminer le taux de taxe correct appliqué dans le panier. Lorsque vous créez un produit, il est affecté à une classe de taxe spécifique. Par exemple, les aliments peuvent ne pas être taxés, ou être taxés à un taux différent.

- **Expédition** — Si votre boutique impose une taxe supplémentaire sur les frais d’expédition, vous devez désigner une classe de taxe spécifique sur les produits pour l’expédition. Ensuite, dans la configuration, indiquez-le comme classe de taxe utilisée pour l’expédition.

## Configuration des classes de taxe

La classe de taxe utilisée pour la livraison et les classes de taxe par défaut pour les [produits et clients](#add-a-product-tax-class) sont définies dans la configuration _[!UICONTROL Sales]_.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Tax Classes]** .

   ![Configuration - classes de taxe](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Choisissez la classe de taxe pour chacune des catégories suivantes :

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Ajout de classes de taxe

Il est facile d’ajouter des classes de taxe pour les clients et les produits, de les affecter ensuite à des clients et des produits individuels et de les utiliser dans les règles fiscales.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Cliquez sur **[!UICONTROL Add New Tax Rule]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Additional Settings]** .

   ![Ajouter une nouvelle classe d’impôt](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Sous _Customer Tax Class_, cliquez sur **[!UICONTROL Add New Tax Class]**.

1. Saisissez le **[!UICONTROL Name]** de la nouvelle classe de taxe dans la zone de texte.

   ![Ajouter une nouvelle classe d’impôt](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Pour ajouter la nouvelle classe à la liste des classes de taxe client disponibles, cliquez sur la coche.

   ![Nouvelles classes d’impôts](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Ajouter une classe de taxe de produit

1. Sous _Product Tax Class_, cliquez sur **[!UICONTROL Add New Tax Class]**.

1. Saisissez le **[!UICONTROL Name]** de la nouvelle classe de taxe dans la zone de texte.

1. Pour ajouter la nouvelle classe à la liste des classes de taxe de produit disponibles, cliquez sur la coche.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Back]** dans la barre de boutons pour revenir à la grille _Règles fiscales_.

## Destination de la taxe par défaut

Les paramètres de destination de la taxe par défaut déterminent le pays, l’état et le code postal utilisés comme base de calcul de la taxe.

**_Pour configurer la destination de taxe par défaut pour les calculs :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Default Tax Destination Calculation]** .

   ![Calcul de destination de taxe par défaut](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Default Country]** sur le pays sur lequel reposent les calculs fiscaux.

1. Définissez **[!UICONTROL Default State]** sur l’état ou la province utilisé comme base des calculs fiscaux.

1. Définissez **[!UICONTROL Default Post Code]** sur le code postal qui sert de base aux calculs des impôts locaux.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
