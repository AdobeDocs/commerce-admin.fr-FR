---
title: '[!UICONTROL My Quote Templates]'
description: Découvrez l’expérience client des modèles de devis, disponible dans le tableau de bord du compte de storefront.
feature: B2B, Companies, Quotes
exl-id: 3d95a44e-b874-442b-af96-0dc6b589d0f7
source-git-commit: 71b9326aa5a8c3d7656b3c0f166cf25291b2abba
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# [!UICONTROL My Quote Templates]

Si les guillemets sont activés, la section _[!UICONTROL My Quotes Template]_du tableau de bord du compte client répertorie tous les modèles de devis associés au compte client. En fonction de leurs permissions, seuls les acheteurs qui effectuent des achats pour le compte d’une société peuvent demander un modèle de devis et négocier les tarifs et les conditions des commandes récurrentes.

![Mes modèles de devis](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

La liste de modèles de devis classe les modèles par état.

- **[!UICONTROL Active Quote Templates]** répertorie les modèles qui ont été négociés et approuvés pour utilisation. Les informations comprennent le nombre total de guillemets minimum et les commandes passées si ces options ont été configurées pendant le processus de négociation. Les acheteurs peuvent générer un devis lié à partir du modèle pour envoyer une commande en fonction des termes de devis.

- **[!UICONTROL In Review]** répertorie les modèles du processus de négociation qui affichent l’état actuel et fournissent un lien pour ouvrir le modèle.

- **[!UICONTROL Inactive]** répertorie les modèles qui ont expiré, ont été annulés ou ne sont plus valides car un acheteur a épuisé le nombre de commandes engagées autorisées.

Pour l’acheteur, la page *[!UICONTROL My Quotes Templates]* est le point focal de toute communication entre l’acheteur et le vendeur pendant le processus de négociation.

Un acheteur qui accepte les conditions négociées proposées par le vendeur peut accepter le modèle, puis l’utiliser pour générer des devis liés prévalidés qui peuvent être utilisés pour passer des commandes.

- Actions relatives à la gestion du modèle de devis :

   - Annulation d’un modèle
   - Envoyer au vendeur pour révision
   - Accepter le modèle de devis
   - Modification de la date d’expiration du modèle de devis
   - Ajouter une adresse de livraison

- Actions de mise à jour des détails du modèle de devis lors du processus de négociation :

   - Examinez les prix et les mises à jour des articles.
   - Si des seuils de quantité ont été configurés sur le modèle de devis, ajustez les valeurs minimale et maximale.
   - Suivez le processus de négociation à partir des sections [!UICONTROL Comments] et [!UICONTROL History] .
   - Pour les modèles en cours de révision, l’acheteur peut modifier le modèle de devis en supprimant les éléments.
   - Communiquez et négociez avec le vendeur en ajoutant des notes au niveau de l’article et du guillemet.

  Après avoir apporté des modifications, l’acheteur renvoie le modèle au vendeur pour révision.

- Actions générales lors de la négociation :

   - Envoyer un modèle de devis au vendeur pour révision
   - Accepter le modèle de devis
   - Annuler pour mettre fin à la négociation et fermer le devis

L&#39;exemple suivant illustre un modèle de devis mis à jour par l&#39;acheteur et renvoyé au vendeur pour révision.

![Modèle de devis vue par l’utilisateur](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

Les modèles avec le statut `Submitted` sont verrouillés jusqu’à ce que le vendeur passe en revue et mette à jour le modèle et le renvoie à l’acheteur.

## Créer un modèle de devis

L&#39;acheteur peut lancer le processus de négociation du modèle de devis en utilisant l&#39;une des méthodes suivantes :

- Créez un modèle à partir d’un guillemet existant en cliquant sur l’action **[!UICONTROL Create quote template]**.

- Envoyez une demande de devis depuis le storefront et ajoutez des commentaires demandant au représentant commercial de créer un modèle de devis à partir de la demande de devis.

## Afficher un modèle de devis

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quote Templates]**.

1. Recherche le modèle de guillemet dans la liste et clique sur **[!UICONTROL View]** dans la colonne _[!UICONTROL Action]_.

## Ajouter une adresse de livraison

L&#39;acheteur ne peut pas accepter un modèle de devis tant qu&#39;il ne possède pas d&#39;adresse de livraison.

1. L&#39;acheteur se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL My Quote Templates]**.

1. Sélectionne le modèle de guillemet désiré.

1. Dans la section **[!UICONTROL Shipping Information]**, cliquez sur **[!UICONTROL Add New Address]**.

1. Renseigne les détails de la nouvelle adresse.

1. Clics **[!UICONTROL Save Address]**.

Une fois que l’acheteur a ajouté l’adresse, il renvoie le modèle au vendeur pour révision. Le vendeur fournit les options d’expédition et de livraison. Ces mises à jour peuvent avoir une incidence sur le prix négocié. Les options d’expédition sont verrouillées lors du passage en caisse.

## Générer un guillemet lié

Une fois que l’acheteur a accepté un modèle de devis, il peut l’utiliser pour générer des guillemets liés prévalidés à partir de *[!UICONTROL My Quote Templates dashboard]* ou du modèle de devis à l’aide de l’action **[!UICONTROL Generate a quote]**.

Le guillemet lié comprend une notification indiquant qu’il est approuvé et prêt à être extrait. Il fournit également un lien vers le modèle de guillemet dans les informations de l’en-tête.

![Guillemet lié généré à partir d’un modèle de guillemet](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

Si le modèle de guillemet a été configuré avec un seuil de commande, le nombre est incrémenté lors de la génération du guillemet associé.

Les acheteurs peuvent effectuer les actions suivantes à partir d’un guillemet lié :

- Si le guillemet est configuré avec des seuils de quantité, ajustez la quantité de commande pour les éléments de ligne.
- Passez à la caisse pour envoyer une commande.
- Supprimez ou imprimez le guillemet.
- Ouvrez le modèle de guillemet utilisé pour générer le guillemet.

## Annuler un modèle de devis

Sur la page du modèle de guillemet, cliquez sur **[!UICONTROL Cancel Quote Template]**.

Le modèle de guillemet est annulé et l’état du guillemet passe à `Closed`. Les guillemets fermés restent dans la liste de *[!UICONTROL Inactive]* guillemets et sont répertoriés dans la grille _[!UICONTROL Quote Templates]_de l’administrateur.
