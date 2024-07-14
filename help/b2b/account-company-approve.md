---
title: Approbation d’un compte d’entreprise
description: Découvrez comment approuver les demandes de compte d’entreprise dans l’Admin.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Approbation d’un compte d’entreprise

L’état des demandes reçues du storefront pour créer une société est de `Pending Approval` jusqu’à ce que la demande soit examinée par l’administrateur du magasin, et approuvée ou rejetée. L’état d’un compte de société peut être défini sur l’un des paramètres suivants :

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Vous pouvez également utiliser le [contrôle Actions](account-company-manage.md) pour approuver plusieurs demandes de l’entreprise.

![Autorisation en attente](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Approbation d’un compte de société en attente

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Vous pouvez utiliser le sélecteur _[!UICONTROL Columns]_situé au-dessus de la grille pour afficher la colonne **[!UICONTROL Status]**.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Edit]**.

1. Définissez **[!UICONTROL Company Status]** sur `Active`.

   ![Définir le statut de la société](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Change status]**.

   L’administrateur de la société reçoit un courrier électronique l’informant que la société est désormais active.

1. Le cas échéant, définissez **[!UICONTROL Sales Representative]** sur un compte d’utilisateur administrateur spécifique.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Account Information]** et utilisez le champ **[!UICONTROL Comment]** pour saisir des notes sur le compte.

   Les commentaires ne sont pas visibles à partir du storefront.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   Un message de confirmation est envoyé à l’administrateur de la société et de la société pour confirmer que le compte de la société est approuvé.

## Statut de la société

| État | Description |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | L’entreprise est approuvée et peut être gérée à partir du storefront par l’administrateur de l’entreprise. |
| [!UICONTROL Pending Approval] | Une demande de création d’un compte d’entreprise a été envoyée à partir du storefront, mais n’est pas encore examinée. |
| [!UICONTROL Rejected] | La demande de création d’un compte d’entreprise a été rejetée par l’administrateur du magasin. |
| [!UICONTROL Blocked] | Le compte de la société n&#39;est plus en règle. Le client peut accéder au compte à partir du storefront, mais ne peut pas effectuer d’achat. |

{style="table-layout:auto"}
