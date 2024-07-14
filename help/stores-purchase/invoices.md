---
title: Facturations
description: Découvrez comment créer et imprimer des factures pour prendre en charge le traitement des commandes et les opérations de service client.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# Facturations

Une facture est un enregistrement de l’enregistrement du paiement pour une commande. Plusieurs factures peuvent être [créées](#create-an-invoice) pour une seule commande et chacune peut inclure autant ou autant de produits achetés que vous le spécifiez. Vous pouvez également créer des [factures de PDF prêtes à l’impression](#print-invoices) comme documents de vente pour vos clients.

Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _Opérations_ > **Factures** pour ouvrir la grille _Factures_ et accéder aux factures que vous avez créées.

![Grille de factures](./assets/invoices.png){width="700" zoomable="yes"}

## Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez les cases pour que les guillemets soient soumis à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | Identifiant numérique unique attribué lors de l’envoi d’une facture par l’administrateur. Lors de l’affichage des détails de la facture, ce numéro s’affiche en haut de la page, au lieu du nom du guillemet. |
| [!UICONTROL Invoice Date] | Date et heure auxquelles l’administrateur a soumis la facture pour la première fois. |
| [!UICONTROL Order#] | Identifiant numérique unique attribué lorsqu’une commande est passée par un acheteur. Lors de l’affichage des détails de la facture, ce numéro apparaît sous la forme d’un lien dans le bloc Informations sur la commande et le compte . |
| [!UICONTROL Order Date] | Date et heure auxquelles le client a passé une commande pour la première fois. |
| [!UICONTROL Bill-to Name] | Nom de la personne chargée de payer la commande. |
| [!UICONTROL Status] | Indique l’état actuel d’une facture. Le statut ne peut être modifié que par une action de la part de l&#39;acheteur ou du vendeur. |
| [!UICONTROL Grand Total (Base)] | Prix total des produits à acheter. Le montant total apparaît dans la devise de base du site web et dans la devise du storefront. |
| [!UICONTROL Grand Total (purchase)] | Total général des produits achetés dans la commande. Le montant total apparaît dans la devise de base du site web et dans la devise du storefront. |
| [!UICONTROL Purchased From] | La vue de site web/magasin/magasin à partir de laquelle la facture a été créée. |
| [!UICONTROL Billing Address] | Adresse de facturation du client qui a passé la commande. |
| [!UICONTROL Shipping Address] | Adresse à laquelle la commande doit être expédiée. |
| [!UICONTROL Customer Name] | Prénom et nom du client qui reçoit la facture. |
| [!UICONTROL Email] | Adresse électronique du client qui a reçu la facture. |
| [!UICONTROL Customer Group] | Groupe de clients affecté au client qui a reçu la facture. |
| [!UICONTROL Payment Method] | Mode de paiement à utiliser pour le paiement. |
| [!UICONTROL Shipping Information] | Méthode à utiliser pour envoyer la commande. |
| [!UICONTROL Subtotal] | Sous-total de la commande, sans frais d’expédition et de gestion, ni taxes. |
| [!UICONTROL Shipping and Handling] | Montant imputé à l’expédition et à la manipulation. |
| [!UICONTROL Action] | **[!UICONTROL View]** : ouvre la facture en mode d’édition. |

{style="table-layout:auto"}

## Créer une facture

La création d&#39;une facture pour une commande la déplace vers un état dans lequel elle ne peut pas être annulée ni modifiée. Une nouvelle page de facture ressemble à une commande finalisée, avec des champs supplémentaires. Chaque activité liée à une commande est indiquée dans la section Commentaires de la facture.

Normalement, les commandes sont facturées et capturées lorsque le processus d’expédition commence. Si le mode de paiement est un bon de commande, ou si l’[action de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) est défini sur `Authorize and Capture`, la commande est facturée et le paiement est capturé pendant le passage en caisse. Vous pouvez générer une facture avec un bon de livraison et imprimer les libellés d’expédition depuis votre compte d’opérateur. Une seule commande peut être divisée en envois partiels, qui sont facturés séparément, si nécessaire.

Lorsque l’état des nouvelles commandes est défini sur `Processing`, l’option _Facturer automatiquement tous les éléments_ devient disponible dans la configuration. Certains modes de paiement par carte de crédit effectuent l’étape de facturation dans le cadre du processus lorsque l’ [action de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) est définie sur `Authorize and Capture`. Dans ce cas, le bouton Facture n’apparaît pas et la commande est prête à être expédiée.

>[!NOTE]
>
>Les factures ne sont pas créées automatiquement pour les commandes passées à l’aide de `Gift Card`, `Store Credit`, `Reward Points` ou d’autres méthodes de paiement hors ligne.

Une facture pour la commande doit être générée avant d&#39;être imprimée. Pour afficher ou imprimer le PDF, téléchargez et installez d’abord un lecteur de PDF tel que [Adobe Acrobat Reader][1].

**_Pour facturer une commande :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Recherchez la commande client dont l’état est `Processing` dans la grille. Ensuite, procédez comme suit :

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL View]**.

1. Dans l’en-tête de la commande client, sélectionnez l’option **[!UICONTROL Invoice]** .

   >[!NOTE]
   >
   >L’option _[!UICONTROL Invoice]_n’apparaît pas lorsque l’ [ action de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) pour votre [ méthode de paiement ](../configuration-reference/sales/payment-methods.md) spécifique est définie sur `Authorize and Capture`, qui génère automatiquement une facture. C’est également le cas si la commande est passée et que l’action de paiement pour votre mode de paiement est définie sur `Authorize` et que la commande est facturée.

   ![Commande de ventes de factures](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   La nouvelle page de facture ressemble à une page de commande finalisée, avec des champs supplémentaires qui peuvent être modifiés.

1. Si les articles sont prêts à être livrés, générez un bon de livraison pour l&#39;envoi en même temps que vous créez la facture :

   - Dans la section _Informations d’expédition_, cochez la case **[!UICONTROL Create Shipment]** pour la sélectionner.

     L&#39;enregistrement de l&#39;expédition est créé au même moment que la facture est générée.

   - Inclure un numéro de suivi :

      - Cliquez sur **[!UICONTROL Add Tracking Number]**.
      - Saisissez les informations de suivi : _[!UICONTROL Carrier]_,_[!UICONTROL Title]_ et _[!UICONTROL Number]_

     ![Créer une expédition Fedex](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - Vous pouvez éventuellement générer une facture partielle :

      - Dans la section _Éléments à facturer_, mettez à jour la colonne **[!UICONTROL Qty to Invoice]** pour inclure uniquement des éléments spécifiques sur la facture.
      - Cliquez ensuite sur **[!UICONTROL Update Qty's]**.

        ![Éléments à facturer](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Si un mode de paiement en ligne a été utilisé pour la commande, définissez **[!UICONTROL Amount]** sur l’option appropriée.

1. Pour notifier les clients par email lors de la génération de la facture, procédez comme suit :

   - Cochez la case **[!UICONTROL Email Copy of Invoice]** .

   - Saisissez tout **[!UICONTROL Invoice Comments]**. Pour inclure les commentaires dans l&#39;email de notification, cochez la case **[!UICONTROL Append Comments]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Submit Invoice]** en bas de la page.

   **_Méthode de paiement en ligne :_**

   ![Submit Invoice - online payment method](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Méthode de paiement hors ligne :_**

   ![Submit Invoice - offline payment method)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   L’état de la commande passe de `Pending` à `Complete`.

   ![Résumé de facture terminé](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Imprimer les factures

Les factures peuvent être imprimées individuellement ou par lots. Toutefois, avant qu&#39;une facture puisse être imprimée, elle doit d&#39;abord être générée pour la commande. Vous pouvez télécharger un logo haute résolution pour une facture de PDF prête à être imprimée et inclure l’[ID de commande](../stores-purchase/sales-documents.md#add-reference-ids) dans l’en-tête . Pour personnaliser le modèle de facture avec votre logo et votre adresse, voir [Conditions requises du logo du PDF](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>Pour afficher ou imprimer le PDF, vous devez disposer d’un lecteur de PDF. Vous pouvez télécharger [Adobe Reader][1] gratuitement.

### Imprimer une seule facture

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Dans la grille _[!UICONTROL Invoices]_, recherchez la facture et cliquez sur **[!UICONTROL View]**dans la colonne_ Action _.

1. En haut de la facture, cliquez sur **[!UICONTROL Print]** pour générer un PDF de la facture.

1. Enregistrez le PDF généré dans un fichier ou imprimez-le.

### Imprimer plusieurs factures

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Dans la grille _[!UICONTROL Invoices]_, cochez la case pour chaque facture à imprimer.

1. Définissez le contrôle **[!UICONTROL Actions]** sur `PDF Invoices`.

   ![Imprimer plusieurs factures](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

Les factures sont enregistrées dans un seul fichier de PDF qui peut être envoyé vers une imprimante ou enregistré.

## Ressources de dépannage

Pour obtenir de l’aide sur la résolution des problèmes liés aux factures, reportez-vous aux articles suivants de la _base de connaissances de support Commerce_ :

- [Impossible de facturer des produits groupés, virtuels et simples](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html)
- [Facture sans informations de crédit de magasin](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [La taxe apparaît sur une facture avec une remise de 100 %](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [Les factures de commande ne sont pas envoyées automatiquement](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Obtenir Adobe Reader"
