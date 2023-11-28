---
title: Thèmes
description: En savoir plus [!DNL Commerce] les thèmes, notamment les fichiers de mise en page, les fichiers de modèle, les fichiers de traduction et les habillages qui définissent l’aspect de votre magasin.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Thèmes

Un thème est un ensemble de fichiers qui détermine la présentation visuelle de votre magasin. Lors de la première installation [!DNL Commerce], les éléments de conception du magasin sont basés sur la variable _Par défaut_ thème. Outre le thème par défaut initial fourni avec votre [!DNL Commerce] installation, il existe une grande variété de thèmes disponibles que vous pouvez utiliser. _as is_ ou modifiez selon vos besoins.

Un thème réactif ajuste la mise en page en fonction du port d’affichage de l’appareil. L’exemple _Luma_ Le thème dispose d’une disposition flexible et réactive qui peut être affichée à partir de l’ordinateur, de la tablette ou de l’appareil mobile.

[!DNL Commerce] les thèmes incluent les fichiers de mise en page, les fichiers de modèle, les fichiers de traduction et les habillages. Un habillage est un ensemble de fichiers CSS, d’images et JavaScript pris en charge qui, ensemble, créent la présentation visuelle et les interactions que vos clients rencontrent lorsqu’ils visitent votre magasin. Les thèmes et les habillages peuvent être modifiés et personnalisés par un développeur ou un professionnel de la conception qui comprend la conception de thèmes Commerce et qui a accès à votre serveur. Pour en savoir plus, voir la section [_Guide du développeur de Frontend_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Thème Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## Thème par défaut

La variable `Magento Blank` responsive theme affiche votre storefront pour différents appareils et incorpore les bonnes pratiques pour les ordinateurs de bureau, les tableaux et les appareils mobiles. Certains thèmes sont conçus pour être utilisés uniquement avec des appareils spécifiques. When [!DNL Commerce] détecte un ID de navigateur spécifique, ou agent utilisateur, il utilise le thème configuré pour le navigateur spécifique. La chaîne de recherche peut également inclure des expressions régulières compatibles avec les perles (PCRE).

![Thèmes](./assets/themes.png){width="700" zoomable="yes"}

### Filtrer la grille de thème

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Entrez une plage d’identifiants, un nom de thème (ou un titre), un chemin d’accès au dossier ou un thème parent.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour mettre à jour la liste des thèmes.

## Afficher les paramètres actuels du thème

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Dans la liste des thèmes installés, recherchez le thème à examiner, puis cliquez sur la ligne pour afficher les paramètres.

1. Pour afficher un exemple de page, cliquez sur le bouton **[!UICONTROL Theme Preview Image]**.

![Thème Aperçu](./assets/theme-settings.png){width="600" zoomable="yes"}

## Appliquer un thème par défaut

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _[!UICONTROL Default Theme]_, définit **[!UICONTROL Applied Theme]**à celle que vous souhaitez utiliser pour la vue actuelle.

   ![Thème appliqué](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

## Ajout d’une règle d’agent utilisateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Sous _[!UICONTROL Design Rule]_, cliquez sur **[!UICONTROL Add New User Agent Rule]**.

   ![Règle de conception](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Search String]**, saisissez l’identifiant du navigateur de l’appareil spécifique.

   Les chaînes de recherche correspondent dans l’ordre dans lequel elles sont entrées. Par exemple, pour Firefox, saisissez :

   `/^mozilla/i`

1. Pour entrer d’autres périphériques, répétez le processus.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.
