---
title: Options du nouveau compte client
description: Découvrez les options de configuration des nouveaux comptes clients de votre boutique.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Options du nouveau compte client

Dans le _[!UICONTROL Create New Account Options]_dans la configuration, les options de compte de base sont combinées à des options plus avancées relatives à la validation du numéro individuel d&#39;identification de TVA et aux intégrations personnalisées. Les instructions suivantes ne couvrent que les options les plus utilisées. Pour en savoir plus sur les affectations automatiques de groupes de clients, voir [Validation TVA](../stores-purchase/vat.md).

![Options de création de compte](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configurer les options de base du compte client

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développer le **[!UICONTROL Create New Account Options]** section :

   ![Paramètres par défaut des options Créer un nouveau compte](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Définissez chacune des options en fonction de l’expérience client que vous devez prendre en charge sur votre storefront :

   - Définir **[!UICONTROL Default Group]** au groupe de clients affecté aux nouveaux clients lors de la création d’un compte.

   - Si vous avez _Taxe sur la valeur ajoutée_ nombre et souhaitez qu’il soit visible pour les clients, définissez **[!UICONTROL Show VAT Number on Storefront]** vers `Yes`.

   - Pour demander l’e-mail d’un client lors de la création d’une commande administrateur pour un client, définissez **[!UICONTROL Email is required field for Admin order creation]** vers `Yes`.

   - Saisir le **[!UICONTROL Default Email Domain]** pour le magasin, par exemple `mystore.com`

   - Définir **[!UICONTROL Default Welcome Email]** au modèle utilisé pour l’e-mail de bienvenue envoyé aux nouveaux clients .

   - Pour demander aux clients de confirmer leur demande d’ouverture d’un compte dans votre boutique, définissez **[!UICONTROL Require Emails Confirmation]** vers `Yes`. Ensuite, définissez **[!UICONTROL Confirmation Link Email]** au modèle utilisé pour l’e-mail de confirmation.

     >[!NOTE]
     >
     >À partir de la version 2.4.7, les clients doivent saisir à nouveau leur adresse e-mail et leur mot de passe pour se connecter à leur compte après confirmation par e-mail, quel que soit le navigateur.

   - Définir **[!UICONTROL Welcome Email]** au modèle utilisé pour le message de bienvenue envoyé une fois le compte confirmé.

   - Définir **[!UICONTROL Default Welcome Email without Password]** au modèle utilisé lors de la création d’un compte client qui n’a pas encore de mot de passe. Par exemple, aucun mot de passe n’a encore été attribué au compte client créé à partir de l’administrateur.

   - Définir **[!UICONTROL Email Sender]** au contact du magasin qui apparaît comme expéditeur de l’e-mail de bienvenue.

   - Pour demander aux clients de confirmer leur demande d’ouverture d’un compte dans votre boutique, définissez **[!UICONTROL Require Emails Confirmation]** vers `Yes`. Ensuite, définissez **[!UICONTROL Confirmation Link Email]** au modèle utilisé pour l’e-mail de confirmation.

   ![Créer de nouvelles options de compte avec TVA activée](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Pour plus d’informations sur chacune des options disponibles dans ce jeu d’options de configuration, voir le _Options de création de compte_ [référence de configuration](../configuration-reference/customers/customer-configuration.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
