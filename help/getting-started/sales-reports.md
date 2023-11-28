---
title: Rapports sur les ventes
description: La variable [!DNL Commerce] les rapports sur les ventes vous aident à effectuer le suivi des commandes, des taxes, des factures, des frais d’expédition, des remboursements, des bons de réduction et des soldes.
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# Rapports sur les ventes

La sélection des rapports de ventes inclut les commandes, les taxes, les factures, l’expédition, les remboursements, les bons et le règlement de paiement.

## Filtres de rapport

Vous pouvez générer un rapport de ventes pour un site web entier ou pour une boutique. Les rapports sur les ventes peuvent être filtrés par intervalle de temps, date et état.

![Filtres de rapports de ventes](./assets/tax-report.png){width="600"}

Pour filtrer un rapport de ventes, définissez les options suivantes :

| Option | Description |
|--- |--- |
| [!UICONTROL Date Used] | Définit les données à utiliser pour le rapport. |
| [!UICONTROL Period] | La période pour laquelle les données sont utilisées : Jour/Mois/Année. |
| [!UICONTROL From/To] | Utilisé pour définir les données de recherche par date de début et de fin. |
| [!UICONTROL Order Status] | Indique l’état de la commande. |
| [!UICONTROL Empty Rows] | Indique s’il faut ajouter des lignes vides au rapport. |

## [!UICONTROL Orders Report]

La variable [!UICONTROL Orders Report] inclut le nombre de commandes passées et annulées, avec les totaux pour les ventes, les montants facturés, remboursés, la taxe collectée, les frais d’expédition facturés et les remises.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.

1. Cliquez sur **[!UICONTROL Show Report]**.

![Enregistrements de rapport commandes](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

La variable [!UICONTROL Tax Report] inclut la règle fiscale appliquée, le taux de taxe, le nombre de commandes et le montant de la taxe perçue.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.


1. Cliquez sur **[!UICONTROL Show Report]**.

![Rapport Taxe](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

La variable [!UICONTROL Invoice Report] inclut le nombre de commandes et de factures effectuées au cours de la période, avec les montants facturés, payés et impayés.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.

1. Cliquez sur **[!UICONTROL Show Report]**.

![Rapport de facture](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

La variable [!UICONTROL Shipping Report] inclut le nombre de commandes de l’opérateur ou du mode de livraison utilisé, y compris les montants des ventes totales et de l’expédition totale.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.

1. Cliquez sur **[!UICONTROL Show Report]**.

![Rapport d’expédition](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

La variable [!UICONTROL Refunds Report] inclut le nombre de commandes remboursées et le montant total remboursé en ligne et hors ligne.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.

1. Cliquez sur **[!UICONTROL Show Report]**.

![Rapport Remboursements](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

La variable [!UICONTROL Coupons Report] inclut chaque code de coupon utilisé pendant l’intervalle de temps spécifié, la règle de prix associée et le nombre de fois utilisés, avec les totaux et les sous-totaux pour les ventes et les remises.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Dans le **[!UICONTROL Filter]** sélectionnez les options de période de rapport et l’état de la commande utilisés pour renseigner le rapport.

1. Cliquez sur **[!UICONTROL Show Report]**.

Pour plus d’informations sur l’utilisation de la variable [!UICONTROL Coupons Report] pour collecter des données pour vos campagnes de promotion, reportez-vous à la section [Rapports sur les coupons](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) dans le _Guide de marchandisage et de promotions_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

La variable [Rapports de règlement PayPal] page comprend le type d’événement, tel qu’une transaction par carte de débit, les dates de début et de fin, le montant brut et les frais connexes. Le rapport peut être automatiquement mis à jour avec les données les plus récentes de PayPal. Il existe des options de filtrage pour la période, le compte marchand, l’identifiant de transaction, l’identifiant de facture ou l’identifiant de référence PayPal.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![Rapport de règlement PayPal](./assets/reports-sales-paypal-settlement.png){width="600"}

Pour plus d’informations sur l’utilisation de la variable [!UICONTROL PayPal Settlement Reports] pour obtenir des informations sur chaque transaction PayPal qui affecte le règlement des fonds, voir [Rapports de règlement PayPal](../stores-purchase/paypal-settlement-reports.md) dans le _Guide d’expérience des magasins et des achats_.

## [!UICONTROL Braintree Settlement Report]

La variable [Braintree](../stores-purchase/braintree.md) Le rapport de règlement peut être filtré en fonction de la date de création, du montant, de l’état, du type de transaction, du type de paiement, de l’ID de transaction, de l’ID de commande, de l’ID de paiement PayPal, du type, de l’ID de compte marchand ou de l’ID de lot de règlement. Le rapport contient l’identifiant de transaction, l’identifiant de commande, l’identifiant de paiement PayPal, le type, la date de création, le montant, le code de règlement, l’état, le texte de réponse de la transaction, les identifiants de remboursement, l’identifiant de compte marchand, l’identifiant de lot de règlement et la devise.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Exporter des rapports

1. Pour exporter le rapport, sélectionnez le type de fichier : `Excel XML` ou `CSV`

1. Cliquez sur **[!UICONTROL Export]**.

## Actualiser les statistiques

Pour réduire l’impact sur les performances de la génération de rapports de vente, [!DNL Commerce] calcule et stocke les statistiques requises pour chaque rapport. Au lieu de recalculer les statistiques à chaque génération d&#39;un rapport, les statistiques stockées sont utilisées, sauf si vous actualisez les statistiques. Pour inclure les données les plus récentes, les statistiques du rapport doivent être actualisées avant la génération d’un rapport de ventes.

![Actualiser les statistiques](./assets/refresh-stats.png){width="700"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. Dans la liste, cochez la case correspondant à chaque rapport à actualiser.

1. Définissez la variable **[!UICONTROL Actions]** à l’une des options suivantes :

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Cliquez sur **[!UICONTROL Submit]**.
