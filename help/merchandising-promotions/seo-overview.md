---
title: Optimisation des moteurs de recherche
description: Découvrez les outils d’optimisation du moteur de recherche (SEO) pour les sites Commerce et les bonnes pratiques pour une SEO optimale.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Présentation de l’optimisation pour les moteurs de recherche

Le _référencement naturel_ (SEO) consiste à affiner le contenu et la présentation d’un site afin d’améliorer la façon dont les pages sont indexées par les moteurs de recherche. Commerce comprend différentes fonctionnalités pour prendre en charge votre effort continu d’optimisation du moteur de recherche.

>[!TIP]
>
>Pour Adobe Commerce as a Cloud Service, consultez les [directives SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) de la documentation du Storefront Commerce

## Métadonnées

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Découvrez comment ajouter et améliorer des [métadonnées](meta-data.md) riches en mots-clés pour votre site et votre boutique.

## Utilisation d’un plan de site

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Un [plan de site](sitemap-xml.md) améliore la façon dont votre boutique est indexée par les moteurs de recherche et est conçu pour trouver les pages qui pourraient être ignorées par les robots d’exploration web. Un plan de site peut être configuré pour indexer toutes les pages et images.

## Réécritures d’URL

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

L’outil [Réécriture d’URL](url-rewrite.md) vous permet de modifier toute URL associée à un produit, une catégorie ou une page CMS.

## Robots pour moteurs de recherche

La configuration Commerce comprend des paramètres permettant de générer et de gérer des instructions pour les robots d’exploration et les robots web qui indexent votre site. Si la demande de `robots.txt` atteint Commerce (plutôt qu&#39;un fichier physique), elle est acheminée dynamiquement vers le contrôleur robots. Les instructions sont des directives reconnues et suivies par la plupart des moteurs de recherche.

Par défaut, le fichier robots.txt généré par Commerce contient des instructions pour que le moteur de recherche web évite d’indexer certaines parties du site qui contiennent des fichiers utilisés en interne par le système. Vous pouvez utiliser les paramètres par défaut ou définir vos propres instructions personnalisées pour tous les moteurs de recherche ou pour des moteurs spécifiques. Il existe de nombreux articles en ligne qui explorent le sujet en détail.

### Exemple d’instructions personnalisées

**Autorise un accès complet**

    User-agent:*
    Disallow:

**Interdit l’accès à tous les dossiers**

    User-agent:*
    Interdire : /

**Instructions par défaut**

    User-agent : *
    Refuser : /index.php/
    Refuser : /*?
    Interdire : /checkout/
    Interdire : /app/
    Interdire : /lib/
    Interdire : /*.php$
    Interdire : /pkginfo/
    Interdire : /report/
    Interdire : /var/
    Interdire : /catalog/
    Interdire : /customer/
    Interdire : /sendfriend/
    Interdire : /review/
    Interdire : /*SID=

### Configurer `robots.txt`

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la configuration **[!UICONTROL Global]** dans la première ligne de la grille et cliquez sur **[!UICONTROL Edit]**.

   ![Configuration de la conception globale](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Robots]**, puis procédez comme suit :

   ![Configuration de la conception - robots de moteurs de recherche](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Default Robots]** sur l’une des options suivantes :

     | Option | Description |
     |------|------------|
     | `INDEX, FOLLOW` | Indique aux robots d’exploration Web d’indexer le site et de vérifier ultérieurement les modifications. |
     | `NOINDEX, FOLLOW` | Indique aux robots d’exploration Web d’éviter d’indexer le site, mais de revenir ultérieurement pour prendre connaissance des modifications. |
     | `INDEX, NOFOLLOW` | Indique aux robots d’indexation web d’indexer le site une fois, mais de ne pas revenir ultérieurement pour connaître les modifications. |
     | `NOINDEX, NOFOLLOW` | Indique aux robots d’exploration Web d’éviter d’indexer le site et de ne pas revenir ultérieurement pour connaître les modifications. |

     {style="table-layout:auto"}

   - Si nécessaire, saisissez des instructions personnalisées dans la zone de **[!UICONTROL Edit Custom instruction of robots.txt file]**. Par exemple, lorsqu’un site est en développement, vous pouvez interdire l’accès à tous les dossiers.

   - Pour restaurer les instructions par défaut, cliquez sur **[!UICONTROL Reset to Default]**.

1. Cliquez ensuite sur **[!UICONTROL Save Configuration]**.
