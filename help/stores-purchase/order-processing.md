---
title: Workflow et traitement des commandes
description: Découvrez le workflow de commande, le statut qui s’applique à chaque étape et comment déplacer des commandes tout au long de ce processus.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 82f040fa34cf96af6f1e9752f8d9f1ddeab9f84c
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# Workflow et traitement des commandes

Lorsqu&#39;un client passe une commande, une commande client est créée comme enregistrement temporaire de la transaction. Dans la grille Commandes, les commandes client ont initialement le statut « En attente » et peuvent être annulées à tout moment jusqu&#39;à ce que le paiement soit traité. Une fois le paiement confirmé, la commande peut être facturée et expédiée.

**Étape 1 : passer une commande** - Le processus de passage en caisse commence lorsque l’acheteur clique sur **[!UICONTROL Go to Checkout]** page du panier ou [passe une nouvelle commande](reorders-allow.md) directement depuis son compte client.

**Étape 2 : Commande en attente** - Le statut initial de la commande client est `Pending`. Dans ce cas, le paiement n&#39;a pas été traité et la commande peut toujours être modifiée ou annulée. Cet état se produit lorsque le mode de paiement est configuré pour le mode d&#39;autorisation.

**Étape 3 : recevoir le paiement** - Le statut de la commande devient `Processing` à la réception ou à l’autorisation du paiement. Selon le mode de paiement, vous pouvez recevoir une notification lorsque la transaction est autorisée ou traitée. Cet état se produit automatiquement lorsque le mode de paiement est configuré pour le mode de capture ou d&#39;intention de vente.

**Étape 4 : Commande de facture** - Une commande est généralement facturée après réception du paiement. Le mode de paiement détermine les options de facturation nécessaires pour la commande. Une fois la facture générée et soumise, une copie est envoyée au client. Si le mode de paiement est configuré avec l&#39;action de paiement `capture` ou `intent sale`, une facture est générée automatiquement lorsque le paiement est autorisé et capturé.

>[!NOTE]
>
>Les factures ne sont pas créées automatiquement pour les commandes passées à l&#39;aide de `Gift Card`, `Store Credit`, `Reward Points` ou d&#39;autres méthodes de paiement hors ligne.

**Étape 5 : Enregistrer une expédition unique** - Le statut de la commande devient `Complete` lorsque les détails de l&#39;expédition sont terminés, que l&#39;expédition est enregistrée et que l&#39;expédition est définie. L&#39;exigence d&#39;expédition est satisfaite avec un bon de livraison imprimé et une étiquette d&#39;expédition ou l&#39;option _Notifier prêt pour le retrait_ est sélectionnée (méthode de livraison en magasin). Le client reçoit une notification et le colis est expédié. Si des numéros de suivi sont utilisés, l&#39;expédition peut être suivie à partir du compte du client.

>[!NOTE]
>
>Pour plus d&#39;informations sur le statut de la commande et les options de configuration du mode de paiement, voir [Statut de la commande](order-status.md) et [Paiements](payments.md).

## Afficher une commande

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Recherchez la commande dans la grille.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL View]**.

1. Vérifier le statut de la commande :

   - Une commande `Pending` peut être modifiée, mise en attente, annulée ou facturée et expédiée.

   - Une commande `Processing` ne peut plus être modifiée ou annulée en grande partie, mais l’adresse de facturation et d’expédition peut être modifiée.

   - Un ordre de `Completed` peut être réorganisé.

L’e-mail du client ou de la cliente peut être modifié à tout moment dans le workflow de commande en modifiant le ou la client(e). L’e-mail ne peut pas être modifié si la commande a été passée par un invité.

Le panneau de gauche d’une commande ouverte permet d’accéder à différents types d’informations liés à la commande.

![Afficher la commande](./assets/order-view.png){width="700" zoomable="yes"}

## Traitement d’une commande

