---
title: Gestion des clés d’accès restreint dans Commerce
description: Créez, attribuez et supprimez les clés d’accès restreint qui sécurisent les vues de catalogue partagé B2B synchronisées avec Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# Gestion des clés d’accès restreintes

Utilisez la page Clés d&#39;accès restreintes pour gérer les clés d&#39;accès pour les vues de catalogue privées créées par le [!DNL Adobe Commerce Optimizer Connector for B2B]. Le connecteur synchronise les configurations de catalogue partagé B2B d’Adobe Commerce vers Adobe Commerce Optimizer.

>[!NOTE]
>
>Pour les clés créées manuellement utilisées pour gérer des catalogues privés dans des scénarios non B2B, tels que les portails de partenaire, gérez les clés à partir de [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}.

## Audience et disponibilité {#audience}

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets d’infrastructure cloud et locaux d’Adobe Commerce."}

La page [!UICONTROL Restricted Access Keys] est disponible pour Adobe Commerce on Cloud Infrastructure et les commerçants sur site qui utilisent des catalogues partagés B2B avec le [!DNL Adobe Commerce Optimizer Connector for B2B]. Le connecteur installe et active automatiquement la page.

Lorsqu’une vue de catalogue est créée pour la première fois pour un catalogue partagé, le connecteur génère et affecte automatiquement une clé. Utilisez cette page pour afficher cette clé et pour créer, attribuer ou supprimer des clés supplémentaires.

## Accès à la page Clés d’accès restreint {#access-restricted-access-keys-page}

Dans la zone d’administration, accédez à **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Page Clés d’accès limité répertoriant les clés et les vues de catalogue qui leur sont attribuées](assets/restricted-access-keys.png){width="600" zoomable="yes"}

Cette page répertorie toutes les clés, qu’elles soient affectées ou non à une vue de catalogue. Pour attribuer une clé à une vue de catalogue spécifique, utilisez plutôt l’action [!UICONTROL Edit Restricted Access Keys] sur cette vue de catalogue. Voir [Attribuer des clés à une vue de catalogue](#assign-keys-to-a-catalog-view).

## Résumé des clés d&#39;accès restreint {#restricted-access-keys-summary}

La grille contient une clé par ligne.

| Champ | Description |
| --- | --- |
| **Identifiant de clé** | Identifiant de clé unique. |
| **Titre** | Libellé que vous fournissez pour identifier la clé. |
| **Vues de catalogue affectées** | Vues de catalogue auxquelles cette clé est actuellement attribuée. |
| **Expire À** | Date d’expiration de la clé. |
| **Actions** | Actions au niveau des lignes. Voir [Gestion des clés](#manage-keys). |

## Gestion des clés {#manage-keys}

- **[!UICONTROL Create Key]** : génère une nouvelle paire de clés non affectée. Commerce génère la paire de clés et stocke la clé privée. La clé publique n’est pas enregistrée auprès de [!DNL Adobe Commerce Optimizer] tant que vous ne l’avez pas affectée à une vue de catalogue.
- **[!UICONTROL View Public Key]** : ouvre une vue en lecture seule de la clé publique de la clé, afin que vous puissiez la copier pour réenregistrer ou resynchroniser la clé si nécessaire. La clé privée n’est jamais affichée.
- **[!UICONTROL Delete]** : supprime la clé et révoque son enregistrement à distance dans [!DNL Adobe Commerce Optimizer]. Les jetons Storefront déjà émis avec cette clé restent valides jusqu’à leur expiration. Cette action est irréversible.

>[!NOTE]
>
>Une clé expirée ne peut être supprimée que. Vous ne pouvez pas affecter ni annuler l’affectation d’une clé expirée.

## Création d’une clé

Sur la page [!UICONTROL Restricted Access Keys], créez une clé en sélectionnant **[!UICONTROL Create Key]**.

Commerce génère une nouvelle paire de clés et stocke la clé privée. Le tableau Clés d’accès limité est mis à jour avec une nouvelle entrée de clé indiquant l’ID de clé unique. Utilisez cette [!UICONTROL Key ID] lorsque vous affectez la clé à une vue de catalogue.

La clé publique n’est pas enregistrée auprès de [!DNL Adobe Commerce Optimizer] tant que vous ne l’avez pas affectée à une vue de catalogue. Après l’enregistrement, l’entrée de table Clés d’accès limité est mise à jour pour afficher l’affectation du catalogue et la date d’expiration.

## Attribuer ou supprimer des clés d’accès restreintes {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Sélection et rotation des clés {#key-selection-and-rotation}

Lorsque plusieurs clés sont affectées à une vue de catalogue, [!DNL Adobe Commerce] utilise automatiquement la clé affectée non expirée avec la dernière date d’expiration pour signer des jetons.

>[!IMPORTANT]
>
>La rotation automatique des clés n’est pas encore disponible. Les clés ont par défaut une longue période d’expiration. Pour faire pivoter une clé manuellement, créez une clé, puis affectez-la à la vue de catalogue à côté de la clé existante. Après avoir confirmé que la nouvelle clé est en cours d’utilisation, supprimez l’ancienne clé.

Pour modifier la période d’expiration par défaut appliquée aux clés nouvellement créées, accédez à **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. Voir [Services > Clés d’accès restreintes ACO](../configuration-reference/services/aco-restricted-access-keys.md).

## Limites connues {#known-limitations}

- Il n’y a aucun indicateur actif ou d’état sur la grille de [!UICONTROL Restricted Access Keys] principale.

  Le statut du lien s’affiche sur la page [!UICONTROL Edit Restricted Access Keys]. Utilisez la liste déroulante pour afficher les clés disponibles et leur statut. Si une clé est affectée à une vue de catalogue, elle est liée. S’il n’est pas affecté, il n’a aucun statut. Vous pouvez affecter ces clés à la vue de catalogue que vous modifiez.

  Dans la page [!UICONTROL Catalog View Sync Status], vous pouvez voir les clés liées à une vue de catalogue à partir de la page des détails de la vue de catalogue (action **[!UICONTROL View details]**). La page de détails affiche également l’historique des clés, y compris le moment où elles ont été affectées ou non à partir d’une vue de catalogue.

- La rotation automatique des clés n’est pas encore disponible.

>[!MORELIKETHIS]
>
> - [Gérer la configuration de la vue du catalogue](/help/b2b/catalog-views-manage.md) — Attribuez ces clés à partir du catalogue partagé ou du compte d&#39;entreprise
> - [Surveillance du statut de synchronisation de la vue du catalogue](catalog-view-sync-status.md) — Surveillez et réconciliez les vues du catalogue protégées par ces clés
> - [Services > Clés d’accès restreint ACO](../configuration-reference/services/aco-restricted-access-keys.md) — Configurer la période d’expiration par défaut des clés
> - [Services > Vue Catalogue ACO](../configuration-reference/services/aco-catalog-view.md) — Configurez la durée de vie du jeton d’accès du storefront et activez ou désactivez l’émission
> - [Gérer les clés d’accès restreint](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} dans le *Guide du connecteur Adobe Commerce Optimizer* — Découvrez comment ces clés s’intègrent dans la synchronisation de catalogue partagé B2B
> - [Clés d’accès restreintes](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} dans le *Guide Adobe Commerce Optimizer* — Flux de clés manuel basé sur ACO Studio pour les cas d’utilisation non-B2B
