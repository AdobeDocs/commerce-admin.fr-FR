---
title: Ajouter des blocs de contenu
description: Créez des blocs de contenu personnalisés que vous pouvez réutiliser dans n’importe quelle page ou dans un autre bloc.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Ajouter des blocs de contenu

Il est possible de créer des blocs de contenu personnalisés, puis de les ajouter à n’importe quelle page, groupe de pages ou même à un autre bloc. Par exemple, vous pouvez placer un curseur d’image dans un bloc, puis placer le bloc sur la page d’accueil. L’espace de travail Blocs utilise le même [contrôles de base](pages-workspace.md) comme la propriété _Pages_ workspace pour vous aider à trouver les blocs disponibles et à effectuer une maintenance de routine. Une fois le bloc terminé, vous pouvez utiliser la variable [Widget](widget-static-block.md) pour le placer sur des pages spécifiques de votre magasin.

![La page Blocs affiche une grille de blocs existants](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Création d’un bloc

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **Ajouter un nouveau bloc**.

   ![La page Nouveau bloc affiche des options et un espace de contenu.](./assets/block-detail.png){width="500" zoomable="yes"}

1. Si vous souhaitez modifier l’état activé par défaut du nouveau bloc, définissez **Activer le bloc** to `No`.

1. Attribuer une **Titre du bloc** pour référence interne.

1. Attribution d’une **Identifiant** pour le bloc.

   Utilisez tous les caractères minuscules avec des traits de soulignement au lieu d’espaces.

1. Sélectionner chaque **[!UICONTROL Store View]** où le bloc doit être disponible.

1. Ajoutez le contenu du bloc à l&#39;aide de l&#39;ensemble d&#39;outils de contenu affiché :

   - If [Page Builder](../page-builder/introduction.md) est activé, sélectionnez **[!UICONTROL Edit with Page Builder]** pour utiliser les outils du Créateur de pages dans le contenu [workspace](../page-builder/workspace.md).

     ![Espace de travail du créateur de pages](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Pour plus d’informations sur l’ajout de blocs à l’aide du générateur de pages, voir [Tutoriel 2 : Blocs](../page-builder/2-blocks.md).

   - Utilisez la variable [éditeur](editor.md) pour mettre en forme du texte, créer des liens et ajouter des tableaux, des images, de la vidéo et du contenu audio.

     Si vous préférez utiliser du code HTML, cliquez sur **Afficher/masquer l’éditeur**.

     ![Éditeur de blocs (masqué)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur le **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

   Le nouveau bloc apparaît au bas de la liste dans la grille Blocs .

1. Utilisez la variable [Widget](widget-static-block.md) pour placer le bloc renseigné sur une page spécifique de votre magasin.

## Suppression d’un bloc

Il existe deux manières de supprimer un bloc personnalisé. Vous pouvez la supprimer de la _Blocs_ ou à partir de la page de modification de bloc.

### Méthode 1 : supprimer un bloc de la grille Blocs

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Localisez les blocs à l&#39;aide de filtres au-dessus de la grille et cochez la case correspondant à un ou plusieurs blocs à supprimer.
1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** to `Delete`.
1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Méthode 2 : supprimer un bloc de la page de modification

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Recherchez le bloc à supprimer.
1. Dans le _Actions_ pour le bloc, cliquez sur **[!UICONTROL Select]** et choisissez **[!UICONTROL Edit]**.
1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete Block]**.
1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Menu Enregistrer

| Commande | Description |
|----------|----------- |
| [!UICONTROL Save] | Enregistrez le bloc actuel et continuez à travailler. |
| [!UICONTROL Save & Duplicate] | Enregistrez et fermez le bloc actuel, puis ouvrez une nouvelle copie en double. |
| [!UICONTROL Save & Close] | Enregistrez et fermez le bloc courant, puis revenez à la grille Blocs . |

{style="table-layout:auto"}

## Ajout d’un cadre lumineux ou d’un curseur

- Il est facile d’ajouter une [curseur](../page-builder/slider.md) à votre boutique avec [[!DNL Page Builder]](../page-builder/introduction.md). Le curseur peut être configuré pour une lecture automatique ou contrôlé manuellement à l’aide des boutons de navigation.

  ![Curseur du créateur de pages](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Il existe également un large éventail de Lightbox d’image basés sur jQuery disponibles sur [[!DNL Commerce Marketplace]][1]et certains sont libres.

- Vous pouvez également télécharger une extension depuis [!DNL Commerce Marketplace]. Pour obtenir une aide supplémentaire, consultez la documentation fournie par le développeur de l’extension.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
