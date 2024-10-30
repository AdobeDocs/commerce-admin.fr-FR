---
title: Devis négociables
description: Découvrez les workflows de devis et comment fournir ce service aux comptes de votre société.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 7f4993ff8b16beda2a371737fb5a8ecb5f9c9396
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 0%

---

# Devis négociables

Les acheteurs et les vendeurs utilisent les guillemets pour gérer le processus de négociation d’un ajout de commande, de la mise à jour des quantités, de la demande et de l’application de remises, etc., jusqu’à ce qu’ils parviennent à un accord. Le processus de négociation des devis peut être initié par un acheteur autorisé d’une société ou par un représentant commercial de la société.

![Mode Liste de citations dans Admin](./assets/quotes-admin-list-view-intro.png){width="700" zoomable="yes"}

Une fois le devis créé, le processus de négociation commence lorsque l’acheteur ou le vendeur l’envoie pour examen. La grille _Guillemets_ qui répertorie chaque guillemet reçu et conserve un historique de la communication entre l’acheteur et le vendeur. Utilisez les [contrôles sur le lieu de travail](../getting-started/admin-workspace.md) standard pour filtrer la liste, modifier la disposition des colonnes, enregistrer les vues et exporter les données.

- Dans le storefront, les acheteurs soumettent le devis en tant que [ demande de négociation](quote-price-negotiation.md) du prix du panier. Lors de la création de la demande de devis, un acheteur peut enregistrer le devis en tant que brouillon ou le soumettre directement au vendeur.

- Dans l’administrateur, les vendeurs peuvent créer des devis pour le compte de l’acheteur de la société. Lors de la création du devis, un vendeur peut enregistrer le devis en tant que brouillon ou le soumettre directement à l&#39;acheteur pour lancer le processus de négociation.

Au cours du processus de négociation, la citation ne peut être mise à jour que par la personne qui examine et qui propose des termes pour d&#39;autres négociations.

## Conditions préalables

Les guillemets négociables ne sont disponibles que si Adobe Commerce dispose des paramètres de configuration suivants :

- [L’extension Adobe Commerce B2B est installée.](install.md)
- [Fonctionnalités B2B configurées](enable-basic-features.md)
   - Activation des comptes d’entreprise
   - Activer le guillemet B2B

## Processus des citations

Les devis peuvent être initiés par l&#39;acheteur ou le vendeur.

Ce diagramme présente les statuts des devis d’un acheteur et d’un vendeur (administrateur) dans les différentes étapes de lancement d’un devis.

![Workflow d’état des citations](./assets/quote-status-workflow.svg){width="700" zoomable="yes"}

**Étape 1 : création de citations (nouvelle)**

- **Demande de devis par l’acheteur** - L’acheteur [ demande un devis](quote-request.md) auprès du panier. La demande apparaît dans la liste _Mes guillemets_ du tableau de bord du compte de l’acheteur et une notification électronique est envoyée au représentant commercial affecté au compte de la société. Dans l’Admin, la requête apparaît dans la grille _Guillemets_, avec l’état `New`. Une demande de devis peut être modifiée par l&#39;acheteur jusqu&#39;à ce qu&#39;elle soit ouverte par le vendeur.

  ![Guillemets](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}

