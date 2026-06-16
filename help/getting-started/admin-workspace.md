---
title: Outils et espace de travail d’administration
description: Découvrez l’espace de travail d’administration, qui permet d’accéder à tous les outils, données et contenus utilisés pour exécuter votre boutique.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
TQID: https://experienceleague.adobe.com/RGT21TI5joLEYx3fiOErU5ZoIrXsq0nqZpnI8c40hz4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 528
ht-degree: 0%

---

# Outils et espace de travail d’administration

L’espace de travail d’administration permet d’accéder à tous les outils, données et contenus utilisés pour exécuter votre boutique. La page de démarrage par défaut peut être définie dans la configuration. De nombreuses pages d’administration comportent une grille qui répertorie les données de la section, avec un ensemble d’outils pour rechercher, trier, filtrer, sélectionner et appliquer des actions. Par défaut, le [Tableau de bord](admin-dashboard.md) est la page de démarrage de l’administrateur. Cependant, vous pouvez choisir n’importe quelle autre page à afficher comme page de démarrage lorsque vous vous connectez. Vous pouvez cliquer sur le logo dans la barre latérale d’administration pour revenir à la page de démarrage de l’administrateur.

![Administrateur - Espace de travail](./assets/admin-workspace.png){zoomable="yes"}

## Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Global Search] | L’icône de recherche en haut à droite peut être utilisée pour trouver n’importe quelle valeur dans la base de données, y compris les enregistrements de produit, de client ou de commande. |
| [!UICONTROL Grid Search] | La zone de recherche située au-dessus de la grille peut être utilisée pour filtrer rapidement l’affichage de la grille en fonction des mots-clés trouvés dans les enregistrements. |
| [!UICONTROL Sort] | L’en-tête de chaque colonne peut être utilisé pour trier la liste par ordre croissant ou décroissant. |
| [!UICONTROL Filters] | Définit un ensemble de paramètres de recherche qui déterminent les enregistrements qui apparaissent dans la grille. En outre, les filtres dans l’en-tête de certaines colonnes peuvent être utilisés pour limiter la liste à des valeurs spécifiques. Certains filtres comportent des options supplémentaires qui peuvent être sélectionnées à partir d’une zone de liste. |
| [!UICONTROL Default View] | Détermine la disposition de colonne par défaut de la grille. |
| [!UICONTROL Columns] | Détermine la sélection des [colonnes](admin-grid-controls.md) et leur ordre dans la grille. La disposition des colonnes peut être modifiée et enregistrée en tant que _vue_. Par défaut, seules certaines des colonnes sont incluses dans la grille. |
| [!UICONTROL Paginate] | Les commandes de pagination sont utilisées pour afficher les pages de résultats supplémentaires. |
| [!UICONTROL Actions] | Le contrôle Actions applique une opération à tous les enregistrements sélectionnés. |
| [!UICONTROL Select] | La commande Sélectionner permet de sélectionner plusieurs enregistrements qui doivent faire l&#39;objet d&#39;une action. Options : `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Recherche Workspace

Pour rechercher un enregistrement dans la base de données, utilisez l’icône en forme de loupe située dans l’en-tête de l’_Admin_. Les résultats peuvent inclure des clients, des produits, des commandes ou tout attribut associé. Par exemple, si vous saisissez un nom de client, les résultats peuvent inclure l&#39;enregistrement du client et toutes les commandes associées à ce nom.

![Outil de recherche d’administration](./assets/admin-search.png){width="700" zoomable="yes"}

1. Dans l’en-tête, cliquez sur l’icône _Rechercher_ (![loupe](../assets/icon-magnify-search.png)) pour ouvrir la zone de recherche.

1. Effectuez l’une des opérations suivantes :

   - Pour trouver une correspondance proche, saisissez les premières lettres de ce que vous souhaitez rechercher.
   - Pour rechercher une correspondance exacte, saisissez le ou les mots que vous souhaitez rechercher.

1. Dans les résultats de recherche affichés, cliquez sur un élément pour ouvrir l’enregistrement.

## Modification de la page de démarrage de l’administrateur

Le [tableau de bord](admin-workspace.md#the-dashboard) est la page de démarrage par défaut de l’administrateur, bien que vous puissiez configurer une autre page de démarrage.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, sous **[!UICONTROL Advanced]**, choisissez **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Startup Page]** .

   ![Configuration avancée - Paramètre de la page de démarrage de l’administrateur](./assets/admin-startup-page.png){width="600"}

1. Définissez **[!UICONTROL Startup Page]** sur la page qui doit apparaître en premier après la connexion à l’administrateur.

   Pour obtenir la liste détaillée de toutes les options d’administration, voir [Admin](../configuration-reference/advanced/admin.md) dans la _Référence de configuration_.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
