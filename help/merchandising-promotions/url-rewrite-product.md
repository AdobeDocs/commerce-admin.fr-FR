---
title: Réécritures d’URL de produit
description: Découvrez comment utiliser les réécritures d’URL de produit pour rediriger les liens vers l’URL d’un autre produit de votre boutique Commerce.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Réécritures d’URL de produit

Avant de commencer, veillez à comprendre exactement ce que la redirection doit accomplir. Pensez en termes de _cible_ / _requête d’origine_ ou _rediriger vers_ / _rediriger depuis_. Bien que les visiteurs puissent toujours accéder à l’ancienne page à partir de moteurs de recherche ou de liens obsolètes, la redirection entraîne le passage de votre magasin vers la nouvelle cible.

If [redirections automatiques](url-redirect-product-automatic.md) sont activés pour votre magasin, il n’est pas nécessaire de créer une réécriture lorsqu’un produit [Clé URL](../catalog/catalog-urls.md) est modifiée.

{{url-rewrite-skip}}

## Étape 1. Planification de la réécriture

Pour éviter les erreurs, notez la variable _rediriger vers_ chemin et _rediriger depuis_ chemin et incluez la clé URL et le suffixe (le cas échéant).

Si vous n’en êtes pas certain, ouvrez chaque page de produit dans votre boutique, puis copiez le chemin d’accès depuis la barre d’adresse de votre navigateur. Lors de la création d’une redirection de produit, vous pouvez inclure ou exclure la variable [chemin de catégorie](../catalog/catalog-urls.md). Pour cet exemple, nous créons une redirection de produit sans chemin de catégorie.

### Produit avec chemin de catégorie

Rediriger vers : `gear/bags/impulse-duffle.html`

Rediriger à partir de : `gear/bags/overnight-duffle.html`

### Produit sans chemin de catégorie

Rediriger vers : `impulse-duffle.html`

Rediriger à partir de : `overnight-duffle.html`

## Étape 2. Créer la réécriture

