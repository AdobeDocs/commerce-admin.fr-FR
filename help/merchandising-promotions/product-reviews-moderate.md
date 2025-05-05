---
title: Modération des révisions de produit
description: Découvrez comment modérer les révisions de produits pour vous assurer que les révisions envoyées sont appropriées pour l’affichage public de votre boutique.
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Modération des révisions de produit

Pour les révisions de produit Commerce, une révision de produit envoyée doit être approuvée avant de pouvoir être affichée. Cela garantit que les révisions sont appropriées pour l’affichage public de votre magasin. Une révision envoyée a l’état `Pending` jusqu’à ce qu’elle soit approuvée ou rejetée.

## Affichage des révisions de produit dans l’administrateur

Pour afficher toutes les révisions d’un produit spécifique dans l’administrateur, procédez comme suit :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit que vous souhaitez afficher et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sur la page du produit, faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Product Reviews]** .

   Dans cette grille, vous pouvez également modifier la révision spécifique en cliquant sur le lien **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

## Mise à jour de l’état des révisions

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**&#x200B;ou **[!UICONTROL All Reviews]**.

1. Dans la liste, cliquez sur une révision en attente pour afficher les détails et les modifier si nécessaire.

1. Modifiez le **[!UICONTROL Status]** en fonction de votre évaluation :

   - Pour approuver une révision en attente, sélectionnez `Approved`.

   - Pour rejeter une révision, sélectionnez `Not Approved`. Les révisions non approuvées disparaissent de la liste de la page _[!UICONTROL Pending Reviews]_.

   >[!NOTE]
   >
   >Les révisions avec les états `Pending` et `Not Approved` ne s’affichent pas sur le storefront.

1. Le cas échéant, définissez la **[!UICONTROL Visibility]** d’une révision de produit pour qu’elle apparaisse dans différentes vues de magasin.

1. Si nécessaire, modifiez les valeurs de **[!UICONTROL Detailed Rating]**, **[!UICONTROL Nickname]** et **[!UICONTROL Summary of Review]**.

   Pour modifier la vue de magasin où une révision est disponible, choisissez la vue de magasin nécessaire dans la colonne _[!UICONTROL Visibility]_.

   ![Modifier la page de révision](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Review]**.

## Mise à jour par lots

Vous pouvez mettre à jour ou supprimer plusieurs révisions en même temps :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Sélectionnez les révisions à mettre à jour.

1. Utilisez le sélecteur _[!UICONTROL Action]_&#x200B;dans le coin supérieur gauche pour appliquer une action.

1. Cliquez sur **[!UICONTROL Submit]**

## Suppression d’une révision de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Recherchez la révision de produit à supprimer et ouvrez-la en mode d’édition.

1. Dans la barre de menus, cliquez sur le bouton **[!UICONTROL Delete Review]** .

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Barre de boutons

| Bouton | Description |
|----------|--------------|
| **[!UICONTROL Back]** | Renvoie à la page Révisions sans enregistrer les modifications |
| **[!UICONTROL Delete Review]** | Supprime la révision. |
| **[!UICONTROL Reset]** | Réinitialise toutes les modifications non enregistrées du formulaire de révision sur leurs valeurs précédentes. |
| **[!UICONTROL Previous]** | Ouvre la révision précédente |
| **[!UICONTROL Next]** | Ouvre la prochaine révision |
| **[!UICONTROL Save and Previous]** | Enregistre les modifications en cours et ouvre la révision précédente. Ce bouton s’affiche en cas de révision. |
| **[!UICONTROL Save and Next]** | Enregistre les modifications actuelles et ouvre la vue suivante. Ce bouton s’affiche en cas de révision. |
| **[!UICONTROL Save Review]** | Enregistre les modifications et ferme la page de modification de révision |
