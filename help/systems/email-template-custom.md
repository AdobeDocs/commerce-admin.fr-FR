---
title: Personnalisation des modèles de courrier électronique
description: Découvrez comment personnaliser des modèles de courrier électronique pour chaque vue de site Web, de magasin ou de magasin.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Personnalisation des modèles de courrier électronique

Commerce comprend un modèle de courrier électronique par défaut pour la section body de chaque message envoyé par le système. Le modèle du contenu du corps est combiné avec les modèles d’en-tête et de pied de page pour créer le message complet. Le contenu est formaté avec HTML et CSS et peut être facilement modifié et personnalisé en ajoutant [variables](variables-predefined.md). Les modèles de courrier électronique peuvent être personnalisés pour chaque site web, magasin ou vue de magasin. Si vous utilisez des modèles personnalisés, veillez à mettre à jour la [configuration système](email-templates.md#configure-email-templates) pour vous assurer que le modèle correct est utilisé. Pour savoir comment utiliser des instructions conditionnelles dans la personnalisation du modèle de courrier électronique, consultez la [documentation destinée aux développeurs](https://developer.adobe.com/commerce/frontend-core/guide/templates/email/#theme-based-customizations-1).

![Exemple - aperçu de l’email de bienvenue](./assets/email-template-preview.png){width="500" zoomable="yes"}

Les modèles par défaut incluent votre logo et les informations de magasin. Ils peuvent être utilisés sans autre personnalisation. Toutefois, il est recommandé de consulter chaque modèle et d’apporter les modifications nécessaires avant de les envoyer aux clients.

- [Modèle d’en-tête](email-template-custom.md#header-template)
- [Modèle de pied de page](email-template-custom.md#footer-template)
- [Modèles de message](email-template-custom.md#message-templates)

![Modèles d’email](./assets/email-templates.png){width="700" zoomable="yes"}

## Informations sur les modèles

| Champ | Description |
| ----- | ----------- |
| [!UICONTROL Template Name] | Nom de votre modèle personnalisé. |
| [!UICONTROL Insert Variable] | Insère une variable dans le modèle à l’emplacement du curseur. |
| [!UICONTROL Template Subject] | L’ objet du modèle apparaît dans la colonne Objet. Il peut être utilisé pour trier et filtrer les modèles de la liste. |
| [!UICONTROL Template Content] | Contenu du modèle en HTML. |
| [!UICONTROL Template Styles] | Toutes les déclarations de style CSS nécessaires au format du modèle peuvent être saisies dans la zone _[!UICONTROL Template Styles]_. |

{style="table-layout:auto"}

## Modèle d’en-tête

Une fois la [configuration](email-templates.md#configure-email-templates) terminée, le modèle d’en-tête d’email inclut votre logo associé à votre boutique. Si vous avez une connaissance de base de l’HTML, vous pouvez facilement utiliser [des variables prédéfinies](variables-predefined.md) pour ajouter des informations de contact de magasin à l’en-tête.

### Étape 1. Chargement du modèle par défaut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Dans la section **[!UICONTROL Load default template]** , cliquez sur le sélecteur **[!UICONTROL Template]** et choisissez `Magento_Email` > `Header`.

   ![ En-tête du modèle de courrier électronique - Charger le modèle par défaut](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Load Template]**.

   Le code d’HTML et les variables du modèle apparaissent dans le formulaire.

### Étape 2. Personnaliser le modèle

1. Saisissez le **[!UICONTROL Template Name]** de votre en-tête personnalisé.

1. Saisissez un **[!UICONTROL Template Subject]** pour organiser les modèles.

   Dans la grille, la liste des modèles peut être triée et filtrée par la colonne _[!UICONTROL Subject]_.

   ![Informations sur l’en-tête du modèle de courrier électronique](./assets/email-template-information.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Template Content]**, modifiez l’HTML selon vos besoins.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas écraser les éléments placés entre deux accolades.

1. Pour insérer une [variable](variables-reference.md), placez le curseur dans le code à l’endroit où vous souhaitez placer la variable et cliquez sur **[!UICONTROL Insert Variable]**.

1. Sélectionnez la variable à insérer.

   ![Modèle d’en-tête - Insérer une variable](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Lorsqu’une variable est sélectionnée, une [balise de balisage](markup-tags.md) pour la variable est insérée dans le code.

   Bien que les variables Store Email Address soient les plus souvent incluses dans l’en-tête, vous pouvez saisir le code de n’importe quel système ou [variable personnalisée](variables-custom.md) directement dans le modèle.

1. Si vous devez faire des déclarations CSS, saisissez les styles dans la zone **[!UICONTROL Template Styles]**.

1. Lorsque vous êtes prêt à passer en revue votre travail, cliquez sur **[!UICONTROL Preview Template]**.

   Apportez les modifications nécessaires au modèle.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Template]**.

   Votre en-tête personnalisé apparaît désormais dans la liste des modèles de courrier électronique disponibles.

### Étape 3. Mise à jour de la configuration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Transactional Emails]** .

1. Sélectionnez le **[!UICONTROL Header Template]** utilisé par défaut pour les notifications par e-mail.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

![Configuration de la conception d’email transactionnel - modèle d’en-tête](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modèle de pied de page

Le pied de page du modèle d’email contient la ligne de fermeture et de signature du message. Vous pouvez modifier la fermeture pour l’adapter à votre style et ajouter des informations supplémentaires, telles que le nom et l’adresse de la société sous votre nom.

### Étape 1. Chargement du modèle par défaut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Dans la section **[!UICONTROL Load default template]** , cliquez sur le sélecteur **[!UICONTROL Template]** et choisissez `Magento_Email` > `Footer`.

1. Cliquez sur **[!UICONTROL Load Template]**.

   Le code d’HTML et les variables du modèle apparaissent dans le formulaire.

### Étape 2. Personnaliser et prévisualiser le modèle

1. Saisissez le **[!UICONTROL Template Name]** correspondant au pied de page personnalisé.

1. Saisissez un **[!UICONTROL Template Subject]** pour organiser les modèles.

   Dans la grille, les modèles peuvent être triés et filtrés par colonne _[!UICONTROL Subject]_.

   ![ Pied de page de modèle de courrier électronique - informations](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Template Content]**, modifiez l’HTML selon vos besoins.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas écraser les éléments placés entre deux accolades.

1. Pour insérer une [variable](variables-reference.md), placez le curseur dans le code à l’endroit où vous souhaitez placer la variable et cliquez sur **[!UICONTROL Insert Variable]**.

1. Sélectionnez la variable à insérer.

   Lorsqu’une variable est sélectionnée, une [balise de balisage](markup-tags.md) pour la variable est insérée dans le code.

   Bien que les variables de contact du magasin soient les plus souvent incluses dans le pied de page, vous pouvez saisir le code de n’importe quel système ou la [variable personnalisée](variables-custom.md) directement dans le modèle.

1. Si vous devez faire des déclarations CSS, saisissez les styles dans la zone **[!UICONTROL Template Styles]**.

### Étape 3. Mise à jour de la configuration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Transactional Emails]** .

1. Sélectionnez le **[!UICONTROL Footer Template]** utilisé comme pied de page par défaut dans les notifications par e-mail.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

![ Configuration de la conception d’email transactionnel - modèle de pied de page](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modèles de message

La personnalisation du corps de chaque message est identique à celle de l&#39;en-tête ou du pied de page. La seule différence est le modèle de message pour chaque activité ou événement qui déclenche une notification. Vous pouvez utiliser les modèles tels quels ou les personnaliser pour qu’ils correspondent à votre voix et à votre marque. Outre le texte du modèle, il existe une grande sélection de variables [prédéfinies](variables-predefined.md) et de variables [personnalisées](variables-custom.md) que vous pouvez créer et incorporer dans le modèle.

### Étape 1. Chargement du modèle par défaut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

   ![ Modèles d’email - Charger le modèle par défaut](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Procédez comme suit :

   - Sous **[!UICONTROL Load default template]**, sélectionnez le **[!UICONTROL Template]** que vous souhaitez personnaliser.

   - Cliquez sur **[!UICONTROL Load Template]**.

### Étape 2. Personnaliser le modèle

1. Pour **[!UICONTROL Template Name]**, saisissez un nom pour votre modèle personnalisé.

1. Si nécessaire, modifiez le **[!UICONTROL Template Subject]**.

   Il s’agit de la première ligne du message, qui est la formule de salutation par défaut. Vous pouvez la laisser telle quelle ou saisir quelque chose de plus explicite.

1. Prenez note du chemin d’accès **[!UICONTROL Currently Used For]** au modèle, qui est le chemin d’accès utilisé pour mettre à jour la configuration.

   ![ Modèles d’email - informations sur le modèle](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Template Content]**, modifiez l’HTML selon vos besoins.

   Le contenu se compose d’une combinaison de balises d’HTML, de directives CSS, de variables et de texte.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas taper accidentellement le code encadré de doubles accolades.

1. Pour insérer une variable, placez le curseur dans le code à l’endroit où la variable doit apparaître.

   La sélection des variables varie selon le modèle et inclut les variables [prédéfinies](variables-predefined.md) et [personnalisées](variables-custom.md) autorisées, le cas échéant.

1. Cliquez sur **[!UICONTROL Insert Variable]** et sélectionnez la variable à insérer.

   Une commande permettant d’insérer la variable est placée entre accolades et ajoutée au code à l’emplacement du curseur. Par exemple :

   `customVar code=my_custom_variable`

1. Pour effectuer des déclarations CSS, saisissez les styles dans **[!UICONTROL Template Styles]**.

   ![Modèles d’email - ajouter des styles personnalisés](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Les styles personnalisés ne sont appliqués à l&#39;email que si `{{template config_path="design/email/header_template"}}` est présent dans _[!UICONTROL Template Styles]_. Pour utiliser une page CSS personnalisée sans modèle d’en-tête par défaut, vous devez les fournir ici dans la balise d’HTML `<style>`.

### Étape 3. Mise à jour de la configuration

Le chemin de navigation _[!UICONTROL Currently Used For]_&#x200B;indique l’emplacement d’utilisation du modèle. Dans cet exemple, la configuration du modèle se trouve sur la page&#x200B;_[!UICONTROL Customer Configuration]_, dans la section _[!UICONTROL Create New Account Options]_&#x200B;et dans le champ&#x200B;_[!UICONTROL Default Welcome Email]_.

- Page - [!UICONTROL Customer Configuration]
- Section - [!UICONTROL Create New Account Options]
- Field - [!UICONTROL Default Welcome Email]

1. Dans le chemin de navigation **[!UICONTROL Currently Used For]**, cliquez sur le lien pour ouvrir la page de configuration du modèle.

   ![Modèle d’email actuel](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et recherchez le champ du modèle de courrier électronique que vous avez personnalisé.

1. Décochez la case **[!UICONTROL Use system value]** et cliquez sur le nom de votre modèle personnalisé.

   ![Configuration des clients - modèle d’email de bienvenue par défaut](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Dans le message situé en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et effacez tout cache non valide.

### Étape 4. Prévisualiser et enregistrer le modèle

1. Lorsque vous êtes prêt à passer en revue votre travail, cliquez sur **[!UICONTROL Preview Template]**.

1. Mettez le modèle à jour selon vos besoins.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Template]**.

   Votre modèle personnalisé est désormais disponible dans la liste des modèles d’email.
