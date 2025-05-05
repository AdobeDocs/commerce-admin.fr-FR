---
title: Tableau de bord de gestion des données
description: Découvrez comment accéder aux informations sur les flux de données pour [!DNL Catalog Service],  [!DNL Live Search] et  [!DNL Product Recommendation].
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Tableau de bord de gestion des données

Le tableau de bord de gestion des données offre un aperçu de l’état de synchronisation des données de produit transférées de la base de données Commerce vers les services SaaS Commerce. Les utilisateurs peuvent facilement surveiller les états de synchronisation des produits et lancer une resynchronisation des données à partir d’un tableau de bord unifié. Cette fonctionnalité fournit des informations précieuses sur la disponibilité des données de produit pour votre storefront, afin qu’elles puissent être rapidement affichées pour vos acheteurs.

## Audience

Le tableau de bord de gestion des données est disponible sans frais supplémentaires pour tous les commerçants Commerce utilisant [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/fr/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/fr/docs/commerce/live-search/guide-overview) ou [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/fr/docs/commerce/catalog-service/guide-overview) avec une licence principale.

Le tableau de bord de gestion des données se trouve à l’adresse *Système* > Transfert de données > *Tableau de bord de gestion des données*.

![Tableau de bord de gestion des données](assets/data-management-dashboard.png)

Le tableau de bord contient les champs suivants :

| Champ | Description |
|--- |--- |
| Champ d’application | Site web spécifique pour les données synchronisées. |
| [!DNL Product Recommendations] | Affiche le statut de synchronisation, le nombre de produits synchronisés et un tableau des produits synchronisés [affichables](https://experienceleague.adobe.com/fr/docs/commerce-admin/config/catalog/inventory#stock-options) pour [!DNL Product Recommendations]. |
| [!DNL Live Search] | Affiche le statut de synchronisation, le nombre de produits synchronisés et un tableau des produits synchronisés [affichables](https://experienceleague.adobe.com/fr/docs/commerce-admin/config/catalog/inventory#stock-options) pour [!DNL Live Search]. |
| [!DNL Catalog Service] | Affiche le statut de synchronisation, le nombre de produits synchronisés et un tableau des produits synchronisés pour [!DNL Catalog Service]. |
| Paramètres | Ouvre une boîte de dialogue dans laquelle vous pouvez [ resynchroniser manuellement les données du catalogue ](#resync-catalog-data). |
| Statut de synchronisation | Affiche le nombre de produits qui ont été transférés de la base de données Commerce vers l&#39;un des services SaaS au cours des trois dernières heures. Si vous effectuez des mises à jour peu fréquentes de votre catalogue, cette valeur est souvent égale à zéro. Si une synchronisation est en cours, cliquez sur **[!UICONTROL Refresh]** pour obtenir un comptage mis à jour. |
| Nombre de produits | Reflète le nombre total de produits de catalogue disponibles pour le service. Les tableaux de bord [!DNL Product Recommendations] et [!DNL Live Search] affichent le nombre total de produits _affichables_. [!DNL Catalog Service] ne filtre pas les produits en fonction du nombre d’affichages. Par conséquent, si vous avez installé à la fois [!DNL Catalog Service] et [!DNL Live Search] ou [!DNL Product Recommendations], il est possible que les deux tableaux de bord affichent deux valeurs différentes pour le nombre de produits. |
| Produits synchronisés | Fournit des détails sur les produits de l’index Commerce principal. Par défaut, ce tableau est trié par « Dernière mise à jour ». Pour rechercher un produit spécifique, utilisez le champ **[!UICONTROL Search by SKU]** . Pour contrôler les colonnes à afficher, cliquez sur **[!UICONTROL Customize Table]** à droite du tableau. |

## Utilisation du tableau de bord de gestion des données

Lorsque vous mettez à jour des produits dans la base de données Commerce, les données des produits sont transférées vers les services SaaS en fonction de la configuration de votre système. Lorsque le processus de synchronisation démarre, **Nombre de produits** indique le nombre de produits envoyés aux services SaaS.

>[!IMPORTANT]
>
>Le temps nécessaire à la synchronisation varie en fonction de la taille de votre catalogue et du volume de données mises à jour.

Lorsque le nombre de produits traités correspond au nombre de produits mis à jour, cela indique que la synchronisation est terminée.

>[!NOTE]
>
>Adobe fournit également une interface de ligne de commande et des journaux système que les développeurs et les intégrateurs système peuvent utiliser pour gérer et suivre les opérations de synchronisation et résoudre les erreurs pour les services SaaS Commerce. Pour plus d&#39;informations, consultez le [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/fr/docs/commerce/saas-data-export/overview).

### Liste des produits synchronisés

Pour afficher les détails d’un produit synchronisé, cliquez sur le produit dans le tableau.

![Détails du produit Syncd](assets/sync-product-detail.png)

### Resynchroniser les données du catalogue

Pour vous assurer que vos services SaaS Commerce sont toujours à jour avec les dernières informations sur les produits, vous devez [implémenter un planning](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) pour synchroniser les données du catalogue.

Bien que vous puissiez [initier manuellement](#manually-resync-catalog) une resynchronisation des données de catalogue de la base de données Commerce vers les services SaaS, elle n’est pas recommandée, car elle peut augmenter la charge sur les ressources matérielles. Cependant, une resynchronisation manuelle du catalogue peut être nécessaire dans les scénarios suivants :

- Chaque fois que des modifications importantes sont apportées à votre catalogue de produits, telles que l’ajout de nouveaux produits, la mise à jour des détails du produit ou la modification de catégories

- Si vous constatez des incohérences ou des problèmes de performances dans l’affichage des données de produits sur vos storefronts

- À la suite de mises à jour ou de modifications apportées aux intégrations entre la base de données Commerce et les services SaaS

- Lors du déploiement de personnalisations ou de configurations qui affectent la gestion des données de produit ou les processus de synchronisation

En suivant ces instructions et en resynchronisant proactivement les données de catalogue selon les besoins, vous pouvez maintenir la cohérence, la précision et la fiabilité des données dans l’ensemble de votre écosystème Adobe Commerce.

#### Resynchronisation manuelle du catalogue

Si vous devez resynchroniser les données du catalogue, cliquez sur **[!UICONTROL Settings]** sur le côté droit de la page pour afficher une boîte de dialogue dans laquelle vous pouvez lancer une resynchronisation. La resynchronisation des données de catalogue force le service à récupérer les données de la base de données Commerce vers les services SaaS.

![Synchronisation manuelle des produits](assets/resync-data.png)
