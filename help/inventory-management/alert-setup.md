---
title: Alertes de produit
description: Découvrez les alertes de produits et comment les utiliser pour informer les clients de l’état des stocks et des changements de prix des produits.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Alertes de produit

Les clients peuvent s’abonner à deux types d’alertes par email : les alertes de changement de prix et les alertes en stock. Pour chaque type d&#39;alerte, vous pouvez déterminer si les clients peuvent s&#39;abonner, sélectionner le modèle d&#39;email utilisé et identifier l&#39;expéditeur de l&#39;email.

![Inscrivez-vous à une alerte de produit](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Alertes de changement de prix

Lorsque les alertes de changement de prix sont activées, un lien _Me avertir lorsque les baisses de prix_ s’affiche sur chaque page de produit. Les clients peuvent cliquer sur le lien pour s’abonner à des alertes liées au produit. Les invités sont invités à ouvrir un compte dans votre boutique. Dès que les prix changent ou que le produit est spécial, toute personne qui s&#39;est inscrite à l&#39;alerte reçoit une alerte par email.

## Alertes en stock

L’alerte en stock crée un lien appelé _Avertissez-moi lorsque ce produit est en stock_ pour chaque produit en rupture de stock. Les clients peuvent cliquer sur le lien pour s’abonner à l’alerte. Lorsque le produit est de nouveau en stock, les clients reçoivent un e-mail les informant qu’il est disponible. Les produits avec des alertes ont un onglet _Alertes produit_ dans le panneau Informations sur les produits qui répertorie les clients qui se sont abonnés à une alerte.

![Liste des abonnements aux produits et aux alertes de prix](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Configuration des alertes de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Cliquez pour développer la section _[!UICONTROL Product Alerts]_&#x200B;et procédez comme suit :

   ![Alertes produit](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Pour proposer des alertes de changement de prix à vos clients, définissez **[!UICONTROL Allow Alert When Product Price Changes]** sur `Yes`.

   - Définissez **[!UICONTROL Price Alert Email Template]** sur le modèle que vous souhaitez utiliser pour les notifications d’alerte de prix.

   - Pour proposer des alertes lorsque des produits en rupture de stock redeviennent disponibles, définissez **[!UICONTROL Allow Alert When Product Comes Back in Stock]** sur `Yes`.

     >[!NOTE]
     >
     >Le message _Avertissez-moi lorsque ce produit est en stock_ s’affiche uniquement lorsque **[!UICONTROL Display Out of Stock Products]** est défini sur `Yes` (dans la configuration à [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Définissez **[!UICONTROL Stock Alert Email Template]** sur le modèle que vous souhaitez utiliser pour les alertes de stock de produits.

   - Définissez **[!UICONTROL Alert Email Sender]** sur le [contact de magasin](../getting-started/store-details.md#store-email-addresses){target="_blank"} que vous souhaitez afficher comme expéditeur de l’alerte par e-mail. Pour en savoir plus sur [stocker les adresses électroniques](../configuration-reference/general/store-email-addresses.md){target="_blank"} dans le guide d’utilisation principal.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Configuration des modèles d’email d’alertes de produit

Ensuite, configurez, ajoutez ou modifiez le modèle d’email correspondant à votre alerte de prix. Vous pouvez modifier vos configurations d’alerte de prix après avoir créé des modèles supplémentaires.

Pour plus d’informations sur l’utilisation de la messagerie électronique, voir [Modèles de message](../systems/email-template-custom.md#message-templates) dans le _Guide des systèmes d’administration_.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Sous _Charger le modèle par défaut_, sélectionnez le **[!UICONTROL Template]** que vous souhaitez personnaliser.

   Vous pouvez choisir le modèle d’alerte inclus dans votre thème. Vous pouvez également sélectionner les modèles `Price Alert` ou `Stock Alert` sous _[!UICONTROL Magento_PriceAlert]_.

1. Cliquez sur **[!UICONTROL Load Template]**.

1. Saisissez un **[!UICONTROL Template Name]**.

   Vous pouvez sélectionner ce nom dans la configuration _Alertes sur le prix_.

1. Lisez le contenu existant et apportez les modifications nécessaires pour les éléments suivants :

   | Champ | Description |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Ce texte s’affiche dans l’objet d’un email. |
   | [!UICONTROL Template Content] | Ce texte est affiché dans le contenu complet de l&#39;email envoyé. |

1. Pour ajouter des informations générées à partir de données [!DNL Commerce], utilisez l’option **[!UICONTROL Insert Variable]** pour utiliser une liste de variables disponibles.

1. Cliquez sur **[!UICONTROL Save Template]**.

## Paramètres d’exécution d’alerte de produit

Ces paramètres vous permettent de sélectionner la fréquence à laquelle [!DNL Commerce] recherche les modifications qui nécessitent l’envoi d’alertes. Vous pouvez également sélectionner le destinataire, l’expéditeur et le modèle des emails envoyés en cas d’échec de l’envoi d’alertes.

![Paramètres d’exécution d’alerte de produit](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Product Alerts Run Settings]** .

1. Pour déterminer la fréquence d’envoi des alertes de produit, définissez **[!UICONTROL Frequency]** sur l’une des options suivantes :

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Pour déterminer l’heure d’envoi des alertes de produit par jour, définissez **[!UICONTROL Start Time]** sur l’heure, la minute et la seconde.

   >[!NOTE]
   >
   >Les alertes de produit sont envoyées par le consommateur &quot;product_alert&quot;.

1. Pour **[!UICONTROL Error Email Recipient]**, saisissez l’adresse électronique de la personne à contacter en cas d’erreur.

1. Pour le **[!UICONTROL Error Email Sender]**, sélectionnez l’identité du magasin qui apparaît comme expéditeur de la notification d’erreur.

1. Définissez **[!UICONTROL Error Email Template]** sur le modèle d’email transactionnel à utiliser pour la notification d’erreur.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
