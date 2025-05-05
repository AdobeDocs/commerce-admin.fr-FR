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

Parfois, les clients ont besoin d’aide pour leur commande. Les administrateurs de magasin peuvent utiliser _Se connecter en tant que client_, ce qui leur permet de voir ce que le client voit et d’effectuer des mises à jour pour l’aider.

Toutes les actions entreprises lors de la connexion en tant que client sont appliquées au compte du client réel.

Lorsqu’il est activé pour un utilisateur _Admin_, le bouton _[!UICONTROL Login as Customer]_&#x200B;s’affiche sur plusieurs pages :

* [Page Modifier le client](../customers/update-account.md)
* [Page Afficher la commande](../stores-purchase/order-processing.md)
* [Page Affichage de la facture](../stores-purchase/invoices.md)
* [Page Affichage des envois](../stores-purchase/shipments.md)
* [Page Affichage de la note de crédit](../stores-purchase/credit-memo-create.md)

![Se connecter en tant que client](assets/login-as-customer.png){width="600" zoomable="yes"}

## Activation de la connexion en tant que client

L’activation de _Se connecter en tant que client_ nécessite que vous activiez la fonctionnalité dans votre instance Commerce, puis que vous autorisiez l’accès des utilisateurs administrateurs dans les autorisations de rôle d’utilisateur.

### Activation de la fonctionnalité

1. Dans la barre latérale Admin, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Login as Customer]**.

   ![Options de configuration - Connexion en tant que client](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Login as Customer]** sur `Yes`.

1. _(Facultatif)_ Définissez **[!UICONTROL Disable Page Cache for Admin User]** sur `No` pour activer le cache de page lorsque l’utilisateur administrateur se connecte en tant que client.

   >[!WARNING]
   >
   > La désactivation du cache de page (`Yes` - valeur par défaut) garantit que l’utilisateur qui se connecte en tant que client obtient des données nouvelles et non mises en cache.

1. _(Facultatif)_ Définissez **[!UICONTROL Store View to Log in]** sur `Manual Selection` si vous disposez d’une configuration multi-site et/ou multi-magasin et souhaitez que l’utilisateur administrateur sélectionne la vue de magasin lors de sa connexion en tant que client.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Activation de l’accès pour les utilisateurs administrateurs

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _Autorisations_ > **[!UICONTROL User Roles]**.

1. Cliquez sur le rôle dans la liste.

1. Dans le panneau de gauche [!UICONTROL _Role Information_], cliquez sur **[!UICONTROL Role Resources]**.

1. Remplacez **[!UICONTROL Role Resources]** sur la page par `Custom`.

   >[!INFO]
   >
   > Lorsque cette option est sélectionnée, la hiérarchie des ressources s’affiche dans la page.

1. Faites défiler l’écran jusqu’à l’élément parent **[!UICONTROL Customers]** et l’élément **[!UICONTROL Login as Customer]** situé en dessous. Sélectionnez ensuite les ressources à activer pour le rôle :

   * **[!UICONTROL Allow Login as Customer]** - Permet à l’utilisateur administrateur d’utiliser la fonction _Se connecter en tant que client_.
   * **[!UICONTROL View Login as Customer Log]** - Permet à l’utilisateur administrateur d’afficher le _journal de connexion en tant que client_.

   ![Ressources du rôle - Connexion en tant que client](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Role]**.

## Se connecter en tant que client auprès de l’administrateur

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > [!UICONTROL _Tous les clients_].

1. Ouvrez un utilisateur en mode d’édition.

1. Dans le panneau **[!UICONTROL Customer Information]**, sélectionnez la section **[!UICONTROL Account Information]** .

1. Définissez le **[!UICONTROL Allow remote shopping assistance]** sur `Yes`.

   >[!INFO]
   >
   >L’administrateur peut désormais se connecter en tant qu’utilisateur sans son autorisation à partir du storefront.

## Autorisation du compte client pour l’assistance technique pour les achats à distance

Pour permettre l’accès au compte au personnel de l’assistance de la boutique depuis l’administrateur, un client doit activer la fonctionnalité pour son compte :

1. Le client accède à la page **[!UICONTROL Account Information]**.

1. Sélectionne la case à cocher **[!UICONTROL Allow remote shopping assistance]**.

1. Le client clique sur **[!UICONTROL Save]**.

![Page d’informations sur le compte](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Sans cette autorisation, un utilisateur administrateur ne peut pas se connecter en tant que client.

## Utilisation de la connexion en tant que client

>[!INFO]
>
>Pour utiliser _Connectez-vous en tant que client_, assurez-vous que votre administrateur est configuré comme décrit précédemment.

_Connectez-vous en tant que client_ vous permet de voir le site comme le fait le client et de résoudre les problèmes et d’agir pour le client. Si vous disposez d’un rôle utilisateur attribué avec les autorisations requises :

1. Vous pouvez cliquer sur **[!UICONTROL Login as Customer]** sur les pages répertoriées dans la section précédente.
1. Les actions Se connecter en tant que client sont disponibles dans le rapport Actions .

>[!WARNING]
>
>Toutes les actions entreprises lors de la connexion à [!UICONTROL _en tant que client_] (telles que l’ajout/la suppression de produits) sont appliquées à la commande réelle du client. Sur le storefront, une bannière s’affiche lorsque vous êtes `logged in as customer_name` pour vous rappeler l’état spécial.

## Connexion en tant que connexion client

{{ee-feature}}

Adobe Commerce fournit une journalisation pour les actions _Se connecter en tant que client_. Il répertorie toutes les sessions pendant lesquelles un utilisateur administrateur accède à la fonctionnalité. Pour accéder aux actions consignées, accédez au [rapport des actions d’administration](../systems/action-log-report.md).

Vous pouvez filtrer le paramètre de rapport **[!UICONTROL Action Group]** sur `Login As Customer` en haut de la page et cliquer sur **[!UICONTROL Search]**.

![Filtrer le rapport Actions](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
