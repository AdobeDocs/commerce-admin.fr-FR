---
title: Statut de la commande et réservations
description: Découvrez la saisie automatique des réservations ou les modifications qui mettent à jour la quantité vendable pour un stock (ou canal de vente) et la quantité en stock disponible par source.
exl-id: d264cb49-5aa8-4949-ae87-5efcd463d38c
feature: Inventory, Orders, Shipping/Delivery
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 0%

---

# Statut de la commande et réservations

[!DNL Inventory Management] prend en charge la facturation, les paiements, l’expédition et les annulations partiels et complets par commande. Lorsque vous gérez une commande par le biais du traitement, de la facturation, de l&#39;envoi et éventuellement des remboursements, [!DNL Commerce] entre automatiquement ou modifie les réservations pour mettre à jour la quantité vendable d&#39;un stock (ou canal de vente) et la quantité en stock disponible par source. Vous n’avez pas à accéder activement aux réservations ni à les enregistrer. Pour vous, il vous suffit d’exécuter, d’annuler ou de rembourser une commande.

Ces réservations ajustent toujours votre quantité vendable, avec des quantités positives ou négatives pour augmenter ou diminuer les quantités. Le résultat est une mise à jour de votre stock disponible et de vos quantités vendables pour une disponibilité de produit à jour.

Pour plus d’informations sur les commandes et les envois, voir [Gestion des commandes et des envois](shipments.md).

## Options de gestion des commandes

Selon l’état du stock et les demandes des clients, vous pouvez mettre à jour les commandes avec des paiements et annulations partiels, des envois partiels provenant de plusieurs sources ou pour les commandes différées, ou des notes de crédit pour rembourser les produits renvoyés.

### Expéditions

Après la facturation des commandes, envoyez des envois partiels ou complets jusqu’à ce que vous exécutiez la commande entière. Chaque expédition convertit les réservations, en déduisant le montant de la quantité du produit par source. Les compensations de réservation sont renseignées pour mettre à jour la quantité salable de votre stock. Si vous envoyez des envois partiels, chaque expédition déduit ce montant de la quantité et des réservations de votre produit. Toutes les réservations de produits non expédiées restent en place jusqu’à ce qu’elles soient également expédiées, de sorte que votre montant vendable soit à jour et que vous puissiez contrôler l’inventaire des produits et prendre en charge plusieurs envois à source et commandes différées.

### Commandes annulées

Si un client annule sa commande avant l’expédition (partielle ou totale), une nouvelle réservation est saisie pour renvoyer le montant de l’inventaire à la quantité vendable. Les réservations s&#39;annulent effectivement l&#39;une l&#39;autre, sans déduire la quantité provenant d&#39;aucune source. D’autres clients peuvent acheter activement ces quantités de produits par le biais des stocks et des canaux de vente associés.

### Commandes remboursées

Si un client demande un remboursement, émettez l’avoir pour les montants de produit partiels ou complets. Lorsque vous recevez les produits renvoyés, saisissez un avis de crédit pour fournir les fonds et mettre à jour le montant du produit. Lorsque vous sélectionnez l’option Revenir au stock , [!DNL Commerce] ajoute les quantités aux produits et aux sources qui ont expédié les commandes et les compensations de réservation pour mettre à jour les quantités vendables pour le stock associé.

## Types de commande

Les commandes simples commencent par un panier, continuent de payer et se terminent par une livraison satisfaite. Dans ces commandes, [!DNL Inventory Management] traite facilement les réservations par rapport à la disponibilité (ou à la quantité vendable) dans le panier et le passage en caisse, et déduit du stock disponible à l&#39;expédition.

![Processus pour une commande simple](assets/diagram-simple-order-flow.png){width="600" zoomable="yes"}

Une commande plus compliquée peut comporter des annulations partielles, des envois partiels et des remboursements. Dans ce cas, les réservations affectent l&#39;inventaire disponible afin d&#39;ajouter des quantités pour les annulations et les remboursements et de diminuer les quantités lorsqu&#39;elles sont commandées et expédiées.

![Processus pour une commande compliquée](assets/diagram-complicated-order-flow.png){width="600" zoomable="yes"}

Les réservations de disponibilité et les modifications de stock se produisent en fonction de l’état de la commande.

## Statut et réservations

Les tableaux suivants détaillent la commande et le statut de l’avoir avec les modifications de réservation entrées par [!DNL Commerce] pour gérer votre inventaire.

