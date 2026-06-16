---
title: Classes d'impôts
description: Découvrez comment configurer les classes de taxe utilisées pour les règles fiscales.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
TQID: https://experienceleague.adobe.com/wzq0p5sH7Ulpl6hiY5IaWPe9AvsrwJjrAZsX4PFZ2-Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 501
ht-degree: 0%

---

# Classes d&#39;impôts

Les classes de taxe peuvent être attribuées aux clients, aux produits et aux frais d&#39;expédition. Commerce analyse le panier de chaque client et calcule la taxe appropriée en fonction de la classe du client, de la classe des produits du panier et de la région. La région est déterminée par l’adresse de livraison, l’adresse de facturation ou l’origine de livraison du client. De nouvelles classes de taxe peuvent être créées lorsqu&#39;une [règle de taxe](tax-rules.md) est définie.

- **Client** — Vous pouvez créer autant de classes de taxe client que nécessaire et les affecter à des [groupes de clients](../customers/customer-groups.md). Par exemple, dans certaines juridictions, les transactions de gros ne sont pas taxées, mais les transactions de détail le sont. Vous pouvez associer les membres du groupe de clients en gros à la classe de taxe en gros.

- **Produit** — Les classes de produits sont utilisées dans les calculs pour déterminer le taux de taxe correct appliqué au panier. Lorsque vous créez un produit, il est affecté à une classe de taxe spécifique. Par exemple, les aliments peuvent ne pas être taxés ou l&#39;être à un taux différent.

- **Expédition** — Si votre magasin facture une taxe supplémentaire sur l&#39;expédition, vous devez désigner une classe de taxe de produit spécifique pour l&#39;expédition. Ensuite, dans la configuration, spécifiez-la comme classe de taxe utilisée pour l’expédition.

## Configurer les classes de taxe

La classe de taxe utilisée pour l&#39;expédition et les classes de taxe par défaut pour les [produits et clients](#add-a-product-tax-class) sont définies dans la configuration _[!UICONTROL Sales]_.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Tax Classes]** .

   ![Configuration - Classes de taxe](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Choisissez la classe de taxe pour chacun des éléments suivants :

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Ajouter des classes de taxe

Les classes de taxe pour les clients et les produits peuvent être facilement ajoutées, puis affectées à des clients et des produits individuels, et utilisées dans les règles de taxe.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Cliquez sur **[!UICONTROL Add New Tax Rule]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Additional Settings]** .

   ![Ajouter une nouvelle classe de taxe](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Sous _Classe de taxe client_, cliquez sur **[!UICONTROL Add New Tax Class]**.

1. Saisissez le **[!UICONTROL Name]** de la nouvelle classe de taxe dans la zone de texte.

   ![Ajouter une nouvelle classe de taxe](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Pour ajouter la nouvelle classe à la liste des classes de taxe client disponibles, cliquez sur la coche.

   ![Nouvelles classes de taxe](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Ajouter une classe de taxe de produit

1. Sous _Classe de taxe de produit_, cliquez sur **[!UICONTROL Add New Tax Class]**.

1. Saisissez le **[!UICONTROL Name]** de la nouvelle classe de taxe dans la zone de texte.

1. Pour ajouter la nouvelle classe à la liste des classes de taxe sur les produits disponibles, cliquez sur la coche.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Back]** dans la barre de boutons pour revenir à la grille _Règles fiscales_.

## Destination fiscale par défaut

Les paramètres de destination de taxe par défaut déterminent le pays, l’État et le code postal utilisés comme base de calcul des taxes.

**_Pour configurer la destination de taxe par défaut pour les calculs:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Default Tax Destination Calculation]** .

   ![Calcul de la destination de taxe par défaut](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Default Country]** sur le pays sur lequel les calculs de taxe sont basés.

1. Définissez **[!UICONTROL Default State]** sur l’État ou la province utilisé(e) comme base de calcul des taxes.

1. Définissez **[!UICONTROL Default Post Code]** sur le code postal utilisé comme base de calcul des taxes locales.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
