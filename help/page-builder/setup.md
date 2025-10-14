---
title: '[!DNL Page Builder] setup'
description: Découvrez la configuration des fonctionnalités  [!DNL Page Builder] dans Admin pour Adobe Commerce et Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] setup

Lorsqu’il est activé dans la configuration, [!DNL Page Builder] est l’outil de création de contenu par défaut pour les pages CMS, les blocs et les blocs dynamiques. En outre, le bouton _[!UICONTROL Enable Advanced CMS]_&#x200B;propose [!DNL Page Builder] comme option pour les catégories et les produits. Vous pouvez également choisir la [mise en page](../content-design/page-layout.md) par défaut que vous souhaitez utiliser pour les produits, les catégories et les pages CMS. [!DNL Page Builder] n’est pas disponible pour le contenu de la newsletter, qui utilise l’ [éditeur](../content-design/editor.md) WYSIWYG.

>[!NOTE]
>
>Lorsqu&#39;il est installé, [!DNL Page Builder] remplace le paramètre par défaut du champ de configuration [!UICONTROL Mask for Meta Description]. La valeur a été changée de `{{name}} {{description}}` en `{{name}}`.
><br>
>Vous pouvez accéder à ce paramètre lorsque vous accédez à [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], développez [!UICONTROL Catalog] et choisissez [!UICONTROL Catalog] en dessous. Le champ [!UICONTROL Mask for Meta Description] se trouve dans la section [!UICONTROL Product Fields Auto-generation].

>[!NOTE]
>
>Un utilisateur administrateur doit disposer de [!UICONTROL Content] autorisations pour sa [portée de rôle](../systems/permissions-user-roles.md) pour afficher les boutons [!UICONTROL Edit with Page Builder] et pouvoir utiliser le générateur de pages.

Pour plus d’informations sur les options de configuration des outils avancés de gestion de contenu, consultez le [_Guide de référence de configuration_](../configuration-reference/general/content-management.md).

## Configurer [!DNL Page Builder]

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![&#x200B; Développeur de sélecteur &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** et vérifiez que **[!UICONTROL Enable Page Builder]** est défini sur `Yes`.

   ![Outils de contenu avancé](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Si vous êtes prêt à configurer [!DNL Google Maps], procédez comme suit :

   - Si nécessaire, suivez les instructions [Obtenir la clé API][1], puis copiez et collez votre **[!UICONTROL Google Maps API Key]**.

   - Pour modifier le **[!UICONTROL Google Maps Style]**, collez le code JSON généré par l’ [[!DNL Google Maps] assistant de style des API][2].

   >[!NOTE]
   >
   >Voir [Media - Map](map.md) pour plus d’informations sur l’utilisation de [!DNL Google Maps] dans votre contenu [!DNL Page Builder].

1. Pour configurer le nombre de directives dans la grille de colonnes [!DNL Page Builder], procédez comme suit :

   - Pour **[!UICONTROL Default Column Grid Size]**, saisissez le nombre de colonnes par défaut à afficher dans la grille.

   - Pour **[!UICONTROL Maximum Column Grid Size]**, saisissez le plus grand nombre de colonnes que vous souhaitez voir disponibles dans la grille.

   >[!NOTE]
   >
   >Voir [Disposition - Colonne](column.md) pour plus d’informations sur l’utilisation de la grille de colonnes lors de l’utilisation de votre contenu [!DNL Page Builder].

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Configuration des dispositions par défaut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** et procédez comme suit :

   ![Disposition par défaut](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Pour plus d’informations sur les options de configuration Web, consultez le [_Guide de référence de configuration_](../configuration-reference/general/web.md#default-layouts).

   - Sélectionnez le **[!UICONTROL Default Product Layout]** que vous souhaitez utiliser pour les pages de produits.

   - Sélectionnez le **[!UICONTROL Default Category Layout]** à utiliser pour les pages de catégorie.

   - Sélectionnez le **[!UICONTROL Default Page Layout]** que vous souhaitez utiliser pour les pages CMS.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Désactiver [!DNL Page Builder]

>[!NOTE]
>
>La désactivation de [!DNL Page Builder] remplace les outils de contenu avancés par l’éditeur [&#x200B; WYSIWYG &#x200B;](../content-design/editor.md) et peut entraîner des erreurs d’affichage dans le storefront. Le contenu que vous avez précédemment créé avec [!DNL Page Builder] peut ne pas être modifiable à partir de l’administrateur.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![&#x200B; Développeur de sélecteur &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** et définissez **[!UICONTROL Enable Page Builder]** sur `No`.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Turn Off]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, [actualiser](../systems/cache-management.md) n’importe quel cache non valide.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
