---
title: Tableau de bord de la gestion des données
description: Découvrez comment accéder à des insights sur les flux de données pour les  [!DNL Catalog Service], [!DNL Live Search] et [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Tableau de bord de la gestion des données

Le tableau de bord Data Management offre un aperçu de l’état de synchronisation des données de produit transférées de la base de données Commerce vers les services SaaS Commerce. Les utilisateurs peuvent facilement surveiller les états de synchronisation des produits et lancer la resynchronisation des données à partir d’un tableau de bord unifié. Cette fonctionnalité fournit des informations précieuses sur la disponibilité des données de produit pour votre storefront, afin qu’elles puissent être rapidement affichées pour vos clients.

## Audience

Le tableau de bord de Data Management est disponible sans frais supplémentaires pour tous les marchands Commerce utilisant [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) ou [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) avec une licence active.

Le tableau de bord de Data Management se trouve à l’emplacement suivant : *Système* > Transfert de données > *Tableau de bord de Data Management*.

![Tableau de bord de Data Management](assets/data-management-dashboard.png)

Le tableau de bord contient les champs suivants :

| Champ | Description |
|--- |--- |
| Portée | Site web spécifique pour les données synchronisées. |
| [!DNL Product Recommendations] | Affiche l’état de synchronisation, le nombre de produits synchronisés et un tableau des [ produits synchronisés affichables ](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) pour [!DNL Product Recommendations]. |
| [!DNL Live Search] | Affiche l’état de synchronisation, le nombre de produits synchronisés et un tableau des [ produits synchronisés affichables ](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) pour [!DNL Live Search]. |
| [!DNL Catalog Service] | Affiche l’état de synchronisation, le nombre de produits synchronisés et un tableau des produits synchronisés pour [!DNL Catalog Service]. |
| Paramètres | Ouvre une boîte de dialogue dans laquelle vous pouvez [resynchroniser manuellement les données du catalogue ](#resync-catalog-data). |
| État de la synchronisation | Affiche le nombre de produits qui ont été transférés de la base de données Commerce vers l’un des services SaaS au cours des trois dernières heures. Si vous effectuez des mises à jour peu fréquentes de votre catalogue, cette valeur est souvent égale à zéro. Si une synchronisation est en cours, cliquez sur **[!UICONTROL Refresh]** pour obtenir un nombre mis à jour. |
| Nombre de produits | Reflète le nombre total de produits du catalogue disponibles pour le service. Les tableaux de bord [!DNL Product Recommendations] et [!DNL Live Search] affichent le nombre total de produits _affichables_. [!DNL Catalog Service] ne filtre pas les produits par affichables. Par conséquent, si [!DNL Catalog Service] et [!DNL Live Search] ou [!DNL Product Recommendations] sont installés, il est possible que les deux tableaux de bord affichent deux valeurs différentes pour le nombre de produits. |
| Produits synchronisés | Fournit des détails sur les produits de l’index Commerce principal. Par défaut, ce tableau est trié par &quot;Dernière mise à jour&quot;. Pour rechercher un produit spécifique, utilisez le champ **[!UICONTROL Search by SKU]**. Pour contrôler les colonnes affichées, cliquez sur **[!UICONTROL Customize Table]** à droite du tableau. |

## Utilisation du tableau de bord Data Management

Lorsque vous mettez à jour des produits dans la base de données Commerce, les données de produit sont transférées vers les services SaaS en fonction de la configuration de votre système. Lorsque le processus de synchronisation démarre, le **nombre de produits** indique le nombre de produits envoyés aux services SaaS.

>[!IMPORTANT]
>
>Le temps nécessaire pour terminer la synchronisation varie en fonction de la taille de votre catalogue et du volume des données mises à jour.

Lorsque le nombre de produits traités correspond au nombre de produits mis à jour, cela indique que la synchronisation est terminée.

>[!NOTE]
>
>Adobe fournit également une interface de ligne de commande et des journaux système que les développeurs et les intégrateurs système peuvent utiliser pour gérer et suivre les opérations de synchronisation et résoudre les erreurs pour les services SaaS Commerce. Pour plus d’informations, consultez le [Guide d’exportation des données SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Liste des produits synchronisés

Pour afficher les détails d’un produit synchronisé, cliquez sur le produit dans le tableau.

![Détails Du Produit Syncd](assets/sync-product-detail.png)

### Resynchronisation des données de catalogue

Pour vous assurer que vos services Commerce SaaS sont toujours à jour avec les dernières informations sur les produits, vous devez [ implémenter un planning](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) pour synchroniser les données du catalogue.

Bien que vous puissiez [lancer manuellement](#manually-resync-catalog) une resynchronisation de données de catalogue de la base de données Commerce vers les services SaaS, cela n’est pas recommandé, car cela peut augmenter la charge sur les ressources matérielles. Toutefois, la resynchronisation manuelle du catalogue peut s’avérer nécessaire dans les scénarios suivants :

- Lorsque des modifications importantes sont apportées à votre catalogue de produits, telles que l’ajout de nouveaux produits, la mise à jour des détails du produit ou la modification de catégories,

- Si vous constatez des incohérences ou des problèmes de performances lors de l’affichage des données de produit sur vos vitrines

- Suite à toute mise à jour ou modification des intégrations entre la base de données Commerce et les services SaaS

- Lors du déploiement de personnalisations ou de configurations ayant un impact sur la gestion des données de produit ou les processus de synchronisation

En adhérant à ces directives et en resynchronisant de manière proactive les données de catalogue si nécessaire, vous pouvez maintenir la cohérence, la précision et la fiabilité des données dans votre écosystème Adobe Commerce.

#### resynchronisation manuelle du catalogue

Si vous devez resynchroniser les données du catalogue, cliquez sur **[!UICONTROL Settings]** sur le côté droit de la page pour afficher une boîte de dialogue dans laquelle vous pouvez lancer une nouvelle synchronisation. La resynchronisation des données de catalogue force le service à récupérer les données de la base de données Commerce vers les services SaaS.

![Synchroniser manuellement les produits](assets/resync-data.png)
