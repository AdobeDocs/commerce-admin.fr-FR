---
title: Créer des rappels par e-mail
description: Découvrez comment configurer une règle de rappel par e-mail qui utilise une règle de prix de panier existante.
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Créer des rappels par e-mail

Avant de configurer une règle de rappel par e-mail, vous devez [configurer une règle de prix de panier](price-rules-cart-create.md) pour définir la promotion proposée. Les conditions de règle qui déclenchent un rappel par e-mail peuvent être basées sur les propriétés de panier, de liste de souhaits ou les deux.

>[!NOTE]
>
>Les rappels par e-mail peuvent promouvoir une règle de prix de panier avec ou sans coupon. Une règle de prix de panier qui définit un coupon généré automatiquement génère un code de coupon aléatoire pour chaque client.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rule]**.

1. Effectuez la _[!UICONTROL Rule Information]_comme suit :

   ![Règle de rappel d’e-mail](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - Saisissez un **[!UICONTROL Rule Name]** pour identifier la règle en interne.

   - Saisissez un bref **[!UICONTROL Description]** de la règle.

   - Pour choisir la promotion **[!UICONTROL Cart Price Rule]** que ce rappel doit promouvoir, cliquez sur **[!UICONTROL Select Rule…]**, puis sélectionnez la règle.

     ![Règle du panier - sélectionner](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - Si vous souhaitez que la règle entre en vigueur immédiatement, définissez **[!UICONTROL Status]** sur `Active`.

   - Pour configurer une période afin que la règle soit active, saisissez les dates **[!UICONTROL From]** et **[!UICONTROL To]**.

     Vous pouvez également choisir la date dans le Calendrier ( ![icône Calendrier](../assets/icon-calendar.png) ).

   - Pour envoyer le rappel plusieurs fois, saisissez le nombre de jours avant la prochaine explosion d’e-mail dans le champ **[!UICONTROL Repeat Schedule]** .

1. Dans le panneau de gauche, choisissez **[!UICONTROL Conditions]**.

   Au moins une condition doit être définie pour la règle. Le processus est similaire à la création d’une [ règle de prix de catalogue ](price-rules-catalog.md).

   ![Conditions de rappel des emails](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   Cliquez sur _Ajouter_ ( ![Icône Ajouter](../assets/icon-add-green-circle.png)) pour afficher la liste des options, puis choisissez l&#39;une des conditions suivantes :

   - Liste de souhaits
   - Panier

   >[!NOTE]
   >
   >Si un client possède plusieurs paniers abandonnés, listes de souhaits ou combinaisons des deux, l’e-mail de rappel n’est déclenché qu’une seule fois pour ce client. Pour déclencher à nouveau le même rappel par e-mail, utilisez le champ _[!UICONTROL Repeat Schedule]_pour définir le nombre de jours entre les e-mails. <br/>
   >
   >Le même rappel par e-mail n’est **_pas redéclenché_** pour le même client pour les **_nouveaux_** paniers abandonnés et listes de souhaits **_après_** la période de _[!UICONTROL Repeat Schedule]_est terminée.

   Renseignez la condition pour décrire le scénario qui déclenche l’e-mail de rappel.

   ![exemple de conditions de rappel d’e-mail](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. Dans le panneau de gauche, choisissez **[!UICONTROL Emails and Labels]**.

   ![Règle de rappel d’e-mail - Modèles d’e-mails et de libellés ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. Dans la section **[!UICONTROL Email Templates]** , choisissez le modèle d’e-mail à utiliser pour chaque site web et vue de magasin dans votre [hiérarchie de magasin](../getting-started/websites-stores-views.md).

   Si vous ne souhaitez pas envoyer l’e-mail de rappel aux clients d’une vue de magasin, laissez la valeur `Not Selected`.

1. Dans la section _Titres et description par défaut_, procédez comme suit :

   - Saisissez le **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >Cette valeur peut être incorporée dans des modèles d’e-mail à l’aide de la variable `promotion_name` .

   - Saisissez le **[!UICONTROL Rule Description for All Store Views]**.

     ![Rappels par e-mail - titres et descriptions](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - Dans la section _[!UICONTROL Titles and Descriptions Per Store View]_, saisissez les **[!UICONTROL Rule Title]**et **[!UICONTROL Description]**de l’_ Affichage de la boutique par défaut _. Pour plusieurs vues de magasin, saisissez le titre et la description appropriés pour chacune d’elles.

     >[!NOTE]
     >
     >La description peut être incorporée dans les modèles d’e-mail à l’aide de la variable promotion_description .

     ![Titres et descriptions - vue boutique](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Conditions de déclenchement

| Source | Déclencheur |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Rule Name] | Le nom de la règle de rappel automatique identifie la règle en interne. |
| [!UICONTROL Description] | Description de la règle pour référence interne. |
| [!UICONTROL Shopping Cart Price Rule] | Règle de panier associée à ce rappel par e-mail. Les e-mails de rappel peuvent promouvoir une règle de prix de panier avec ou sans coupon. Si une règle de prix de panier d’achats comprend un coupon généré automatiquement, la règle de rappel génère un code de coupon aléatoire et unique pour chaque client. |
| [!UICONTROL Assigned to Website] | Sites web recevant un e-mail de rappel automatisé basé sur cette règle. |
| [!UICONTROL Status] | Active la règle. Si le statut est inactif, tous les autres paramètres sont ignorés et la règle n’est pas déclenchée. Options : `Active` / `Inactive` |
| [!UICONTROL From Date] | Date de début de cette règle de rappel automatisée. Si aucune date n’est spécifiée, la règle devient active immédiatement. |
| [!UICONTROL To Date] | Date de fin de cette règle de rappel automatisée. Si aucune date n’est spécifiée, la règle devient active indéfiniment. |
| [!UICONTROL Repeat Schedule] | Le nombre de jours avant le déclenchement de la règle et l’e-mail de rappel envoyé à nouveau, à condition que les conditions soient remplies. Pour déclencher la règle plusieurs fois, saisissez le nombre de jours avant la prochaine explosion d’e-mail, en les séparant par une virgule. Par exemple, saisissez `7` pour que la règle soit déclenchée à nouveau sept jours plus tard ; saisissez `7,14` pour que la règle soit déclenchée dans sept jours, puis à nouveau 14 jours plus tard. |
| [!UICONTROL Email Templates] | Détermine le modèle d’e-mail à utiliser pour chaque vue de magasin. |
| [!UICONTROL Rule Title for All Store Views] | Détermine le titre de la règle pour chaque vue de magasin. |
| [!UICONTROL Rule Description for All Store Views] | Détermine la description de la règle pour chaque vue de magasin. |

{style="table-layout:auto"}
