---
title: Personnalisation des modèles de courrier électronique
description: Découvrez comment personnaliser des modèles de courrier électronique pour chaque vue de site Web, de magasin ou de magasin.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Personnalisation des modèles de courrier électronique

Commerce inclut un modèle d’email par défaut pour la section body de chaque message envoyé par le système. Le modèle du contenu du corps est combiné avec les modèles d’en-tête et de pied de page pour créer le message complet. Le contenu est formaté avec HTML et CSS et peut être facilement modifié et personnalisé en ajoutant des [variables](variables-predefined.md) et [widgets](../content-design/widgets.md). Les modèles de courrier électronique peuvent être personnalisés pour chaque site web, magasin ou vue de magasin. Si vous utilisez des modèles personnalisés, veillez à mettre à jour la variable [configuration du système](email-templates.md#configure-email-templates) pour vous assurer que le modèle correct est utilisé.

![Exemple : aperçu de l&#39;email de bienvenue](./assets/email-template-preview.png){width="500" zoomable="yes"}

Les modèles par défaut incluent votre logo et les informations de magasin. Ils peuvent être utilisés sans autre personnalisation. Toutefois, il est recommandé de consulter chaque modèle et d’apporter les modifications nécessaires avant de les envoyer aux clients.

- [Modèle d’en-tête](email-template-custom.md#header-template)
- [Modèle de pied de page](email-template-custom.md#footer-template)
- [Modèles de message](email-template-custom.md#message-templates)

![Modèles d&#39;email](./assets/email-templates.png){width="700" zoomable="yes"}

## Informations sur les modèles

| Champ | Description |
| ----- | ----------- |
| [!UICONTROL Template Name] | Nom de votre modèle personnalisé. |
| [!UICONTROL Insert Variable] | Insère une variable dans le modèle à l’emplacement du curseur. |
| [!UICONTROL Template Subject] | L’ objet du modèle apparaît dans la colonne Objet. Il peut être utilisé pour trier et filtrer les modèles de la liste. |
| [!UICONTROL Template Content] | Contenu du modèle en HTML. |
| [!UICONTROL Template Styles] | Toutes les déclarations de style CSS nécessaires au format du modèle peuvent être saisies dans la variable _[!UICONTROL Template Styles]_de la boîte. |

{style="table-layout:auto"}

## Modèle d’en-tête

Après avoir terminé la [configuration](email-templates.md#configure-email-templates), le modèle d’en-tête d’email comprend votre logo associé à votre boutique. Si vous avez une connaissance de base du HTML, vous pouvez facilement utiliser [variables prédéfinies](variables-predefined.md) pour ajouter les coordonnées du magasin à l’en-tête .

### Étape 1. Chargement du modèle par défaut

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Dans le **[!UICONTROL Load default template]** , cliquez sur le bouton **[!UICONTROL Template]** sélecteur et choisissez `Magento_Email` > `Header`.

   ![En-tête de modèle de courrier électronique - modèle de chargement par défaut](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Load Template]**.

   Le code de HTML et les variables du modèle apparaissent dans le formulaire.

### Étape 2. Personnaliser le modèle

1. Saisissez le **[!UICONTROL Template Name]** pour votre en-tête personnalisé.

1. Saisissez un **[!UICONTROL Template Subject]** pour organiser les modèles.

   Dans la grille, la liste des modèles peut être triée et filtrée par le _[!UICONTROL Subject]_colonne .

   ![Informations d’en-tête du modèle de courrier électronique](./assets/email-template-information.png){width="600" zoomable="yes"}

1. Dans le **[!UICONTROL Template Content]** , modifiez le HTML suivant vos besoins.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas écraser les éléments placés entre deux accolades.

1. Pour insérer une [variable](variables-reference.md), placez le curseur dans le code à l’endroit où vous souhaitez placer la variable, puis cliquez sur **[!UICONTROL Insert Variable]**.

1. Sélectionnez la variable à insérer.

   ![Modèle d’en-tête - Insérer une variable](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Lorsqu’une variable est sélectionnée, une [balise marketing](markup-tags.md) pour la variable est insérée dans le code.

   Bien que les variables Store Email Address soient les plus souvent incluses dans l’en-tête, vous pouvez saisir le code de n’importe quel système ou [variable personnalisée](variables-custom.md) directement dans le modèle.

1. Si vous devez faire des déclarations CSS, saisissez les styles dans la variable **[!UICONTROL Template Styles]** de la boîte.

1. Lorsque vous êtes prêt à réviser votre travail, cliquez sur **[!UICONTROL Preview Template]**.

   Apportez les modifications nécessaires au modèle.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Template]**.

   Votre en-tête personnalisé apparaît désormais dans la liste des modèles de courrier électronique disponibles.

### Étape 3. Mise à jour de la configuration

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Transactional Emails]** .

1. Choisissez la **[!UICONTROL Header Template]** qui est utilisé par défaut pour les notifications par e-mail.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

![Configuration de la conception d’email transactionnel - modèle d’en-tête](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modèle de pied de page

Le pied de page du modèle d’email contient la ligne de fermeture et de signature du message. Vous pouvez modifier la fermeture pour l’adapter à votre style et ajouter des informations supplémentaires, telles que le nom et l’adresse de la société sous votre nom.

### Étape 1. Chargement du modèle par défaut

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

1. Dans le **[!UICONTROL Load default template]** , cliquez sur le bouton **[!UICONTROL Template]** sélecteur et choisissez `Magento_Email` > `Footer`.

1. Cliquez sur **[!UICONTROL Load Template]**.

   Le code de HTML et les variables du modèle apparaissent dans le formulaire.

### Étape 2. Personnaliser et prévisualiser le modèle

1. Saisissez le **[!UICONTROL Template Name]** pour votre pied de page personnalisé.

1. Saisissez un **[!UICONTROL Template Subject]** pour organiser les modèles.

   Dans la grille, les modèles peuvent être triés et filtrés par le _[!UICONTROL Subject]_colonne .

   ![Pied de page de modèle de courrier électronique - informations](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. Dans le **[!UICONTROL Template Content]** , modifiez le HTML suivant vos besoins.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas écraser les éléments placés entre deux accolades.

1. Pour insérer une [variable](variables-reference.md), placez le curseur dans le code à l’endroit où vous souhaitez placer la variable, puis cliquez sur **[!UICONTROL Insert Variable]**.

1. Sélectionnez la variable à insérer.

   Lorsqu’une variable est sélectionnée, une [balise marketing](markup-tags.md) pour la variable est insérée dans le code.

   Bien que les variables Contact boutique soient les plus souvent incluses dans le pied de page, vous pouvez saisir le code de n’importe quel système ou [variable personnalisée](variables-custom.md) directement dans le modèle.

1. Si vous devez faire des déclarations CSS, saisissez les styles dans la variable **[!UICONTROL Template Styles]** de la boîte.

### Étape 3. Mise à jour de la configuration

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Transactional Emails]** .

1. Choisissez la **[!UICONTROL Footer Template]** qui est utilisé comme pied de page par défaut dans les notifications par e-mail.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

![Configuration de la conception d’email transactionnel - modèle de pied de page](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modèles de message

La personnalisation du corps de chaque message est identique à celle de l&#39;en-tête ou du pied de page. La seule différence est le modèle de message pour chaque activité ou événement qui déclenche une notification. Vous pouvez utiliser les modèles tels quels ou les personnaliser pour qu’ils correspondent à votre voix et à votre marque. Outre le texte du modèle, il existe un large choix de [prédéfini](variables-predefined.md) et [custom](variables-custom.md) que vous pouvez créer et incorporer dans le modèle.

### Étape 1. Chargement du modèle par défaut

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Cliquez sur **[!UICONTROL Add New Template]**.

   ![Modèles de courrier électronique - modèle de chargement par défaut](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Procédez comme suit :

   - Sous **[!UICONTROL Load default template]**, choisissez la variable **[!UICONTROL Template]** que vous souhaitez personnaliser.

   - Cliquez sur **[!UICONTROL Load Template]**.

### Étape 2. Personnaliser le modèle

1. Pour **[!UICONTROL Template Name]**, saisissez un nom pour votre modèle personnalisé.

1. Si nécessaire, modifiez la variable **[!UICONTROL Template Subject]**.

   Il s’agit de la première ligne du message, qui est la formule de salutation par défaut. Vous pouvez la laisser telle quelle ou saisir quelque chose de plus explicite.

1. Prenez note de la **[!UICONTROL Currently Used For]** chemin d’accès au modèle, qui est le chemin d’accès utilisé pour mettre à jour la configuration.

   ![Modèles d’email - Informations sur les modèles](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. Dans le **[!UICONTROL Template Content]** , modifiez le HTML suivant vos besoins.

   Le contenu se compose d’une combinaison de balises de HTML, de directives CSS, de variables et de texte.

   >[!NOTE]
   >
   >Lorsque vous travaillez dans le code du modèle, veillez à ne pas taper accidentellement le code encadré de doubles accolades.

1. Pour insérer une variable, placez le curseur dans le code à l’endroit où la variable doit apparaître.

   La sélection de variables varie en fonction du modèle et inclut les [prédéfini](variables-predefined.md) et [custom](variables-custom.md) , le cas échéant.

1. Cliquez sur **[!UICONTROL Insert Variable]** et choisissez la variable à insérer.

   Une commande permettant d’insérer la variable est placée entre accolades et ajoutée au code à l’emplacement du curseur. Par exemple :

   `customVar code=my_custom_variable`

1. Pour effectuer des déclarations CSS, saisissez les styles dans **[!UICONTROL Template Styles]**.

   ![Modèles de courrier électronique - ajouter des styles personnalisés](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Les styles personnalisés ne sont appliqués à l&#39;email que si `{{template config_path="design/email/header_template"}}` est présent dans la variable _[!UICONTROL Template Styles]_. Pour utiliser une page CSS personnalisée sans modèle d’en-tête par défaut, vous devez les fournir ici dans la `<style>` Balise de HTML.

### Étape 3. Mise à jour de la configuration

La variable _[!UICONTROL Currently Used For]_Le cheminement de navigation indique l’emplacement d’utilisation du modèle. Dans cet exemple, la configuration du modèle se trouve sur la page_[!UICONTROL Customer Configuration]_ , dans la variable _[!UICONTROL Create New Account Options]_et dans la section_[!UICONTROL Default Welcome Email]_ champ .

- Page - [!UICONTROL Customer Configuration]
- Section - [!UICONTROL Create New Account Options]
- Field - [!UICONTROL Default Welcome Email]

1. Dans le **[!UICONTROL Currently Used For]** dans le cheminement de navigation, cliquez sur le lien pour ouvrir la page de configuration du modèle.

   ![Modèle de courrier électronique actuel](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) recherchez la section et le champ du modèle d’email que vous avez personnalisé.

1. Effacez la variable **[!UICONTROL Use system value]** et cliquez sur le nom de votre modèle personnalisé.

   ![Configuration des clients - modèle d’email de bienvenue par défaut](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Dans le message situé en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et effacez tout cache non valide.

### Étape 4. Prévisualiser et enregistrer le modèle

1. Lorsque vous êtes prêt à réviser votre travail, cliquez sur **[!UICONTROL Preview Template]**.

1. Mettez le modèle à jour selon vos besoins.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Template]**.

   Votre modèle personnalisé est désormais disponible dans la liste des modèles d’email.
