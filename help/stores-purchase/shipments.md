---
title: Expéditions
description: Découvrez comment créer des enregistrements d’expédition pour des factures et annuler des envois.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Expéditions

La grille _[!UICONTROL Shipments]_&#x200B;répertorie l’enregistrement de l’expédition de toutes les factures qui ont été préparées pour l’expédition. Un enregistrement d’expédition peut être généré lorsqu’une commande est [facturée](invoices.md) ou supérieure.

Adobe Commerce et Magento Open Source prennent en charge l’envoi de commandes partiel et complet, avec des options supplémentaires disponibles à partir d’[Inventory management](../inventory-management/introduction.md) et des extensions tierces.

![ Grille des envois](./assets/shipments.png){width="600" zoomable="yes"}

## Descriptions des colonnes

| Colonne ou contrôle | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez la case pour que chaque guillemet soit soumis à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Numéro séquentiel unique attribué lors de la première sauvegarde d’une nouvelle expédition. |
| [!UICONTROL Ship Date] | Date d’expédition |
| [!UICONTROL Order] | Numéro unique de la commande |
| [!UICONTROL Order Date] | Date et heure auxquelles la commande a été passée |
| [!UICONTROL Ship-to Name] | Nom de la personne à qui la commande est envoyée. |
| [!UICONTROL Total Quantity] | Quantité totale d’articles à envoyer |
| [!UICONTROL Action] | Afficher ouvre l’envoi en mode d’édition |

{style="table-layout:auto"}

Colonnes supplémentaires :

| Colonne | Description |
|--- |--- |
| [!UICONTROL Order Status] | Indique l’état de la commande. |
| [!UICONTROL Purchased From] | Indique la vue du site web, du magasin et du magasin où la commande a été passée. |
| [!UICONTROL Customer Name] | Nom du client ou de l’acheteur qui a passé la commande |
| [!UICONTROL Email] | Adresse électronique d’un client enregistré |
| [!UICONTROL Customer Group] | Nom du groupe de clients ou du catalogue partagé auquel le client est affecté. |
| [!UICONTROL Billing Address] | Nom du client ou de l’acheteur qui a passé la commande |
| [!UICONTROL Shipping Address] | Nom de la personne à qui la commande est envoyée. |
| [!UICONTROL Payment Method] | Mode de paiement à utiliser pour la commande |
| [!UICONTROL Shipping Information] | Méthode à utiliser pour envoyer la commande. |

{style="table-layout:auto"}

## Créer une expédition

Les instructions suivantes vous guident tout au long du processus de création d’une expédition dans Adobe Commerce ou Magento Open Source. Si Inventory management est activé, vous pouvez consulter [Créer des envois multiSource](../inventory-management/shipments-create.md) et sélectionner une source (ou un emplacement) et une quantité à envoyer par article.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre dans la grille et ouvrez-le.

1. Si la commande est payée, facturée et prête à être expédiée, cliquez sur **[!UICONTROL Ship]**.

   Les sections en haut de l’envoi contiennent le nom, l’adresse et les informations de paiement de la commande client.

1. Remplissez chaque section du formulaire d&#39;expédition en suivant les instructions des sections suivantes.

### [!UICONTROL Items to Ship]

Pour chaque élément de ligne dans l’ordre, modifiez le **[!UICONTROL Qty to Ship]** suivant les besoins.

### [!UICONTROL Shipping Information]

**Méthode 1 :** Utilisation de la page de commande

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Dans la colonne **[!UICONTROL Action]** de l&#39;ordre sélectionné, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Ship]**.

1. Faites défiler l’écran jusqu’au bloc _[!UICONTROL Payment & Shipping Method]_&#x200B;et cliquez sur **[!UICONTROL Add Tracking Number]**.

1. Définissez **[!UICONTROL Carrier]** :

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Pour tracker l&#39;envoi, saisissez les valeurs **[!UICONTROL Title]** et **[!UICONTROL Number]** .

**Méthode 2 :** à l’aide de la page d’expédition

Cette méthode n’est autorisée que si l’expédition de commande a déjà été créée à partir de la page de commande.
Vous pouvez modifier les informations d’expédition et de tracking si nécessaire à l’aide de la page d’expédition directe :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Recherchez et ouvrez l&#39;envoi en mode d&#39;édition.

1. Faites défiler l’écran jusqu’au bloc _[!UICONTROL Payment & Shipping Method]_.

1. Sélectionnez le **[!UICONTROL Carrier]**.

1. Saisissez un **[!UICONTROL Title]** pour le package.

1. Saisissez le suivi **[!UICONTROL Number]**.

1. Cliquez sur **[!UICONTROL Add]**.

