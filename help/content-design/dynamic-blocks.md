---
title: Blocs dynamiques
description: Utilisez des blocs dynamiques pour créer du contenu riche et interactif qui est piloté par la logique des règles de prix et des segments de clientèle.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Blocs dynamiques

{{ee-feature}}

Créez du contenu riche et interactif piloté par une logique issue des [règles de prix](../merchandising-promotions/introduction.md#price-rules) et [segments clients](../customers/customer-segments.md). Les [blocs dynamiques](../page-builder/dynamic-block.md) existants peuvent être ajoutés directement à la [!DNL Page Builder] [étape](../page-builder/workspace.md). Pour obtenir un exemple détaillé et détaillé de l’utilisation de blocs dynamiques, consultez [Tutoriel 2 : blocs](../page-builder/2-blocks.md).

>[!NOTE]
>
>L’option _[!UICONTROL Banner]_du menu [[!UICONTROL Content] ](content-menu.md) a été abandonnée dans la version 2.3.1 et supprimée dans la version 2.4.0. Sa fonctionnalité est remplacée par Blocs dynamiques.

![[!DNL Page Builder] - bloc dynamique avec règle de prix et segment client](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Étape 1 : créer un bloc dynamique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Liste Blocs dynamiques](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Dynamic Block]**.

   ![Nouveau bloc dynamique](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Le cas échéant, définissez **[!UICONTROL Store View]** sur une vue de magasin spécifique où le bloc dynamique doit apparaître.

1. Pour activer le bloc dynamique, définissez **[!UICONTROL Enable Dynamic Block]** sur `Yes`.

1. Pour référence interne, saisissez un **[!UICONTROL Dynamic Block Name]** descriptif.

1. Définissez **[!UICONTROL Dynamic Block Type]** sur la zone de la page où vous souhaitez que le bloc dynamique apparaisse, puis cliquez sur **[!UICONTROL Done]**.

   ![Définition du type de bloc dynamique](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. Dans la liste **[!UICONTROL Customer Segment]**, cochez la case de chaque segment pour lequel vous souhaitez afficher le bloc dynamique, puis cliquez sur **[!UICONTROL Done]** pour enregistrer le paramètre.

   ![Choix d’un segment client](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Si aucun segment n’est créé, le bloc dynamique est visible par tous.
   >- Si le client n’appartient à aucun segment et que le bloc dynamique est créé pour tous les segments, le contenu du bloc dynamique reste affiché.
   >- Si tous les segments de clients affectés à un bloc dynamique sont supprimés, leur contenu est alors visible par tous.

### Utilisation des audiences Real-Time CDP dans les blocs dynamiques

Si vous [installé](../customers/audience-activation.md#install-the-extension) et [configuré](../customers/audience-activation.md#configure-the-extension) l’extension [!DNL Audience Activation], une section appelée **[!UICONTROL Audiences]** s’affiche.

![Choisir une audience Real-Time CDP](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

Dans la liste **[!UICONTROL Real-Time CDP Audience]**, cochez la case de chaque audience pour laquelle vous souhaitez afficher le bloc dynamique, puis cliquez sur **[!UICONTROL Done]** pour enregistrer le paramètre.

## Étape 2 : terminer le contenu

Utilisez l’[!DNL Page Builder] [espace de travail](../page-builder/workspace.md) pour terminer le contenu.

![[!DNL Page Builder] - espace de travail de bloc dynamique](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Étape 3 : choisir une promotion associée

1. Faites défiler vers le bas et développez le **[!UICONTROL Related Promotions]** ![Sélecteur d’extension](../assets/icon-display-expand.png).

1. Cliquez sur le type de promotion à associer au bloc dynamique :

   - **[!UICONTROL Add Cart Price Rules]** (voir [Règles de prix du panier](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (voir [Règles de prix de catalogue](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Les règles de prix de catalogue ne sont pas prises en charge pour les audiences Real-Time CDP.

1. Dans la liste des règles disponibles, cochez la case de chaque règle que vous souhaitez utiliser, puis cliquez sur **[!UICONTROL Add Selected]**.

1. Une fois le bloc dynamique terminé, cliquez sur **[!UICONTROL Save]**.

## Étape 4 : ajouter le bloc dynamique à une page

1. Ouvrez la page sur laquelle vous souhaitez que le bloc dynamique apparaisse.

1. Utilisez le type de contenu [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) pour ajouter le bloc dynamique à l’étape.

## Descriptions des champs et des outils

| Champ | Description |
|--- |--- |
| [!UICONTROL Store View] | Spécifie les vues du magasin où le bloc dynamique doit être disponible. |
| [!UICONTROL Enable Dynamic Block] | Active ou désactive le bloc dynamique. Options : Oui / Non |
| [!UICONTROL Dynamic Block Name] | Nom descriptif qui identifie le bloc dynamique dans l’Administration. |
| [!UICONTROL Dynamic Block Type] | Identifie l’emplacement du bloc dynamique dans la [mise en page standard](layout-updates.md). Options : <br/>**[!UICONTROL Content Area]**- place le bloc dynamique dans la zone de [ principale de la page](layout-updates.md)<br/>**[!UICONTROL Footer]** - Place le bloc dynamique dans le [pied de page](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Place le bloc dynamique dans l’en-tête [de la page](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Place le bloc dynamique dans la barre latérale [gauche](page-layout.md#standard-page-layouts) d’une disposition à deux ou trois colonnes. <br/>**[!UICONTROL Right Column]**- Place le bloc dynamique dans la [barre latérale droite](page-layout.md#standard-page-layouts) d’une disposition à deux ou trois colonnes. |
| Segment client | Associe un segment client au bloc dynamique pour déterminer quels clients peuvent le voir. |
| Audience Real-Time CDP | Associe une audience [Real-Time CDP](../customers/audience-activation.md) au bloc dynamique pour déterminer quels clients peuvent la voir. |

{style="table-layout:auto"}

### Contenus

| Champ | Description |
|--- |--- |
| [!UICONTROL Layout] | Ajoutez des lignes, des colonnes ou des onglets à l’étape. |
| [!UICONTROL Elements] | Ajoutez du texte, des en-têtes, des boutons, des séparateurs et du code HTML à n’importe quel conteneur de mises en page sur la scène. |
| [!UICONTROL Media] | Ajoutez des images, des vidéos, des bannières, des curseurs et des cartes Google à n’importe quel conteneur de mises en page existant sur la scène. |
| [!UICONTROL Add Content] | Ajoutez des blocs existants, des blocs dynamiques et des produits à l’étape. |

{style="table-layout:auto"}

### Promotions connexes

| Champ | Description |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Associez une règle de prix de panier [ existante](../merchandising-promotions/price-rules-cart.md) au bloc dynamique en tant que promotion. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Associez une [règle de prix de catalogue](../merchandising-promotions/price-rules-catalog.md) existante au bloc dynamique en tant que promotion. |

{style="table-layout:auto"}
