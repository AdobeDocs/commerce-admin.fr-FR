---
title: Ajouter des variables personnalisées
description: Découvrez comment créer des variables personnalisées et les insérer dans des pages, des blocs et du contenu de produit.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: 'https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
subfeature_v2:
  - id: 2191e157-828a-5358-ad69-ebcaa8402915
    internal-label: Variables
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 1%
---
# Ajouter des variables personnalisées

Pour répondre aux besoins spécifiques de votre entreprise, vous pouvez créer des variables personnalisées et les insérer dans des [pages](../content-design/pages.md), [blocs](../content-design/blocks.md) et [modèles d’e-mail](email-templates.md). La liste des variables autorisées qui s’affiche lorsque vous cliquez sur le bouton _Insérer une variable_ comprend à la fois des variables [prédéfinies](variables-predefined.md) et des variables personnalisées. La liste des variables disponibles pour un modèle d’e-mail spécifique est déterminée par les données associées au modèle. Consultez la [Référence de variable](variables-reference.md) pour obtenir une liste des modèles d’e-mail fréquemment utilisés et des variables associées.

![Variables personnalisées ](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Seules les variables prédéfinies ou personnalisées autorisées peuvent être utilisées dans les modèles d’e-mail et de newsletter.

## Étape 1 : créer une variable personnalisée

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Cliquez sur **[!UICONTROL Add New Variable]**.

1. Saisissez un identifiant pour **[!UICONTROL Variable Code]**, en utilisant uniquement des caractères minuscules sans espaces.

   Si nécessaire, vous pouvez utiliser un caractère de soulignement ou un trait d’union pour représenter un espace. Par exemple : `my_custom_variable`

1. Saisissez un **[!UICONTROL Variable Name]**, qui est utilisé comme référence interne. Par exemple : `My Custom Variable`

1. Pour saisir la valeur associée à la variable, effectuez l’une des opérations suivantes :

   - Par **[!UICONTROL Variable HTML Value]**, saisissez la valeur de la variable au format avec de simples balises HTML. Par exemple :

     `<b>This formatted content appears in place of the variable.</b>`

   - Par **[!UICONTROL Variable Plain Value]**, saisissez la valeur de la variable en tant que texte brut sans mise en forme. Par exemple :

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Si vous avez besoin de plus d’espace, faites glisser le coin inférieur droit de la zone de texte.

   ![Nouvelle variable personnalisée ](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Étape 2 : insérer la variable personnalisée dans votre contenu

Utilisez [!DNL Page Builder] pour insérer une variable personnalisée.

1. Ouvrez la page, le bloc, la catégorie ou le produit où vous souhaitez ajouter la variable au contenu.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

1. Cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL Elements]** et effectuez l’une des opérations suivantes :

   - Cliquez dans une zone de texte existante où vous souhaitez insérer la variable.

   - Faites glisser un nouvel objet **[!UICONTROL Text]** vers la scène.

1. À l’extrême droite de la barre d’outils de l’éditeur, cliquez sur ( ![Insérer une variable](./assets/editor-btn-insert-variable.png) ) pour insérer une variable.

   ![[!DNL Page Builder] l’étape et le panneau](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. Dans la liste, sélectionnez la variable personnalisée à insérer, puis cliquez sur **[!UICONTROL Insert Variable]**.

   ![Nouvelle variable personnalisée ](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   L’identifiant de variable apparaît comme espace réservé dans l’éditeur.

   ![[!DNL Page Builder] stage - espace réservé variable](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.
