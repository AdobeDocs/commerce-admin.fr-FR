---
title: Catalogues plats
description: Découvrez comment créer un catalogue plat, où chaque ligne contient toutes les données nécessaires sur un produit ou une catégorie.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Catalogues plats

>[!IMPORTANT]
>
>L’utilisation d’un catalogue plat n’est plus recommandée comme bonne pratique. L’utilisation continue de cette fonctionnalité provoque une dégradation des performances et d’autres problèmes d’indexation. Une description détaillée et une solution sont disponibles dans le [centre d&#39;aide](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html?lang=fr).<br/><br/> Les versions affectées incluent : <br/>- Adobe Commerce sur l’infrastructure cloud, 2.3.x et versions ultérieures<br/>- Adobe Commerce (On-Premise), 2.3.x et versions ultérieures<br/>- Magento Open Source, 2.3.x et versions ultérieures <br/><br/>Sur toute version de publication, certaines extensions fonctionnent uniquement avec des tables plates, ce qui crée un risque si vous désactivez les tables plates. Si vous savez que certaines extensions utilisent des indexeurs de catalogue plat, vous devez tenir compte de ce risque lorsque vous définissez ces valeurs sur `No`.

Commerce stocke généralement les données de catalogue dans plusieurs tables, en fonction du modèle Entity-Attribute-Value (EAV). Comme les attributs de produit sont stockés dans de nombreuses tables, les requêtes SQL sont parfois longues et complexes.

En revanche, un catalogue plat crée des tableaux à la volée, où chaque ligne contient toutes les données nécessaires sur un produit ou une catégorie. Un catalogue plat est automatiquement mis à jour, soit toutes les minutes, soit selon votre tâche cron. L’indexation de catalogue plat peut également accélérer le traitement des règles de prix de catalogue et de panier. Un catalogue comportant jusqu’à 500 000 SKU peut être indexé rapidement en tant que catalogue plat.

>[!NOTE]
>
>Avant d’activer un catalogue plat pour un magasin en ligne, veillez à tester la configuration dans un environnement de développement.

## Etape 1 : Activer le catalogue plat

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section _Storefront_ et procédez comme suit :

   - Définissez **[!UICONTROL Use Flat Catalog Category]** sur `Yes`. (Si nécessaire, décochez la case **[!UICONTROL Use system value]** .)

   - Définissez **[!UICONTROL Use Flat Catalog Product]** sur `Yes`.

   ![Configuration de catalogue plat](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur **[!UICONTROL Cache Management]** dans le message système et suivez les instructions pour actualiser le cache.

## Etape 2 : vérification des résultats

Vous pouvez utiliser deux méthodes pour vérifier les résultats.

### Méthode 1 : vérification des résultats pour un seul produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode d’édition.

1. Pour **[!UICONTROL Name]**, ajoutez le texte `_TEST` à la fin du nom du produit.

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans un nouvel onglet du navigateur, accédez à la page d’accueil de votre boutique et procédez comme suit :

   - Recherchez le produit que vous avez modifié.

   - Utilisez la navigation pour accéder au produit sous sa catégorie affectée.

     Si nécessaire, actualisez la page pour afficher les résultats. La modification s’affiche dans la minute ou selon votre planning [Cron](../systems/cron.md).

   ![Storefront avec catalogue plat](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Méthode 2 : vérification des résultats pour une catégorie

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans le coin supérieur gauche, vérifiez que **[!UICONTROL Store View]** est défini sur `All Store Views`.

   Si vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Dans l’arborescence de catégories, sélectionnez une catégorie existante, cliquez sur **[!UICONTROL Add Subcategory]**, puis procédez comme suit :

   - Pour **[!UICONTROL Category Name]**, saisissez `Test Category`.

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

     ![Sous-catégorie de test](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Products in Category]** et cliquez sur **[!UICONTROL Reset Filter]** pour afficher tous les produits.

   - Cochez la case de plusieurs produits à ajouter à la nouvelle catégorie.

   - cliquez sur **[!UICONTROL Save]**.

   ![Test de produits de catégorie](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. Dans un nouvel onglet du navigateur, accédez à la page d’accueil de votre magasin et utilisez la navigation du magasin pour accéder à la catégorie que vous avez créée.

   Si nécessaire, actualisez la page pour afficher les résultats. La modification s’affiche dans la minute ou selon votre planning cron.

## Étape 3 : suppression des données de test

Procédez comme suit pour supprimer les données de test et restaurer le nom du produit et la configuration du catalogue d’origine.

### Supprimer la catégorie de test

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence des catégories, sélectionnez la sous-catégorie de test que vous avez créée.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

   Cette suppression de catégorie ne supprime pas les produits affectés à la catégorie.

### Restaurer le nom du produit d’origine

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Ouvrez le produit test en mode d’édition.

1. Supprimez le texte `_TEST` que vous avez ajouté à **[!UICONTROL Product Name]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

### Restaurer la configuration du catalogue d’origine

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section _Storefront_ et procédez comme suit :

   - Définissez **[!UICONTROL Use Flat Catalog Category]** sur `No`.

   - Définissez **[!UICONTROL Use Flat Catalog Product]** sur `No`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez le cache.
