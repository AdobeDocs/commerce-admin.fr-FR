---
title: Documents vente
description: Découvrez comment configurer des documents de vente pour prendre en charge les commandes et l’exécution des clients de votre boutique Commerce.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
TQID: https://experienceleague.adobe.com/0SZsaPiyOc4E-0e34IDvWATtKz9HMaeZAIMhKeysvTg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 1%

---

# Documents vente

Pour prendre en charge le workflow de commande et fournir une documentation à vos clients sur les commandes qu’ils envoient, configurez les documents de vente associés pour refléter la marque de votre boutique et inclure des informations de référence.

## Configurer les factures et les bons de livraison

Contrairement aux images de logo utilisées dans les pages de storefront, le logo des factures PDF et d’autres documents de vente peut être une image haute résolution de 300 dpi. Veillez à conserver les proportions lorsque vous redimensionnez le logo. Redimensionnez le logo afin qu’il s’adapte à la hauteur et ne vous inquiétez pas des espaces inutilisés à droite.

![Exemple de logo](./assets/logo-pdf.png){width="200"}

Pour redimensionner votre logo en fonction de la taille requise, vous pouvez créer une image vierge aux dimensions correctes. Collez ensuite l’image de votre logo et redimensionnez-la pour l’adapter à la hauteur. Dans la plupart des programmes de modification d’images, vous pouvez mettre l’image à l’échelle selon un pourcentage afin de conserver ses proportions, ou maintenir la touche Maj enfoncée et redimensionner manuellement l’image.

**_Pour mettre à jour le logo:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Invoice and Packing Slip Design]** et procédez comme suit :

   ![Configuration des ventes - facture de vente et conception du bon de livraison](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Pour télécharger le **[!UICONTROL Logo for PDF Print-outs]**, cliquez sur **[!UICONTROL Choose File]**, recherchez le logo que vous avez préparé, puis cliquez sur **[!UICONTROL Open]**.

   - Pour télécharger le **[!UICONTROL Logo for HTML Print View]**, cliquez sur **[!UICONTROL Choose File]**, recherchez le logo que vous avez préparé, puis cliquez sur **[!UICONTROL Open]**.

   - Saisissez votre adresse telle que vous souhaitez qu&#39;elle apparaisse sur les factures et les bons de livraison.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

   À titre de référence, une miniature de l’image chargée s’affiche avant chaque champ. Ne vous inquiétez pas si la miniature semble déformée. La proportion du logo est correcte sur la facture.

### Remplacer une image

1. Cliquez sur **[!UICONTROL Choose File]** et choisissez un autre fichier de logo.

1. Cochez la case **[!UICONTROL Delete Image]** de l’image à remplacer.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Formats d’image

| Format | Conditions requises |
|--- |------------------------------------------|
| **__** |  |
| Format du fichier | JPG (JPEG), PNG, TIF (TIFF) |
| Taille de l’image | Jusqu’à 1 080 pixels de large sur 270 pixels de haut |
| Résolution | 300 ppp recommandés |
| **__** |  |
| Format du fichier | JPG (JPEG), PNG, GIF |
| Taille de l’image | Déterminé par thème. |
| Résolution | 72 ou 96 ppp |

{style="table-layout:auto"}

## Ajout d’identifiants de référence

L’ID de commande et l’adresse IP du client peuvent être inclus dans l’en-tête des documents de vente qui accompagnent une commande. Par défaut, l&#39;ID commande et l&#39;adresse IP du client apparaissent dans l&#39;en-tête des factures, des bons de livraison et des avoirs.

![Configuration des ventes - Impressions PDF](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_Pour modifier le paramètre d’ID de commande:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL PDF Print-outs]**.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **Facture**.

1. Définissez **[!UICONTROL Display Order ID in Header]** selon vos préférences.

1. Répétez l’opération pour les sections **[!UICONTROL Shipment]** et **[!UICONTROL Credit Memo]**.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

**_Pour modifier le paramètre d’adresse IP du client:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General]** .

   ![Configuration des ventes - Paramètres généraux des ventes](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Hide Customer IP]** sur vos préférences.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
