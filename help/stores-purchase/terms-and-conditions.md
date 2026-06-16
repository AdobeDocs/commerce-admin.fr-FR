---
title: Termes et conditions de passage en caisse
description: Découvrez les fonctionnalités des termes et conditions qui peuvent être configurées pour votre boutique.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
TQID: https://experienceleague.adobe.com/xHlKdFJPVInadvAyFbs6jFYz4AECWJdkbV8FRoHxE8U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 0%

---

# Termes et conditions de passage en caisse

Lorsque la fonctionnalité manuelle _Conditions générales_ est activée, les clients doivent accepter les conditions générales de la vente avant que l’achat ne soit finalisé. Les Conditions générales de la vente incluent généralement des informations de divulgation qui peuvent être requises par la loi pour les sites B2C ou B2B, et décrivent les droits de l&#39;acheteur et du vendeur. Le message Conditions générales apparaît après les informations de paiement, juste avant le bouton _Passer une commande_.

![Conditions générales au passage en caisse](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Étape 1 : activer les conditions générales pour le passage en caisse

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Checkout Options]** .

   ![Options de paiement](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Vérifiez que **[!UICONTROL Enable Onepage Checkout]** est défini sur `Yes`.

1. Définissez **[!UICONTROL Enable Terms and Conditions]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 2 : ajouter vos propres informations de termes et conditions

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Grille des termes et conditions](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Condition]**.

1. Saisissez le **[!UICONTROL Condition Name]** pour référence interne.

   ![Nouvelle condition](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Status]** sur `Enabled`.

1. Définissez **[!UICONTROL Applied]** sur l’une des options suivantes :

   - `Automatically` - Les conditions sont automatiquement acceptées lors du passage en caisse.
   - `Manually` - Les clients doivent accepter manuellement les conditions de passation d&#39;une commande.

1. Définissez **[!UICONTROL Show Content as]** sur l’une des options suivantes :

   - `Text` - Affiche le contenu des termes et conditions sous forme de texte non formaté.
   - `HTML` - Affiche le contenu au format HTML qui peut être formaté.

1. Sélectionnez chaque **[!UICONTROL Store View]** où vous souhaitez que ces termes et conditions soient utilisés.

1. Faites défiler vers le bas et renseignez les informations à afficher :

   - Saisissez le **[!UICONTROL Checkbox Text]** à utiliser comme texte pour le lien des conditions générales. Par exemple, `I understand and accept the terms and conditions of the sale`.

   - Dans la boîte de **[!UICONTROL Content]**, entrez le texte complet des conditions générales de la vente.

1. (Facultatif) Saisissez le **[!UICONTROL Content Height (css)]** en pixels pour déterminer la hauteur de la zone de texte dans laquelle l’instruction des conditions générales s’affiche lors du passage en caisse.

   Par exemple, pour que la zone de texte ait une hauteur de 1 pouce sur un affichage de 96 ppp, saisissez `96`. Une barre de défilement s’affiche si le contenu s’étend au-delà de la hauteur de la zone.

1. Cliquez sur **[!UICONTROL Save Condition]**.
