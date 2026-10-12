---
title: Présentation visuelle du marchandiseur
description: Découvrez les outils de marchandisage visuel qui vous permettent de positionner des produits et de déterminer les produits qui apparaissent dans la liste des catégories.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: 'https://experienceleague.adobe.com/MbeCfIBdepAr5U2B1I-lfFGNm1b5DiKGevM5365brpo'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---
# Marchandiseur visuel

{{ee-feature}}

Le _Marchandiseur visuel_ est un ensemble d’outils avancés qui vous permet de positionner des produits et d’appliquer des conditions qui déterminent quels produits apparaissent dans la liste des catégories. Le résultat peut être une sélection dynamique de produits qui s’adapte aux modifications du catalogue. Vous pouvez travailler en _mode visuel_, qui affiche chaque produit sous la forme d’une mosaïque sur une grille, ou à partir d’une liste de produits de la catégorie. Les mêmes outils sont disponibles dans chaque mode et vous pouvez utiliser les boutons situés dans le coin supérieur droit pour basculer entre chaque type d’affichage.

![Produits de catégorie en mode mosaïque](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Accéder au marchandiseur visuel

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Parcourez l’arborescence des catégories et cliquez sur la catégorie à modifier.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Products in Category]** .

1. Cliquez sur le bouton _Afficher sous forme de mosaïque_ ( ![Afficher sous forme de mosaïque](../assets/icon-view-tiles.png) ) pour afficher les produits sous forme de grille.

1. Cliquez ensuite sur **[!UICONTROL Save Category]**.

## Modifier la position d’un produit

1. Utilisez l’[ordre de tri](../catalog/navigation-product-listings.md) pour afficher le produit à déplacer.

   - **Méthode 1 : glisser-déposer**

     Saisissez la commande _Faire glisser_ (![Faire glisser l’icône](../assets/icon-move.png)) dans le coin supérieur droit de la mosaïque du produit et déposez le produit en position. Le numéro de chaque produit s’ajuste pour refléter la nouvelle position.

   - **Méthode 2 : Définir la valeur de la position**

     Dans le contrôleur _Position_ (![champ Position](../assets/control-position.png)) de la mosaïque du produit, saisissez le numéro où vous souhaitez que le produit apparaisse. Saisissez `0` pour placer le produit en haut de la liste.

1. Cliquez ensuite sur **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Dans une installation propre, Adobe Commerce réserve l’ID de catégorie `2` au catalogue racine du magasin par défaut. Visual Merchandiser ne peut utiliser que des catégories dont le numéro d’ID est supérieur ou égal à `3`.

## Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| ![Icône Afficher la liste](../assets/icon-view-list.png) | Afficher comme liste |
| ![Icône Afficher en tant que mosaïques](../assets/icon-view-tiles.png) | Afficher sous forme de mosaïque |
| ![Bouton bascule Correspondance par règle - non](../assets/toggle-no.png) | Correspondance par règle - non |
| ![Bouton bascule Correspondance par règle - oui](../assets/toggle-yes.png) | Correspondance par règle - oui |
| ![ Icône Déplacer ](../assets/icon-move.png) | Faire glisser |
| ![Contrôleur de position](../assets/control-position.png) | Position |
| ![Icône Supprimer de la catégorie](../assets/icon-delete-x.png) | Supprimer de la catégorie |
| ![Éléments par contrôle de page](../assets/control-items-per-page.png) | Afficher par page |
| ![Modifier l’affichage de la page](../assets/control-page-display.png) | Aller au suivant/précédent |

{style="table-layout:auto"}
