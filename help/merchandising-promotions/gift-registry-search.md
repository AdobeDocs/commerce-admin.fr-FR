---
title: Ajouter une recherche de registre des cadeaux
description: Découvrez comment placer une boîte de recherche de registre des cadeaux pour aider les visiteurs de la boutique à acheter des produits auprès des registres des clients.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Ajouter une recherche de registre des cadeaux

{{ee-feature}}

L’outil [Widget](../content-design/widgets.md) peut être utilisé pour placer une zone de recherche dans le registre des cadeaux presque n’importe où dans votre boutique. Vous pouvez spécifier les options de recherche qui seront disponibles pour les clients, telles que le nom, l’adresse électronique et l’identifiant du registre des cadeaux. Lorsque le client clique sur le bouton de recherche, les résultats s’affichent sur la page de recherche du registre des cadeaux. Si la recherche ne renvoie aucun résultat, le client peut réessayer avec d’autres paramètres.

![Exemple de vitrine - recherche de registre des cadeaux](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Configuration de la recherche dans le registre des cadeaux

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Sélectionnez l’onglet **[!UICONTROL Settings]** et procédez comme suit :

   - Définissez **[!UICONTROL Type]** sur `Gift Registry Search`.

   - Définissez **[!UICONTROL Design Theme]** sur le thème utilisé par le magasin.

   - Cliquez sur **[!UICONTROL Continue]**.

   ![Registre cadeau - paramètres de recherche](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Saisissez un **[!UICONTROL Widget Title]** pour référence interne.

   - Définissez **[!UICONTROL Assign to Store Views]** sur les vues de magasin où la recherche du registre des cadeaux doit être disponible.

   - Définissez **[!UICONTROL Sort Order]** pour déterminer l’ordre dans lequel le bloc de recherche du registre des cadeaux s’affiche lorsque d’autres blocs sont affectés au même emplacement sur la page.

   ![Registre cadeau - propriétés storefront](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. Dans la section **[!UICONTROL Layout Updates]**, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Pour déterminer où la recherche du registre des cadeaux apparaît dans le magasin, procédez comme suit :

   - Définissez **[!UICONTROL Display On]** sur les pages de votre magasin où vous souhaitez que le bloc de recherche du registre des cadeaux s’affiche.

   - Le cas échéant, choisissez l’ **[!UICONTROL Categories]** où vous souhaitez qu’il apparaisse.

   - Définissez **[!UICONTROL Container]** sur l’emplacement de la page pour placer le bloc de recherche du registre des cadeaux.

   ![Registre cadeau - mises à jour de mise en page](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Pour déterminer comment les visiteurs de votre site peuvent rechercher des registres de cadeaux, sélectionnez autant de ceux qui s’appliquent :

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Registre cadeau - options de widget](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache de la page, cliquez sur le lien contenu dans le message situé en haut de l’espace de travail, puis suivez les instructions.

## Descriptions des champs

### [!UICONTROL Settings]

| Champ | Description |
|--- |--- |
| [!UICONTROL Type] | Identifie `Gift Registry Search` comme type de widget. |
| [!UICONTROL Design Theme] | Thème utilisé par le magasin où doit apparaître la recherche du registre des cadeaux. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Champ | Description |
|--- |--- |
| [!UICONTROL Widget Title] | Nom de référence interne. |
| [!UICONTROL Assign to Store Views] | Identifie les vues du magasin où la recherche du registre des cadeaux doit être disponible. |
| [!UICONTROL Sort Order] | Indique l’ordre dans lequel le bloc de recherche du registre des cadeaux s’affiche si d’autres blocs sont affectés pour apparaître au même emplacement. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Champ | Description |
|--- |--- |
| [!UICONTROL Display On] | Indiquez les pages ou les types de pages spécifiques dans lesquels le bloc de recherche du registre des cadeaux s’affiche. |
| [!UICONTROL Categories] | Le cas échéant, identifie les pages de catégorie dans lesquelles la recherche du registre des cadeaux s’affiche. |
| [!UICONTROL Container] | Indique le bloc de mise en page dans lequel la recherche du registre des cadeaux est placée. Les options varient selon le modèle et le thème. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Champ | Description |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Détermine les types de recherches pouvant être effectués avec la recherche du registre des cadeaux. Options : `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
