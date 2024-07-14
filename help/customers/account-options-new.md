---
title: Nouvelles options du compte client
description: Découvrez les options de configuration des nouveaux comptes clients de votre boutique.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Nouvelles options du compte client

Dans la section _[!UICONTROL Create New Account Options]_de la configuration, les options de base du compte sont combinées avec des options plus avancées liées à la validation de l’ID de TVA et aux intégrations personnalisées. Les instructions suivantes portent uniquement sur les options les plus fréquemment utilisées. Pour en savoir plus sur les affectations automatiques de groupes de clients, voir [Validation de la TVA](../stores-purchase/vat.md).

![Créer des options de compte](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configuration des options de base du compte client

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Create New Account Options]** :

   ![ Paramètres par défaut Créer des options de compte ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Définissez chacune des options en fonction de l’expérience client que vous devez prendre en charge sur votre storefront :

   - Définissez **[!UICONTROL Default Group]** sur le groupe de clients affecté à de nouveaux clients lors de la création d’un compte.

   - Si vous avez un numéro _Taxe à valeur ajoutée_ et que vous souhaitez qu’il soit visible par les clients, définissez **[!UICONTROL Show VAT Number on Storefront]** sur `Yes`.

   - Pour demander l’adresse électronique d’un client lors de la création d’une commande d’administrateur pour un client, définissez **[!UICONTROL Email is required field for Admin order creation]** sur `Yes`.

   - Saisissez le **[!UICONTROL Default Email Domain]** correspondant au magasin, par exemple `mystore.com`

   - Définissez **[!UICONTROL Default Welcome Email]** sur le modèle utilisé pour l’e-mail de bienvenue envoyé aux nouveaux clients.

   - Pour obliger les clients à confirmer leur demande d’ouverture d’un compte avec votre magasin, définissez **[!UICONTROL Require Emails Confirmation]** sur `Yes`. Définissez ensuite **[!UICONTROL Confirmation Link Email]** sur le modèle utilisé pour l&#39;email de confirmation.

     >[!NOTE]
     >
     >À partir de la version 2.4.7, les clients doivent saisir à nouveau leur adresse électronique et leur mot de passe pour se connecter à leur compte après confirmation par e-mail, quel que soit le navigateur.

   - Définissez **[!UICONTROL Welcome Email]** sur le modèle utilisé pour le message de bienvenue envoyé une fois le compte confirmé.

   - Définissez **[!UICONTROL Default Welcome Email without Password]** sur le modèle utilisé lors de la création d’un compte client qui n’a pas encore de mot de passe. Par exemple, un mot de passe n’est pas encore attribué pour un compte client créé à partir de l’administrateur.

   - Définissez **[!UICONTROL Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur de l’e-mail de bienvenue.

   - Pour obliger les clients à confirmer leur demande d’ouverture d’un compte avec votre magasin, définissez **[!UICONTROL Require Emails Confirmation]** sur `Yes`. Définissez ensuite **[!UICONTROL Confirmation Link Email]** sur le modèle utilisé pour l&#39;email de confirmation.

   ![Créer des options de compte avec la TVA activée](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Pour plus d’informations sur chacune des options disponibles dans cet ensemble d’options de configuration, voir la _référence de configuration_ [ de ](../configuration-reference/customers/customer-configuration.md) pour créer de nouvelles options de compte.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
