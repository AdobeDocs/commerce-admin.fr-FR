---
title: '[!UICONTROL My Quotes]'
description: Découvrez l’expérience client des guillemets, disponible dans le tableau de bord de leur compte.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Si les guillemets sont activés, la section _[!UICONTROL My Quotes]_du tableau de bord du compte client répertorie toutes les guillemets envoyés par le client. En fonction de leurs autorisations, seuls les acheteurs qui effectuent des achats pour le compte d’une société peuvent soumettre des demandes de négociation du prix d’un achat.

![Mes citations](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

L’acheteur commence le processus en [envoyant une demande](quote-request.md) pour un devis du panier. L&#39;échange d&#39;e-mails entre l&#39;acheteur et le vendeur se fait au cours du [processus de négociation](quote-price-negotiation.md). Pour l’acheteur, la page [!UICONTROL My Quotes] est le point focal de toute communication entre l’acheteur et le vendeur pendant le processus de négociation. Un acheteur qui accepte le prix négocié proposé par le vendeur peut accéder directement à la page de paiement à partir du devis. Des remises supplémentaires ne peuvent pas être ajoutées au devis négocié.

Un acheteur peut effectuer les actions suivantes lors de la négociation d’un devis :

* Vérification des prix et des mises à jour des articles
* Suivi du processus de négociation à partir des sections [!UICONTROL Comments] et [!UICONTROL History]
* Modifier le guillemet pour supprimer des éléments
* Communiquez et négociez avec le vendeur en ajoutant des notes au niveau de l’article et des guillemets.
* Envoyer un devis au vendeur pour révision
* Convertir le devis en ordre si les termes sont acceptables
* Fermez le guillemet
* Supprimer le guillemet
* [!BADGE Fonctionnalités bêta 1.5.0]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme Beta"}

L’exemple suivant illustre une citation qui a été mise à jour par l’acheteur et renvoyée au vendeur pour révision.


![Vue de l’acheteur du devis](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Les guillemets dont l’état est `Updated` sont verrouillés jusqu’à ce que le vendeur renvoie la citation.

## Afficher les guillemets

Avec les [autorisations requises pour leur rôle](account-company-roles-permissions.md), les clients associés à un compte de société peuvent voir les citations demandées par [les utilisateurs subordonnés](account-company-structure.md). Les administrateurs de l’entreprise peuvent voir tous les guillemets pour le compte de l’entreprise.

1. Le client se connecte à son compte sur le storefront.

1. Cliquez sur **[!UICONTROL My Quotes]** dans le volet de navigation de gauche.

1. Pour afficher toutes les guillemets qu’ils ont créés, cliquez sur le lien **[!UICONTROL Show My Quotes]** (affiché uniquement pour l’administrateur de la société ou pour le compte des utilisateurs subordonnés).

1. Pour afficher tous les guillemets de tous les utilisateurs de l’entreprise, cliquez sur **[!UICONTROL Show All Quotes]**.

## Afficher un guillemet

1. Le client se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Recherche le guillemet dans la liste et clique sur **[!UICONTROL View]** dans la colonne _[!UICONTROL Action]_.

## Imprimer un devis

1. Dans la citation ouverte située à droite de la section _[!UICONTROL Items Quoted]_, le client clique sur **[!UICONTROL Print]**.

1. Vérifie le **[!UICONTROL Destination]** comme imprimante ou PDF.

1. Clics **[!UICONTROL Print]**.

## Annulation d’une demande de devis

1. Dans la citation ouverte juste au-dessus de la section Éléments cités , cliquez sur **[!UICONTROL Close quote]**.

   La demande est annulée et l’état du guillemet passe à `Closed`. Les guillemets fermés restent dans la liste des guillemets et sont répertoriés dans la grille _[!UICONTROL Quotes]_de l’administrateur.

1. Pour supprimer le guillemet annulé de la liste des guillemets, cliquez sur **[!UICONTROL Delete]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

   Les guillemets fermés sont retirés de leur liste de citations. Toutefois, il reste répertorié sur la grille _[!UICONTROL Quotes]_dans l’Admin, avec l’état `Closed`.

## Actions citées

| Action | Description |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Renommer | [!BADGE 1.5.0-beta features]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponible uniquement pour les participants au programme Beta&quot;} Modification du nom du guillemet |
| Création d’une copie | [!BADGE Fonctionnalités bêta 1.5.0]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponible uniquement pour les participants au programme Beta&quot;} Un acheteur peut créer un nouveau devis à partir du guillemet actuel en le copiant et en le renommant. |
| Fermer le guillemet | Lorsqu&#39;un acheteur ferme un devis, il ne peut pas le rouvrir. Si nécessaire, l’acheteur peut le recréer à l’aide de l’action [!UICONTROL Create Copy]. Cette option n’est pas disponible si l’état du guillemet est `Draft`. |
| Supprimer un guillemet | Lorsqu’un acheteur supprime un devis, il est retiré du système et n’est plus disponible. |
| Imprimer | Ouvre un formulaire d’impression pour enregistrer le guillemet sous la forme d’un PDF, d’un fichier ou de l’imprimer sur une imprimante configurée. |

## Descriptions des colonnes

| Colonne | Description |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Nom attribué à la demande de devis par l’acheteur. |
| [!UICONTROL Created] | Date à laquelle la demande de devis a été soumise pour la première fois. |
| [!UICONTROL Created By] | Prénom et nom de l’acheteur qui a soumis la demande de devis. |
| [!UICONTROL Status] | Indique le statut du guillemet. Le statut d&#39;un devis ne peut être modifié que par une action de la part de l&#39;acheteur ou du vendeur. <br/>**[!UICONTROL Submitted]**- La demande de devis de l’acheteur n’a pas encore été ouverte par le vendeur. Dans cet état, l&#39;acheteur peut toujours modifier la demande de devis. Actions disponibles : `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Le vendeur a ouvert la demande et est en train de la réviser et de préparer une réponse. Actions disponibles : `View` / `Close` <br/>**[!UICONTROL Updated]**- Le vendeur a envoyé une réponse à l’acheteur et le bouton _[!UICONTROL Proceed to Checkout]_est activé. Dans cet état, l&#39;acheteur peut continuer à modifier le devis. Actions disponibles : `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- L’acheteur met toujours à jour le devis et le bouton_[!UICONTROL Proceed to Checkout]_ est désactivé. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- L’acheteur a soumis une commande basée sur le devis négocié. Le guillemet est verrouillé et ne peut pas être modifié. Action disponible : View<br/>**[!UICONTROL Closed]** - L&#39;acheteur a mis fin à la négociation et annule le devis. Le devis est verrouillé et ne peut être édité ni par l&#39;acheteur ni par le vendeur. Actions disponibles : `View` / `Delete` <br/>**[!UICONTROL Declined]**- Le vendeur a refusé la demande de devis, ou pour apporter une modification proposée pendant le processus de négociation. Une citation peut être refusée à n’importe quelle étape du workflow. Toute tarification personnalisée est supprimée du devis. L&#39;acheteur peut continuer à modifier le devis et le soumettre à nouveau, ou effectuer l&#39;achat avec les prix standards du catalogue. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - La durée de vie du guillemet a expiré. Tous les prix proposés sont réinitialisés. L’acheteur peut soit effectuer l’achat en fonction des prix standard du catalogue, soit lancer une autre série de négociations. Actions disponibles : `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
