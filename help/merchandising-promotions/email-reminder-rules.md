---
title: Rappels électroniques
description: Découvrez les rappels par email qui peuvent être envoyés automatiquement aux clients lorsqu’un ensemble spécifique de conditions est satisfait.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Rappels électroniques

{{ee-feature}}

Le but d’un rappel par email est d’encourager les personnes qui ont visité votre boutique à profiter d’une promotion et à faire un achat. Des rappels par email peuvent être envoyés automatiquement aux clients lorsqu’un ensemble spécifique de conditions est satisfait. Par exemple, vous pouvez envoyer un rappel aux clients qui ont ajouté un article à leur panier ou à leur liste de souhaits, mais qui n’ont pas encore effectué d’achat. Vous pouvez utiliser des rappels par e-mail pour encourager les clients à retourner dans votre boutique et inclure une [code de coupon](price-rules-cart-coupon.md) comme une incitation. Les codes coupon peuvent être générés automatiquement pour chaque lot de rappels par email, afin de vous permettre de contrôler les offres associées à chaque lot.

Les rappels par email peuvent être déclenchés après qu’un nombre spécifique de jours a été passé depuis l’abandon d’un panier ou pour toute autre condition que vous souhaitez définir. Les conditions courantes comprennent la valeur totale du panier, la quantité, les articles dans le panier, etc.

>[!NOTE]
>
>Si un client possède plusieurs paniers abandonnés correspondants, une liste de souhaits ou une combinaison des deux, le rappel par e-mail n’est déclenché qu’une seule fois pour ce client. Pour déclencher à nouveau le même rappel par e-mail, utilisez le _[!UICONTROL Repeat Schedule]_pour définir le nombre de jours entre les emails.

![Rappels électroniques](./assets/email-reminders.png){width="700" zoomable="yes"}

## Configuration de rappels par courrier électronique

Les règles de rappel de courrier électronique peuvent être envoyées à intervalles réguliers par minute, heure ou jour. La configuration détermine le nombre d’emails envoyés par lot et l’identité du magasin qui apparaît comme expéditeur du message.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Promotions]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Automated Email Reminder Rules]** et procédez comme suit :

   ![Configuration des clients - règles de rappel de courrier électronique automatisé](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Enable Reminder Emails]** to `Yes`.

   - Pour définir la fréquence d’exécution des vérifications pour les nouveaux clients qui répondent aux critères des rappels de courrier électronique automatisés, définissez **[!UICONTROL Frequency]** à l’une des options suivantes :

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Définissez les **[!UICONTROL Interval]**, en fonction de la variable _[!UICONTROL Frequency]_.

   - Définir **[!UICONTROL Start Time]** à l’heure, à la minute et à la seconde, l’email est envoyé, sur la base d’une horloge de 24 heures.

   - Pour limiter le nombre d’emails pouvant être envoyés par lot, saisissez le nombre dans la variable **[!UICONTROL Maximum Emails per One Run]** champ .

   - Pour éviter les tentatives répétées d’envoi d’un email en échec, saisissez le nombre maximum de tentatives dans la variable **[!UICONTROL Email Send Failure Threshold]** champ .

   - Définir **[!UICONTROL Reminder Email Sender]** à la fonction [contact de magasin](../getting-started/store-details.md#store-email-addresses) qui s’affiche comme expéditeur de l’email de rappel.

   Pour obtenir la liste détaillée de ces options, voir [Règles de rappel de courrier électronique automatisé](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) dans le _Référence de configuration_.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Modèles de rappel par email

Le modèle de rappel par e-mail par défaut peut être personnalisé et des modèles supplémentaires peuvent être créés pour différentes promotions. Les rappels par email contiennent une sélection de variables spécifiques qui peuvent être intégrées dans le message. Les informations contenues dans ces variables sont déterminées par la règle de rappel par email que vous configurez, ainsi que par la règle de prix du panier associée au coupon. Le bouton Insérer une variable peut être utilisé pour insérer la balise avec la variable dans le modèle. Pour en savoir plus, voir [Email](../systems/email-templates.md).

![Aperçu du rappel par email](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### Personnalisation d’un modèle de rappel d’email

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Dans le **[!UICONTROL Template]** Liste sous `Magento_Reminder`, choisissez la variable **[!UICONTROL Promotion Notification/Reminder]** modèle.

1. Cliquez sur **[!UICONTROL Load Template]**.

Respectez les [instructions](../systems/email-template-custom.md) pour personnaliser le modèle.

### Variables de rappel de courrier électronique

#### Code coupon

```
{{var coupon.getCode()|escape}}
```

#### Limite d’utilisation du bon

```
{{var coupon.usage_limit|escape}}
```

#### Utilisation du coupon par client

```
{{var coupon.usage_per_customer|escape}}
```

#### URL du compte client

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### Nom du client

```
{{var customer_data.name|escape}}
```

#### Modèle de pied de page de courrier électronique

```
{{template config_path="design/email/footer_template"}}
```

#### Modèle d’en-tête de courrier électronique

```
{{template config_path="design/email/header_template"}}
```

#### Email Logo Image Alt

```
{{var logo_alt}}
```

#### URL de l’image du logo de l’email

```
{{var logo_url}}
```

#### Description de la promotion

```
{{var promotion_description|escape|nl2br}}
```

#### Nom de la promotion

```
{{var promotion_name|escape}}
```

#### Nom de la boutique

```
{{var store.frontend_name}}
```

#### URL du magasin

```
{{store url=""}}
```
