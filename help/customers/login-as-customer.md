---
title: Fournir une assistance aux acheteurs
description: Lorsque vous utilisez la fonction Se connecter en tant que client , vous pouvez voir ce que les clients voient et effectuer des mises à jour en leur nom.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Fournir une assistance aux acheteurs

Parfois, les clients ont besoin d’aide pour leur commande. Les administrateurs de magasin peuvent utiliser _Connexion en tant que client_, qui leur permet de voir ce que le client voit et d’effectuer des mises à jour pour l’aider.

Toutes les actions entreprises lors de la connexion en tant que client sont appliquées au compte du client réel.

Lorsqu’il est activé pour une _Administration_ l’utilisateur, _[!UICONTROL Login as Customer]_s’affiche sur plusieurs pages :

* [Page Modifier le client](../customers/update-account.md)
* [Page Afficher la commande](../stores-purchase/order-processing.md)
* [Page Affichage de la facture](../stores-purchase/invoices.md)
* [Page Affichage des envois](../stores-purchase/shipments.md)
* [Page Affichage de la note de crédit](../stores-purchase/credit-memo-create.md)

![Se connecter en tant que client](assets/login-as-customer.png){width="600" zoomable="yes"}

## Activation de la connexion en tant que client

Activation _Connexion en tant que client_ nécessite que vous activiez la fonction dans votre instance Commerce, puis que vous autorisiez l’accès des utilisateurs administrateurs dans les autorisations de rôle utilisateur.

### Activation de la fonctionnalité

1. Dans la barre latérale d’administration, accédez à  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez  **[!UICONTROL Login as Customer]**.

   ![Options de configuration - Connexion en tant que client](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enable Login as Customer]** to `Yes`.

1. _(Facultatif)_ Définir **[!UICONTROL Disable Page Cache for Admin User]** to `No` pour activer le cache de page lorsque l’utilisateur administrateur se connecte en tant que client.

   >[!WARNING]
   >
   > Désactivation du cache de page (`Yes` - par défaut) s’assure que l’utilisateur qui se connecte en tant que client obtient des données nouvelles et non mises en cache.

1. _(Facultatif)_ Définir **[!UICONTROL Store View to Log in]** to `Manual Selection` si vous disposez d’une configuration multi-site et/ou multi-magasin et que vous souhaitez que l’utilisateur administrateur sélectionne la vue de magasin lors de sa connexion en tant que client.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### Activation de l’accès pour les utilisateurs administrateurs

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _Autorisations_ > **[!UICONTROL User Roles]**.

1. Cliquez sur le rôle dans la liste.

1. Dans le [!UICONTROL _Informations sur les rôles_] panneau de gauche, cliquez sur **[!UICONTROL Role Resources]**.

1. Modifier **[!UICONTROL Role Resources]** sur la page vers `Custom`.

   >[!INFO]
   >
   > Lorsque cette option est sélectionnée, la hiérarchie des ressources s’affiche dans la page.

1. Faites défiler l’écran jusqu’à  **[!UICONTROL Customers]** élément parent et **[!UICONTROL Login as Customer]** sous-jacent. Sélectionnez ensuite les ressources à activer pour le rôle :

   * **[!UICONTROL Allow Login as Customer]** - Permet à l’utilisateur administrateur d’utiliser la variable _Connexion en tant que client_ fonction .
   * **[!UICONTROL View Login as Customer Log]** - Permet à l’utilisateur administrateur d’afficher la variable _Connexion en tant que client_ Journal.

   ![Ressources de rôle - Connexion en tant que client](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Role]**.

## Se connecter en tant que client auprès de l’administrateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > [!UICONTROL _Tous les clients_].

1. Ouvrez un utilisateur en mode d’édition.

1. Dans le **[!UICONTROL Customer Information]** , choisissez la variable **[!UICONTROL Account Information]** .

1. Définissez la variable **[!UICONTROL Allow remote shopping assistance]** to `Yes`.

   >[!INFO]
   >
   >L’administrateur peut désormais se connecter en tant qu’utilisateur sans son autorisation à partir du storefront.

## Autorisation du compte client pour l’assistance technique pour les achats à distance

Pour permettre l’accès au compte au personnel de l’assistance de la boutique depuis l’administrateur, un client doit activer la fonctionnalité pour son compte :

1. Le client se rend au **[!UICONTROL Account Information]** page.

1. Sélectionne la variable **[!UICONTROL Allow remote shopping assistance]** .

1. Le client clique **[!UICONTROL Save]**.

![Page Informations du compte](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Sans cette autorisation, un utilisateur administrateur ne peut pas se connecter en tant que client.

## Utilisation de la connexion en tant que client

>[!INFO]
>
>Pour utiliser _Connexion en tant que client_, assurez-vous que votre administrateur est configuré comme décrit précédemment.

_Connexion en tant que client_ vous permet de voir le site comme le fait le client et de résoudre les problèmes et d’agir pour le client. Si vous disposez d’un rôle utilisateur attribué avec les autorisations requises :

1. Cliquez sur **[!UICONTROL Login as Customer]** sur les pages répertoriées dans la section précédente.
1. Les actions Se connecter en tant que client sont disponibles dans le rapport Actions .

>[!WARNING]
>
>Toutes les actions entreprises lors de la connexion [!UICONTROL _en tant que client_] (par exemple, ajouter/supprimer des produits) sont appliqués à la commande réelle du client. Sur le storefront, une bannière s’affiche lorsque vous êtes `logged in as customer_name` pour vous rappeler l’état spécial.

## Connexion en tant que connexion client

{{ee-feature}}

Adobe Commerce fournit une journalisation de la variable _Connexion en tant que client_ actions. Il répertorie toutes les sessions pendant lesquelles un utilisateur administrateur accède à la fonctionnalité. Pour accéder aux actions consignées, accédez à la [Rapport Actions de l’administrateur](../systems/action-log-report.md).

Vous pouvez filtrer les paramètres du rapport. **[!UICONTROL Action Group]** to `Login As Customer` en haut de la page et en cliquant sur **[!UICONTROL Search]**.

![Filtrage du rapport Actions](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
