---
title: Envoi d’une note de crédit
description: Découvrez comment générer et imprimer un avoir pour une commande facturée.
exl-id: 84ec72ba-7f72-4fa1-a9bf-91c17f43a3a7
feature: Orders, Invoices
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2132'
ht-degree: 0%

---

# Envoi d’une note de crédit

Avant de pouvoir imprimer une note de crédit, elle doit d’abord être générée pour une [commande facturée](invoices.md#create-an-invoice). Vous pouvez émettre des remboursements en ligne et hors ligne (partiels ou complets) à partir d’un avoir ouvert, selon le mode de paiement.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les remboursements peuvent être appliqués au crédit de magasin.
- ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Les remboursements peuvent être appliqués au crédit de la société.
- Les achats effectués par carte de crédit peuvent être remboursés en ligne ou hors ligne.
- Les achats effectués par chèque ou par mandat doivent être remboursés hors ligne.

Toute note de crédit avec un [état d&#39;ouverture](order-status.md) a un remboursement dû en suspens.

Avec les notes de crédit, vous pouvez :

- Remboursez le montant complet d&#39;une facture.
- Rembourser une partie d&#39;une facture.
- Rembourser plusieurs montants partiels d&#39;une facture.
- Rembourser plusieurs factures par commande, sans dépasser le montant total de la commande.
- Remboursez une partie de la quantité pour un article, par exemple trois des cinq chemises dans une commande.

Voir [Créer une facture](invoices.md#create-an-invoice) pour plus d’informations.

## Paramètre d’action de paiement

Le processus de remboursement des commandes payées par carte de crédit est déterminé par le [paramètre d’action de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) dans la configuration de chaque mode de paiement disponible. Les remboursements ne peuvent pas être émis tant que la transaction n&#39;a pas été réglée.

![ Paramètre d’action de paiement ](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- Si l’action de paiement de votre mode de paiement configuré est définie sur `Authorize`, vous devez d’abord générer la facture auprès de l’administrateur avant de pouvoir créer un avoir de crédit.
- Si l’action de paiement pour le mode de paiement que vous avez configuré est définie sur `Authorize and Capture`, la facture a déjà été générée par l’entité de traitement des paiements, mais les fonds ne sont pas disponibles tant que la transaction n’a pas été réglée. Cette courte période d’attente est recommandée par de nombreux responsables de paiement comme mesure de sécurité et peut généralement être gérée automatiquement. Les transactions peuvent également être réglées manuellement à partir de votre compte marchand auprès du responsable du traitement des paiements.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Si vous créez un avoir pour une commande qui comprend des options de cadeau, le remboursement de l’emballage cadeau et/ou de la carte imprimée s’affiche dans la section Totaux des remboursements de la note de crédit. Pour exclure ces coûts du montant à rembourser, indiquez le montant en tant que frais d’ajustement. Si plusieurs notes de crédit sont émises pour la même commande, le remboursement des options de cadeau n’apparaît que dans la première note de crédit.

## Création d’une note de crédit

Déterminez le type de remboursement que vous souhaitez émettre (pour un [achat de crédit](#issue-a-refund-for-a-credit-purchase) ou pour un [chèque ou mandat financier](#issue-an-offline-refund-for-check-or-money-order)), générez l’avoir de crédit et effectuez un remboursement.

### Émettre un remboursement pour un achat de crédit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![Grille de commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

1. Recherchez l’ordre dans la grille, puis cliquez sur **[!UICONTROL View]**.

1. Si le bouton _[!UICONTROL Credit Memo]_est visible dans la barre de boutons, effectuez l’une des opérations suivantes :

   - Pour effectuer un remboursement `offline`, suivez l&#39;étape #6.
   - Pour effectuer un remboursement `online`, passez à l&#39;étape #4.

   Pour plus d’informations sur les remboursements en ligne et hors ligne, voir [Mémos de crédit](credit-memos.md) .

1. Cliquez sur **[!UICONTROL Invoices]** dans le panneau de gauche.

1. Recherchez la facture dans la grille et cliquez sur **[!UICONTROL View]**.

   ![Grille de factures](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. Faites défiler l’écran jusqu’à la section **[!UICONTROL Invoice Totals]** de la facture, vérifiez que la facture est définie sur `Capture Online`, puis cliquez sur **[!UICONTROL Submit Invoice]**.

   ![Capture en ligne](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   Si cette option n&#39;est pas disponible, la facture est déjà créée. Passez à l’étape suivante.

1. Dans la barre de boutons située en haut de la facture, cliquez sur **[!UICONTROL Credit Memo]**.

1. Vérifiez les informations de la section **[!UICONTROL Items to Refund]** et procédez comme suit, le cas échéant :

   - Pour renvoyer le produit à l’inventaire, cochez la case **[!UICONTROL Return to Stock]** .

     Le produit revient automatiquement en stock si _Product Stock Options_ est défini sur `Automatically Return Credit Memo Item to Stock`. Avec [Inventory management activé](../inventory-management/enable.md), l’élément revient à la source qui a envoyé l’envoi.

   - Mettez à jour **[!UICONTROL Qty to Refund]**, puis cliquez sur **[!UICONTROL Update Qty's]**.

     ![Éléments à rembourser](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. Mettez à jour la section **[!UICONTROL Refunds Totals]** comme suit :

   - Pour **[!UICONTROL Refund Shipping]**, saisissez le montant qui doit être remboursé à partir des frais de livraison.

     Ce champ indique initialement le montant total des frais de livraison de la commande qui peut être remboursée. Il est égal au montant total de livraison de la commande, moins le montant de livraison qui a déjà été remboursé. Comme la quantité, le montant peut être réduit, mais pas augmenté.

   - Pour **[!UICONTROL Adjustment Refund]**, saisissez une valeur à ajouter au montant total remboursé en tant que remboursement supplémentaire qui ne s’applique à aucune partie particulière de la commande (expédition, articles ou taxe). Il peut également être utilisé pour un remboursement partiel avec de l’argent virtuel, par exemple une carte-cadeau, lorsqu’un administrateur souhaite d’abord rembourser un mode de paiement non virtuel.

     Le montant saisi ne peut pas augmenter le montant total du remboursement au-delà du montant payé.

   - Pour **[!UICONTROL Adjustment Fee]**, saisissez une valeur à soustraire du montant total remboursé.

     Ce montant n’est pas soustrait d’une section spécifique de la commande, telle que les frais d’expédition, les articles ou la taxe.

1. Pour ajouter un commentaire, saisissez le texte dans la zone **[!UICONTROL Credit Memo Comments]**.

   - Pour envoyer une notification électronique au client, cochez la case **[!UICONTROL Email Copy of Credit Memo]** .

1. Cliquez sur **[!UICONTROL Update Totals]**.

1. Effectuez les opérations suivantes, le cas échéant :

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour rembourser le montant au crédit de la boutique du client, cochez la case **[!UICONTROL Refund to Store Credit]** .

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Pour rembourser le montant au crédit de la société du client, cochez la case **[!UICONTROL Refund to Company Credit]** .

   - Pour émettre un remboursement hors ligne, cliquez sur **[!UICONTROL Refund Offline]**.

   - Pour effectuer un remboursement en ligne, cliquez sur **[!UICONTROL Refund]**.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Si l’achat a été payé avec le crédit de la société, cliquez sur **[!UICONTROL Refund to Company Credit]**.

   Pour plus d’informations sur les remboursements en ligne et hors ligne, voir [Mémos de crédit](credit-memos.md) .

   ![}Remboursement total de la commande](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### Émettre un remboursement hors ligne pour un chèque ou un mandat

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre terminé dans la grille et ouvrez-le en cliquant sur le lien **[!UICONTROL View]** .

1. Dans la barre de boutons en haut de la page, cliquez sur **[!UICONTROL Invoice]**.

1. Faites défiler la page vers le bas et cliquez sur **[!UICONTROL Submit Invoice]**.

1. Dans la barre de boutons située en haut de la facture, cliquez sur **[!UICONTROL Credit Memo]**.

   ![Créer un avoir](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. Vérifiez les informations de la section **[!UICONTROL Items to Refund]** et procédez comme suit, le cas échéant :

   ![Éléments à rembourser](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - Cochez la case **[!UICONTROL Return to Stock]** si vous souhaitez renvoyer le produit renvoyé à l’inventaire.

     Lorsque Inventory management est activé, la quantité de stock revient à la source qui a envoyé l’envoi. Le produit revient automatiquement en stock si [Product Stock Options](../inventory-management/enable.md) est défini sur `Automatically Return Credit Memo Item to Stock`.

   - Mettez à jour **[!UICONTROL Qty to Refund]** et cliquez sur **[!UICONTROL Update Qty's]**.

     Le montant à créditer ne peut excéder le montant maximum disponible pour le remboursement.

1. Mettez à jour la section **[!UICONTROL Refunds Totals]** selon le cas :

   - Pour **[!UICONTROL Refund Shipping]**, saisissez le montant qui doit être remboursé à partir des frais de livraison.

     Ce champ affiche initialement le montant total des frais d’expédition de la commande disponible pour le remboursement. Il est égal au montant total de livraison de la commande, moins le montant de livraison qui a déjà été remboursé. Comme la quantité, le montant peut être réduit, mais pas augmenté.

   - Pour **[!UICONTROL Adjustment Refund]**, saisissez une valeur à ajouter au montant total remboursé en tant que remboursement supplémentaire qui ne s’applique à aucune partie particulière de la commande (expédition, articles ou taxe). Il peut également être utilisé pour un remboursement partiel avec de l’argent virtuel, par exemple une carte-cadeau, lorsqu’un administrateur souhaite d’abord rembourser un mode de paiement non virtuel.

     Le montant saisi ne peut pas augmenter le montant total du remboursement au-delà du montant payé.

   - Pour **[!UICONTROL Adjustment Fee]**, saisissez une valeur à soustraire du montant total remboursé.

     Ce montant n’est pas soustrait d’une section spécifique de la commande, telle que les frais d’expédition, les articles ou la taxe.

   - Si l’achat a été payé avec un crédit de magasin, cochez la case **[!UICONTROL Refund to Store Credit]** pour créditer le montant au solde du compte client.

1. Pour ajouter un commentaire, saisissez le texte dans la zone **[!UICONTROL Credit Memo Comments]** et procédez comme suit :

   - Pour envoyer une notification électronique au client, cochez la case **[!UICONTROL Email Copy of Credit Memo]** .

   - Pour inclure les commentaires que vous avez saisis dans l&#39;email, cochez la case **[!UICONTROL Append Comments]** .

     L’état d’une notification de note de crédit s’affiche dans la note de crédit terminée en regard du numéro de la note de crédit.

     ![Totaux de remboursement](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. Pour terminer le processus et émettre le remboursement, cliquez sur **[!UICONTROL Refund Offline]**.

## Descriptions des champs

### [!UICONTROL Order & Account Information]

| Champ | Description |
|--- |--- |
| [!UICONTROL Order Number] | Le numéro de commande apparaît dans les _Informations sur la commande et le compte_, suivies d’une note indiquant si l’e-mail de confirmation a été envoyé. |
| [!UICONTROL Order Date] | Date et heure auxquelles la commande a été passée. |
| [!UICONTROL Order Status] | Indique l’état de la commande comme `Complete`. |
| [!UICONTROL Purchased From] | Indique la vue du site web, du magasin et du magasin où la commande a été passée. |
| [!UICONTROL Placed from IP] | Indique l’adresse IP de l’ordinateur sur lequel la commande a été passée. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Champ | Description |
|--- |--- |
| [!UICONTROL Customer Name] | Nom du client ou de l’acheteur qui a passé la commande. Le nom du client est lié au profil du client. |
| [!UICONTROL Email] | Adresse électronique du client ou de l’acheteur. L’adresse électronique est liée pour ouvrir un nouveau message électronique. |
| [!UICONTROL Customer Group] | Nom du groupe de clients ou du catalogue partagé auquel le client est affecté. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Nom de la société associée à l’acheteur et pour le compte de laquelle la commande est passée. Le nom de la société est lié au profil de la société. |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| Champ | Description |
|--- |--- |
| [!UICONTROL Billing Address] | Nom du client ou de l’acheteur qui a passé la commande, suivi de l’adresse de facturation, du numéro de téléphone et de la [TVA](vat.md), le cas échéant. Le numéro de téléphone est associé à une numérotation automatique sur un appareil mobile. |
| [!UICONTROL Shipping Address] | Nom de la personne à l’attention de laquelle la commande doit être expédiée, suivi de l’adresse de livraison et du numéro de téléphone. Le numéro de téléphone est associé à une numérotation automatique sur un appareil mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| Champ | Description |
|--- |--- |
| [!UICONTROL Payment Information] | Mode de paiement à utiliser pour la commande et numéro de la commande, le cas échéant, suivi de la devise utilisée pour la commande. Si la commande est imputée au crédit de l’entreprise par l’intermédiaire de l’option [ Paiement sur le compte ](../b2b/enable-basic-features.md#configure-payment-on-account), le montant imputé au compte est indiqué. |
| [!UICONTROL Shipping & Handling Information] | Le mode d’expédition à utiliser et les frais de gestion applicables. |

{style="table-layout:auto"}

### [!UICONTROL Items to Refund]

| Champ | Description |
|--- |--- |
| [!UICONTROL Product] | Nom du produit, SKU et options (le cas échéant). |
| [!UICONTROL Price] | Prix d’achat de l’article. Pour Adobe Commerce B2B, cette valeur reflète toute remise appliquée à l’article à partir du catalogue partagé, le cas échéant. |
| [!UICONTROL Qty] | La quantité commandée. |
| [!UICONTROL Return to Stock] | Case à cocher qui indique si l’élément renvoyé doit être retourné en stock. |
| [!UICONTROL Qty to Refund] | Indique le nombre d’unités renvoyé par le produit. |
| [!UICONTROL Subtotal] | Le sous-total est le prix d’achat multiplié par la quantité d’unités de produit renvoyées. |
| [!UICONTROL Tax Amount] | Montant de la taxe qui s’applique à l’élément renvoyé sous forme de valeur décimale. |
| [!UICONTROL Tax Percent] | Pourcentage de la taxe appliquée à l’article renvoyé en pourcentage. |
| [!UICONTROL Discount Amount] | Toute remise s’appliquant à l’article renvoyé. |
| [!UICONTROL Row Total] | Total de l’article, y compris les taxes applicables qui sont dues pour le niveau de produit renvoyé, moins les remises. |
| _total de commande_ |  |

{style="table-layout:auto"}

### [!UICONTROL Credit Memo Comments]

| Champ | Description |
|--- |--- |
| [!UICONTROL Comment Text] | Zone de texte utilisée pour saisir un commentaire au client au sujet de la note de crédit. |

{style="table-layout:auto"}

### [!UICONTROL Refund Totals]

| Champ | Description |
|--- |--- |
| [!UICONTROL Refund Shipping] | Le montant des frais d&#39;expédition à rembourser. |
| [!UICONTROL Adjustment Refund] | Montant ajouté au montant total remboursé sous la forme d’un remboursement supplémentaire qui ne s’applique à aucune partie particulière de la commande, comme les frais d’expédition, les articles ou la taxe. Le montant saisi ne peut pas augmenter le montant total du remboursement au-delà du montant payé. |
| [!UICONTROL Adjustment Fee] | Montant soustrait du montant total remboursé, tel qu’un frais de redémarrage, ou un montant lié à l’emballage cadeau ou aux options de cadeau. |
| [!UICONTROL Grand Total] | Montant total à rembourser |
| [!UICONTROL Append Comments] | Case à cocher qui détermine si les commentaires sont inclus dans l’avoir. |
| [!UICONTROL Email Copy of Credit Memo] | Case à cocher qui détermine si une copie de la note de crédit est envoyée par courrier électronique. |
| [!UICONTROL Refund to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Case à cocher qui détermine si le total doit être remboursé à [crédit de magasin](../customers/store-credit-using.md). |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Le total de tous les éléments de ligne à rembourser. |

{style="table-layout:auto"}

### Boutons Remboursement

Le mode de paiement utilisé pour la commande détermine les boutons de remboursement disponibles pour un avoir.

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Refund]** | Si l&#39;achat initial a été payé par carte de crédit via une passerelle de paiement, le montant du remboursement est géré par le responsable du traitement des paiements. Pour gérer les remboursements, consultez la documentation fournie par votre fournisseur de paiement. |
| **[!UICONTROL Refund Offline]** | Si l&#39;achat d&#39;origine a été payé par chèque ou par mandat, le remboursement est versé directement au client, par l&#39;émission d&#39;un chèque, d&#39;une carte-cadeau ou d&#39;un liquide si vous avez une vitrine en brique et mortier. L’avoir sert d’enregistrement de la transaction hors ligne. |
| **[!UICONTROL Refund to Company Credit]** | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) Si l’achat a été imputé au crédit de la société, le remboursement est renvoyé au [compte de la société](../b2b/credit-company.md). |

{style="table-layout:auto"}

## Imprimer une note de crédit

Pour imprimer ou afficher l’avoir terminé, un lecteur de PDF doit être installé. Vous pouvez télécharger [Adobe Reader][1] gratuitement.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. Utilisez l’une des méthodes suivantes pour imprimer la note de crédit :

### Méthode 1 : Imprimer l’avoir actuel

1. Dans la grille, ouvrez la note de crédit.

1. Cliquez sur **[!UICONTROL Print]**.

   ![Imprimer la note de crédit](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### Méthode 2 : impression de plusieurs avoir

1. Dans la liste, cochez la case de chaque note de crédit à imprimer.

1. Définissez la commande **[!UICONTROL Actions]** sur `PDF Credit Memos` et cliquez sur **[!UICONTROL Submit]**.

   ![Imprimer les avoirs sélectionnés](./assets/credit-memos-print.png){width="600" zoomable="yes"}

1. Lorsque vous y êtes invité, effectuez l’une des opérations suivantes :

   - Pour enregistrer le document, cliquez sur **[!UICONTROL Save]** et suivez les invites pour enregistrer le fichier sur votre ordinateur. Une fois le téléchargement terminé, ouvrez le PDF dans Adobe Reader et imprimez le document.

   - Pour afficher le document, cliquez sur **[!UICONTROL Open]**. L’avis de crédit de PDF prêt à l’impression s’ouvre dans Adobe Reader. À partir de là, vous pouvez imprimer la note de crédit ou l’enregistrer sur votre ordinateur.


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Obtenir Adobe Reader"
