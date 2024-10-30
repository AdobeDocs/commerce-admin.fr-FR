---
title: '[!UICONTROL My Quotes]'
description: Découvrez l’expérience client des guillemets, disponible dans le tableau de bord de leur compte.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 6cf53c7caf37c24be473afecfba829595c14cb8c
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Si les guillemets sont activés, la section _[!UICONTROL My Quotes]_du tableau de bord du compte client répertorie toutes les guillemets envoyés par le client. En fonction de leurs autorisations, seuls les acheteurs qui effectuent des achats pour le compte d’une société peuvent soumettre des demandes de négociation du prix d’un achat.

![Mes citations](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

L’acheteur commence le processus en [envoyant une demande](quote-request.md) pour un devis du panier. L&#39;échange d&#39;e-mails entre l&#39;acheteur et le vendeur se fait au cours du [processus de négociation](quote-price-negotiation.md). Pour l’acheteur, la page [!UICONTROL My Quotes] est le point focal de toute communication entre l’acheteur et le vendeur pendant le processus de négociation. Un acheteur qui accepte le prix négocié proposé par le vendeur peut accéder directement à la page de paiement à partir du devis. Des remises supplémentaires ne peuvent pas être ajoutées au devis négocié.

Lors de la négociation d’un devis, un acheteur dispose de plusieurs options pour gérer le devis ou mettre à jour le détail du devis.

* Actions relatives à la gestion des guillemets :

   * Créer une copie du guillemet
   * Fermez le guillemet
   * Supprimer le guillemet
   * Renommer le guillemet
   * Imprimer le guillemet
   * Créer un modèle

* Actions de mise à jour des détails des guillemets :

   * Vérification des prix et des mises à jour des articles
   * Suivi du processus de négociation à partir des sections [!UICONTROL Comments] et [!UICONTROL History]
   * Modifier le guillemet pour supprimer des éléments
   * Communiquez et négociez avec le vendeur en ajoutant des notes au niveau de l’article et des guillemets.
   * Ajouter une adresse de livraison
   * Déplacer des éléments de ligne vers une liste de demandes
   * Convertir le devis en ordre si les termes sont acceptables

* Actions générales lors de la négociation :

   * Envoyer un devis au vendeur pour révision
   * Passez à l’extraction

L’exemple suivant illustre une citation qui a été mise à jour par l’acheteur et renvoyée au vendeur pour révision.


![Vue de l’acheteur du devis](./assets/account-dashboard-my-quote-detailed.png){width="700" zoomable="yes"}

Les guillemets dont l’état est `Updated` sont verrouillés jusqu’à ce que le vendeur renvoie la citation.

## Afficher les guillemets

Avec les [autorisations requises pour leur rôle](account-company-roles-permissions.md), les acheteurs associés à un compte de société peuvent voir les citations demandées par les [utilisateurs subordonnés](account-company-structure.md). Les administrateurs de l’entreprise peuvent voir tous les guillemets pour le compte de l’entreprise.

1. L&#39;acheteur se connecte à son compte sur la vitrine.

1. Cliquez sur **[!UICONTROL My Quotes]** dans le volet de navigation de gauche.

1. Pour afficher toutes les guillemets qu’ils ont créés, cliquez sur le lien **[!UICONTROL Show My Quotes]** (affiché uniquement pour l’administrateur de la société ou pour le compte des utilisateurs subordonnés).

1. Pour afficher tous les guillemets de tous les utilisateurs de l’entreprise, cliquez sur **[!UICONTROL Show All Quotes]**.

## Afficher un guillemet

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Recherche le guillemet dans la liste et clique sur **[!UICONTROL View]** dans la colonne _[!UICONTROL Action]_.

## Copier un guillemet

1. L&#39;acheteur se connecte au compte de sa société sur le storefront.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Recherchez et accédez au guillemet souhaité dans la liste, puis cliquez sur **[!UICONTROL Create Copy]** dans le guillemet original.

## Créer un modèle

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quote Templates]**.

1. Recherche le guillemet dans la liste **[!UICONTROL My Quotes]** et clique sur **[!UICONTROL Create Quote Template]** dans la colonne _[!UICONTROL Action]_.

## Déplacer des éléments de ligne d’un guillemet vers une liste de demandes

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Recherchez et accédez au guillemet souhaité dans la liste.

1. Sélectionnez les éléments de ligne.

1. Cliquez sur **[!UICONTROL Move to Requisition list]** dans la liste déroulante _[!UICONTROL Actions]_.

1. Sélectionnez une liste de commandes existante pour déplacer les éléments sélectionnés.

1. Cliquez sur **[!UICONTROL Move item]**.

Pour en savoir plus sur ce processus, voir [Ajout de produits à une liste de demandes](requisition-lists.md) .

>[!NOTE]
>
> Vous ne pouvez pas créer de liste de demandes lors du déplacement d’éléments. Les éléments ne peuvent être déplacés que vers une liste de demandes d’achat existante.

## Déplacer des éléments de ligne vers un nouveau guillemet

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Recherchez et accédez au guillemet souhaité dans la liste.

1. Sélectionnez les éléments de ligne.

1. Cliquez sur **[!UICONTROL Move item to new quote]** dans la liste déroulante _[!UICONTROL Actions]_.

1. Nommez le nouveau guillemet dans le modal.

1. Sélectionnez **[!UICONTROL Move to quote]** pour déplacer l’élément sélectionné vers le nouveau guillemet.

>[!NOTE]
>
> Lors de la sélection de plusieurs éléments, le modal s’affiche sous la forme **[!UICONTROL Move selected items to new quote]**.

## Ajouter une adresse de livraison

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quotes]**.

1. Sélectionne la citation souhaitée.

1. Dans la section **[!UICONTROL Shipping Information]**, cliquez sur **[!UICONTROL Add New Address]**.

1. Renseigne les détails de la nouvelle adresse.

1. Clics **[!UICONTROL Save Address]**.

Lorsque l&#39;acheteur ajoute l&#39;adresse, le vendeur fournit les options d&#39;expédition et de livraison. Ces mises à jour peuvent avoir une incidence sur le prix négocié. Les options d’expédition sont verrouillées lors du passage en caisse.

## Imprimer un devis

1. Dans la citation ouverte située à droite de la section _[!UICONTROL Items Quoted]_, l&#39;acheteur clique sur **[!UICONTROL Print]**.

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
| Renommer | Modifier le nom du guillemet |
| Créer une copie | Un acheteur peut créer un devis à partir du devis actuel en le copiant et en le renommant. |
| Fermer le guillemet | Lorsqu&#39;un acheteur ferme un devis, il ne peut pas le rouvrir. Si nécessaire, l’acheteur peut le recréer à l’aide de l’action [!UICONTROL Create Copy]. Cette option n’est pas disponible si l’état du guillemet est `Draft`. |
| Créer un modèle | Créez un modèle de devis basé sur le guillemet actuel. Les modèles de devis rationnalisent la négociation des devis en permettant aux acheteurs et aux vendeurs de se mettre d&#39;accord sur les termes du contrat et des prix qui peuvent être appliqués à plusieurs devis.  Sur accord, l’acheteur peut générer un devis prévalidé et lié à partir du modèle pour les commandes ultérieures au lieu de redémarrer le processus de demande de devis (RFQ). |
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
