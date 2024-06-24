---
title: Groupes de clients
description: Utilisez les groupes de clients pour déterminer les remises disponibles pour les clients affectés à un groupe et la classe de taxe associée au groupe.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: c2fd228311a4b990be9c1409d2cdd2b5677fe2af
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Groupes de clients

Les groupes de clients déterminent quelles remises sont disponibles et la classe de taxe associée au groupe. Les groupes de clients par défaut sont : `General`, `Not Logged In`, et `Wholesale`.

![Groupes de clients](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrez les [!UICONTROL Customer Groups] list

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Saisissez les critères de recherche de groupes, y compris une plage d’identifiants, de groupe ou de classe fiscale.

   ![Options de filtrage](assets/groups-filters.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Apply Filters]**.

## Créer un groupe de clients

>[!NOTE]
>
>Utilisateurs administrateurs qui n’ont pas accès à tous les sites web (auxquels est affecté un rôle &quot;Personnalisé&quot;) [!UICONTROL Role Scope]) ne peuvent pas créer, modifier ou supprimer des groupes de clients.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Cliquez sur **[!UICONTROL Add New Customer Group]**.

1. Pour [!DNL **Group Name]**, saisissez un nom unique de moins de 32 caractères pour identifier le groupe.

1. Sélectionnez la variable **[!UICONTROL Tax Class]** qui s’applique au groupe.

   ![Informations sur le groupe](assets/group-information.png){width="600" zoomable="yes"}

1. Sélectionnez la variable **[!UICONTROL Excluded Website(s)]** que vous souhaitez exclure du groupe.

   >[!IMPORTANT]
   >
   >L’exclusion de sites web peut diminuer le prix du produit et le temps d’indexation des règles de catalogue, car les sites web exclus ne sont pas indexés. Lorsqu’un groupe de clients est enregistré avec une exclusion de site web ajoutée, le prix du produit, la règle de catalogue et les index de recherche de catalogue sont invalidés. Si vous disposez de nombreux produits, sites Web et groupes de clients, il est recommandé de suspendre le processus de réindexation jusqu’à ce que vous ayez exclu les sites Web des groupes de clients.

   Aucun site web n’est exclu par défaut. Pour sélectionner plusieurs valeurs, maintenez la touche _Ctrl_ clé (PC) ou le _Commande_ (Mac) et cliquez sur chaque option.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Customer Group]**.

## Modifier un groupe de clients

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Customer Group]**.

## Affectation d’un client à un autre groupe

>[!NOTE]
>
>Après avoir modifié le groupe de la société, un utilisateur de la société doit se déconnecter et se connecter à Storefront pour afficher les nouveaux prix dans le catalogue.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la liste et cochez la case dans la première colonne.

1. Définissez la variable **Actions** contrôler à `Assign a Customer Group` et choisissez le groupe dans le menu .

   ![Attribution d’un groupe de clients](assets/group-assign.png){width="600" zoomable="yes"}

1. Lorsque vous y êtes invité, cliquez sur **OK**.

## Associer un groupe de clients à des remises spécifiques

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Sélectionnez la règle de prix du panier à laquelle vous souhaitez associer un groupe pour la remise appliquée, ou [créer une règle de prix ;](../merchandising-promotions/price-rules-catalog.md).

1. Sélectionnez les groupes de clients auxquels s’applique la règle.

   ![Groupe de clients vers des remises spécifiques](assets/group-discount.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
> Vous pouvez également utiliser les tarifs avancés pour appliquer des remises à des groupes de clients. Voir [Tarifs avancés](../catalog/product-price-group.md).

## Supprimer un groupe de clients

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Delete Customer Group]**.

1. Lorsque vous y êtes invité, cliquez sur **OK**.

## Démonstration des groupes de clients

Découvrez comment créer des groupes de clients en regardant cette démonstration :

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
