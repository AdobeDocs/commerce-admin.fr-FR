---
title: Réécritures d’URL de catégorie
description: Découvrez comment utiliser les réécritures d’URL de catégorie pour rediriger les liens vers l’URL d’une autre catégorie de votre boutique Commerce.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Réécritures d’URL de catégorie

Si une catégorie est supprimée de votre catalogue, vous pouvez utiliser une réécriture de catégorie pour rediriger les liens vers l’URL d’une autre catégorie de votre magasin. Pensez en termes de _cible_ / _requête d’origine_  ou _rediriger vers_ / _rediriger depuis_. Bien que les visiteurs puissent toujours accéder à l’ancienne page à partir de moteurs de recherche ou de liens obsolètes, la redirection entraîne le passage de votre magasin vers la nouvelle cible.

If [redirections automatiques](url-redirect-product-automatic.md) sont activés pour votre magasin, il n’est pas nécessaire de créer une réécriture lorsqu’une catégorie [Clé URL](../catalog/catalog-urls.md) est modifiée.

{{url-rewrite-skip}}

## Étape 1. Planification de la réécriture

Pour éviter les erreurs, notez la variable _rediriger vers_ chemin et _rediriger depuis_ chemin et incluez la clé URL et le suffixe (le cas échéant).

Si vous n’en êtes pas sûr, ouvrez chaque page de catégorie de votre magasin, puis copiez le chemin d’accès depuis la barre d’adresse de votre navigateur.

**Exemple :**

Rediriger vers : `gear/backpacks-and-bags.html`

Rediriger à partir de : `gear/bags.html`

## Étape 2. Créer la réécriture

{{url-rewrite-params}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Avant de poursuivre, procédez comme suit pour vérifier que le chemin de requête est disponible :

   - Dans le filtre de recherche situé en haut de la page **[!UICONTROL Request Path]** , saisissez la clé URL de la catégorie à rediriger et cliquez sur **[!UICONTROL Search]**.

   - S’il existe plusieurs enregistrements de redirection pour la page, recherchez celui qui correspond à la vue de magasin applicable et ouvrez l’enregistrement de redirection en mode d’édition.

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Lorsque vous revenez à la variable _[!UICONTROL URL Rewrites]_page, cliquez sur **[!UICONTROL Add URL Rewrite]**.

1. Définir **[!UICONTROL Create URL Rewrite]** to `For category` et sélectionnez la catégorie cible dans l’arborescence qui est la destination de la redirection.

   ![Réécriture d’URL - catégorie de choix](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. Dans le _URL Rewrite_ , procédez comme suit :

   - Si vous disposez de plusieurs magasins, sélectionnez la variable **[!UICONTROL Store]** où la réécriture s’applique.

   - Pour **[!UICONTROL Request Path]**, saisissez la clé URL de la catégorie que le client demande. Il s’agit de la variable _rediriger depuis_ catégorie.

     >[!NOTE]
     >
     >Le chemin d’accès de la requête doit être unique pour le magasin spécifié. Si une redirection utilise déjà le même chemin de requête, vous recevez une erreur lorsque vous essayez d’enregistrer la redirection. La redirection précédente doit être supprimée avant de pouvoir en créer une.

   - Définir **[!UICONTROL Redirect]** à l’une des options suivantes :

      - `Temporary (302)`
      - `Permanent (301)`

   - À titre de référence, saisissez une brève description de la réécriture.

   ![Ajouter une réécriture d’URL pour la catégorie](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Avant d’enregistrer la redirection, vérifiez les éléments suivants :

   - Le lien situé dans le coin supérieur gauche affiche le nom de la catégorie cible.
   - Le chemin d’accès à la requête contient le chemin d’accès de l’original. _rediriger depuis_ catégorie.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** bouton .

   La nouvelle réécriture de catégorie s’affiche en haut de la grille Réécritures d’URL .

## Étape 3. Tester le résultat

1. Accédez à la page d’accueil de votre magasin.

1. Effectuez l’une des opérations suivantes :

   - Accédez à l’original _rediriger depuis_ catégorie.
   - Dans la barre d’adresse du navigateur, saisissez le chemin d’accès à l’original _rediriger depuis_ catégorie juste après l’URL du magasin et appuyez sur **[!UICONTROL Enter]**.

   La nouvelle catégorie cible apparaît à la place de la demande de catégorie d’origine.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indique le type de réécriture. Une fois la réécriture créée, le type ne peut plus être modifié. Options : `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | La catégorie à rediriger. Selon votre configuration, le chemin d’accès à la requête peut inclure le suffixe .html ou .htm, ainsi que la catégorie parente. Le chemin de la requête doit être unique et ne peut pas être utilisé par une autre redirection. Si vous recevez une erreur indiquant que le chemin de requête existe, supprimez la redirection existante, puis réessayez. |
| [!UICONTROL Target Path] | Chemin d’accès interne utilisé par le système pour pointer vers la destination de la redirection. Le chemin cible est grisé et ne peut pas être modifié. |
| [!UICONTROL Redirect] | Détermine le type de redirection. Options : <br/>**[!UICONTROL No]**- Aucune redirection n’est spécifiée. De nombreuses opérations créent des requêtes de redirection de ce type. Par exemple, chaque fois que vous ajoutez des produits à une catégorie, une redirection de la fonction `No` est créé pour chaque vue de magasin.<br/>**[!UICONTROL Temporary (302)]** - Indique aux moteurs de recherche que la réécriture est limitée dans le temps. En règle générale, les moteurs de recherche ne conservent pas les informations de classement de page pour les réécritures temporaires. <br/>**[!UICONTROL Permanent (301)]**- Indique aux moteurs de recherche que la réécriture est permanente. Les moteurs de recherche conservent généralement les informations de classement de page pour les réécritures permanentes. |
| [!UICONTROL Description] | Décrit l’objectif de la réécriture à des fins de référence interne. |

{style="table-layout:auto"}
