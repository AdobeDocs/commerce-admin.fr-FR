---
title: Rapport de règlement PayPal
description: Découvrez le rapport de règlement PayPal comme outil de gestion des transactions PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Rapport de règlement PayPal

Le rapport de règlement de PayPal fournit aux marchands les informations sur chaque transaction qui affecte le règlement des fonds.

>[!NOTE]
>
>Avant de générer des rapports de règlement, l’administrateur du magasin doit demander aux services techniques du commerce de PayPal de créer un compte utilisateur SFTP, d’activer la génération de rapports de règlement et d’activer SFTP dans leur compte commercial PayPal.

Après avoir configuré et activé les rapports de règlement dans le compte marchand PayPal, Adobe Commerce et Magento Open Source commencent à générer des rapports pendant les 24 heures suivantes. Vous pouvez consulter la liste des rapports de règlement disponibles à partir de l’administrateur.

**_Pour afficher les rapports de colonisation :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![Rapports de règlement PayPal](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Pour les mises à jour les plus récentes, cliquez sur **[!UICONTROL Fetch Updates]** dans le coin supérieur droit.

   Le système se connecte au serveur SFTP PayPal pour récupérer les rapports. Une fois le processus terminé, un message s’affiche avec le nombre de rapports récupérés. Le rapport contient les informations suivantes pour chaque transaction :

   | Colonne de rapport | Description |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | L’un des codes de référence suivants :<br/>- ID de commande<br/>- ID de transaction<br/>- ID d’abonnement |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Texte saisi par le commerçant lors de la transaction à PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- La direction du mouvement monétaire du montant brut.<br/>**[!UICONTROL Fee Debit or Credit]** - La direction du mouvement de l&#39;argent pour les frais. |

   {style="table-layout:auto"}
