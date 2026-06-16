---
title: '[!UICONTROL Catalog] > [!UICONTROL XML Sitemap]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL XML Sitemap] de [!UICONTROL Catalog] &gt ; de l’administrateur Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
TQID: https://experienceleague.adobe.com/1oTTRT977C3zcifhCRFBuXf7ny-6rqGSC--enriyj-Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Options de catégories](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage de la boutique | Détermine la fréquence de mise à jour des catégories de plan de site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage de la boutique | Valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan de site des catégories par rapport aux autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Options de produits](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage de la boutique | Détermine la fréquence de mise à jour des produits du plan de site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage de la boutique | Valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan du site du produit par rapport aux autres contenus. Zéro (`0.0`) a la priorité la plus faible. |
| [!UICONTROL Add Images into Sitemap] | Affichage de la boutique | Détermine la mesure dans laquelle les images sont incluses dans le plan du site. Options : `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Options de pages ](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage de la boutique | Détermine la fréquence de mise à jour des pages CMS du plan du site. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage de la boutique | Valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour du plan de site de la page CMS par rapport aux autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Affichage de la boutique | Détermine la fréquence de mise à jour des URL des magasins. Options : `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Affichage de la boutique | Valeur comprise entre `0.0` et `1.0` qui détermine la priorité des mises à jour des URL de boutique par rapport à d’autres contenus. Zéro (`0.0`) a la priorité la plus faible. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Paramètres de génération](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage de la boutique | Détermine si un plan de site XML est disponible pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Generation Method] | Affichage de la boutique | Détermine comment le plan de site XML est généré. `Standard` utilise le processus de génération synchrone traditionnel et traite toutes les données en mémoire, tandis que `Batch` utilise un mode batch asynchrone optimisé en mémoire pour une plus grande flexibilité et évolutivité. Cette option est disponible à partir de la version 2.4.9. Options : `Standard` / `Batch` |
| [!UICONTROL Start Time] | Affichage de la boutique | Indique l’heure, la minute et la seconde de la journée où le plan de site est mis à jour. |
| [!UICONTROL Frequency] | Affichage de la boutique | Détermine la fréquence de mise à jour du plan du site. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Affichage de la boutique | Adresse e-mail de la personne qui reçoit la notification en cas d’erreur lors du processus de mise à jour du plan de site. Pour plusieurs adresses, séparez-les par une virgule. |
| [!UICONTROL Error Email Sender] | Site internet | Identifie le contact du magasin qui apparaît comme l’expéditeur de la notification d’erreur. Options : `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Site internet | Identifie le modèle d’e-mail utilisé pour la notification d’erreur. Modèle par défaut : `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Limites du fichier de plan de site](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Affichage de la boutique | Détermine le nombre maximal d’URL qui peuvent être incluses dans un seul plan de site. |
| [!UICONTROL Maximum File Size] | Affichage de la boutique | Détermine la taille maximale du plan de site généré, en octets. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Paramètres d’envoi du moteur de recherche](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Affichage de la boutique | Permet l&#39;envoi de directives pour le fichier robots.txt. Options : `Yes` / `No` |

{style="table-layout:auto"}