| État de la commande | Description | Réservation pour une quantité acceptable |
|--|--|--|
| [!UICONTROL Open] | Nouveau et récemment soumis, aucun traitement | La réservation est enregistrée lorsque la commande est envoyée pour le stock. |
| [!UICONTROL Canceled] | Annulé en partie ou en totalité avant paiement | La compensation de réservation est saisie afin de restituer la quantité totale ou partielle à la quantité salable en stock. |
| [!UICONTROL On Hold] | Paiement et expédition non traités ou facturés | La réservation reste en place. |
| [!UICONTROL Suspected Fraud] | Non traité en raison de la fraude | Si elle est approuvée ou en révision, la réservation reste en place.<br/>Si vous refusez, la réservation reste en place jusqu’à ce que le marchand décide d’approuver ou d’annuler.<br/> Si l&#39;annulation est annulée, la compensation de la réservation est renseignée pour renvoyer la quantité complète à la quantité vendable en stock. |
| [!UICONTROL Pending] | En attente de paiement | La réservation reste en place. |
| [!UICONTROL Processing] | Traitement du paiement non reçu | La réservation reste en place. |
| [!UICONTROL Pending Payment] | Paiement non reçu | La réservation reste en place. |
| [!UICONTROL Payment Review] | Paiement en cours de révision pour traitement et achèvement | La réservation reste en place. |
| [!UICONTROL Complete] | Payée et expédiée en intégralité | Le montant de la réservation est déduit de la quantité du produit pour la source sélectionnée lorsqu’elle est facturée partiellement ou intégralement. La compensation de la réservation est renseignée pour mettre à jour la quantité totale vendable. |
| [!UICONTROL Closed] | Remboursé ou archivé | En cas d’archivage, les quantités ne changent pas. Si elle est remboursée en totalité ou partiellement, la compensation de la réservation est saisie et convertie afin de rajouter les quantités de produits par source et la quantité vendable par stock. |

| État de la note de crédit | Description | Réservation pour une quantité acceptable |
|--|--|--|
| [!UICONTROL Open] | Le remboursement est exigible, non complété | Les réservations ne changent pas. |
| [!UICONTROL Refunded] | Finalisés, les fonds restitués | Si elle est remboursée en partie ou en totalité, la compensation de la réservation est saisie et convertie afin d&#39;additionner les quantités de produits par source et la quantité vendable par stock. |

## Exemple d’ordre complexe

Blake Sanders commande des vélos et des vêtements pour ses vacances en famille et pour s&#39;amuser. Ils voient de grandes ventes dans votre magasin Biking Adventures avec des stocks et des sources couvrant les États-Unis, le Canada et l&#39;Europe.

Ils achètent deux superbes vélos de parc pour leurs petits enfants, un BMX pour leur adolescent, un joli vélo tout-terrain pour eux-mêmes, et un vélo allemand moderne de fond pour leur conjoint. Le magasin avait une vente sur de mignonnes chemises, alors ils en ont acheté pour toute la famille. Consultez la liste des achats de vacances ci-dessous, les SKU correspondants et les réservations renseignées par rapport aux quantités négociables en stock.

![Ordre complexe](assets/diagram-order-complex.png){width="600" zoomable="yes"}

Ils montrent à leur famille ce qu&#39;ils ont trouvé, mais font quelques changements. Avant la fin du paiement, ils annulent deux des SKU 33-BikeFun (les enfants ne les aimaient pas). Il s’agit d’une annulation partielle en raison d’un paiement en attente, donc aucune note de crédit n’est nécessaire. Pour mettre à jour, [!DNL Commerce] ajoute à nouveau le stock de quantité vendable pour le Canada. La commande est payée et tous les produits sont livrés, arrivant à temps pour les vacances. [!DNL Commerce] met à jour la quantité vendable et les quantités sources pour les entrepôts d&#39;expédition pour les produits expédiés.

Mais la chemise ne correspondait pas tout à fait à leur conjoint. Blake demande un remboursement et renvoie sa chemise. La création de la note de crédit ajoute une chemise 54-BikeLife à l&#39;entrepôt de stock et de livraison du Canada.

- **Produits livrés** - Avec les produits achetés et expédiés, [!DNL Commerce] met à jour l’inventaire. Les compensations de réservation sont converties en déductions de quantité en stock à partir de la source expédiée. La quantité disponible pouvant être vendue est mise à jour pour le stock.

- **Produits annulés** - En annulant le stock, [!DNL Commerce] supprime la réservation de ce produit. Une compensation de réservation est alors renseignée au niveau des stocks afin de rajouter les quantités salables pour l&#39;annulation partielle de deux chemises. Cela n’a aucune incidence sur la quantité de stock au niveau de la source.

- **Crédit mémo/produit remboursé** - En retournant du stock, il doit être ajouté aux quantités. Lors de l’émission de l’avoir, vous pouvez choisir de retourner en stock. [!DNL Commerce] ajoute la quantité d’inventaire à la source expédiée du produit. Les compensations de réservation permettent d&#39;effacer les éventuelles réserves restantes. La quantité vendable est recalculée par rapport à la quantité mise à jour.

![Mises à jour de la quantité de remboursement de la commande](assets/diagram-order-refund.png){width="600" zoomable="yes"}
