---
title: Tableau de bord de la gestion des données
description: Découvrez comment accéder à des informations sur les flux de données pour le service de catalogue, la recherche en direct, le Recommendations de produit.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Tableau de bord de la gestion des données

Le tableau de bord Data Management fournit des informations sur les flux de données pour les produits Adobe Commerce SaaS. Utilisateurs de [!DNL Live Search], [!DNL Product Recommendations], et [!DNL Catalog Service] Vous pouvez afficher les états de synchronisation des produits et resynchroniser les données à partir d’un seul tableau de bord.

Le tableau de bord de Data Management se trouve à l’adresse *Système* > Transfert de données > *Tableau de bord de la gestion des données*.

![Tableau de bord de la gestion des données](assets/data-management-dashboard.png)

## Paramètres

La variable **[!UICONTROL Settings]** sur le côté droit de la page, vous ouvrez la boîte de dialogue dans laquelle vous pouvez resynchroniser les données du catalogue.

La resynchronisation des données de catalogue force le service à récupérer les données de la base de données Commerce. Cette action est généralement utilisée lors de la première intégration lorsque la synchronisation du catalogue ne s’est pas exécutée pendant deux heures.

## État de la synchronisation

La variable _[!UICONTROL Sync]_le panneau d’état indique le nombre de produits qui ont été synchronisés au cours des trois dernières heures. Si vous effectuez des mises à jour peu fréquentes de votre catalogue, cette valeur est souvent égale à zéro. Cliquez sur **[!UICONTROL Refresh]**pour actualiser le nombre.

## Nombre de produits

Le panneau Nombre de produits indique le nombre total de produits du catalogue disponibles pour le service.

La variable [!DNL Product Recommendations] et [!DNL Live Search] Les tableaux de bord affichent le nombre total de _affichable_ produits. [!DNL Catalog Service] ne filtre pas les produits par éléments affichables. Par conséquent, si vous avez les deux [!DNL Catalog Service] et [!DNL Live Search] ou [!DNL Product Recommendations] installé, il est possible que les deux tableaux de bord affichent deux valeurs différentes pour le nombre de produits.

## Produits synchronisés

Le tableau Produits synchronisés fournit des détails sur les produits de l’index. Par défaut, ce tableau est trié par &quot;Dernière mise à jour&quot;.

Pour rechercher un produit spécifique, utilisez la méthode **[!UICONTROL Search by SKU]** champ .
Pour contrôler les colonnes affichées, cliquez sur **[!UICONTROL Customize Table]** à droite de la table.
