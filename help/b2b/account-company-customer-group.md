---
title: Affectation d’un groupe de clients à une entreprise
description: Découvrez comment affecter un groupe de clients à un compte de société dans votre boutique Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
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
source-wordcount: 236
ht-degree: 0%

---

# Affectation d’un groupe de clients à une entreprise

L’affectation d’un groupe de clients à une entreprise est essentiellement identique à l’affectation d’un catalogue partagé. Si le catalogue partagé n’est pas activé [dans la configuration](enable-basic-features.md), un groupe de clients, plutôt qu’un catalogue partagé, est affecté à une entreprise.

- Un seul groupe de clients ou catalogue partagé peut être affecté à une entreprise à la fois. Impossible de supprimer un groupe de clients associé à un catalogue partagé.
- La modification du groupe de clients affecté à la société met à jour les profils de tous les membres de la société.
- Si l&#39;affectation d&#39;un groupe de clients est changée d&#39;un catalogue partagé en un groupe de clients standard, les membres de la société perdent l&#39;accès au catalogue partagé et le catalogue principal devient disponible à partir du storefront.
- Après avoir modifié le groupe de sociétés, un utilisateur de société doit se déconnecter et se connecter au Storefront pour voir les nouveaux prix dans le catalogue.

## Modifier le groupe de clients

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez la société dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

   ![Modifier entreprise](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Dans la page d’entreprise, faites défiler la page vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Advanced Settings]** .

1. Définissez la **[!UICONTROL Customer Group]** appropriée.

   La liste [!UICONTROL Customer Group] répertorie tous les catalogues partagés existants, même si l’option Catalogues partagés est désactivée dans la configuration.

   ![Modifier le groupe de clients ou le catalogue partagé](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL Proceed]**.

1. Cliquez sur **[!UICONTROL Save]**.
