---
title: "[!UICONTROL My Purchase Orders]"
description: Découvrez les commandes d’achat et comment les entreprises peuvent les utiliser pour gérer leurs achats.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Lorsque les commandes d’achat sont [activées pour une société](purchase-order-flow.md), toute commande pour un client connecté à un compte utilisateur de société est automatiquement créée en tant que commande d’achat (PO). Les utilisateurs de l’entreprise disposant des autorisations requises peuvent créer, modifier et supprimer les PO qu’ils créent, ainsi que les PO créés par les utilisateurs subordonnés.

![Mes commandes](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Les commandes d’achat créent un _instantané_ des prix des articles, des remises et des prix d’expédition au moment de la création de la commande. Si le prix d’un article change après la création du bon de commande, le prix d’origine est utilisé.

## Gestion des commandes d’achat

Sur la page _Afficher le bon de commande_, le client peut gérer le bon de commande, en fonction de ses [ autorisations de rôle](account-company-roles-permissions.md).

- Pour afficher le bon de commande, cliquez sur **[!UICONTROL View]**.
- Pour afficher les commentaires sur le bon de commande, cliquez sur l’onglet **[!UICONTROL Comments]** .
- Pour afficher l’historique complet des commandes, cliquez sur l’onglet **[!UICONTROL History Log]** .

>[!IMPORTANT]
>
>Si un article d’une commande est en rupture de stock ou n’est pas disponible en quantité suffisante, une erreur se produit lorsque la commande est convertie en commande réelle. Si les commandes en arrière-plan sont activées, la commande est traitée normalement.

## Nouveau bon de commande d’un bon de commande existant

Si le client dispose d’une commande d’achat existante et souhaite ajouter de nouveaux articles, il peut générer une commande d’achat en double avec de nouveaux produits ajoutés au nouveau bon de commande. Le client effectue les étapes suivantes :

1. Sur la page _Mon bon de commande_, le client localise le bon de commande et clique sur le lien **[!UICONTROL View]**.

1. Le client clique sur **[!UICONTROL Add Items to Shopping Cart]**.

   La page Panier s’ouvre avec tous les éléments répertoriés.

1. Effectue des ajouts ou des modifications.

1. (Facultatif) Utilise **[!UICONTROL Custom Reference Number]** pour ajouter un numéro de facture/de bon de commande interne à la commande.

1. Suit le workflow de passage en caisse normal et clique sur **[!UICONTROL Place Purchase Order]**.

S’il y a des articles dans son panier lorsqu’il clique sur _[!UICONTROL Add Items to Shopping Cart]_, le système affiche une boîte de dialogue. Cette boîte de dialogue leur permet de fusionner les articles du panier avec les nouveaux articles ou de remplacer les articles du panier par ceux du bon de commande.

Le bon de commande d’origine peut être fermé s’il n’est plus nécessaire.

## Approbation des commandes d’achat

Pour un client désigné comme approbateur en fonction de la structure de la société ou du rôle de société attribué, la page de tableau de bord _[!UICONTROL My Purchase Orders]_affiche l’onglet **[!UICONTROL Requires My Approval]**. Le client clique sur cet onglet pour consulter les PO qui attendent leur approbation. Le compteur indique le nombre de commandes en attente d’approbation.

Après avoir cliqué sur **[!UICONTROL View]** pour un bon de commande et consulté les détails, l’approbateur peut cliquer sur **[!UICONTROL Approve]** ou **[!UICONTROL Reject]**.

### Validation/rejet en bloc

Depuis Adobe Commerce 2.4.1, les approbateurs peuvent approuver ou rejeter simultanément plusieurs commandes.

1. Sur la page _[!UICONTROL My Purchase Order]_, cliquez sur l’onglet **[!UICONTROL Requires My Approval]**.

1. Cochez la case correspondant à chaque bon de commande à approuver ou à rejeter.

1. Cliquez sur **[!UICONTROL Approve Selected]** ou **[!UICONTROL Reject Selected]**.

Un client ne peut sélectionner que les commandes dont le statut lui permet d’agir. Les administrateurs d’entreprise peuvent approuver ou rejeter en bloc les commandes actives de leur société.
