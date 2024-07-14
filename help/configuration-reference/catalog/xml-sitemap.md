---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] de l’administrateur Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Options des catégories](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage en magasin | Détermine la fréquence de mise à jour des catégories du plan de site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage en magasin | Une valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan de site de catégorie par rapport à d’autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Options de produits](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage en magasin | Détermine la fréquence de mise à jour des produits du plan de site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage en magasin | Une valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan de site du produit par rapport à d’autres contenus. Zéro (`0.0`) a la priorité la plus faible. |
| [!UICONTROL Add Images into Sitemap] | Affichage en magasin | Détermine l’étendue de l’inclusion des images dans le plan du site. Options : `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Options de pages CMS](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage en magasin | Détermine la fréquence de mise à jour des pages CMS du plan de site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage en magasin | Une valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan de site de la page CMS par rapport à d’autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage en magasin | Détermine la fréquence de mise à jour des URL de stockage. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage en magasin | Une valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour de l’URL de magasin par rapport à d’autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Paramètres de génération](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage en magasin | Détermine si un plan de site XML est disponible pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Start Time] | Affichage en magasin | Indique l’heure, la minute et la seconde du jour où le plan du site est mis à jour. |
| [!UICONTROL Frequency] | Affichage en magasin | Détermine la fréquence de mise à jour du plan du site. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Affichage en magasin | Adresse électronique de la personne qui reçoit la notification en cas d’erreur lors du processus de mise à jour du plan du site. Pour plusieurs adresses, séparez-les par une virgule. |
| [!UICONTROL Error Email Sender] | Site Web | Identifie le contact du magasin qui apparaît comme l’expéditeur de la notification d’erreur. Options : `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Site Web | Identifie le modèle d’email utilisé pour la notification d’erreur. Modèle par défaut : `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![ Limites de fichier plan du site ](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Affichage en magasin | Détermine le nombre maximal d’URL pouvant être incluses dans un seul plan de site. |
| [!UICONTROL Maximum File Size] | Affichage en magasin | Détermine la taille maximale du plan de site généré, en octets. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Paramètres d’envoi du moteur de recherche](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Affichage en magasin | Permet l’envoi de directives pour le fichier robots.txt. Options : `Yes` / `No` |

{style="table-layout:auto"}
