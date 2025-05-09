---
title: Rapport Règlement PayPal
description: Découvrez le rapport Règlement PayPal comme outil de gestion des transactions PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Rapport Règlement PayPal

Le rapport Règlement PayPal fournit aux commerçants les informations sur chaque transaction qui affecte le règlement des fonds.

>[!NOTE]
>
>Avant de générer des rapports de règlement, l&#39;administrateur du magasin doit demander aux services techniques des commerçants PayPal de créer un compte utilisateur SFTP, d&#39;activer la génération des rapports de règlement et d&#39;activer le protocole SFTP dans leur compte professionnel PayPal.

Après avoir configuré et activé les rapports de règlement dans le compte marchand PayPal, Adobe Commerce et Magento Open Source commenceront à générer des rapports au cours des 24 heures suivantes. La liste des rapports de règlement disponibles peut être consultée à partir de l&#39;administrateur.

**_Pour afficher les rapports de liquidation, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![ Rapports de règlement PayPal ](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Pour les mises à jour les plus récentes, cliquez sur **[!UICONTROL Fetch Updates]** dans le coin supérieur droit.

   Le système se connecte au serveur SFTP PayPal pour récupérer les rapports. Une fois le processus terminé, un message indiquant le nombre de rapports récupérés s’affiche. L&#39;état comprend les informations suivantes pour chaque transaction :

   | Colonne du rapport | Description |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Un des codes de référence suivants : <br/>- Identifiant de commande<br/>- Identifiant de transaction<br/>- Identifiant d’abonnement |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Texte saisi par le commerçant sur la transaction sur PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- Direction du mouvement monétaire du montant brut.<br/>**[!UICONTROL Fee Debit or Credit]** - La direction du mouvement de l&#39;argent contre rémunération. |

   {style="table-layout:auto"}
