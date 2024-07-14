---
title: Optimisation du moteur de recherche
description: Découvrez les outils d’optimisation du moteur de recherche (SEO) pour les sites Commerce et les bonnes pratiques pour optimiser l’optimisation du référencement.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Présentation du SEO

_L’optimisation du moteur de recherche_ est une pratique consistant à affiner le contenu et la présentation d’un site afin d’améliorer la manière dont les pages sont indexées par les moteurs de recherche. Commerce comprend différentes fonctionnalités pour prendre en charge votre travail d’optimisation pour les moteurs de recherche en cours.

## Métadonnées

En savoir plus sur l’ajout et l’amélioration de [métadonnées](meta-data.md) riches en mots-clés pour votre site et votre magasin.

## Utilisation d’un plan de site

Une [carte du site](sitemap-xml.md) améliore la façon dont votre boutique est indexée par les moteurs de recherche et est conçue pour trouver des pages qui peuvent être ignorées par les moteurs de recherche web. Un plan du site peut être configuré pour indexer toutes les pages et toutes les images.

## URL rewrites

L’outil [ de réécriture d’URL ](url-rewrite.md) vous permet de modifier toute URL associée à un produit, une catégorie ou une page CMS.

## Robots de moteur de recherche

La configuration de Commerce comprend des paramètres pour générer et gérer des instructions pour les robots et les robots d’indexation de votre site web. Si la demande de `robots.txt` atteint Commerce (plutôt qu’un fichier physique), elle est acheminée dynamiquement vers le contrôleur des robots. Les instructions sont des directives reconnues et suivies par la plupart des moteurs de recherche.

Par défaut, le fichier robots.txt généré par Commerce contient des instructions pour le moteur de recherche Web afin d’éviter l’indexation de certaines parties du site qui contiennent des fichiers utilisés en interne par le système. Vous pouvez utiliser les paramètres par défaut ou définir vos propres instructions personnalisées pour tous les moteurs de recherche ou pour certains d’entre eux. De nombreux articles en ligne explorent le sujet en détail.

### Exemple d’instructions personnalisées

**Permet Un Accès Complet**

    User-agent:*
    Disallow:

**Désactive l’accès à tous les dossiers**

    User-agent:*
    Disallow: /

**Instructions par défaut**

    User-agent: *
    Disallow: /index.php/
    Disallow: /*?
    Ne pas autoriser : /checkout/
    Ne pas autoriser : /app/
    Ne pas autoriser : /lib/
    Ne pas autoriser : /*.php$
    Ne pas autoriser : /pkginfo/
    Ne pas autoriser : /report/
    Ne pas autoriser : /var/
    Ne pas autoriser : /catalog/
    Ne pas autoriser : /customer/
    Ne pas autoriser : /sendautoriser 10}Disallow: /review/
    Disallow: /*SID=

    
### Configurer `robots.txt`

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la configuration **[!UICONTROL Global]** dans la première ligne de la grille et cliquez sur **[!UICONTROL Edit]**.

   ![Configuration de conception globale](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Faites défiler l’écran vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Search Engine Robots]** et procédez comme suit :

   ![Configuration de conception - robots de moteur de recherche](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Default Robots]** sur l’une des options suivantes :

     | Option | Description |
     |------|------------|
     | `INDEX, FOLLOW` | Indique aux moteurs de recherche Web d’indexer le site et de vérifier ultérieurement les modifications. |
     | `NOINDEX, FOLLOW` | Indique aux moteurs de recherche Web d’éviter d’indexer le site, mais de vérifier les modifications ultérieurement. |
     | `INDEX, NOFOLLOW` | Indique aux moteurs de recherche Web d’indexer le site une seule fois, mais de ne pas vérifier les modifications ultérieurement. |
     | `NOINDEX, NOFOLLOW` | Indique aux moteurs de recherche Web d’éviter d’indexer le site et de ne pas vérifier les modifications ultérieurement. |

     {style="table-layout:auto"}

   - Si nécessaire, saisissez des instructions personnalisées dans la zone **[!UICONTROL Edit Custom instruction of robots.txt file]**. Par exemple, lorsqu’un site est en cours de développement, vous pouvez interdire l’accès à tous les dossiers.

   - Pour restaurer les instructions par défaut, cliquez sur **[!UICONTROL Reset to Default]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Configuration]**.
