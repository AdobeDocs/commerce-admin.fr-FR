---
title: Conditions générales du passage en caisse
description: Découvrez la fonctionnalité des conditions générales qui peut être configurée pour votre magasin.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Conditions générales du passage en caisse

Lorsque la fonctionnalité manuelle _Termes et conditions_ est activée, les clients doivent accepter les conditions générales de la vente avant que l’achat ne soit finalisé. Les Conditions générales de la vente incluent généralement des informations de divulgation qui peuvent être requises par la loi pour les sites B2C ou B2B, et qui définissent les droits de l’acheteur et du vendeur. Le message Conditions générales s’affiche après les informations de paiement, juste avant le bouton _Passer commande_ .

![Termes et conditions à l’extraction](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Étape 1 : activation des conditions générales pour l’extraction

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Checkout Options]** .

   ![Options de passage en caisse](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Vérifiez que **[!UICONTROL Enable Onepage Checkout]** est défini sur `Yes`.

1. Définissez **[!UICONTROL Enable Terms and Conditions]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 2 : Ajout de vos propres informations sur les conditions générales

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Grille Termes et conditions](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Condition]**.

1. Saisissez le **[!UICONTROL Condition Name]** pour référence interne.

   ![Nouvelle condition](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Status]** sur `Enabled`.

1. Définissez **[!UICONTROL Applied]** sur l’une des options suivantes :

   - `Automatically` - Les conditions sont automatiquement acceptées lors du passage en caisse.
   - `Manually` - Les clients doivent accepter manuellement les conditions de commande.

1. Définissez **[!UICONTROL Show Content as]** sur l’une des options suivantes :

   - `Text` : affiche le contenu des termes et conditions sous forme de texte non formaté.
   - `HTML` - Affiche le contenu sous la forme d’un HTML pouvant être formaté.

1. Sélectionnez chaque **[!UICONTROL Store View]** où vous souhaitez que ces termes et conditions soient utilisés.

1. Faites défiler l’écran vers le bas et renseignez les informations à afficher :

   - Saisissez le **[!UICONTROL Checkbox Text]** à utiliser comme texte pour le lien Termes et conditions . Par exemple, `I understand and accept the terms and conditions of the sale`.

   - Dans la zone **[!UICONTROL Content]**, saisissez le texte intégral des conditions générales de la vente.

1. (Facultatif) Saisissez le **[!UICONTROL Content Height (css)]** en pixels pour déterminer la hauteur de la zone de texte dans laquelle l’instruction des conditions s’affiche lors de l’extraction.

   Par exemple, pour que la zone de texte ait une hauteur de 1 pouce sur un affichage de 96 ppp, saisissez `96`. Une barre de défilement s’affiche si le contenu s’étend au-delà de la hauteur de la zone.

1. Cliquez sur **[!UICONTROL Save Condition]**.
