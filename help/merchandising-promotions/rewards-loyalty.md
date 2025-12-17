---
title: Programmes de récompense et de fidélité
description: Découvrez le système de points de récompense que vous pouvez utiliser pour stimuler l’engagement des clients et promouvoir la fidélisation de la clientèle.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: b0e9087016f7a6ce682e84feb931f7ad870e6420
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 0%

---

# Programmes de récompense et de fidélité

{{ee-feature}}

Le système _points de récompense_ d’Adobe Commerce vous permet de mettre en œuvre des programmes uniques qui stimulent l’engagement des clients et favorisent la fidélisation de la clientèle. Des points peuvent être attribués pour un large éventail de transactions et d’activités client, et la configuration peut être définie pour contrôler l’attribution des points, le solde et l’expiration. Les clients peuvent échanger des points contre des achats, en fonction du taux de conversion que vous établissez entre les points de récompense et la devise.

## Règles de prix des paniers

Les points peuvent être récompensés aux clients selon une [ règle de panier d’achat ](price-rules-cart.md). Ils peuvent être récompensés comme la seule action de la règle de prix, ou avec une remise.

## Solde client

Les soldes des points de récompense peuvent être gérés par les utilisateurs administrateurs par client. Si cette option est activée dans le storefront, les clients peuvent également afficher les détails de leur solde de points.

## Échange de points

>[!NOTE]
>
>La configuration [Taux de change de récompense](reward-exchange-rates.md) est requise pour l’échange de points de récompense par les clients et les utilisateurs administrateurs lors du passage en caisse.

Les points peuvent être échangés par les utilisateurs administrateurs et les clients (si activé) lors du passage en caisse. Dans la section Mode de paiement, une case à cocher Utiliser mes points de récompense apparaît au-dessus des modes de paiement activés. Les points disponibles et le taux de change monétaire sont inclus. Si le solde disponible est supérieur au total général de la commande, aucun mode de paiement supplémentaire n&#39;est nécessaire. Le nombre de points de récompense appliqués à la commande s’affiche avec les totaux des commandes, soustraits du total général, comme pour les cartes de crédit ou les cartes-cadeaux du magasin. Si des points de récompense sont utilisés avec un crédit de magasin ou une carte cadeau, les points de récompense sont déduits en premier. La carte de crédit ou cadeau de la boutique est ensuite déduite si le total de la commande est supérieur au nombre de points de récompense échangeables.

>[!NOTE]
>
>Les points de récompense et le crédit de magasin ne réduisent pas la base imposable de la commande. La taxe est calculée sur le sous-total avant l&#39;application de ces remises. Les points ou le crédit ne réduisent que le montant final que le client paie.

>[!NOTE]
>
>Les points de récompense ne sont pas recommandés pour les achats contre remboursement, car la réception du paiement ne peut être confirmée qu&#39;après la facturation de la commande.

## Rembourser aux points de récompense

Les commandes passées avec des points de récompense peuvent être remboursées sur le solde des points de récompense jusqu’à concurrence du montant remboursé dans la commande. Dans la page [_Nouvel avoir_](../stores-purchase/credit-memo-create.md), vous pouvez saisir le nombre de points à appliquer au solde du client. Par défaut, le champ contient le nombre complet de points utilisés dans l’ordre.

## Activer les opérations de point de récompense pour votre boutique

La configuration des Points de récompense détermine la manière dont les points de récompense sont présentés dans le magasin et définit les paramètres de fonctionnement de base.

![Configuration des clients - Points de récompense](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Étape 1. Configurer les points de récompense

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Reward Points]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Reward Points]** et procédez comme suit :

   - Pour activer les points de récompense, définissez **[!UICONTROL Enable Reward Points Functionality]** sur `Yes`.

   - Pour permettre aux clients de gagner leurs propres points de récompense, définissez **[!UICONTROL Enable Reward Points Functionality on Storefront]** sur `Yes`.

   - Pour permettre aux clients de voir un historique détaillé de leurs récompenses, définissez **[!UICONTROL Customers May See Reward Point History]** sur `Yes`.

