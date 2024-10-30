---
title: Affectation d’un groupe de clients à une entreprise
description: Découvrez comment affecter un groupe de clients à un compte d’entreprise dans votre boutique Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Affectation d’un groupe de clients à une entreprise

L’affectation d’un groupe de clients à une entreprise est essentiellement identique à l’affectation d’un catalogue partagé. Si le catalogue partagé n’est pas [activé dans la configuration](enable-basic-features.md), un groupe de clients — plutôt qu’un catalogue partagé — est affecté à une entreprise.

- Un seul groupe de clients ou catalogue partagé peut être attribué à une entreprise à la fois. Un groupe de clients associé à un catalogue partagé ne peut pas être supprimé.
- La modification du groupe de clients affecté à l’entreprise met à jour les profils de tous les membres de l’entreprise.
- Si l’affectation du groupe de clients est changée d’un catalogue partagé à un groupe de clients standard, les membres de l’entreprise perdent l’accès au catalogue partagé et le catalogue principal leur devient disponible à partir du storefront.
- Après avoir modifié le groupe de la société, un utilisateur de la société doit se déconnecter et se connecter à Storefront pour afficher les nouveaux prix dans le catalogue.

## Modifier le groupe de clients

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

   ![Modifier la société](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Sur la page de l’entreprise, faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advanced Settings]** .

1. Définissez le **[!UICONTROL Customer Group]** approprié.

   La liste [!UICONTROL Customer Group] comprend tous les catalogues partagés existants, même si les catalogues partagés sont désactivés dans la configuration.

   ![Modifier le groupe de clients ou le catalogue partagé](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Proceed]**.

1. Cliquez sur **[!UICONTROL Save]**.
