---
title: Nouvelles options du compte client
description: Découvrez les options de configuration des nouveaux comptes clients de votre boutique.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Nouvelles options du compte client

Dans le _[!UICONTROL Create New Account Options]_dans la section de la configuration, les options de base du compte sont combinées avec des options plus avancées liées à la validation de l’ID de TVA et aux intégrations personnalisées. Les instructions suivantes portent uniquement sur les options les plus fréquemment utilisées. Pour en savoir plus sur les affectations automatiques de groupes de clients, voir [Validation TVA](../stores-purchase/vat.md).

{{beta-updates}}

![Créer des options de compte](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configuration des options de base du compte client

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez l’objet **[!UICONTROL Create New Account Options]** section :

   ![Paramètres par défaut des nouvelles options de compte](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Définissez chacune des options en fonction de l’expérience client que vous devez prendre en charge sur votre storefront :

   - Définir **[!UICONTROL Default Group]** au groupe de clients affecté à de nouveaux clients lors de la création d’un compte.

   - Si vous avez une _Taxe sur la valeur ajoutée_ et que vous souhaitez qu’il soit visible par les clients, définissez **[!UICONTROL Show VAT Number on Storefront]** to `Yes`.

   - Pour demander l’adresse électronique d’un client lors de la création d’une commande d’administrateur pour un client, définissez **[!UICONTROL Email is required field for Admin order creation]** to `Yes`.

   - Saisissez le **[!UICONTROL Default Email Domain]** pour le magasin, par exemple `mystore.com`

   - Définir **[!UICONTROL Default Welcome Email]** au modèle utilisé pour l’e-mail de bienvenue envoyé aux nouveaux clients.

   - Définir **[!UICONTROL Default Welcome Email without Password]** au modèle utilisé lors de la création d’un compte client sans mot de passe. Par exemple, un mot de passe n’est pas encore attribué pour un compte client créé à partir de l’administrateur.

   - Définir **[!UICONTROL Email Sender]** au contact du magasin qui apparaît comme expéditeur de l’email de bienvenue.

   - Pour obliger les clients à confirmer leur demande d’ouverture d’un compte avec votre boutique, définissez **[!UICONTROL Require Emails Confirmation]** to `Yes`. Définissez ensuite **[!UICONTROL Confirmation Link Email]** au modèle utilisé pour l&#39;email de confirmation.

   - Définir **[!UICONTROL Welcome Email]** au modèle utilisé pour le message de bienvenue envoyé une fois le compte confirmé.

     ![Créer des options de compte avec la TVA activée](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     Pour plus d’informations sur chacune des options disponibles dans ce jeu d’options de configuration, voir la section _Créer des options de compte_ [référence de configuration](../configuration-reference/customers/customer-configuration.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
