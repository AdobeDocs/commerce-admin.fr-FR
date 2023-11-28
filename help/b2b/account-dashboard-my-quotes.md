---
title: '[!UICONTROL My Quotes]'
description: Découvrez l’expérience client des guillemets, disponible dans le tableau de bord de leur compte.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Si les guillemets sont activés, la variable _[!UICONTROL My Quotes]_du tableau de bord du compte client répertorie toutes les guillemets envoyés par le client. En fonction de leurs autorisations, seuls les acheteurs qui effectuent des achats pour le compte d’une société peuvent soumettre des demandes de négociation du prix d’un achat.

![Mes citations](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

L&#39;acheteur commence la procédure par [envoi d’une demande ;](quote-request.md) pour une citation du panier. L&#39;email est échangé entre l&#39;acheteur et le vendeur lors de la [processus de négociation](quote-price-negotiation.md). Pour l&#39;acheteur, la variable [!UICONTROL My Quotes] La page est le point focal de toute communication entre l&#39;acheteur et le vendeur pendant le processus de négociation. Un acheteur qui accepte le prix négocié proposé par le vendeur peut accéder directement à la page de paiement à partir du devis. Des remises supplémentaires ne peuvent pas être ajoutées au devis négocié.

Un acheteur peut effectuer les actions suivantes lors de la négociation d’un devis :

* Vérification des prix et des mises à jour des articles
* Suivi du processus de négociation à partir de [!UICONTROL Comments] et [!UICONTROL History] sections
* Modifier le guillemet pour supprimer des éléments
* Communiquez et négociez avec le vendeur en ajoutant des notes au niveau de l’article et des guillemets.
* Envoyer un devis au vendeur pour révision
* Convertir le devis en ordre si les termes sont acceptables
* Fermez le guillemet
* Supprimer le guillemet
* [!BADGE Fonctionnalités 1.5.0 bêta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"}

L’exemple suivant illustre une citation qui a été mise à jour par l’acheteur et renvoyée au vendeur pour révision.


![Achat et devis](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Citations avec la fonction `Updated` sont verrouillés jusqu’à ce que le vendeur renvoie le devis.

## Afficher les guillemets

Avec la variable [autorisations pour leur rôle](account-company-roles-permissions.md), les clients associés à un compte de société peuvent voir les guillemets demandés par [utilisateurs subordonnés](account-company-structure.md). Les administrateurs de l’entreprise peuvent voir tous les guillemets pour le compte de l’entreprise.

1. Le client se connecte à son compte sur le storefront.

1. Clics **[!UICONTROL My Quotes]** dans le volet de navigation de gauche.

1. Pour afficher tous les guillemets qu’ils ont créés, cliquez sur le bouton **[!UICONTROL Show My Quotes]** lien (affiché uniquement pour l’administrateur de la société ou pour le compte des utilisateurs subordonnés).

1. Pour afficher tous les guillemets de tous les utilisateurs de l’entreprise, cliquez sur **[!UICONTROL Show All Quotes]**.

## Afficher un guillemet

1. Le client se connecte à son compte.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL My Quotes]**.

1. Recherche le guillemet dans la liste et clique **[!UICONTROL View]** dans le _[!UICONTROL Action]_colonne .

## Imprimer un devis

1. Dans la citation ouverte à droite de la _[!UICONTROL Items Quoted]_, le client clique sur **[!UICONTROL Print]**.

1. Vérifie le **[!UICONTROL Destination]** comme imprimante ou comme PDF.

1. Clics **[!UICONTROL Print]**.

## Annulation d’une demande de devis

1. Dans la citation ouverte juste au-dessus de la section Éléments cités , cliquez sur **[!UICONTROL Close quote]**.

   La demande est annulée et le statut du devis passe à `Closed`. Les guillemets fermés restent dans votre liste de guillemets et sont répertoriés dans la _[!UICONTROL Quotes]_à partir de la grille Admin.

1. Pour supprimer le guillemet annulé de la liste des guillemets, cliquez sur **[!UICONTROL Delete]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

   Les guillemets fermés sont retirés de leur liste de citations. Toutefois, il reste répertorié dans la liste _[!UICONTROL Quotes]_grille dans l’Admin, avec la propriété `Closed` statut.

## Actions citées

| Action | Description |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Renommer | [!BADGE Fonctionnalités 1.5.0 bêta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"} |
| Création d’une copie | [!BADGE Fonctionnalités 1.5.0 bêta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"} |
| Fermer le guillemet | Lorsqu&#39;un acheteur ferme un devis, il ne peut pas le rouvrir. Si nécessaire, l&#39;acheteur peut le recréer à l&#39;aide de la variable [!UICONTROL Create Copy] action. Cette option n’est pas disponible si l’état du guillemet est `Draft`. |
| Supprimer un guillemet | Lorsqu’un acheteur supprime un devis, il est retiré du système et n’est plus disponible. |
| Imprimer | Ouvre un formulaire d’impression pour enregistrer le guillemet sous la forme d’un PDF, d’un fichier ou de l’imprimer sur une imprimante configurée. |

## Descriptions des colonnes

| Colonne | Description |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Nom attribué à la demande de devis par l’acheteur. |
| [!UICONTROL Created] | Date à laquelle la demande de devis a été soumise pour la première fois. |
| [!UICONTROL Created By] | Prénom et nom de l’acheteur qui a soumis la demande de devis. |
| [!UICONTROL Status] | Indique le statut du guillemet. Le statut d&#39;un devis ne peut être modifié que par une action de la part de l&#39;acheteur ou du vendeur. <br/>**[!UICONTROL Submitted]**- La demande de devis de l&#39;acheteur n&#39;a pas encore été ouverte par le vendeur. Dans cet état, l&#39;acheteur peut toujours modifier la demande de devis. Actions disponibles : `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Le vendeur a ouvert la demande et est en train de la réviser et de préparer une réponse. Actions disponibles : `View` / `Close` <br/>**[!UICONTROL Updated]**- Le vendeur a envoyé une réponse à l&#39;acheteur, et la _[!UICONTROL Proceed to Checkout]_est activé. Dans cet état, l&#39;acheteur peut continuer à modifier le devis. Actions disponibles : `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- L&#39;acheteur est toujours en train de mettre à jour le devis, et le_[!UICONTROL Proceed to Checkout]_ est désactivé. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- L&#39;acheteur a soumis une commande basée sur le devis négocié. Le guillemet est verrouillé et ne peut pas être modifié. Action disponible : Afficher<br/>**[!UICONTROL Closed]** - L&#39;acheteur a mis fin à la négociation et annule le devis. Le devis est verrouillé et ne peut être édité ni par l&#39;acheteur ni par le vendeur. Actions disponibles : `View` / `Delete` <br/>**[!UICONTROL Declined]**- Le vendeur a refusé la demande de devis ou a proposé un changement lors du processus de négociation. Une citation peut être refusée à n’importe quelle étape du workflow. Toute tarification personnalisée est supprimée du devis. L&#39;acheteur peut continuer à modifier le devis et le soumettre à nouveau, ou effectuer l&#39;achat avec les prix standards du catalogue. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - La durée de vie du guillemet a expiré. Tous les prix proposés sont réinitialisés. L’acheteur peut soit effectuer l’achat en fonction des prix standard du catalogue, soit lancer une autre série de négociations. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