- **Représentant commercial** — Un représentant commercial peut [créer un devis](sales-rep-initiates-quote.md) de l&#39;administrateur au nom d&#39;un acheteur d&#39;entreprise spécifique. Le représentant commercial doit mettre à jour le devis pour ajouter à l&#39;acheteur des produits et d&#39;autres informations comme des remises et des notes. La Représentation des ventes peut enregistrer le devis comme `draft` ou l&#39;envoyer à l&#39;acheteur pour lancer la négociation. En version préliminaire, la citation est visible uniquement pour le vendeur. Une fois le guillemet envoyé, l’état est `Submitted`. Il ne peut pas être modifié par le vendeur tant que l&#39;acheteur ne l&#39;a pas renvoyé.

  ![Le vendeur lance un devis d’acheteur à partir de la grille Devis dans l’Admin](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

**Étape 2 : Révision et négociation de citations**

La vérification ou la négociation d’un devis peut inclure la modification de quantités, la suppression d’articles, l’ajout de commentaires d’articles, l’application de remises sur les articles ou les devis (vendeur) et l’ajout d’une adresse de livraison (acheteur).

- **Le vendeur consulte la demande et envoie une réponse** - Dans l’administrateur, le vendeur affiche la demande de devis. Sur le storefront, l’état du devis passe à `Pending`, et l’acheteur ne peut pas apporter de modifications. Le [vendeur répond](quote-price-negotiation.md) en offrant des rabais sur les prix et en ajustant les quantités et les articles si nécessaire, en saisissant un commentaire et en renvoyant le devis à l&#39;acheteur. L&#39;acheteur et le représentant commercial sont informés par email que le vendeur a répondu.

- **L’acheteur consulte les guillemets du vendeur et envoie une réponse** : l’acheteur clique sur le lien dans la notification électronique pour ouvrir le devis, ou il ouvre le devis à partir de la page _Mes guillemets_ du tableau de bord du compte. L’acheteur peut laisser des notes au vendeur au niveau de l’article ou du devis, modifier les quantités et supprimer des articles.

L&#39;acheteur et le vendeur peuvent poursuivre le processus de négociation jusqu&#39;à ce qu&#39;un accord soit trouvé, ou le vendeur refuse le devis. Si l’acheteur modifie le devis (ajout ou suppression de produits ou modification des quantités de produits), le devis doit être renvoyé au vendeur pour révision.

- **L’acheteur ajoute une adresse de livraison** : l’acheteur peut ajouter une adresse de livraison au devis. Une fois que l’acheteur a ajouté l’adresse, le vendeur peut fournir des options d’expédition et de livraison. Les méthodes d’expédition affichées dépendent de la configuration de Storefront.

Si l&#39;acheteur ajoute une adresse de livraison, l&#39;accord de négociation doit être révisé et le vendeur peut poursuivre le processus de négociation jusqu&#39;à ce qu&#39;un accord soit trouvé, ou le vendeur refuse le devis.

**Étape 3 : l’acheteur accepte les guillemets (passage en caisse)**

L&#39;acheteur accepte le prix proposé et passe en caisse. Des remises supplémentaires ne peuvent pas être ajoutées au devis négocié.

Les options d’expédition sont verrouillées lors du passage en caisse.

## État des citations

L’état du guillemet fournit des informations sur l’état actuel du guillemet dans le processus de devis. Le statut d&#39;un devis ne change que lorsqu&#39;un acheteur ou un vendeur agit sur le devis. Par exemple, le statut passe à la commande si un acheteur sélectionne [!UICONTROL Proceed to Checkout] sur un devis actif.

- *[!UICONTROL New]** - L’acheteur a soumis une demande de devis, mais elle n’a pas été consultée par le vendeur. La demande peut être mise à jour par l&#39;acheteur jusqu&#39;à ce qu&#39;elle soit ouverte par le vendeur.

- **[!UICONTROL Draft]** - Le vendeur crée un devis préliminaire pour un acheteur. Le devis n&#39;est pas visible pour l&#39;acheteur tant que le vendeur n&#39;a pas ajouté les détails de l&#39;offre (articles, quantité, réduction, etc.) et l&#39;a envoyé à l&#39;acheteur.

- **[!UICONTROL Open]** - Le vendeur a ouvert la demande et est en train de la réviser et de préparer une réponse.

- **[!UICONTROL Submitted]** - Le vendeur a envoyé une réponse à l’acheteur. L’enregistrement de citation ne peut pas être modifié pendant le processus de négociation.

- **[!UICONTROL Client Reviewed]** - L’acheteur a consulté la réponse du vendeur et est en train de préparer une réponse.

- **[!UICONTROL Updated]** - L’acheteur a envoyé une réponse, mais elle n’a pas été consultée par le vendeur.

- **[!UICONTROL Ordered]** - L’acheteur a soumis la commande sur la base du devis négocié.

- **[!UICONTROL Closed]** - L’acheteur a annulé la demande de devis.

- **[!UICONTROL Declined]** - Le vendeur a refusé la demande de devis. Toute tarification personnalisée est supprimée du devis et l’enregistrement est verrouillé pour les modifications ultérieures.

- **[!UICONTROL Expired]** - L’acheteur n’a pas répondu à la réponse du vendeur dans le délai indiqué et le devis n’est plus valide.

## Ressources de rôle B2B pour les guillemets de magasin

Les options de configuration des guillemets sont contrôlées à l’aide des [ressources de rôle](../systems/permissions-user-roles.md#role-resources). Ces ressources de rôle doivent être définies pour le rôle d’utilisateur administrateur attribué à l’administrateur du magasin.

Pour accorder l’accès aux fonctions de guillemet dans l’administrateur, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, sélectionnez le rôle et accédez à [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] dans l’arborescence_ Role Resources _.

![Rôles et autorisations de citations](./assets/roles-permissions-quotes.png){width="700" zoomable="yes"}

## Application d’une action

Dans l’administrateur, les administrateurs et les vendeurs B2B peuvent gérer les guillemets de la grille de devis à l’aide du menu [!UICONTROL Actions].

![Guillemets](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Dans la première colonne de la grille, cochez la case correspondant à chaque enregistrement auquel vous souhaitez appliquer l’action.

1. Dans le **[!UICONTROL Actions]**, sélectionnez l’action à appliquer.

### Afficher un guillemet

1. Dans la colonne **[!UICONTROL Actions]** d&#39;un enregistrement, cliquez sur **[!UICONTROL View]**.

1. Pour répondre à la demande du client, suivez les instructions et commencez le processus de [négociation de prix](quote-price-negotiation.md).

### Activité Afficher le guillemet

Affichez la chronologie de la négociation, la communication et toute autre activité de devis de [!UICONTROL Comments] et [!UICONTROL History Log] : les informations incluent les modifications d’état, les mises à jour des informations sur les clients et l’expédition, les mises à jour des articles et des prix, ainsi que d’autres informations importantes.

1. Ouvre une citation.

1. Affichez les commentaires et l’historique de la négociation des guillemets en accédant à **[!UICONTROL Negotiation]** et en sélectionnant **[!UICONTROL Comments]** et **[!UICONTROL History Log]**.

   ![Afficher l’historique](./assets/quote-view-history.png){width="400"}

1. L’historique est également suivi au niveau des éléments de ligne.

   ![Afficher l’historique des éléments de ligne](./assets/quote-view-line-item-history.png){width="400"}


### Refuser une demande de devis

Seules les demandes de guillemet ayant le statut `Open` peuvent être refusées.

1. Sélectionnez chaque demande de devis ouverte que vous souhaitez refuser.

1. Définissez le contrôle _[!UICONTROL Actions]_sur `Declined`.

1. Lorsque vous y êtes invité, saisissez la raison pour laquelle le guillemet a été refusé, puis cliquez sur **[!UICONTROL Confirm]**.

   ![Refuser la citation ?](./assets/quote-decline-confirm.png){width="400"}
