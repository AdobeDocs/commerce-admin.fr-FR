---
title: État de la commande
description: Découvrez les états de commande prédéfinis et comment définir des états de commande personnalisés pour vous aligner sur vos besoins opérationnels.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# État de la commande

Toutes les commandes ont un état de commande associé à une étape dans le traitement des commandes. [workflow](order-processing.md). L’état de chaque commande est indiqué dans la variable _État_ de la colonne _Commandes_ grid. Votre magasin dispose d’un ensemble de paramètres prédéfinis d’état de commande et d’état de commande. L’état de la commande décrit la position d’une commande dans le workflow.

![État de la commande](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Une commande partiellement remboursée reste en cours `Processing` status jusqu’à **_all_** les articles commandés (y compris les articles remboursés) sont expédiés. L’état de la commande ne passe pas à `Complete` lorsqu’un même article de commande n’est pas encore expédié.

## Workflow d’état des commandes

![Workflow d’état des commandes](./assets/order-workflow.png)

## État prédéfini

| État de la commande | Code d’état |  |
|--- |--- |--- |
| En cours de traitement | `processing` | Lorsque l’état des nouvelles commandes est défini sur &quot;Traitement&quot;, la variable _Facturer automatiquement tous les éléments_ devient disponible dans la configuration. Les factures ne sont pas créées automatiquement pour les commandes passées à l’aide de la carte cadeau, du crédit de magasin, des points de récompense ou d’autres modes de paiement hors ligne. |
| Fraude présumée | `fraud` | Parfois, les commandes payées par PayPal ou une autre passerelle de paiement sont marquées comme _Fraude présumée_. Ce statut signifie que la commande n&#39;a pas de facture émise et que l&#39;email de confirmation n&#39;est pas non plus envoyé. |
| En attente de paiement | `pending_payment` | Cet état est utilisé si la commande est créée et que PayPal ou un mode de paiement similaire est utilisé. Cela signifie que le client a été dirigé vers le site web de la passerelle de paiement, mais qu’aucune information de retour n’a encore été reçue. Ce statut change lorsque le client paie. |
| Révision des paiements | `payment_review` | Cet état s’affiche lorsque la révision des paiements PayPal est activée. |
| En attente | `pending` | Ce statut indique qu&#39;aucune facture et aucun envoi n&#39;ont été soumis. |
| En attente | `holded` | Cet état ne peut être attribué que manuellement. Vous pouvez suspendre n&#39;importe quel ordre. |
| Ouvrir | `STATE_OPEN` | Ce statut signifie qu’une commande ou un avis de crédit est toujours ouvert et peut nécessiter une action supplémentaire. |
| Terminer | `complete` | Ce statut signifie que la commande est créée, payante et expédiée au client. |
| Fermé | `closed` | Ce statut indique qu’une note de crédit a été attribuée à une commande et que le client a reçu un remboursement. |
| Annulé | `canceled` | Ce statut est attribué manuellement dans l’administrateur ou, pour certaines passerelles de paiement, lorsque le client ne paie pas dans le délai spécifié. |
| Revirement annulé de PayPal | `paypay_canceled_reversal` | Ce statut signifie que PayPal a annulé l&#39;annulation. |
| En attente de PayPal | `pending_paypal` | Ce statut signifie que la commande a été reçue par PayPal, mais que le paiement n&#39;a pas encore été traité. |
| PayPal inversé | `paypal_reversed` | Ce statut signifie que PayPal a annulé la transaction. |

{style="table-layout:auto"}

## Statut de la commande personnalisée

Outre les paramètres prédéfinis d’état de commande, vous pouvez créer vos propres paramètres personnalisés d’état de commande, les affecter à l’état de la commande et définir un état de commande par défaut pour les états de commande. L’état de la commande indique la position de la commande dans le workflow de traitement des commandes et l’état de la commande définit l’état de la commande. Par exemple, vous pouvez avoir besoin d’un état de commande personnalisé, tel que `packaging"`, `backordered`ou un état spécifique à vos besoins. Vous pouvez créer un nom explicite pour le statut personnalisé et l’affecter à l’état de commande associé dans le workflow.

>[!NOTE]
>
>Seules les valeurs d’état de commande personnalisée par défaut sont utilisées dans le workflow de commande. Les valeurs d’état personnalisées qui ne sont pas définies par défaut ne peuvent être utilisées que dans la section des commentaires de la commande.

![Paramètres d’état de la commande](./assets/order-status.png){width="700" zoomable="yes"}

### Création d’un état de commande personnalisé

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create New Status]**.

   ![Créer un état de commande](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Mettez à jour le _[!UICONTROL Order Status Information]_section :

   - Saisissez un **[!UICONTROL Status Code]** pour référence interne. Le premier caractère doit être une lettre (a-z) et le reste peut être n’importe quelle combinaison de lettres et de nombres (0-9). Utilisez le caractère de soulignement au lieu d’un espace.

   - Pour **[!UICONTROL Status Label]**, saisissez un libellé qui identifie le paramètre d’état dans Admin et storefront.

1. Dans le _[!UICONTROL Store View Specific Labels]_, saisissez les étiquettes nécessaires pour différentes vues de magasin.

1. Cliquez sur **[!UICONTROL Save Status]**.

### Attribuer un état de commande à un état

1. Sur le _État de la commande_ page, cliquez sur **[!UICONTROL Assign Status to State]**.

   ![Attribuer l’état](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Mettez à jour le **[!UICONTROL Assignment Information]** , procédez comme suit :

   - Choisissez la **[!UICONTROL Order Status]** que vous souhaitez affecter. Elles sont répertoriées par libellé d’état.

   - Définir **[!UICONTROL Order State]** à l’emplacement dans le workflow où se trouve l’état de la commande.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** list inclut les états de commande attribués par défaut. Par exemple, la variable `Pending` l’état de la commande par défaut s’affiche au lieu de `New` valeur de l’état de la commande.

   - Pour que ce statut soit défini par défaut pour l’état de la commande, sélectionnez l’option **[!UICONTROL Use Order Status as Default]** .

     >[!NOTE]
     >
     >Seuls les états de commande par défaut sont utilisés dans le workflow de commande. Les états autres que par défaut ne peuvent être définis que dans la variable **[!UICONTROL Order Comments]** dans la section Admin.

   - Pour rendre cet état visible à partir du storefront, sélectionnez la variable **[!UICONTROL Visible On Storefront]** .

   ![Attribuer l’état à l’état](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Status Assignment]**.

### Modifier un état de commande existant

1. Dans le _[!UICONTROL Order Status]_grille, ouvrez l’enregistrement d’état en mode d’édition.

1. Mettez à jour les paramètres d’état si nécessaire.

1. Cliquez sur **[!UICONTROL Save Status]**.

### Supprimer un état de commande d’un état affecté

>[!NOTE]
>
>Un paramètre d’état ne peut pas être annulé si l’état est en cours d’utilisation.

1. Dans le _[!UICONTROL Order Status]_, recherchez l’enregistrement d’état de commande à ne pas attribuer.

1. Dans le _[!UICONTROL Action]_à l’extrême droite de la ligne, cliquez sur le bouton **[!UICONTROL Unassign]**lien.

   Un message s’affiche en haut de l’espace de travail pour indiquer que l’état de la commande n’a pas été attribué. Bien que le libellé d’état de la commande apparaisse toujours dans la liste, il n’est plus affecté à un état. Les paramètres d’état de la commande ne peuvent pas être supprimés.

>[!NOTE]
>
>Si l’état de la commande par défaut n’est pas attribué à l’état de la commande, _**another**_ l’état de la commande _**définir automatiquement**_ comme valeur par défaut de cet état de commande.

## Notification

Les clients peuvent effectuer le suivi de l’état de leurs commandes en [flux RSS](../merchandising-promotions/social-rss.md) si le flux RSS Commande est activé dans la configuration. Lorsque cette option est activée, un lien vers le flux RSS s’affiche dans chaque commande.

### Activer la notification d’état de commande

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL RSS Feeds]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Order]** .

