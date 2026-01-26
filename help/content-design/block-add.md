---
title: Ajouter des blocs de contenu
description: Créez des blocs de contenu personnalisés que vous pouvez réutiliser dans n’importe quelle page ou dans un autre bloc.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Ajouter des blocs de contenu

Vous pouvez créer des blocs de contenu personnalisés, puis les ajouter à n’importe quelle page, groupe de pages ou même à un autre bloc. Par exemple, vous pouvez placer un curseur d’image dans un bloc, puis placer le bloc sur la page d’accueil. L’espace de travail Blocs utilise les mêmes [commandes de base](pages-workspace.md) que l’espace de travail _Pages_ pour vous aider à trouver les blocs disponibles et à effectuer des opérations de maintenance de routine. Une fois le bloc terminé, vous pouvez utiliser l’outil [Widget](widget-static-block.md) pour le placer sur des pages spécifiques de votre boutique.

![La page Blocs affiche une grille de blocs existants](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Création d’un bloc

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **Ajouter un nouveau bloc**.

   ![La page Nouveau bloc affiche des options et un espace de contenu](./assets/block-detail.png){width="500" zoomable="yes"}

1. Si vous souhaitez modifier l’état du nouveau bloc activé par défaut, définissez **Activer le bloc** sur `No`.

1. Attribuez un **Titre du bloc** pour référence interne.

1. Attribuez un **Identifiant** unique au bloc.

   Utilisez tous les caractères minuscules avec des traits de soulignement au lieu d’espaces.

1. Sélectionnez chaque **[!UICONTROL Store View]** où vous souhaitez que le bloc soit disponible.

1. Ajoutez le contenu du bloc à l’aide de l’ensemble d’outils de contenu affiché :

   - Si [Page Builder](../page-builder/introduction.md) est activé, sélectionnez **[!UICONTROL Edit with Page Builder]** pour utiliser les outils de Page Builder dans l’espace de travail [&#x200B; contenu](../page-builder/workspace.md).

     ![Espace de travail de Page Builder](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Pour plus d’informations sur l’ajout de blocs avec Page Builder, consultez [Tutoriel 2 : blocs](../page-builder/2-blocks.md).

   - Utilisez l’[éditeur](editor.md) pour mettre en forme le texte, créer des liens et ajouter des tableaux, des images, des vidéos et de l’audio.

     Si vous préférez travailler avec le code HTML, cliquez sur **Afficher / Masquer l’éditeur**.

     ![Éditeur de blocs (masqué)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

   Le nouveau bloc s’affiche au bas de la liste dans la grille Blocs .

1. Utilisez l’outil [Widget](widget-static-block.md) pour placer le bloc terminé sur une page spécifique de votre boutique.

## Suppression d’un bloc

Il existe deux manières de supprimer un bloc personnalisé. Vous pouvez le supprimer de la grille _Blocs_ ou de la page Modifier le bloc.

### Méthode 1 : supprimer un bloc de la grille Blocs

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Localisez les blocs à l’aide de filtres au-dessus de la grille et cochez la case d’un ou de plusieurs blocs à supprimer.
1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.
1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Méthode 2 : supprimer un bloc de la page d’édition

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Recherchez le bloc à supprimer.
1. Dans la colonne _Actions_ du bloc, cliquez sur **[!UICONTROL Select]** et choisissez **[!UICONTROL Edit]**.
1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete Block]**.
1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Enregistrer le menu

| Commande | Description |
|----------|----------- |
| [!UICONTROL Save] | Enregistrez le bloc actif et continuez à travailler. |
| [!UICONTROL Save & Duplicate] | Enregistrez et fermez le bloc actif, puis ouvrez un nouveau doublon. |
| [!UICONTROL Save & Close] | Enregistrez et fermez le bloc actif, puis revenez à la grille Blocs . |

{style="table-layout:auto"}

## Ajouter un lightbox ou un curseur

- Il est facile d’ajouter un [curseur](../page-builder/slider.md) à votre boutique avec [[!DNL Page Builder]](../page-builder/introduction.md). Le curseur peut être défini pour une lecture automatique ou contrôlé manuellement à l’aide des boutons de navigation.

  ![curseur du générateur de page](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Il existe également un large éventail de lightbox basés sur jQuery disponibles sur [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions.html?q=lightbox), et certains sont gratuits.

- Vous pouvez également télécharger une extension à partir de [!DNL Commerce Marketplace]. Pour obtenir de l’aide supplémentaire, consultez la documentation fournie par le développeur d’extensions.
