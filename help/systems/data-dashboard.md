---
title: Tableau de bord de la gestion des données
description: En savoir plus sur le tableau de bord Data Management
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Tableau de bord de la gestion des données

Le tableau de bord Data Management fournit des informations sur les flux de données pour les produits Adobe Commerce SaaS. Utilisateurs de [!DNL Live Search], [!DNL Product Recommendations], et [!DNL Catalog Service] Vous pouvez afficher les états de synchronisation des produits et resynchroniser les données à partir d’un seul tableau de bord.

Le tableau de bord de Data Management se trouve à l’adresse *Système* > Transfert de données > *Tableau de bord de la gestion des données*.

![Tableau de bord de la gestion des données](assets/data-management-dashboard.png)

## Paramètres

Le bouton Paramètres situé sur le côté droit de la page ouvre la fenêtre [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) de la boîte de dialogue des paramètres.

Normalement, la variable [!DNL Catalog Sync] le processus s’exécute automatiquement, une fois par heure.

La resynchronisation des données de catalogue force le service à récupérer les données de la base de données Commerce, en s’assurant que les dernières modifications sont répercutées dans le service et sur votre site. Utilisez ce bouton si vous avez apporté plusieurs modifications au produit et que celles-ci doivent être mises à jour avant le processus de synchronisation automatique normal.

## État de la synchronisation

La variable _[!UICONTROL Sync]_le panneau d’état indique le nombre de produits qui ont été synchronisés au cours des trois dernières heures. Si vous effectuez des mises à jour peu fréquentes de votre catalogue, cette valeur est souvent égale à zéro. Cliquez sur **[!UICONTROL Refresh]**pour actualiser le nombre.

## Nombre de produits

Le panneau Nombre de produits indique le nombre total de produits du catalogue disponibles pour le service.

La variable [!DNL Catalog Service] tableau de bord indique le nombre total de produits dans le catalogue disponibles pour le service. Il s’agit généralement de tous les produits de la base de données Commerce.

Les tableaux de bord Recommendations de produit et Recherche en direct affichent le nombre total [_searchable_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) produits. Si certains produits ne sont pas configurés pour pouvoir faire l’objet d’une recherche, cela tient compte de la différence entre les totaux des produits. [!DNL Product Recommendations] et [!DNL Live Search], et [!DNL Catalog Service].

## Produits synchronisés

Le tableau Produits du catalogue synchronisé fournit des détails sur les produits de l’index. Par défaut, ce tableau est trié par &quot;Dernière mise à jour&quot;.

Pour rechercher un produit spécifique, utilisez le**[!UICONTROL Search by SKU]** champ .
Pour contrôler les colonnes affichées, cliquez sur **[!UICONTROL Customize Table]** à droite de la table.
