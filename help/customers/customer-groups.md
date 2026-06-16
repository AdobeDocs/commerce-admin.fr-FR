---
title: Groupes de clients
description: Utilisez les groupes de clients pour déterminer les remises disponibles pour les clients affectés à un groupe et la classe de taxe associée au groupe.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/jbqn6jRo2Pg2fARqEyHGLLzVVG0CyuudtGXklpUCaOw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 445
ht-degree: 0%

---

# Groupes de clients

Les groupes de clients déterminent les remises disponibles et la classe de taxe associée au groupe. Les groupes de clients par défaut sont `General`, `Not Logged In` et `Wholesale`.

![Groupes de clients](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrer la liste des [!UICONTROL Customer Groups]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Saisissez les critères de recherche de groupes, y compris une plage d&#39;ID, de groupe ou de classe de taxe.

   ![Options de filtrage](assets/groups-filters.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Apply Filters]**.

## Créer un groupe de clients

>[!NOTE]
>
>Les utilisateurs administrateurs qui n’ont pas accès à tous les sites web (dotés d’un rôle avec un [!UICONTROL Role Scope] « Personnalisé ») ne peuvent pas créer, modifier ni supprimer des groupes de clients.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Cliquez sur **[!UICONTROL Add New Customer Group]**.

1. Par **, saisissez un nom unique contenant moins de 32 caractères pour identifier le groupe.[!DNL **Group Name]

1. Sélectionnez la **[!UICONTROL Tax Class]** qui s’applique au groupe.

   ![Informations sur le groupe](assets/group-information.png){width="600" zoomable="yes"}

1. Sélectionnez le **[!UICONTROL Excluded Website(s)]** que vous souhaitez exclure du groupe.

   >[!IMPORTANT]
   >
   >L’exclusion de sites web peut réduire le prix des produits et le temps d’indexation des règles de catalogue, car les sites web exclus ne sont pas indexés. Lorsqu’un groupe de clients est enregistré avec une exclusion de site web ajoutée, le prix du produit, la règle de catalogue et les index de recherche catalogue sont invalidés. Si vous disposez de nombreux produits, sites web et groupes de clients, il est recommandé de suspendre le processus de réindexation jusqu’à ce que vous ayez exclu les sites web des groupes de clients.

   Aucun site web n’est exclu par défaut. Pour sélectionner plusieurs valeurs, maintenez la touche _Ctrl_ (PC) ou _Commande_ (Mac) enfoncée et cliquez sur chaque option.

1. Cliquez ensuite sur **[!UICONTROL Save Customer Group]**.

## Modification d’un groupe de clients

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Cliquez ensuite sur **[!UICONTROL Save Customer Group]**.

## Affecter un client à un autre groupe

>[!NOTE]
>
>Après avoir modifié le groupe de sociétés, un utilisateur de société doit se déconnecter et se connecter au Storefront pour voir les nouveaux prix dans le catalogue.
>Une fois qu’un client est affecté à une entreprise, le groupe de clients est en lecture seule et ne peut pas être mis à jour par un utilisateur administrateur.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la liste et cochez la case dans la première colonne.

1. Définissez le contrôle **Actions** sur `Assign a Customer Group` et sélectionnez le groupe dans le menu.

   ![Affecter un groupe de clients](assets/group-assign.png){width="600" zoomable="yes"}

1. Lorsque vous êtes invité à confirmer, cliquez sur **OK**.

## Associer un groupe de clients à des remises spécifiques

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Sélectionnez la règle de prix du panier à laquelle vous souhaitez associer un groupe pour la remise appliquée ou [créez une règle de prix](../merchandising-promotions/price-rules-catalog.md).

1. Sélectionnez les groupes de clients auxquels la règle s’applique.

   ![Groupe de clients pour des remises spécifiques](assets/group-discount.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
> Vous pouvez également utiliser la tarification anticipée pour appliquer des remises produit à des groupes de clients. Voir [Tarification avancée](../catalog/product-price-group.md).

## Supprimer un groupe de clients

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Ouvrez l’enregistrement en mode d’édition.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Delete Customer Group]**.

1. Lorsque vous êtes invité à confirmer, cliquez sur **OK**.

## Démonstration de groupes de clients

Découvrez comment créer des groupes de clients en regardant cette démonstration :

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12&learn=on)