{{url-rewrite-params}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Avant de poursuivre, procédez comme suit pour vérifier que le chemin de requête est disponible.

   - Dans le filtre de recherche situé en haut de la page **[!UICONTROL Request Path]** , saisissez la clé URL de la page à rediriger et cliquez sur **[!UICONTROL Search]**.

   - S’il existe plusieurs enregistrements de redirection pour la page, recherchez celui qui correspond à la vue de magasin applicable et ouvrez-le en mode d’édition.

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Dans le coin supérieur droit de la page Réécritures d’URL, cliquez sur **Ajouter une réécriture d’URL**.

1. Définir **[!UICONTROL Create URL Rewrite]** to `For product`.

1. Dans la grille, recherchez le produit qui est la cible (destination) de la redirection et cliquez sur la ligne .

   ![Réécritures d’URL - produit](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Sous l’arborescence des catégories, cliquez sur **[!UICONTROL Skip Category Selection]**.

   Dans cet exemple, la redirection n’inclut pas de catégorie.

   ![Réécriture de l’URL du produit - sélection de catégorie ignorée](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   La page Ajouter une réécriture d’URL pour un produit affiche un lien vers la cible dans le coin supérieur gauche et le champ Chemin d’accès cible affiche la version système du chemin d’accès, qui ne peut pas être modifiée. Au départ, le champ Chemin de redirection affiche également le chemin cible.

   - Si vous avez plusieurs vues de magasin, définissez **[!UICONTROL Store]** à la vue d’application de la réécriture. Sinon, une réécriture est créée pour chaque vue.

   - Pour **[!UICONTROL Request Path]**, remplacez la valeur par défaut en saisissant la clé d’URL et le suffixe (le cas échéant) de la demande de produit d’origine. Il s’agit de la variable _rediriger depuis_ produit que vous avez identifié à l’étape de planification.

     >[!NOTE]
     >
     >Le chemin d’accès de la requête doit être unique pour le magasin spécifié. Si une redirection utilise déjà le même chemin de requête, vous recevez une erreur lorsque vous essayez d’enregistrer la redirection. La redirection précédente doit être supprimée avant de pouvoir en créer une.

   - Définir **[!UICONTROL Redirect Type]** à l’une des options suivantes :

      - `Temporary (302)`
      - `Permanent (301)`

   - À titre de référence, saisissez un résumé **[!UICONTROL Description]** de la réécriture.

   ![Réécriture de l’URL du produit - informations](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Avant d’enregistrer la redirection, vérifiez les éléments suivants :

   - Le lien situé dans le coin supérieur gauche affiche le nom du produit cible.
   - Le chemin d’accès à la requête contient le chemin d’accès de l’original. _rediriger depuis_ produit.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   La nouvelle réécriture de produit s’affiche désormais en haut de la grille Réécritures d’URL .

## Étape 3. Tester le résultat

1. Accédez à la page d’accueil de votre magasin.

1. Effectuez l’une des opérations suivantes :

   - Accédez à l’original _rediriger depuis_ page de demande de produit.
   - Dans la barre d’adresse du navigateur, saisissez le chemin d’accès à l’original _rediriger depuis_ produit immédiatement après l’URL du magasin et appuyez sur **Entrée**.

   Le nouveau produit cible apparaît à la place de la demande de produit d’origine.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indique le type de réécriture. Une fois la réécriture créée, le type ne peut plus être modifié. Options : `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Le produit à rediriger. Selon votre configuration, le chemin d’accès à la requête peut inclure la variable `.html` ou `.htm` suffixe et catégorie. Le chemin d’accès à la requête doit être unique et ne peut pas être utilisé par une autre redirection. Si vous recevez une erreur indiquant que le chemin d’accès à la requête existe, supprimez la redirection existante, puis réessayez. |
| [!UICONTROL Target Path] | Chemin d’accès interne utilisé par le système pour pointer vers la destination de la redirection. Le chemin cible est grisé et ne peut pas être modifié. |
| [!UICONTROL Redirect] | Détermine le type de redirection. Options : <br/>**[!UICONTROL No]**- Aucune redirection n’est spécifiée. De nombreuses opérations créent des requêtes de redirection de ce type. Par exemple, chaque fois que vous ajoutez des produits à une catégorie, une redirection de la fonction `No` est créé pour chaque vue de magasin.<br/>**[!UICONTROL Temporary (302)]** - Indique aux moteurs de recherche que la réécriture est limitée dans le temps. En règle générale, les moteurs de recherche ne conservent pas les informations de classement de page pour les réécritures temporaires. <br/>**[!UICONTROL Permanent (301)]**- Indique aux moteurs de recherche que la réécriture est permanente. Les moteurs de recherche conservent généralement les informations de classement de page pour les réécritures permanentes. |
| [!UICONTROL Description] | Décrit l’objectif de la réécriture à des fins de référence interne. |

{style="table-layout:auto"}

## Plusieurs réécritures d’URL

Vous pouvez rapidement mettre à jour les réécritures d’URL pour plusieurs ou tous les produits simultanément en procédant comme suit.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Sélectionnez tous les produits pour lesquels vous souhaitez mettre à jour les réécritures d’URL.

1. Sous _[!UICONTROL Actions]_, choisissez **[!UICONTROL Update attributes]**pour mettre à jour plusieurs réécritures ou toutes.

1. Sous _[!UICONTROL PRODUCTS INFORMATION]_, cliquez sur le **[!UICONTROL Websites]**.

1. Dans le _[!UICONTROL Add Product To Websites]_, sélectionnez tous les sites web pour lesquels restaurer les réécritures d’URL.

1. Lorsque vous êtes prêt à mettre à jour, cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Tous les produits sélectionnés sont lisibles sur les sites web sélectionnés et les réécritures d’URL sont régénérées.

![Mise à jour des attributs : mise à jour de plusieurs réécritures d’URL](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
