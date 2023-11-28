---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL General] &gt; [!UICONTROL Content Management] de l’administrateur Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Options WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Affichage en magasin | Détermine si l’éditeur est activé pour le magasin. Options : activé par défaut/désactivé par défaut/désactivé complètement |
| [!UICONTROL WYSIWYG Editor] | Site Web | Détermine la version de l’éditeur TinyMCE utilisé pour l’éditeur WYSIWYG. Options : <br/>**`TinyMCE 5`**- (Par défaut) Utilise la version 5 de TinyMCE comme éditeur WYSIWYG par défaut.<br><br>_** Remarque :**_Une mise à jour de la bibliothèque TinyMCE 5.10 dans Adobe Commerce et Magento Open Source 2.4.5 résout une vulnérabilité qui permettait l’exécution arbitraire de JavaScript lors de la mise à jour d’une image ou d’un lien à l’aide de certains types d’URL. TinyMCE 3 a été abandonné dans la version 2.4.0 et supprimé dans la version 2.4.3. TinyMCE 4 a été supprimé dans la version 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Détermine si [URL statiques](../../content-design/catalog-urls-dynamic-media.md) sont utilisés pour le contenu multimédia référencé à partir de l’éditeur WYSIWYG. Le paramètre s’applique à tous les endroits où l’éditeur WYSIWYG est disponible, y compris les produits, les catégories, les pages et les blocs. Options : <br/>**`Yes`**: utilise des URL statiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG. Les URL statiques sont absolues et cassées si la variable [URL de base](../../stores-purchase/store-urls.md) des modifications du magasin.<br/>**`No`** (Par défaut) : utilise des URL dynamiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG, en fonction de la variable  `{{media url="..."}}` de . Les URL dynamiques sont relatives et ne rompent pas si l’URL de base du magasin change. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Hiérarchie des pages CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Active l’utilisation de la hiérarchie de pages pour vos pages de contenu. Options : `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Permet d’associer des métadonnées à des pages de la hiérarchie. Options : `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Détermine le style de menu par défaut. Options : `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![Outils de contenu avancé](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Détermine si la variable [!DNL Page Builder] des outils de contenu avancé sont disponibles. Options : <br/>**`Yes`**- La variable [!DNL Page Builder] Workspace s’affiche dans la section Contenu des pages, blocs, produits et catégories.<br/>**`No`** - Les outils d’édition CMS standard apparaissent dans la _[!UICONTROL Content]_des pages, des blocs, des produits et des catégories. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Détermine si la variable [!DNL Page Builder] les aperçus de contenu sont activés pour les produits et les catégories. Options : `Yes` / `No` <br/>**_Remarque :_**Défini sur `Yes` par défaut, la désactivation de l’aperçu peut empêcher tout problème de performances résultant du chargement des aperçus dans un formulaire de produit ou de catégorie. |
| [!UICONTROL Google Maps API Key] | Global | La variable [!DNL Google Maps] Clé API de votre compte Google. |
| [!UICONTROL Test Key] |  | Valide le [!DNL Google Maps] Clé API. |
| [!UICONTROL Google Maps Style] | Global | Collez le [!DNL Google Maps] appliquer un style au code JSON ici pour modifier l’aspect du type de contenu Carte . |
| [!UICONTROL Default Column Grid Size] | Global | Détermine le nombre de colonnes par défaut dans la variable [!DNL Page Builder] grid. |
| [!UICONTROL Maximum Column Grid Size] | Global | Détermine le nombre maximal de colonnes dans la variable [!DNL Page Builder] grid. |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>Le créateur de pages facilite la création de pages riches en contenu avec des dispositions personnalisées qui améliorent la narration visuelle et fidélisent les clients. Ces fonctionnalités sont conçues pour améliorer la qualité et réduire le temps et les frais liés à la création de pages personnalisées. Pour plus d’informations sur ces fonctionnalités et sur leur utilisation pour créer du contenu attrayant pour votre boutique Adobe Commerce ou Magento Open Source, voir [_Guide de l’utilisateur de Page Builder_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