1. Pour envoyer un email contenant des informations de suivi au client, cliquez sur **[!UICONTROL Send Tracking Information]**, puis confirmez l’action.

   Pour suivre l’emplacement d’une expédition, ouvrez-la en mode d’édition et cliquez sur **[!UICONTROL Track this shipment]**.

   ![Informations d’expédition et de suivi](./assets/tracking-information.png){width="600" zoomable="yes"}

### Boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Ferme le formulaire Nouvel envoi et revient à la commande |
| **[!UICONTROL Submit Shipment]** | Ajoute l’envoi pour la commande. |
| **[!UICONTROL Reset]** | Restaure toutes les valeurs d’origine. |

{style="table-layout:auto"}

### Commentaires sur l’expédition

1. Saisissez **Comments** pour l’expédition, si nécessaire.

1. Une fois l’envoi prêt, cliquez sur **Submit Shipment**.

## Configuration des commentaires pour les envois

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous _[!UICONTROL Sales]_, sélectionnez **[!UICONTROL Sales Email]**.

1. Développez la section **Commentaires sur l’expédition** et modifiez les paramètres suivant vos besoins :

   ![Configuration des commentaires d’expédition](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - L’option **[!UICONTROL Enabled]** est définie sur `Yes` par défaut, ce qui signifie que l’email est envoyé à un client lorsqu’un commentaire de livraison est saisi.

   - Pour **[!UICONTROL Shipment Comment Email Sender]**, sélectionnez la personne à partir de laquelle l’e-mail de commentaire d’expédition est envoyé. La valeur par défaut propose cinq adresses électroniques.

   - Pour **[!UICONTROL Shipment Comment Email Template]**, sélectionnez le modèle selon vos besoins ou sélectionnez l’option par défaut.

   - Pour **[!UICONTROL Shipment Comment Email Template for Guests]**, choisissez le modèle utilisé pour les clients qui n’ont pas de compte dans votre boutique.

   - Pour **[!UICONTROL Shipment Comment Email Copy To]**, saisissez les adresses électroniques permettant d’envoyer une copie d’email de commentaire d’expédition. Séparez plusieurs adresses électroniques par une virgule.

   - Pour **[!UICONTROL Shipment Comment Email Copy Method]**, sélectionnez la méthode `bcc` (copie de carbone aveugle) ou `separate email copy` en fonction de vos préférences.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Annulation d’une expédition

Avant qu&#39;une cargaison ne soit envoyée à un opérateur, elle peut être annulée en ouvrant la commande et en accédant à l&#39;envoi, à condition que le transporteur prenne en charge les annulations. Certains opérateurs limitent ou limitent les annulations après une réservation. Par exemple, UPS autorise les annulations, mais vous devez attendre 24 heures après la réservation de l’envoi. Si une expédition est annulée, l&#39;annulation ne peut pas être annulée. Le seul recours est de recréer l&#39;ordre.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre dans la grille.

1. Dans la colonne _Action_, choisissez **[!UICONTROL View]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Shipments]**.

   Si l’envoi peut être annulé, _[!UICONTROL Cancel Shipment]_&#x200B;apparaît comme une option dans la barre de boutons supérieure.

1. Cliquez sur **[!UICONTROL Cancel Shipment]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

L’état de l’expédition passe à `Canceled`. Si le transporteur ne prend pas en charge les annulations, un message d&#39;erreur s&#39;affiche et explique pourquoi l&#39;envoi n&#39;a pas pu être annulé.

## Description des champs d’expédition

### [!UICONTROL Shipping Information]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Carrier] | Nom de l’opérateur sélectionné |
| [!UICONTROL Title] | Nom descriptif attribué au package par l’opérateur. |
| [!UICONTROL Number] | Numéro de suivi associé affecté au package. |
| [!UICONTROL Action] | ![Icône de transaction](../assets/icon-delete-trashcan-solid.png) - Supprime les informations de package de l’enregistrement d’expédition. |
| [!UICONTROL Add] | Ajoutez un autre package à l’expédition. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Origin Location] | Affiche une liste des emplacements disponibles. |
| [!UICONTROL International] | Si cette case est cochée, l’expédition est identifiée comme étant internationale. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Description] | Description de l’élément. |
| [!UICONTROL SKU] | Unité de gestion des stocks de l’article. |
| [!UICONTROL Weight] | Le poids de l’élément. |
| [!UICONTROL Qty Ordered] | Quantité de l’article qui a été commandé. |
| [!UICONTROL Qty Shipped] | La quantité d’éléments qui ont été expédiés. |
| [!UICONTROL Qty Packed] | Le nombre d’éléments inclus dans ce module. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Comments] | Les commentaires sur l&#39;envoi sont destinés à un usage interne. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Téléchargez le libellé du package d’expédition. Taille : A6 (105 x 148 mm ; 4,1 x 5,6 pouces) |

{style="table-layout:auto"}
