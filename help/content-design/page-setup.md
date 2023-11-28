---
title: Configuration de la page
description: Découvrez comment configurer les valeurs par défaut des principales parties d’une page de magasin.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuration de la page

Les sections principales de la page sont contrôlées, en partie, par un ensemble de balises de HTML standard. Certaines de ces balises peuvent être utilisées pour déterminer la sélection des polices, de la couleur, de la taille, des couleurs d’arrière-plan et des images utilisées dans chaque section de la page. D’autres paramètres contrôlent les éléments de la page, tels que le logo dans l’en-tête et la mention de copyright dans le pied de page. Ces sections correspondent à la structure sous-jacente de la page HTML et de nombreuses propriétés de base peuvent être définies à partir de l’administrateur.

- [HTML Head](#html-head)
- [En-tête](#header)
- [Pied de page](#footer)

![Sections de page de HTML](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML Head

Les paramètres de la section En-tête de HTML correspondent à la variable `<head>` d’une page de HTML et peut être configurée pour chaque vue de magasin. Outre les métadonnées relatives au titre, à la description et aux mots-clés de la page, la section comprend un lien vers l’icône favicon et divers scripts. Les instructions relatives aux robots de moteur de recherche et à l’affichage de l’avis de démonstration du magasin sont également configurées dans cette section.

### Configuration de l’en-tête du HTML

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _Autres paramètres_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL HTML Head]** .

   ![Paramètres de configuration de HTML Head](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Mettez à jour le [favicon](../getting-started/storefront-branding.md#add-a-favicon) si nécessaire.

1. Mettez à jour les paramètres de titre de page selon vos besoins :

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Vous pouvez utiliser un suffixe et/ou un préfixe avec le titre par défaut pour créer un titre en deux ou trois parties. Vous pouvez ajouter une barre verticale ou deux-points comme séparateur entre le préfixe ou le suffixe et le titre par défaut.

1. Ajoutez ou modifiez des métadonnées qui prennent en charge l’ optimisation du moteur de recherche (SEO) et aident les clients à se diriger vers votre boutique à partir des résultats de recherche :

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Saisissez les **[!UICONTROL Scripts and Style Sheets]** selon les besoins.

1. Activez ou désactivez la variable [avis de boutique de démonstration](../getting-started/storefront-branding.md#set-the-store-demo-notice) si nécessaire.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

### Descriptions des champs d’en-tête de HTML

| Champ | Portée | Description |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Affichage en magasin | Télécharge la petite image graphique qui apparaît dans la barre d’adresse et l’onglet du navigateur. Types de fichiers autorisés : ICO, PNG, APNG, GIF et JPG (JPEG). Tous les navigateurs ne prennent pas en charge ces formats. |
| [!UICONTROL Default Page Title] | Affichage en magasin | Titre qui s’affiche dans la barre de titre de chaque page lorsqu’il est affiché dans un navigateur. Le titre par défaut est utilisé pour toutes les pages, sauf si un autre titre est spécifié pour des pages individuelles. |
| [!UICONTROL Page Title Prefix] | Affichage en magasin | Un préfixe peut être ajouté devant le titre pour créer un titre en deux ou trois parties. Une barre verticale ou deux-points peuvent être utilisés comme séparateur à la fin du préfixe pour le différencier du texte du titre principal. |
| [!UICONTROL Page Title Suffix] | Affichage en magasin | Un suffixe peut être ajouté après le titre pour créer un titre en deux ou trois parties. Une barre verticale ou deux-points peuvent être utilisés comme séparateur à la fin du préfixe pour le différencier du texte du titre principal. |
| [!UICONTROL Default Meta Description] | Affichage en magasin | La description fournit un résumé de votre site pour les listes de moteurs de recherche et ne doit pas dépasser 160 caractères. |
| [!UICONTROL Default Meta Keywords] | Affichage en magasin | Série de mots-clés qui décrivent votre boutique, chacun séparé par une virgule. |
| [!UICONTROL Scripts and Style Sheets] | Affichage en magasin | Contient des scripts qui doivent être inclus dans le HTML avant la fermeture `<head>` balise . Par exemple, tout code JavaScript tiers qui doit être placé avant la variable `<body>` peut être saisie ici. |
| [!UICONTROL Display Demo Store Notice] | Affichage en magasin | Contrôle l’affichage de l’avis de boutique de démonstration en haut de la page. Options : `Yes` / `No` |

{style="table-layout:auto"}

## En-tête

La configuration En-tête identifie le chemin d’accès au logo de votre boutique et spécifie le logo, le texte de remplacement et le message de bienvenue.

![Paramètres de configuration des en-têtes](./assets/configuration-header.png){width="400" zoomable="yes"}

### Configuration de l’en-tête

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _Autres paramètres_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Header]** .

1. Apportez les modifications nécessaires à la vue de magasin :

   - [Logo](../getting-started/storefront-branding.md#upload-your-logo) paramètres
   - [Message de bienvenue](../getting-started/storefront-branding.md#change-the-welcome-message) paramètres

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

### Description des champs d’en-tête

| Champ | Portée | Description |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Affichage en magasin | Identifie le chemin d’accès au logo qui apparaît dans l’en-tête. Types de fichiers pris en charge : PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Affichage en magasin | Largeur de l’image de logo en pixels. |
| [!UICONTROL Logo Attribute Height] | Affichage en magasin | Hauteur de l’image de logo en pixels. |
| [!UICONTROL Welcome Text] | Affichage en magasin | Le message de bienvenue s’affiche dans l’en-tête de la page et comprend le nom des clients connectés. |
| [!UICONTROL Logo Image Alt] | Affichage en magasin | Texte de remplacement associé au logo. |
| [!UICONTROL Translate Title] | Affichage en magasin | Détermine si la variable `Page Title` ou `Meta Title` doit être traduit. |

{style="table-layout:auto"}

## Pied de page

La section Configuration du pied de page vous permet de mettre à jour la variable [avis de copyright](../getting-started/storefront-branding.md#change-the-copyright-notice) qui s’affiche au bas de la page, et saisissez les scripts divers qui doivent être positionnés avant la balise `<body>` balise .

![Paramètres de configuration du pied de page](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Configuration du pied de page

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _Autres paramètres_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Footer]** .

1. Apportez les modifications nécessaires au **[!UICONTROL Copyright]** et **[!UICONTROL Miscellaneous HTML]** paramètres.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

## Descriptions des champs de pied de page

| Champ | Portée | Description |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Affichage en magasin | Une zone de saisie dans laquelle vous pouvez charger des scripts divers sur le serveur qui doivent être placés juste avant la fermeture `<body>` balise . |
| [!UICONTROL Copyright] | Affichage en magasin | L’instruction de copyright qui apparaît au bas de chaque page. Pour inclure le symbole de copyright, utilisez l’entité de caractère de HTML `\&copy;` comme dans : `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Veillez à remplacer l’exemple d’avis de copyright par le vôtre. |
| [!UICONTROL Display Report Bugs Link] | Affichage en magasin | Détermine si le lien du rapport de bogue (pris en charge pour certains thèmes) est activé ou désactivé. |

{style="table-layout:auto"}
