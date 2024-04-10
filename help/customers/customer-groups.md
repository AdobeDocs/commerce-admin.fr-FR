---
title: Groupes de clients
description: Utilisez les groupes de clients pour déterminer les remises disponibles pour les clients affectés à un groupe et la classe de taxe associée au groupe.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 805ceef0fe67c1ed2a4fbd06e6f02d9ad252ecef
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Groupes de clients

Les groupes de clients déterminent les remises disponibles et la classe de taxe associée au groupe. Les groupes de clients par défaut sont les suivants : `General`, `Not Logged In`, et `Wholesale`.

![Groupes de clients](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrer les [!UICONTROL Customer Groups] liste

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Clic **[!UICONTROL Filters]**.

1. Saisissez les critères de recherche de groupes, y compris une plage d&#39;ID, de groupe ou de classe de taxe.

   ![Options de filtrage](assets/groups-filters.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Apply Filters]**.

## Créer un groupe de clients

>[!NOTE]
>
>Utilisateurs administrateurs qui n’ont pas accès à tous les sites web (avec un rôle affecté avec un « Personnalisé ») [!UICONTROL Role Scope]) ne peut pas créer, modifier ou supprimer des groupes de clients.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Clic **[!UICONTROL Add New Customer Group]**.

1. Pour [!DNL **Group Name]**, saisissez un nom unique contenant moins de 32 caractères pour identifier le groupe.

1. Sélectionner le **[!UICONTROL Tax Class]** cela s’applique au groupe .

   ![Informations sur le groupe](assets/group-information.png){width="600" zoomable="yes"}

1. Sélectionner le **[!UICONTROL Excluded Website(s)]** que vous souhaitez exclure du groupe.

   >[!IMPORTANT]
   >
   >L’exclusion de sites web peut réduire le prix du produit et le temps d’indexation des règles de catalogue, car les sites web exclus ne sont pas indexés. Lorsqu’un groupe de clients est enregistré avec une exclusion de site web ajoutée, le prix du produit, la règle de catalogue et les index de recherche catalogue sont invalidés. Si vous disposez de nombreux produits, sites web et groupes de clients, il est recommandé de suspendre le processus de réindexation jusqu’à ce que vous ayez exclu les sites web des groupes de clients.

   Aucun site web n’est exclu par défaut. Pour sélectionner plusieurs valeurs, maintenez la touche enfoncée _Ctrl_ clé (PC) ou _Commande_ (Mac) et cliquez sur chaque option.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Customer Group]**.

## Modification d’un groupe de clients

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Customer Group]**.

## Affecter un client à un autre groupe

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la liste et cochez la case dans la première colonne.

1. Définir le **Actions** contrôle sur `Assign a Customer Group` et choisissez le groupe dans le menu.

   ![Affecter un groupe de clients](assets/group-assign.png){width="600" zoomable="yes"}

1. Lorsque vous êtes invité à confirmer, cliquez sur **OK**.

## Associer un groupe de clients à des remises spécifiques

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Sélectionnez la règle de prix de panier à laquelle vous souhaitez associer un groupe pour la remise appliquée, ou [créer une règle de prix](../merchandising-promotions/price-rules-catalog.md).

1. Sélectionnez les groupes de clients auxquels la règle s’applique.

   ![Remises spécifiques du groupe client](assets/group-discount.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
> Vous pouvez également utiliser la tarification anticipée pour appliquer des remises produit à des groupes de clients. Voir [Tarification avancée](../catalog/product-price-group.md).

## Supprimer un groupe de clients

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Dans la barre de boutons, cliquez **[!UICONTROL Delete Customer Group]**.

1. Lorsque vous êtes invité à confirmer, cliquez sur **OK**.

## Démonstration de groupes de clients

Découvrez comment créer des groupes de clients en regardant cette démonstration :

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