Lorsqu&#39;un client passe une commande, une commande client est créée comme enregistrement temporaire de la transaction. La commande client a le statut `Pending` jusqu&#39;à réception du paiement. Tant que `Pending` statut est défini, les commandes peuvent être modifiées ou annulées jusqu&#39;à la réception du paiement et la génération d&#39;une facture. Il est facile de penser que les commandes deviennent des factures et les factures deviennent des livraisons. La grille Commandes répertorie toutes les commandes, quel que soit leur emplacement dans le workflow. Pour savoir comment aider les clients avec une commande, voir [Mettre à jour une commande](order-update.md).

![Commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

Pour ouvrir un ordre de `Pending`, cliquez sur **[!UICONTROL Edit]** dans le coin supérieur droit.

>[!NOTE]
>
>Les commandes ne peuvent être modifiées que lorsqu’elles ont le statut `Pending`. Le bouton Modifier n&#39;est pas visible pour les commandes dont le statut est différent ou pour les commandes basées sur un [devis négocié](../b2b/quotes.md).

![Modifier commande client](./assets/order-pending.png){width="600" zoomable="yes"}

Consultez les sections suivantes de la commande client à l&#39;aide des descriptions de champ à titre de référence.

### Descriptions de l’affichage des commandes

| Tabulation | Description |
|--- |--- |
| [!UICONTROL Information] | Affichez des informations détaillées sur la commande et le compte, y compris les adresses de facturation et d’expédition, les modes de paiement et de livraison, les articles, les commandes, les totaux et les notes. |
| [!UICONTROL Invoices] | Répertorie chaque facture associée à la commande. |
| [!UICONTROL Credit Memos] | Répertorie chaque avoir associé à la commande. |
| [!UICONTROL Shipments] | Répertorie chaque enregistrement d&#39;expédition associé à la commande. |
| [!UICONTROL Comments History] | Répertorie toutes les notes liées à la commande. |

{style="table-layout:auto"}

>[!NOTE]
>
>Un utilisateur administrateur doit disposer de **[!UICONTROL Sales / Archive]** [autorisations](../systems/permissions-user-roles.md) pour la portée de son rôle afin d’afficher les onglets _Factures_, _Avoirs_ et _Livraisons_ Commande.

### Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Retourne à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Cancel]** | Annule la commande client. |
| **[!UICONTROL Send Email]** | Envoie un e-mail sur la commande au client. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifie le statut de la commande client en `On Hold`. Pour lever le blocage de la commande client, choisissez **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | Crée une facture à partir de la commande client en la convertissant en facture. |
| **[!UICONTROL Ship]** | Crée un enregistrement d&#39;expédition pour la commande. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | S’affiche uniquement lorsqu’une commande est passée en tant que diffusion en magasin. Avertit le client que la commande est prête pour le retrait. |
| **[!UICONTROL Reorder]** | Crée une commande client basée sur la commande actuelle. |
| **[!UICONTROL Edit]** | Ouvre une commande en attente en mode d&#39;édition. Le bouton Modifier n&#39;est pas visible pour les commandes dont le statut est `Processing`, ni pour les commandes basées sur des devis négociés. |

{style="table-layout:auto"}

### Annuler une commande

Vous pouvez [annuler](order-update.md) les commandes qui ne sont pas encore facturées. Un [ avoir ](credit-memos.md) doit être émis si un client souhaite annuler une commande après sa facturation (le paiement est capturé).

Si une commande est `Pending` ou `Processing` et que le paiement n&#39;est pas saisi ou n&#39;est pas entièrement saisi, vous pouvez [annuler la commande](#void-an-order) au lieu de l&#39;annuler.

Pour restaurer une commande annulée, cliquez sur le bouton **[!UICONTROL Reorder]** et une nouvelle commande est créée avec le statut `Pending`.

>[!NOTE]
>
>L&#39;annulation d&#39;une commande entraîne également une annulation, mais l&#39;annulation d&#39;une commande ne déclenche pas une annulation.

### Annuler une commande

Seules les commandes client qui ne sont pas facturées, dont le statut est `Processing` et dont le paramètre d&#39;intégration de paiement [ est `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions), peuvent être [ annulées](order-update.md#void-a-processing-order). Après avoir annulé une commande, vous pouvez l’annuler.

### [!UICONTROL Order and Account Information]

![Informations sur la commande et le compte](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Informations sur la commande

| Champ | Description |
|--- |--- |
| [!UICONTROL Order Number] | Le numéro de commande apparaît en haut de la commande client, suivi d&#39;une note indiquant si l&#39;e-mail de confirmation a été envoyé. |
| [!UICONTROL Order Date] | Date et heure auxquelles la commande a été passée. |
| [!UICONTROL Purchased From] | Indique l’affichage du site web, du magasin et du magasin dans lequel la commande a été passée. |
| [!UICONTROL Placed from IP] | Indique l&#39;adresse IP de l&#39;ordinateur à partir duquel la commande a été passée. |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Indique le [devis](../b2b/quotes.md) à partir duquel la commande a été générée, le cas échéant. Le nom du devis est lié au devis. |

{style="table-layout:auto"}

#### Informations sur le compte

| Champ | Description |
|--- |--- |
| [!UICONTROL Customer Name] | Nom du client ou de l’acheteur qui a passé la commande. Le nom du client est lié au profil du client. |
| [!UICONTROL Email] | Adresse e-mail du client ou de l’acheteur. L’adresse e-mail est liée pour ouvrir un nouvel e-mail. |
| [!UICONTROL Customer Group] | Nom du groupe de clients ou du catalogue partagé auquel le client est affecté. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Nom de la société à laquelle l&#39;acheteur est associé et pour le compte de laquelle la commande est passée. Le nom de la société est lié au [profil de la société](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Informations sur l’adresse](./assets/order-address-information.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Billing Address] | Nom du client ou de l’acheteur qui a passé la commande, suivi de l’adresse de facturation, du numéro de téléphone et de la [TVA](vat.md), le cas échéant. Le numéro de téléphone est lié à la numérotation automatique sur un appareil mobile. |
| [!UICONTROL Shipping Address] | Nom de la personne à l’attention de laquelle la commande doit être expédiée, suivi de l’adresse d’expédition et du numéro de téléphone. Le numéro de téléphone est lié à la numérotation automatique sur un appareil mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Mode de paiement et d’expédition](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Payment Information] | Mode de paiement à utiliser pour la commande et numéro de commande fournisseur, le cas échéant, suivi de la devise utilisée pour passer la commande. Si la commande est imputée au crédit de la société à l’aide de l’option [Paiement sur le compte](../b2b/enable-basic-features.md#configure-payment-on-account), le montant imputé au compte est indiqué. |
| [!UICONTROL Shipping & Handling Information] | La méthode d’expédition à utiliser et les frais de manutention applicables. |

{style="table-layout:auto"}

### Attributs d’ordre personnalisés

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

Les attributs de commande personnalisés vous permettent d’associer à la commande des informations supplémentaires spécifiques aux besoins de votre entreprise.

![Attributs d’ordre personnalisés](./assets/custom-order-attributes.png){width="600" zoomable="yes"}

Dans **[!UICONTROL Custom Order Attributes]** section, affiche tous les attributs de commande personnalisés et leurs valeurs actuelles.

Pour créer un attribut d’ordre personnalisé, saisissez un **[!UICONTROL Attribute Code]** et un **[!UICONTROL Value]**

Pour créer d’autres attributs de commande personnalisés, cliquez sur **[!UICONTROL Add Attribute]**.

Pour supprimer un attribut de commande personnalisé, cliquez sur l’icône **[!UICONTROL X]**.

>[!NOTE]
>
>Les attributs de commande personnalisés ne peuvent être modifiés que lorsque la commande a le statut `Pending`. Pour les commandes avec d’autres statuts, vous pouvez afficher les valeurs d’attribut, mais ne pouvez pas les modifier.

### Vérifier les éléments commandés

![Articles commandés](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Dans la section **[!UICONTROL Order Total]**, procédez comme suit :

1. Saisissez un **[!UICONTROL Comment]** à inclure dans la commande.

1. Si vous souhaitez envoyer le commentaire par e-mail au client ou à la cliente, cochez la case **[!UICONTROL Notify Customer by Email]** .

1. Si vous souhaitez que le commentaire soit visible dans le compte client, cochez la case **[!UICONTROL Visible on Storefront]**.

   ![Total de la commande](./assets/order-total.png){width="600" zoomable="yes"}

1. Si vous êtes prêt à facturer la commande, cliquez sur **[!UICONTROL Invoice]** et suivez les instructions pour [créer une facture](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Champ | Description |
|--- |--- |
| [!UICONTROL Product] | Nom du produit, SKU et options, le cas échéant. |
| [!UICONTROL Item Status] | Indique le statut de l’élément. Valeur : `Ordered` |
| [!UICONTROL Original Price] | Prix catalogue initial de l&#39;article avant remises. |
| [!UICONTROL Price] | Prix d’achat de l’article. Cette valeur reflète toute remise appliquée à l&#39;article du catalogue partagé, le cas échéant. |
| [!UICONTROL Qty] | Quantité commandée. |
| [!UICONTROL Subtotal] | Le sous-total est le prix d&#39;achat multiplié par la quantité. |
| [!UICONTROL Tax Amount] | Montant de taxe qui s&#39;applique à l&#39;article sous forme de valeur décimale. |
| [!UICONTROL Tax Percent] | Pourcentage de taxe appliqué à cet article sous forme de pourcentage. |
| [!UICONTROL Discount Amount] | Remise qui s&#39;applique à cet article. La valeur de remise est nulle si la commande est basée sur un devis. |
| [!UICONTROL Row Total] | Total de l&#39;élément de ligne, y compris les taxes applicables dues au niveau du produit, moins les remises. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Champ | Description |
|--- |--- |
| [!UICONTROL Status] | Affiche le statut de la commande client. |
| [!UICONTROL Comment] | Zone de texte utilisée pour saisir un commentaire à l’intention du client qui accompagne la commande. <br/>**[!UICONTROL Notify Customer by Email]**- Cochez la case si vous souhaitez envoyer le commentaire au client sous forme d’e-mail distinct.<br/>**[!UICONTROL Visible on Storefront]** - Cochez la case si vous souhaitez que le commentaire soit visible à partir du compte du client. <br/>**[!UICONTROL Update]**- Ajoute le commentaire et envoie un e-mail, le cas échéant. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Champ | Description |
|--- |--- |
| [!UICONTROL Shipping & Handling] | Montant facturé pour les frais d’expédition et de manutention. |
| [!UICONTROL Tax] | Montant de taxe appliqué à la commande, le cas échéant. |
| [!UICONTROL Grand Total] | Total de la commande. |
| [!UICONTROL Total Paid] | Montant total payé pour la commande, le cas échéant. |
| [!UICONTROL Total Refunded] | Montant total remboursé de la commande, le cas échéant. |
| [!UICONTROL Total Due] | Montant total dû. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Montant du crédit de magasin disponible appliqué à la commande, le cas échéant. |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Prix total des articles du devis sans taxe, en fonction du prix dans le catalogue partagé ou le catalogue standard utilisé comme base du devis. Si la devise d’affichage du storefront diffère de la devise de base, la valeur s’affiche dans les deux devises, le storefront s’affichant entre crochets. |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Remise résultant d&#39;un devis négocié entre l&#39;acheteur et le vendeur. Si la devise d’affichage du storefront diffère de la devise de base, la valeur s’affiche dans les deux devises, le storefront s’affichant entre crochets. |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Prix total du catalogue moins la remise négociée. |

{style="table-layout:auto"}

## Démonstration du traitement des commandes

Regardez cette vidéo pour en savoir plus sur le traitement et le statut des commandes :

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12&learn=on)
