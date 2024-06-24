---
title: Affectation d’un groupe de clients à une entreprise
description: Découvrez comment affecter un groupe de clients à un compte d’entreprise dans votre boutique Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Affectation d’un groupe de clients à une entreprise

L’affectation d’un groupe de clients à une entreprise est essentiellement identique à l’affectation d’un catalogue partagé. Si le catalogue partagé n’est pas [activé dans la configuration](enable-basic-features.md), un groupe de clients (plutôt qu’un catalogue partagé) est affecté à une entreprise.

>[!NOTE]
>
> Un seul groupe de clients ou catalogue partagé peut être attribué à une entreprise à la fois. Un groupe de clients associé à un catalogue partagé ne peut pas être supprimé.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

   ![Modifier la société](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Sur la page d’entreprise, faites défiler l’écran vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Advanced Settings]** .

1. Définissez les **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >La variable [!UICONTROL Customer Group] La liste comprend tous les catalogues partagés existants, même si l’option Catalogues partagés est désactivée dans la configuration.

   La modification du groupe de clients affecté à l’entreprise met à jour les profils de tous les membres de l’entreprise.

   >[!NOTE]
   >
   >Après avoir modifié le groupe de la société, un utilisateur de la société doit se déconnecter et se connecter à Storefront pour afficher les nouveaux prix dans le catalogue.

   ![Modification d’un groupe de clients ou d’un catalogue partagé](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >Si l’affectation du groupe de clients est changée d’un catalogue partagé à un groupe de clients standard, les membres de l’entreprise perdent l’accès au catalogue partagé et le catalogue principal leur devient disponible à partir du storefront.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Proceed]**.

1. Cliquez sur **[!UICONTROL Save]**.
