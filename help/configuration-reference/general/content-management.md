---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL General] d’[!UICONTROL Content Management] &gt; de l’administrateur Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Options WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Affichage de la boutique | Détermine si l’éditeur est activé pour le magasin. Options : Activé par défaut/Désactivé par défaut/Désactivé complètement |
| [!UICONTROL WYSIWYG Editor] | Site internet | Détermine la version de l’éditeur TinyMCE utilisé pour l’éditeur WYSIWYG. Options : <br/>**`TinyMCE 5`**- (par défaut) Utilise TinyMCE version 5 comme éditeur WYSIWYG par défaut.<br><br>_ **&#x200B; Remarque :**&#x200B;_une mise à jour de la bibliothèque TinyMCE 5.10 dans Adobe Commerce et Magento Open Source 2.4.5 résout une vulnérabilité qui permettait l’exécution arbitraire de JavaScript lors de la mise à jour d’une image ou d’un lien à l’aide de certains types d’URL. TinyMCE 3 a été abandonné dans la version 2.4.0 et supprimé dans la version 2.4.3. TinyMCE 4 a été supprimé dans la version 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Détermine si les [URL statiques](../../content-design/catalog-urls-dynamic-media.md) sont utilisées pour le contenu multimédia référencé à partir de l’éditeur WYSIWYG. Le paramètre s’applique à tous les emplacements où l’éditeur WYSIWYG est disponible, y compris les produits, les catégories, les pages et les blocs. Options : <br/>**`Yes`**- utilise des URL statiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG. Les URL statiques sont absolues et interrompues si l’[URL de base](../../stores-purchase/store-urls.md) du magasin change.<br/>**`No`** (par défaut) - Utilise des URL dynamiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG, en fonction de la directive `{{media url="..."}}`. Les URL dynamiques sont relatives et ne sont pas rompues si l’URL de base du magasin change. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

Hiérarchie de page CMS ![](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Active l’utilisation de la hiérarchie de page pour vos pages de contenu. Options : `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Permet d’associer des métadonnées à des pages dans la hiérarchie. Options : `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Détermine le style de menu par défaut. Options : `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Outils de contenu avancés](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Détermine si les outils de contenu avancés [!DNL Page Builder] sont disponibles. Options : <br/>**`Yes`**- L’espace de travail [!DNL Page Builder] s’affiche dans la section Contenu des pages, des blocs, des produits et des catégories.<br/>**`No`** - Les outils d’édition CMS standard apparaissent dans la section _[!UICONTROL Content]_&#x200B;des pages, blocs, produits et catégories. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Détermine si les aperçus de contenu [!DNL Page Builder] sont activés pour les produits et les catégories. Options : `Yes` / `No` <br/>**_Note:_** cette option est définie sur `Yes` par défaut, mais la désactivation de l’aperçu peut éviter tout problème de performances résultant du chargement des aperçus dans un formulaire de produit ou de catégorie. |
| [!UICONTROL Google Maps API Key] | Global | Clé API [!DNL Google Maps] de votre compte Google. |
| [!UICONTROL Test Key] |  | Valide la clé API [!DNL Google Maps]. |
| [!UICONTROL Google Maps Style] | Global | Collez le code JSON de style [!DNL Google Maps] ici pour modifier l’aspect du type de contenu Map. |
| [!UICONTROL Default Column Grid Size] | Global | Détermine le nombre de colonnes par défaut dans la grille de [!DNL Page Builder]. |
| [!UICONTROL Maximum Column Grid Size] | Global | Détermine le nombre maximal de colonnes dans la grille de [!DNL Page Builder]. |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder facilite la création de pages riches en contenu avec des mises en page personnalisées qui améliorent votre storytelling visuelle et favorisent l’engagement et la fidélité des clients. Ces fonctionnalités sont conçues pour améliorer la qualité et réduire le temps et les dépenses liés à la production de pages personnalisées. Pour plus d’informations sur ces fonctionnalités et leur utilisation pour créer du contenu attrayant pour votre boutique Adobe Commerce ou Magento Open Source, consultez le [_Guide d’utilisation de Page Builder_](../../page-builder/guide-overview.md).