1. Définir **[!UICONTROL Customer Order Status Notification]** to `Enable`.

   ![Notification d’état de la commande client](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### Configuration des notifications par courrier électronique de nouvelle commande

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales Emails]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Order]** .

   ![Configuration - Options de commande](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL New Order Confirmation Email Sender]** à l’une des options suivantes :

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Choisissez les modèles à utiliser pour chaque type de client :

   - **[!UICONTROL New Order Confirmation Template]** - Choisissez un modèle à utiliser pour les clients disposant d’un compte de magasin enregistré.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - Choisissez un modèle à utiliser pour les clients invités sans compte de magasin enregistré.

1. Pour notifier une autre personne (un responsable de l’entreprise, par exemple) de la nouvelle commande, saisissez l’adresse électronique à **[!UICONTROL Send Order Email Copy To]**.

   Vous pouvez ajouter plusieurs adresses électroniques si plusieurs destinataires sont requis.

1. Définissez la variable **[!UICONTROL Send Order Email Copy Method]** à l’une des options suivantes :

   - `Bcc` - Un seul email concernant la nouvelle commande est envoyé au client et au destinataire supplémentaire, mais le client ne voit pas que l&#39;email qu&#39;il a reçu a également été envoyé au destinataire supplémentaire.
   - `Separate Email` - Deux emails distincts sont envoyés : un au destinataire et un au client.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
