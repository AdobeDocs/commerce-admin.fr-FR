---
title: Thèmes
description: Découvrez les thèmes [!DNL Commerce], qui incluent les fichiers de disposition, les fichiers de modèle, les fichiers de traduction et les habillages qui définissent l’aspect de votre boutique.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: 8b440f30-6794-5ed6-981f-391de4e9b0cc
    internal-label: Themes
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%
---
# Thèmes

Un thème est un ensemble de fichiers qui détermine la présentation visuelle de votre boutique. Lorsque vous installez [!DNL Commerce] pour la première fois, les éléments de conception du magasin sont basés sur le thème _Default_. Outre le thème par défaut initial fourni avec votre installation [!DNL Commerce], il existe un large éventail de thèmes disponibles que vous pouvez utiliser _en l’état_ ou modifier selon vos besoins.

Un thème réactif ajuste la disposition de la page en fonction du port d’affichage de l’appareil. L’exemple de thème _Luma_ a une disposition flexible et réactive qui peut être affichée sur un bureau, une tablette ou un appareil mobile.

[!DNL Commerce] thèmes comprennent les fichiers de disposition, les fichiers de modèle, les fichiers de traduction et les habillages. Une apparence est un ensemble de fichiers CSS, d’images et JavaScript qui, ensemble, créent la présentation visuelle et les interactions que vos clients expérimentent lorsqu’ils visitent votre boutique. Les thèmes et les habillages peuvent être modifiés et personnalisés par un développeur ou un professionnel du design maîtrisant la conception de thèmes Commerce et ayant accès à votre serveur. Pour en savoir plus, consultez le [_Guide du développeur Frontend_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![ Thème Luma ](./assets/design-responsive.png){width="600" zoomable="yes"}

## Le thème par défaut

Le thème réactif `Magento Blank` effectue le rendu de l’affichage de votre storefront pour différents appareils et incorpore les bonnes pratiques pour les ordinateurs de bureau, les tableaux et les appareils mobiles. Certains thèmes sont conçus pour être utilisés uniquement avec des appareils spécifiques. Lorsque [!DNL Commerce] détecte un ID de navigateur spécifique, ou un agent utilisateur, il utilise le thème configuré pour le navigateur spécifique. La chaîne de recherche peut également inclure des expressions régulières compatibles avec Perl (PCRE).

![Thèmes](./assets/themes.png){width="700" zoomable="yes"}

### Filtrer la grille de thème

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Saisissez une plage d’identifiants, un nom de thème (ou un titre), un chemin de dossier ou un thème parent.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour mettre à jour la liste des thèmes.

## Afficher les paramètres du thème actuel

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Dans la liste des thèmes installés, recherchez le thème que vous souhaitez examiner, puis cliquez sur la ligne pour afficher les paramètres.

1. Pour afficher un exemple de page, cliquez sur le **[!UICONTROL Theme Preview Image]**.

![Prévisualiser le thème](./assets/theme-settings.png){width="600" zoomable="yes"}

## Appliquer un thème par défaut

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sous _[!UICONTROL Default Theme]_, définissez **[!UICONTROL Applied Theme]**sur celui que vous souhaitez utiliser pour l’affichage actuel.

   ![Thème appliqué](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Configuration]**.

## Ajout d’une règle d’agent utilisateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Sous _[!UICONTROL Design Rule]_, cliquez sur **[!UICONTROL Add New User Agent Rule]**.

   ![Règle de conception](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Search String]**, saisissez l’ID du navigateur pour l’appareil spécifique.

   Les chaînes de recherche correspondent dans l’ordre dans lequel elles sont saisies. Par exemple, pour Firefox, saisissez :

   `/^mozilla/i`

1. Pour entrer des périphériques supplémentaires, répétez le processus.

1. Cliquez ensuite sur **[!UICONTROL Save Configuration]**.
