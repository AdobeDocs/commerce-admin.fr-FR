---
title: Ressources de thème
description: Découvrez comment gérer vos ressources de thème, telles que les fichiers CSS, les polices, les images et les fichiers JavaScript.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: e50b85311f4512fb54c7cb29faf6136eaf07eae6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Ressources de thème

Les _fichiers statiques_ sont l’ensemble des ressources, telles que CSS, polices, images et JavaScript, utilisées par un thème. L’emplacement des fichiers statiques est spécifié dans la configuration [URL de base](../stores-purchase/store-urls.md). Vous pouvez ajouter une signature numérique à l’URL de chaque fichier statique pour permettre aux navigateurs de détecter lorsqu’une version plus récente est disponible. La version la plus récente du fichier est utilisée si la signature diffère de ce qui est stocké dans le cache du navigateur.

Dans le cas d’une installation standard, les ressources associées à un thème sont organisées dans le dossier `web` situé à l’emplacement suivant, sous la racine [!DNL Commerce].

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Ajouter une signature numérique aux URL de fichiers statiques

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Static Files Settings]** .

   ![Paramètres des fichiers statiques](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Définissez **[!UICONTROL Sign Static Files]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

| Type de fichier | Description |
|--- |--- |
| CSS | Contrôlez le style visuel associé à la peau. Exemple d&#39;emplacement sur le serveur : `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Polices | Fournissez les polices qui peuvent être utilisées par le thème. Emplacement sur le serveur : `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Images | Fournissez les ressources graphiques utilisées par le thème, notamment les boutons, les textures d’arrière-plan, etc. Exemple d&#39;emplacement sur le serveur : `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Routines JavaScript et fonctions appelables spécifiques à un thème. Exemple d&#39;emplacement sur le serveur : `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Fusion de fichiers CSS

Dans le cadre de l’optimisation de votre site et de la réduction du temps de chargement des pages, vous pouvez réduire le nombre de fichiers CSS distincts en les fusionnant en un seul fichier condensé. Si vous ouvrez un fichier CSS fusionné, vous voyez un flux continu de texte, sans sauts de ligne. Vous ne pouvez pas modifier le fichier fusionné. Il est donc préférable d’attendre d’être en mode de développement et de ne plus apporter de modifications fréquentes au CSS.

>[!NOTE]
>
>Les fichiers CSS peuvent être fusionnés à partir du panneau _Admin_ uniquement lorsque vous travaillez en [mode développeur](../systems/developer-tools.md#operation-modes).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL CSS Settings]** .

   ![&#x200B; Paramètres CSS &#x200B;](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Pour une description détaillée de ces options de configuration, voir [Paramètres CSS](../configuration-reference/advanced/developer.md#css-settings) dans le _Guide de référence de configuration_.

1. Définissez **[!UICONTROL Merge CSS Files]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Fusion de fichiers JavaScript

Plusieurs fichiers JavaScript peuvent être fusionnés en un seul fichier condensé afin de réduire le temps de chargement des pages. Si vous ouvrez un fichier JavaScript fusionné, vous verrez un flux de texte continu, sans sauts de ligne. Si vous avez terminé le processus de développement et que le code ne contient aucune erreur, vous pouvez envisager de fusionner les fichiers.

>[!NOTE]
>
>Les fichiers JavaScript peuvent être fusionnés à partir du panneau _Admin_ uniquement lorsque vous travaillez en [mode Développeur](../systems/developer-tools.md#operation-modes).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL JavaScript Settings]** .

   ![Paramètres JavaScript](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Pour une description détaillée de ces options de configuration, consultez [Paramètres JavaScript](../configuration-reference/advanced/developer.md#javascript-settings) dans la _Référence de configuration_.

1. Définissez **[!UICONTROL Merge JavaScript Files]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
