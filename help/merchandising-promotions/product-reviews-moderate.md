---
title: Modération des critiques de produits
description: Découvrez comment modérer les avis sur les produits pour vous assurer que les avis soumis sont appropriés pour l'affichage public de votre boutique.
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/DGRJr-P9TUQ1TFh4Da1Z4VwrKfWe2rw5wmbwq9IlAFg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 0%

---

# Modération des critiques de produits

Pour les révisions de produit Commerce, une révision de produit envoyée doit être approuvée avant de pouvoir être affichée. Cela permet de s’assurer que les avis sont appropriés pour l’affichage public de votre boutique. Une révision envoyée a le statut `Pending` jusqu’à ce qu’elle soit approuvée ou rejetée.

## Afficher les avis sur les produits dans l’Admin

Pour afficher toutes les critiques d’un produit spécifique dans l’administration, procédez comme suit :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit à afficher et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sur la page produit, faites défiler la page vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Product Reviews]** .

   Dans cette grille, vous pouvez également modifier la révision spécifique en cliquant sur le lien **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

## Mettre à jour le statut des révisions

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**ou **[!UICONTROL All Reviews]**.

1. Dans la liste, cliquez sur une révision en attente pour afficher les détails et la modifier si nécessaire.

1. Modifiez le **[!UICONTROL Status]** en fonction de votre évaluation :

   - Pour approuver une révision en attente, sélectionnez `Approved`.

   - Pour rejeter une révision, sélectionnez `Not Approved`. Les révisions non approuvées disparaissent de la liste de _[!UICONTROL Pending Reviews]_page.

   >[!NOTE]
   >
   >Les révisions avec les statuts `Pending` et `Not Approved` ne sont pas affichées sur le storefront.

1. Le cas échéant, définissez la **[!UICONTROL Visibility]** d’une révision de produit pour qu’elle apparaisse dans différentes vues de magasin.

1. Si nécessaire, modifiez les valeurs de **[!UICONTROL Detailed Rating]**, **[!UICONTROL Nickname]** et **[!UICONTROL Summary of Review]**.

   Pour modifier l’affichage du magasin dans lequel une révision est disponible, choisissez l’affichage du magasin nécessaire dans la colonne _[!UICONTROL Visibility]_.

   ![Modifier la page de révision](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Review]**.

## Mise à jour par lots

Vous pouvez mettre à jour ou supprimer plusieurs révisions en même temps :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Sélectionnez les révisions à mettre à jour.

1. Utilisez le sélecteur de _[!UICONTROL Action]_dans le coin supérieur gauche pour appliquer une action.

1. Clic **[!UICONTROL Submit]**

## Suppression d’une révision de produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Recherchez la révision du produit à supprimer et ouvrez-la en mode d’édition.

1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete Review]** bouton.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Barre de boutons

| Bouton | Description |
|----------|--------------|
| **[!UICONTROL Back]** | Retourne à la page des révisions sans enregistrer les modifications |
| **[!UICONTROL Delete Review]** | Supprime la révision |
| **[!UICONTROL Reset]** | Rétablit les valeurs précédentes des modifications non enregistrées dans le formulaire de révision |
| **[!UICONTROL Previous]** | Ouvre la révision précédente |
| **[!UICONTROL Next]** | Ouvre la prochaine révision |
| **[!UICONTROL Save and Previous]** | Enregistre les modifications actuelles et ouvre la révision précédente. Ce bouton s’affiche s’il existe d’autres révisions. |
| **[!UICONTROL Save and Next]** | Enregistre les modifications en cours et ouvre la vue suivante. Ce bouton s’affiche s’il existe d’autres révisions. |
| **[!UICONTROL Save Review]** | Enregistre les modifications et ferme la page de modification de la révision |