1. Par **[!UICONTROL Reward Points Balance Redemption Threshold]**, saisissez le nombre de points qui doivent être cumulés avant de pouvoir être échangés (vide pour aucun minimum).

1. Par **[!UICONTROL Cap Reward Points Balance At]**, saisissez le nombre maximal de points qu&#39;un client peut acquérir (vide pour aucune limite).

1. Par **[!UICONTROL Reward Points Expire in (days)]**, saisissez le nombre de jours avant l’expiration des points de récompense (vide pour aucune expiration).

1. Définissez **[!UICONTROL Reward Points Expiry Calculation]** sur l’une des options suivantes :

   - `Static` - Détermine la durée de vie restante des points de récompense en fonction du nombre de jours définis dans la configuration. Si la limite d’expiration dans la configuration change, la date d’expiration des points existants ne change pas.

   - `Dynamic` - Calcule le nombre de jours restant à chaque fois que le solde du point de récompense augmente. Si la limite d’expiration dans la configuration change, l’expiration de tous les points existants est mise à jour en conséquence.

1. Si vous souhaitez rembourser automatiquement les points de récompense disponibles, définissez **[!UICONTROL Refund Reward Points Automatically]** sur `Yes`.

1. Pour annuler les points de récompense gagnés lors d’achats lorsque la commande qui a gagné les points est entièrement ou partiellement remboursée, définissez **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** sur `Yes`.

   >[!NOTE]
   >
   >Seuls les points gagnés avec la commande remboursée sont affectés.

1. Définissez **[!UICONTROL Landing Page]** sur la page de contenu qui explique votre programme de points de récompense.

   Veillez à mettre à jour la page par défaut Points de récompense avec vos propres informations.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Étape 2. Configurer les points gagnés pour les activités du client

