---
title: Configuration de [!DNL Page Builder]
description: Découvrez la configuration  [!DNL Page Builder]  fonctionnalités dans Admin pour Adobe Commerce et Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Configuration de [!DNL Page Builder]

Lorsqu’il est activé dans la configuration, [!DNL Page Builder] est l’outil de création de contenu par défaut pour les pages, les blocs et les blocs dynamiques CMS. En outre, le bouton _[!UICONTROL Enable Advanced CMS]_&#x200B;propose des [!DNL Page Builder] en tant qu’option pour les catégories et les produits. Vous pouvez également choisir la [mise en page](../content-design/page-layout.md) par défaut que vous souhaitez utiliser pour les produits, les catégories et les pages CMS. [!DNL Page Builder] n’est pas disponible pour le contenu de newsletter, qui utilise l’éditeur [editor](../content-design/editor.md) de WYSIWYG.

>[!NOTE]
>
>Une fois installé, [!DNL Page Builder] remplace le paramètre par défaut du champ de configuration [!UICONTROL Mask for Meta Description]. La valeur passe de `{{name}} {{description}}` à `{{name}}`.
><br>
>Vous pouvez accéder à ce paramètre lorsque vous accédez à [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], développez [!UICONTROL Catalog] et choisissez [!UICONTROL Catalog] en dessous. Le champ [!UICONTROL Mask for Meta Description] se trouve dans la section [!UICONTROL Product Fields Auto-generation] .

>[!NOTE]
>
>Un utilisateur administrateur doit disposer d’autorisations [!UICONTROL Content] pour son [étendue de rôle](../systems/permissions-user-roles.md) pour voir [!UICONTROL Edit with Page Builder] boutons et pouvoir utiliser Page Builder.

Pour plus d’informations sur les options de configuration des outils avancés de gestion de contenu, consultez le [_Guide de référence de configuration_](../configuration-reference/general/content-management.md).

## Configurer [!DNL Page Builder]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** et vérifiez que **[!UICONTROL Enable Page Builder]** est défini sur `Yes`.

   ![Outils de contenu avancés](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Si vous êtes prêt à configurer [!DNL Google Maps], procédez comme suit :

   - Si nécessaire, suivez les instructions [Obtenir la clé API](https://developers.google.com/maps/documentation/javascript/get-api-key), puis copiez et collez votre **[!UICONTROL Google Maps API Key]**.

   - Pour modifier le **[!UICONTROL Google Maps Style]**, collez le code JSON généré par l’[[!DNL Google Maps] Assistant de mise en forme des API](https://mapstyle.withgoogle.com/).

   >[!NOTE]
   >
   >Voir [Média - Carte](map.md) pour plus d’informations sur l’utilisation de [!DNL Google Maps] dans votre contenu [!DNL Page Builder].

1. Pour configurer le nombre d’instructions dans la grille de colonne [!DNL Page Builder], procédez comme suit :

   - Par **[!UICONTROL Default Column Grid Size]**, saisissez le nombre de colonnes par défaut à afficher dans la grille.

   - Par **[!UICONTROL Maximum Column Grid Size]**, saisissez le plus grand nombre de colonnes que vous souhaitez rendre disponibles dans la grille.

   >[!NOTE]
   >
   >Voir [Disposition - Colonne](column.md) pour plus d’informations sur l’utilisation de la grille de colonnes lors de l’utilisation de votre contenu [!DNL Page Builder].

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Configurer les dispositions par défaut

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** et procédez comme suit :

   ![Dispositions par défaut](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Pour plus d’informations sur les options de configuration web, consultez le [_Guide de référence de configuration_](../configuration-reference/general/web.md#default-layouts).

   - Choisissez le **[!UICONTROL Default Product Layout]** à utiliser pour les pages de produits.

   - Choisissez le **[!UICONTROL Default Category Layout]** à utiliser pour les pages de catégorie.

   - Choisissez le **[!UICONTROL Default Page Layout]** à utiliser pour les pages CMS.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Désactiver le [!DNL Page Builder]

>[!NOTE]
>
>La désactivation de [!DNL Page Builder] remplace les outils de contenu avancés par l’éditeur [editor](../content-design/editor.md) WYSIWYG et peut entraîner des erreurs d’affichage dans le storefront. Le contenu que vous avez précédemment créé avec [!DNL Page Builder] peut ne pas être modifiable à partir de l’administration.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** et définissez **[!UICONTROL Enable Page Builder]** sur `No`.

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL Turn Off]**.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, [actualisez](../systems/cache-management.md) tout cache non valide.
