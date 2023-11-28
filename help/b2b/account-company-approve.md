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

L’état des demandes reçues du storefront pour créer une société est : `Pending Approval` tant que la demande n’a pas été examinée par l’administrateur du magasin, avant approbation ou rejet. L’état d’un compte de société peut être défini sur l’un des paramètres suivants :

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Vous pouvez également utiliser la variable [Contrôle des actions](account-company-manage.md) pour approuver plusieurs demandes de l’entreprise.

![En attente d’approbation](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Approbation d’un compte de société en attente

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Vous pouvez utiliser la variable _[!UICONTROL Columns]_le sélecteur situé au-dessus de la grille pour afficher le **[!UICONTROL Status]**colonne .

1. Dans le _[!UICONTROL Action]_colonne, cliquez sur **[!UICONTROL Edit]**.

1. Définir **[!UICONTROL Company Status]** to `Active`.

   ![Définition du statut de l’entreprise](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Change status]**.

   L’administrateur de la société reçoit un courrier électronique l’informant que la société est désormais active.

1. Le cas échéant, définissez **[!UICONTROL Sales Representative]** à un compte d’utilisateur administrateur spécifique.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png)  la valeur **[!UICONTROL Account Information]** et utilisez la fonction **[!UICONTROL Comment]** pour saisir des remarques sur le compte.

   Les commentaires ne sont pas visibles à partir du storefront.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   Un message de confirmation est envoyé à l’administrateur de la société et de la société pour confirmer que le compte de la société est approuvé.

## Statut de la société

| État | Description |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | L’entreprise est approuvée et peut être gérée à partir du storefront par l’administrateur de l’entreprise. |
| [!UICONTROL Pending Approval] | Une demande de création d’un compte d’entreprise a été envoyée à partir du storefront, mais n’est pas encore examinée. |
| [!UICONTROL Rejected] | La demande de création d’un compte d’entreprise a été rejetée par l’administrateur du magasin. |
| [!UICONTROL Blocked] | Le compte de la société n&#39;est plus en règle. Le client peut accéder au compte à partir du storefront, mais ne peut pas effectuer d’achat. |

{style="table-layout:auto"}