Au cours de cette étape, le nombre de points de récompense pouvant être gagnés pour diverses activités du client est spécifié. Lorsque les clients effectuent une action à laquelle des points sont attribués, un message leur indiquant le nombre de points qu’ils ont gagnés s’affiche.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Actions for Acquiring Reward Points by Customer]** .

   ![Configuration des clients - actions d’acquisition de points de récompense par client](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Pour permettre l’acquisition de points de récompense pour les achats en fonction du [Taux de change de récompense](reward-exchange-rates.md) configuré, définissez **[!UICONTROL Purchase]** sur `Yes`.

   >[!NOTE]
   >
   >Pour gagner des points de récompense pour leur _première_ commande, le client doit être enregistré _avant_ que la transaction ne soit capturée par le mode de paiement. La plupart des modes de paiement peuvent être configurés pour capturer les transactions _automatiquement_ lorsque la commande est passée, mais _avant_ que l’enregistrement du compte client soit terminé.

1. Par **[!UICONTROL Registration]**, saisissez le nombre de points gagnés pour l’ouverture d’un compte client.

1. Par **[!UICONTROL Newsletter Signup]**, saisissez le nombre de points gagnés par les clients enregistrés qui s’abonnent à une newsletter.

1. Par **[!UICONTROL Converting Invitation to Customer]**, saisissez le nombre de points gagnés par un client qui envoie une invitation, puis le destinataire ouvre un compte client.

   Vous pouvez limiter le nombre de conversions d’invitations pouvant être utilisées pour gagner des points pour le client qui envoie l’invitation (vide pour aucune limite). Pour ce faire, saisissez un nombre dans le champ **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** .

1. Par **[!UICONTROL Converting Invitation to Order]**, saisissez le nombre de points gagnés par un client qui envoie une invitation au destinataire qui passe ensuite une commande et effectue les opérations suivantes :

   - Pour **Limite de quantité des conversions d&#39;invitation à la commande**, saisissez le nombre de points gagnés par le client qui envoie l&#39;invitation lorsque le destinataire passe une commande initiale (vide pour aucune limite).

   - Par **[!UICONTROL Invitation Conversion to Order Reward]**, sélectionnez l’option `Each` pour gagner des points pour chaque commande passée par le destinataire, ou sélectionnez l’option `First` pour gagner des points uniquement pour la première commande passée par le destinataire.

1. Par **[!UICONTROL Review Submission]**, saisissez le nombre de points gagnés par un client qui soumet une révision dont la publication est approuvée.

1. Ensuite, pour limiter le nombre de commentaires qui peuvent être utilisés pour gagner des points par client, saisissez le nombre dans le champ **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** (vide pour aucune limite).

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Étape 3. Compléter les paramètres de notification par e-mail

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Email Notification Settings]** .

   ![Configuration des clients - Notifications par e-mail des points de récompense](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur des mises à jour de solde et des notifications d’expiration.

1. Si vous souhaitez abonner les clients par défaut pour être avertis des mises à jour de solde et des dates d’expiration à venir, définissez **[!UICONTROL Subscribe Customers by Default]** sur `Yes`.

1. Définissez **[!UICONTROL Balance Update Email]** sur le modèle utilisé pour la notification envoyée aux clients chaque fois que leur solde de points est mis à jour.

1. Définissez **[!UICONTROL Reward Points Expiry Warning Email]** sur le modèle utilisé pour la notification envoyée aux clients lorsque la limite d’expiration d’un lot de points est atteinte.

1. Par **[!UICONTROL Expiry Warning Before (days)]**, saisissez le nombre de jours avant l’expiration des points pendant lesquels la notification est envoyée.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Mettre à jour le solde des points de récompense

Le solde des points de récompense peut être mis à jour à partir de l’administrateur.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sous _Informations sur le client_, choisissez la section **[!UICONTROL Reward Points]**.

1. Saisir le nombre de **[!UICONTROL Update Points]** :

   - Pour mettre à jour le montant des points de récompense, saisissez le nombre nécessaire pour augmenter le solde total de points.
   - Pour soustraire le montant des points de récompense, saisissez le nombre négatif que vous souhaitez réduire le solde total de points.

1. Saisissez les **[!UICONTROL Comments]** liées à l’ajustement des points de récompense, si nécessaire.

   ![Solde des points de récompense](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Vous pouvez éventuellement abonner le client aux _notifications de points de récompense_ :

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Cliquez sur **[!UICONTROL Save Customer]**.

Toutes les actions liées aux points de récompense sont affichées dans le bloc de _[!UICONTROL Reward Points History]_du client dans son compte sur le storefront.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Balance] | Solde actuel des points de récompense pour le client |
| [!UICONTROL Amount Balance] | Montant du solde de trésorerie actuel |
| [!UICONTROL Points] | Nombre de points ajoutés ou soustraits |
| [!UICONTROL Amount] | Montant d&#39;argent ajouté ou soustrait |
| [!UICONTROL Rate] | Le [taux de change de récompense](reward-exchange-rates.md) |
| [!UICONTROL Website] | Site web auquel l’historique des points de récompense est attribué |
| [!UICONTROL Reason] | Motifs d’attribution de points :<br>**[!UICONTROL Making purchases]**— Chaque fois que le client effectue un achat, il peut gagner des points.<br>**[!UICONTROL Registering on the site]** - Accumulé à l&#39;enregistrement (une fois).<br>**[!UICONTROL Subscribing to a newsletter]**- Accumulé pour le premier abonnement (une fois).<br>**[!UICONTROL Sending Invitations]** — Gagnez des points en invitant leurs amis à rejoindre le site.<br>**[!UICONTROL Converting Invitations to Customer]**— Gagnez des points pour chaque invitation qu&#39;ils envoient, menant des amis à s&#39;inscrire sur le site.<br>**[!UICONTROL Converting Invitations to Order]** — Gagnez des points pour chaque vente résultant d&#39;une invitation envoyée.<br>**[!UICONTROL Review Submission]**— Gagnez des points en soumettant des avis sur des produits. |
| [!UICONTROL Created] | Date et heure de mise à jour des points de récompense |
| [!UICONTROL Expired] | Nombre de points de récompense expirés |
| [!UICONTROL Comment] | Commentaires lors de l’ajout ou de la soustraction de points |

{style="table-layout:auto"}

