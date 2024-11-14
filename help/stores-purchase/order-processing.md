---
title: Workflow et traitement des commandes
description: Découvrez le workflow des commandes, l’état qui s’applique à chaque étape et comment déplacer les commandes au cours de ce processus.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1718'
ht-degree: 0%

---

# Workflow et traitement des commandes

Lorsqu’un client passe une commande, une commande client est créée en tant qu’enregistrement temporaire de la transaction. Dans la grille Commandes, les commandes client ont initialement un statut &quot;En attente&quot; et peuvent être annulées à tout moment jusqu&#39;à ce que le paiement soit traité. Une fois le paiement confirmé, la commande peut être facturée et expédiée.

**Étape 1 : Passer commande** - Le processus de passage en caisse commence lorsque l’acheteur clique sur **[!UICONTROL Go to Checkout]** sur la page du panier ou [effectue des ](reorders-allow.md) directement depuis son compte client.

**Étape 2 : Commande en attente** - L’état initial de la commande client est `Pending`. Dans cet état, le paiement n&#39;a pas été traité et la commande peut toujours être éditée ou annulée. Cet état se produit lorsque le mode de paiement est configuré pour le mode d’autorisation.

**Étape 3 : Recevoir le paiement** - L’état de la commande passe à `Processing` lorsque le paiement est reçu ou autorisé. Selon le mode de paiement, vous pouvez recevoir une notification lorsque la transaction est autorisée ou traitée. Cet état se produit automatiquement lorsque le mode de paiement est configuré pour le mode de capture ou de vente d’intention.

**Étape 4 : Commande de facture** - Une commande est généralement facturée après réception du paiement. Le mode de paiement détermine les options de facturation nécessaires à la commande. Une fois la facture générée et envoyée, une copie est envoyée au client. Si le mode de paiement est configuré avec l’action de paiement `capture` ou `intent sale`, une facture est générée automatiquement lorsque le paiement est autorisé et capturé.

>[!NOTE]
>
>Les factures ne sont pas créées automatiquement pour les commandes passées à l’aide de `Gift Card`, `Store Credit`, `Reward Points` ou d’autres méthodes de paiement hors ligne.

**Étape 5 : Réserver un seul envoi** - L’état de la commande passe à `Complete` lorsque les détails de l’envoi sont terminés, que l’envoi est réservé et que l’expédition est définie. Les conditions d’expédition sont remplies avec un bon de livraison et une étiquette d’expédition imprimées ou l’option _Notifier prête pour la récupération_ est sélectionnée (méthode de remise en magasin). Le client reçoit la notification et le package est expédié. Si des numéros de tracking sont utilisés, l&#39;envoi peut être tracké à partir du compte du client.

>[!NOTE]
>
>Pour plus d’informations sur l’état de la commande et les options de configuration du mode de paiement, voir [État de la commande](order-status.md) et [Paiements](payments.md).

## Afficher une commande

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Recherchez l’ordre dans la grille.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL View]**.

1. Vérifiez l’état de la commande :

   - Une commande `Pending` peut être modifiée, suspendue, annulée ou facturée et expédiée.

   - Une commande `Processing` ne peut plus être modifiée ou annulée en grande partie, mais l’adresse de facturation et de livraison peut être modifiée.

   - Une commande `Completed` peut être réordonnée.

L’email du client peut être édité à tout moment dans le workflow de commande en modifiant le client. L&#39;email ne peut pas être modifié si la commande a été passée par un invité.

Le panneau de gauche d’une commande ouverte permet d’accéder à différents types d’informations liées à la commande.

![Afficher la commande](./assets/order-view.png){width="700" zoomable="yes"}

## Traitement de la commande

Lorsqu’un client passe une commande, une commande client est créée en tant qu’enregistrement temporaire de la transaction. La commande client a l’état `Pending` jusqu’à ce que le paiement soit reçu. Lorsque le statut est `Pending`, les commandes peuvent être éditées ou annulées jusqu&#39;à la réception du paiement et la génération d&#39;une facture. Une façon facile d&#39;y penser est que les commandes deviennent des factures et les factures deviennent des envois. La grille Commandes répertorie toutes les commandes, où qu’elles se trouvent dans le workflow. Pour savoir comment aider les clients avec une commande, voir [Mise à jour d’une commande](order-update.md).

![Commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

Pour ouvrir une commande `Pending`, cliquez sur **[!UICONTROL Edit]** dans le coin supérieur droit.

>[!NOTE]
>
>Les commandes ne peuvent être modifiées que si leur état est `Pending`. Le bouton Modifier n’est pas visible pour les commandes dont l’état est différent ou pour les commandes basées sur un [ guillemet négocié](../b2b/quotes.md).

![Modifier la commande commerciale](./assets/order-pending.png){width="600" zoomable="yes"}

Consultez les sections suivantes de la commande client à l’aide de la description des champs à titre de référence.

### Descriptions des vues de commande

| Onglet | Description |
|--- |--- |
| [!UICONTROL Information] | Affichez des informations détaillées sur la commande et le compte, notamment les adresses de facturation et d’expédition, les méthodes de paiement et de diffusion, les commandes d’articles, les totaux et les notes. |
| [!UICONTROL Invoices] | Répertorie chaque facture associée à la commande. |
| [!UICONTROL Credit Memos] | Répertorie chaque avoir associé à la commande. |
| [!UICONTROL Shipments] | Répertorie chaque enregistrement d’expédition associé à la commande. |
| [!UICONTROL Comments History] | Répertorie toutes les notes liées à la commande. |

{style="table-layout:auto"}

>[!NOTE]
>
>Un utilisateur administrateur doit disposer de **[!UICONTROL Sales / Archive]** [ autorisations](../systems/permissions-user-roles.md) pour la portée de son rôle afin d’afficher les onglets de commande _Factures_, _Avoir de crédit_ et _Expéditions_.

### Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Cancel]** | Annule la commande client. |
| **[!UICONTROL Send Email]** | Envoie un courrier électronique au client au sujet de la commande. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Définit l’état de la commande client sur `On Hold`. Pour libérer le blocage de la commande client, choisissez **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | Crée une facture à partir de la commande client en la convertissant en facture. |
| **[!UICONTROL Ship]** | Crée un enregistrement d’expédition pour la commande. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | S’affiche uniquement lorsqu’une commande est placée en tant que diffusion en magasin. Avertit le client que la commande est prête à être récupérée. |
| **[!UICONTROL Reorder]** | Crée une commande client en fonction de la commande en cours. |
| **[!UICONTROL Edit]** | Ouvre un ordre en attente en mode d’édition. Le bouton Modifier n’est pas visible pour les commandes dont l’état est `Processing` ou les commandes reposant sur des guillemets négociés. |

{style="table-layout:auto"}

### Annuler une commande

Vous pouvez [annuler](order-update.md) des commandes qui ne sont pas encore facturées. Un [avoir](credit-memos.md) doit être émis si un client souhaite annuler une commande après sa facturation (le paiement est capturé).

Si une commande est `Pending` ou `Processing` et que le paiement n’est pas capturé ou n’est pas entièrement capturé, vous pouvez [annuler la commande](#void-an-order) au lieu de l’annuler.

Pour restaurer une commande annulée, cliquez sur le bouton **[!UICONTROL Reorder]** et une nouvelle commande est créée avec le statut `Pending`.

>[!NOTE]
>
>L’annulation d’une commande engendre également un vide, mais l’annulation d’une commande ne déclenche pas d’annulation.

### Vider une commande

Seules les commandes qui ne sont pas facturées, dont l’état est `Processing` et le [ paramètre d’intégration de paiement `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions) peuvent être [annulées](order-update.md#void-a-processing-order). Après avoir annulé une commande, vous pouvez l’annuler.

### [!UICONTROL Order and Account Information]

![Informations sur la commande et le compte](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Informations sur la commande

| Champ | Description |
|--- |--- |
| [!UICONTROL Order Number] | Le numéro de commande apparaît en haut de la commande client, suivi d’une note indiquant si l’email de confirmation a été envoyé. |
| [!UICONTROL Order Date] | Date et heure auxquelles la commande a été passée. |
| [!UICONTROL Purchased From] | Indique la vue du site web, du magasin et du magasin où la commande a été passée. |
| [!UICONTROL Placed from IP] | Indique l’adresse IP de l’ordinateur sur lequel la commande a été passée. |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Indique le [guillemet](../b2b/quotes.md) à partir duquel la commande a été générée, le cas échéant. Le nom du guillemet est lié au guillemet. |

{style="table-layout:auto"}

#### Informations du compte

| Champ | Description |
|--- |--- |
| [!UICONTROL Customer Name] | Nom du client ou de l’acheteur qui a passé la commande. Le Nom du client est lié au profil du client. |
| [!UICONTROL Email] | Adresse électronique du client ou de l’acheteur. L’adresse électronique est liée pour ouvrir un nouveau message électronique. |
| [!UICONTROL Customer Group] | Nom du groupe de clients ou du catalogue partagé auquel le client est affecté. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Nom de la société à laquelle l’acheteur est associé et pour le compte de laquelle la commande est passée. Le nom de la société est lié au [profil de la société](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Informations sur l’adresse](./assets/order-address-information.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Billing Address] | Nom du client ou de l’acheteur qui a passé la commande, suivi de l’adresse de facturation, du numéro de téléphone et de la [TVA](vat.md), le cas échéant. Le numéro de téléphone est associé à une numérotation automatique sur un appareil mobile. |
| [!UICONTROL Shipping Address] | Nom de la personne à l’attention de laquelle la commande doit être expédiée, suivi de l’adresse de livraison et du numéro de téléphone. Le numéro de téléphone est associé à une numérotation automatique sur un appareil mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Mode de paiement et d’expédition](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Payment Information] | Mode de paiement à utiliser pour la commande et numéro de la commande, le cas échéant, suivi de la devise utilisée pour la commande. Si la commande est imputée au crédit de l’entreprise par l’intermédiaire de l’option [ Paiement sur le compte ](../b2b/enable-basic-features.md#configure-payment-on-account), le montant imputé au compte est indiqué. |
| [!UICONTROL Shipping & Handling Information] | Le mode d’expédition à utiliser et les frais de gestion applicables. |

{style="table-layout:auto"}

### Vérifier les éléments triés

![Éléments commandés](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Dans la section **[!UICONTROL Order Total]** , procédez comme suit :

1. Saisissez un **[!UICONTROL Comment]** à inclure avec la commande.

1. Si vous souhaitez envoyer le commentaire par courrier électronique au client, cochez la case **[!UICONTROL Notify Customer by Email]** .

1. Si vous souhaitez que le commentaire soit visible dans le compte client, cochez la case **[!UICONTROL Visible on Storefront]** .

   ![Total de commande](./assets/order-total.png){width="600" zoomable="yes"}

1. Si vous êtes prêt à facturer la commande, cliquez sur **[!UICONTROL Invoice]** et suivez les instructions pour [créer une facture](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Champ | Description |
|--- |--- |
| [!UICONTROL Product] | Nom du produit, SKU et options, le cas échéant. |
| [!UICONTROL Item Status] | Indique l’état de l’élément. Valeur : `Ordered` |
| [!UICONTROL Original Price] | Prix du catalogue d’origine de l’article avant remises. |
| [!UICONTROL Price] | Prix d’achat de l’article. Cette valeur reflète toute remise appliquée à l’article à partir du catalogue partagé, le cas échéant. |
| [!UICONTROL Qty] | La quantité commandée. |
| [!UICONTROL Subtotal] | Le sous-total est le prix d’achat multiplié par la quantité. |
| [!UICONTROL Tax Amount] | Montant de la taxe qui s’applique à l’élément en tant que valeur décimale. |
| [!UICONTROL Tax Percent] | Pourcentage de la taxe appliquée à cet article en pourcentage. |
| [!UICONTROL Discount Amount] | La remise qui s’applique à cet article. La valeur de remise est zéro si la commande est basée sur un guillemet. |
| [!UICONTROL Row Total] | Total de l’article, y compris les taxes applicables qui sont dues au niveau du produit, moins les remises. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Champ | Description |
|--- |--- |
| [!UICONTROL Status] | Affiche l’état de la commande client. |
| [!UICONTROL Comment] | Zone de texte utilisée pour saisir un commentaire pour le client qui accompagne la commande. <br/>**[!UICONTROL Notify Customer by Email]**- Cochez la case si vous souhaitez envoyer le commentaire au client sous la forme d’un email distinct.<br/>**[!UICONTROL Visible on Storefront]** - Cochez la case si vous souhaitez que le commentaire soit visible à partir du compte du client. <br/>**[!UICONTROL Submit Comment]**- Envoie le commentaire et envoie par courrier électronique, le cas échéant. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Champ | Description |
|--- |--- |
| [!UICONTROL Shipping & Handling] | Montant des frais d’expédition et de gestion. |
| [!UICONTROL Tax] | Le montant de la taxe appliquée à la commande, le cas échéant. |
| [!UICONTROL Grand Total] | Total de la commande. |
| [!UICONTROL Total Paid] | Montant total payé pour la commande, le cas échéant. |
| [!UICONTROL Total Refunded] | Montant total remboursé de la commande, le cas échéant. |
| [!UICONTROL Total Due] | Montant total qui est dû. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Le montant du crédit de magasin disponible appliqué à la commande, le cas échéant. |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Prix total des articles du devis, sans taxe, selon la tarification du catalogue partagé ou du catalogue standard utilisé comme base du devis. Si la devise d’affichage du storefront diffère de la devise de base, la valeur apparaît dans les deux devises, l’affichage du storefront étant placé entre crochets. |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) La remise résultant d’un devis négocié entre l’acheteur et le vendeur. Si la devise d’affichage du storefront diffère de la devise de base, la valeur apparaît dans les deux devises, l’affichage du storefront étant placé entre crochets. |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Prix total du catalogue inférieur à la remise négociée. |

{style="table-layout:auto"}

## Démonstration du traitement des commandes

Regardez cette vidéo et en savoir plus sur le traitement des commandes et l’état :

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12&learn=on)
