---
title: Optimisation des moteurs de recherche
description: Découvrez les outils d’optimisation du moteur de recherche (SEO) pour les sites Commerce et les bonnes pratiques pour une SEO optimale.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
TQID: https://experienceleague.adobe.com/cEXR2743G7ZzRSKqb9r344Osipo-R-GlqxNZwC-u-Nk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 0%

---

# Présentation de l’optimisation pour les moteurs de recherche

Le _référencement naturel_ (SEO) consiste à affiner le contenu et la présentation d’un site afin d’améliorer la façon dont les pages sont indexées par les moteurs de recherche. Commerce comprend différentes fonctionnalités pour prendre en charge votre effort continu d’optimisation du moteur de recherche.

>[!TIP]
>
>Pour Adobe Commerce as a Cloud Service, consultez les [directives SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=fr) de la documentation du Storefront Commerce

## Métadonnées

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Découvrez comment ajouter et améliorer des [métadonnées](meta-data.md) riches en mots-clés pour votre site et votre boutique.

## Utilisation d’un plan de site

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Un [plan de site](sitemap-xml.md) améliore la façon dont votre boutique est indexée par les moteurs de recherche et est conçu pour rechercher les pages qui pourraient être ignorées par les robots d&#39;exploration web. Un plan de site peut être configuré pour indexer toutes les pages et images.

## Réécritures d’URL

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

L’outil [Réécriture d’URL](url-rewrite.md) vous permet de modifier toute URL associée à un produit, une catégorie ou une page CMS.

## Robots pour moteurs de recherche

La configuration Commerce comprend des paramètres permettant de générer et de gérer des instructions pour les robots d&#39;exploration web et les robots qui indexent votre site. Si la demande de `robots.txt` atteint Commerce (plutôt qu&#39;un fichier physique), elle est acheminée dynamiquement vers le contrôleur robots. Les instructions sont des directives reconnues et suivies par la plupart des moteurs de recherche.

Par défaut, le fichier robots.txt généré par Commerce contient des instructions pour le robot d&#39;exploration web afin d’éviter d’indexer certaines parties du site qui contiennent des fichiers utilisés en interne par le système. Vous pouvez utiliser les paramètres par défaut ou définir vos propres instructions personnalisées pour tous les moteurs de recherche ou pour des moteurs spécifiques. Il existe de nombreux articles en ligne qui explorent le sujet en détail.

### Exemple d’instructions personnalisées

**Autorise un accès complet**

    User-agent:*
    Disallow:

**Interdit l’accès à tous les dossiers**

    User-agent:*
    Interdire : /

**Instructions par défaut**

    User-agent : *
    Disallow : /index.php/
    Disallow: /*?
    Disallow: /checkout/
    Disallow: /app/
    Disallow: /lib/
    Disallow: /*.php$
    Disallow: /pkginfo/
    Disallow: /report/
    Disallow: /var/
    Disallow: /catalog/
    Disallow: /customer/
    Disallow: /sendfriend/
    Disallow: /review/
    Disallow: /*SID=

### Configurer `robots.txt`

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la configuration **[!UICONTROL Global]** dans la première ligne de la grille et cliquez sur **[!UICONTROL Edit]**.

   ![Configuration de la conception globale](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Robots]**, puis procédez comme suit :

   ![Configuration de la conception - robots de moteurs de recherche](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Default Robots]** sur l’une des options suivantes :

     | Option | Description |
     |------|------------|
     | `INDEX, FOLLOW` | Indique aux robots d&#39;exploration web d’indexer le site et de vérifier ultérieurement les modifications. |
     | `NOINDEX, FOLLOW` | Indique aux robots d&#39;exploration web d’éviter d’indexer le site, mais de vérifier ultérieurement les modifications. |
     | `INDEX, NOFOLLOW` | Indique aux robots d&#39;exploration web d’indexer le site une fois, mais de ne suivre aucun lien sur la page. |
     | `NOINDEX, NOFOLLOW` | Indique aux robots d&#39;exploration web de ne pas indexer le site et de ne pas suivre les liens de la page. |

     {style="table-layout:auto"}

   - Si nécessaire, saisissez des instructions personnalisées dans la zone de **[!UICONTROL Edit Custom instruction of robots.txt file]**. Par exemple, lorsqu’un site est en développement, vous pouvez interdire l’accès à tous les dossiers.

   - Pour restaurer les instructions par défaut, cliquez sur **[!UICONTROL Reset to Default]**.

1. Cliquez ensuite sur **[!UICONTROL Save Configuration]**.
