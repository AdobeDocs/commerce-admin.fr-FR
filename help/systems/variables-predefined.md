---
title: Utiliser des variables prédéfinies
description: Découvrez les variables prédéfinies et comment les ajouter dans un modèle d'email.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Utiliser des variables prédéfinies

Les variables [prédéfinies](variables-predefined.md) facilitent la personnalisation des modèles [email](email-templates.md) et [newsletter](../merchandising-promotions/newsletters.md) et d’autres types de contenu. La liste des variables [prédéfinies](variables-predefined.md) autorisées s’affiche lorsque vous cliquez sur le bouton Insérer une variable . Comme illustré ci-dessous, la liste des variables disponibles pour un modèle d’email spécifique est déterminée par les données associées au modèle. Consultez la [référence de variable](variables-reference.md) pour obtenir la liste des modèles d’email fréquemment utilisés et de leurs variables associées.

![Variables prédéfinies pour le modèle de courrier électronique](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Ajout d’une variable à un modèle de courrier électronique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Effectuez l’une des opérations suivantes :

   - Pour ajouter la variable à un modèle existant, cliquez sur le modèle de la liste pour l’ouvrir en mode d’édition.

   - Pour utiliser la variable dans un nouveau modèle, cliquez sur **[!UICONTROL Add New Template]** et personnalisez le code de modèle par défaut. Voir [Modèles de message](email-template-custom.md#message-templates).

1. Sous _[!UICONTROL Load default template]_, sélectionnez le **[!UICONTROL Template]**que vous souhaitez personnaliser.

1. Pour appliquer un modèle, cliquez sur **[!UICONTROL Load Template]**.

   Le champ _[!UICONTROL Currently used for]_affiche le chemin de configuration du modèle. Les_[!UICONTROL Template Subject]_ et _[!UICONTROL Template Content]_sont automatiquement générés par rapport au modèle sélectionné.

   - **[!UICONTROL Template Subject]** - Ce texte s’affiche dans l’objet d’un email.

   - **[!UICONTROL Template Content]** - Ce texte s’affiche dans le contenu complet de l’email envoyé.

   ![Contenu du modèle de courrier électronique](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Template Name]**.

1. Pour obtenir la liste des variables [prédéfinies](variables-predefined.md) pouvant être utilisées avec ce modèle d’email, cliquez sur **[!UICONTROL Insert Variable]**.

   Déterminez la variable que vous souhaitez insérer dans le modèle. Cliquez ensuite sur _Fermer_ (X) dans le coin supérieur droit. (Vous y reviendrez ultérieurement.)

1. Pour afficher une maquette du modèle, cliquez sur **[!UICONTROL Preview Template]** dans la barre de boutons.

   Lorsque l’aperçu s’ouvre dans un nouvel onglet, déterminez où vous souhaitez placer la variable par rapport à l’autre contenu. Revenez ensuite à l’onglet d’origine pour continuer.

   ![Modèle d’aperçu](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Template Content]**, positionnez le point d’insertion à l’endroit où vous souhaitez que la variable apparaisse, puis cliquez sur **[!UICONTROL Insert Variable...]**.

1. Dans la liste des variables disponibles, cliquez sur celle que vous souhaitez insérer dans le modèle.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Template]**.

## Convertir le modèle en texte brut

1. Ouvrez un modèle en mode d’édition.

1. En haut de la page, cliquez sur **[!UICONTROL Convert to Plain Text]**.

1. Lorsque vous êtes invité à supprimer des balises, cliquez sur **[!UICONTROL OK]**.

1. Pour enregistrer la version en texte brut, cliquez sur **[!UICONTROL Save Template]**.

## Restaurer la version de l’HTML

1. En haut de la page, cliquez sur **[!UICONTROL Return HTML Version]**.

1. Pour enregistrer la version HTML du modèle, cliquez sur **[!UICONTROL Save Template]**.
