---
title: Réécritures des URL de catégorie
description: Découvrez comment utiliser les réécritures d’URL de catégorie pour rediriger les liens vers l’URL d’une autre catégorie de votre boutique Commerce.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Réécritures des URL de catégorie

Si une catégorie est supprimée de votre catalogue, vous pouvez utiliser une réécriture de catégorie pour rediriger les liens vers l’URL d’une autre catégorie de votre boutique. Pensez en termes de _cible_ / _requête originale_ ou _rediriger vers_ / _rediriger depuis_. Bien que des personnes puissent toujours accéder à l’ancienne page à partir de moteurs de recherche ou de liens obsolètes, la redirection entraîne le passage de votre magasin vers la nouvelle cible.

Si les [redirections automatiques](url-redirect-product-automatic.md) sont activées pour votre boutique, il n’est pas nécessaire de créer une réécriture lorsqu’une catégorie [clé d’URL](../catalog/catalog-urls.md) est modifiée.

{{url-rewrite-skip}}

## Étape 1. Planifier la réécriture

Pour éviter les erreurs, notez le chemin _redirection vers_ et le chemin _redirection depuis_ et incluez la clé d’URL et le suffixe (le cas échéant).

En cas de doute, ouvrez chaque page de catégorie de votre boutique, puis copiez le chemin d’accès à partir de la barre d’adresse de votre navigateur.

**Exemple:**

Rediriger vers : `gear/backpacks-and-bags.html`

Rediriger depuis : `gear/bags.html`

## Étape 2. Créer la réécriture

{{url-rewrite-params}}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Avant de poursuivre, procédez comme suit pour vérifier que le chemin d’accès de la requête est disponible :

   - Dans le filtre de recherche en haut de la colonne **[!UICONTROL Request Path]**, saisissez la clé URL de la catégorie à rediriger et cliquez sur **[!UICONTROL Search]**.

   - S’il existe plusieurs enregistrements de redirection pour la page, recherchez celui qui correspond à la vue de magasin applicable et ouvrez l’enregistrement de redirection en mode d’édition.

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Lorsque vous revenez à la page _[!UICONTROL URL Rewrites]_, cliquez sur **[!UICONTROL Add URL Rewrite]**.

1. Définissez **[!UICONTROL Create URL Rewrite]** sur `For category` et choisissez la catégorie cible dans l’arborescence qui est la destination de la redirection.

   ![Réécriture d’URL : sélectionnez une catégorie](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. Dans la section _Réécriture d’URL_, procédez comme suit :

   - Si vous disposez de plusieurs magasins, sélectionnez le **[!UICONTROL Store]** auquel s’applique la réécriture.

   - Par **[!UICONTROL Request Path]**, saisissez la clé URL de la catégorie demandée par le client. Il s’agit de la catégorie _redirection depuis_.

     >[!NOTE]
     >
     >Le chemin d’accès de la requête doit être unique pour le magasin spécifié. S’il existe déjà une redirection qui utilise le même chemin de requête, vous recevez une erreur lorsque vous essayez d’enregistrer la redirection. La redirection précédente doit être supprimée avant de pouvoir en créer une.

   - Définissez **[!UICONTROL Redirect]** sur l’une des options suivantes :

      - `Temporary (302)`
      - `Permanent (301)`

   - À titre de référence, saisissez une brève description de la réécriture.

   ![Ajouter une réécriture d’URL pour la catégorie](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Avant d’enregistrer la redirection, vérifiez les points suivants :

   - Le lien situé dans le coin supérieur gauche affiche le nom de la catégorie cible.
   - Le Chemin d’accès à la requête contient le chemin d’accès de la catégorie d’origine _redirection depuis_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** bouton .

   La nouvelle réécriture de catégorie s’affiche en haut de la grille Réécritures d’URL.

## Étape 3. Tester le résultat

1. Accédez à la page d’accueil de votre boutique.

1. Effectuez l’une des opérations suivantes :

   - Accédez à la catégorie d’origine _redirection à partir de_.
   - Dans la barre d’adresse du navigateur, saisissez le chemin d’accès à la catégorie d’origine _rediriger depuis_ immédiatement après l’URL du magasin et appuyez sur **[!UICONTROL Enter]**.

   La nouvelle catégorie cible s’affiche au lieu de la requête de catégorie d’origine.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indique le type de réécriture. Le type ne peut pas être modifié une fois la réécriture créée. Options : `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Catégorie à rediriger. Selon votre configuration, le chemin d’accès à la requête peut inclure le suffixe .html ou .htm et la catégorie parente. Le chemin d’accès de la requête doit être unique et ne peut pas être utilisé par une autre redirection. Si vous recevez une erreur indiquant que le chemin de requête existe, supprimez la redirection existante, puis réessayez. |
| [!UICONTROL Target Path] | Chemin d’accès interne utilisé par le système pour pointer vers la destination de la redirection. Le chemin cible est grisé et ne peut pas être modifié. |
| [!UICONTROL Redirect] | Détermine le type de redirection. Options : <br/>**[!UICONTROL No]**- Aucune redirection n’est spécifiée. De nombreuses opérations créent des demandes de redirection de ce type. Par exemple, chaque fois que vous ajoutez des produits à une catégorie, une redirection de type `No` est créée dans chaque vue de magasin.<br/>**[!UICONTROL Temporary (302)]** - Indique aux moteurs de recherche que la réécriture est limitée dans le temps. Les moteurs de recherche ne conservent généralement pas les informations de classement de page pour les réécritures temporaires. <br/>**[!UICONTROL Permanent (301)]**- Indique aux moteurs de recherche que la réécriture est permanente. Les moteurs de recherche conservent généralement les informations de classement de page pour les réécritures permanentes. |
| [!UICONTROL Description] | Décrit l’objectif de la réécriture à des fins de référence interne. |

{style="table-layout:auto"}
