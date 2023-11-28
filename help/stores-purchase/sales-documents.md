---
title: Documents commerciaux
description: Découvrez comment configurer des documents de vente pour prendre en charge les commandes et l’exécution des clients pour votre boutique de commerce.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Documents commerciaux

Pour prendre en charge le processus de commande et fournir à vos clients de la documentation sur les commandes qu’ils envoient, configurez les documents de vente associés afin qu’ils reflètent votre marque de magasin et incluent des informations de référence.

## Configurer des factures et des bordereaux d&#39;emballage

Contrairement aux images de logo utilisées dans les pages de vitrine, le logo des factures PDF et d’autres documents de vente peut être une image haute résolution de 300 ppp. Veillez à conserver les proportions lorsque vous redimensionnez le logo. Redimensionnez le logo pour qu’il s’adapte à la hauteur et ne vous souciez pas de l’espace inutilisé à droite.

![Exemple de logo](./assets/logo-pdf.png){width="200"}

Pour redimensionner votre logo en fonction de la taille requise, vous pouvez créer une nouvelle image vierge aux dimensions correctes. Ensuite, collez l’image de votre logo et redimensionnez-la pour l’adapter à la hauteur. Avec la plupart des programmes de retouche d’images, vous pouvez soit l’adapter en pourcentage afin de conserver les proportions, soit maintenir la touche Maj enfoncée et redimensionner manuellement l’image.

**_Pour mettre à jour le logo :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Invoice and Packing Slip Design]** et procédez comme suit :

   ![Configuration des ventes - conception des factures de ventes et des bordereaux de livraison](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Pour charger la variable **[!UICONTROL Logo for PDF Print-outs]**, cliquez sur **[!UICONTROL Choose File]**, recherchez le logo préparé, puis cliquez sur **[!UICONTROL Open]**.

   - Pour charger la variable **[!UICONTROL Logo for HTML Print View]**, cliquez sur **[!UICONTROL Choose File]**, recherchez le logo préparé, puis cliquez sur **[!UICONTROL Open]**.

   - Saisissez votre adresse telle qu&#39;elle apparaîtra sur les factures et les bordereaux d&#39;emballage.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

   À titre de référence, une miniature de l’image téléchargée s’affiche avant chaque champ. Ne vous inquiétez pas si la miniature semble déformée. La proportion du logo est correcte sur la facture.

### Remplacement d’une image

1. Cliquez sur **[!UICONTROL Choose File]** et choisissez un fichier de logo différent.

1. Sélectionnez la variable **[!UICONTROL Delete Image]** de l’image à remplacer.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Formats d’image

| Format | Conditions |
|--- |------------------------------------------|
| **_PDF_** |  |
| Format du fichier | JPG (JPEG), PNG, TIF (TIFF) |
| Taille de l’image | Jusqu’à 1 080 pixels de large x 270 pixels de haut |
| Résolution | 300 ppp recommandé |
| **_HTML_** |  |
| Format du fichier | JPG (JPEG), PNG, GIF |
| Taille de l’image | Déterminé par le thème. |
| Résolution | 72 ou 96 ppp |

{style="table-layout:auto"}

## Ajout d’identifiants de référence

L’identifiant de commande et l’adresse IP du client peuvent être inclus dans l’en-tête des documents de vente accompagnant une commande. Par défaut, l’identifiant de commande et l’adresse IP du client apparaissent dans l’en-tête des factures, des bordereaux de livraison et des notes de crédit.

![Configuration des ventes - Impressions de PDF](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_Pour modifier le paramètre d’ID de commande :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL PDF Print-outs]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **Facture** .

1. Définir **[!UICONTROL Display Order ID in Header]** selon vos préférences.

1. Répétez l’opération pour le **[!UICONTROL Shipment]** et **[!UICONTROL Credit Memo]** sections.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

**_Pour modifier le paramètre d’adresse IP du client :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL General]** .

   ![Configuration des ventes - Paramètres généraux de vente](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Hide Customer IP]** selon vos préférences.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
