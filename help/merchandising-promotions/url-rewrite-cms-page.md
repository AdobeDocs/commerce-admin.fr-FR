---
title: L’URL de la page de contenu réécrit
description: Découvrez comment utiliser les réécritures d’URL de page de contenu pour rediriger les liens vers l’URL d’une autre page de contenu de votre boutique Commerce.
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# L’URL de la page de contenu réécrit

Avant de commencer, veillez à comprendre exactement ce que la redirection est à accomplir. Pensez en termes de _cible_ / _source_ ou _rediriger vers_ / _rediriger depuis_. Bien que les visiteurs puissent toujours accéder à l’ancienne page à partir de moteurs de recherche ou de liens obsolètes, la redirection entraîne le passage de votre magasin vers la nouvelle cible.

![Réécritures d’URL - page CMS](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## Étape 1. Planification de la réécriture

Pour éviter les erreurs, notez la clé URL de la variable _rediriger vers_ et _rediriger depuis_ page.

Si vous n’en êtes pas sûr, ouvrez chaque page de votre magasin, puis copiez le chemin d’accès depuis la barre d’adresse de votre navigateur.

### Chemin de page CMS

Rediriger vers : `new-page`

Rediriger à partir de : `old-page`

## Étape 2. Créer la réécriture

{{url-rewrite-params}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Avant de poursuivre, procédez comme suit pour vérifier que le chemin de requête est disponible.

   - Dans le filtre de recherche situé en haut de la page **[!UICONTROL Request Path]** , saisissez la clé URL de la page à rediriger et cliquez sur **[!UICONTROL Search]**.

   - S’il existe plusieurs enregistrements de redirection pour la page, recherchez celui qui correspond à la vue de magasin applicable et ouvrez-le en mode d’édition.

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Lorsque vous revenez à la page Réécritures d’URL, cliquez sur **[!UICONTROL Add URL Rewrite]**.

1. Définir **[!UICONTROL Create URL Rewrite]** to `for CMS page`.

1. Recherchez la nouvelle page cible dans la grille et ouvrez-la en mode d’édition.

   ![Ajout d’une réécriture d’URL - pour la page CMS](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. Sous Informations de réécriture d’URL, procédez comme suit :

   - Si vous avez plusieurs vues de magasin, sélectionnez la variable **[!UICONTROL Store]** où la réécriture s’applique.

   - Pour **[!UICONTROL Request Path]**, saisissez la clé URL de la page d’origine que le client demande. Il s’agit de la variable _rediriger depuis_ page.

     >[!NOTE]
     >
     >Le chemin d’accès à la requête doit être unique pour le magasin spécifié. Si une redirection utilise déjà le même chemin d’accès à la requête, une erreur s’affiche lorsque vous essayez d’enregistrer la redirection. La redirection précédente doit être supprimée avant de pouvoir en créer une.

   - Définir **[!UICONTROL Redirect]** à l’une des options suivantes :

      - `Temporary (302)`
      - `Permanent (301)`

   - À titre de référence, saisissez une brève description de la réécriture.

   ![Informations de réécriture d’URL](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. Avant d’enregistrer la redirection, vérifiez les éléments suivants :

   - Le lien situé dans le coin supérieur gauche affiche le nom de la page cible.
   - Le chemin d’accès à la requête contient le chemin d’accès de l’original. _rediriger depuis_ page.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   La nouvelle réécriture apparaît dans la grille en haut de la liste.

## Étape 3. Tester le résultat

1. Accédez à la page d’accueil de votre magasin.

1. Effectuez l’une des opérations suivantes :

   - Accédez à l’original _rediriger depuis_ page.
   - Dans la barre d’adresse du navigateur, saisissez le nom de l’original _rediriger depuis_ page juste après l’URL du magasin et appuyez sur **Entrée**.

   La nouvelle page cible apparaît à la place de la requête de page d’origine.

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indique le type de réécriture. Une fois la réécriture créée, le type ne peut plus être modifié. Options : `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | La page CMS à rediriger. Le chemin de la requête doit être unique et ne peut pas être utilisé par une autre redirection. Si vous recevez un message d’erreur indiquant que le chemin de requête existe, supprimez la redirection existante, puis réessayez. |
| [!UICONTROL Target Path] | Chemin d’accès interne utilisé par le système pour pointer vers la destination. Le chemin cible est grisé et ne peut pas être modifié. |
| [!UICONTROL Redirect] | Détermine le type de redirection. Options : <br/>**[!UICONTROL No]**- Aucune redirection n’est spécifiée.<br/>**[!UICONTROL Temporary (302)]** - Indique aux moteurs de recherche que la réécriture est limitée dans le temps. En règle générale, les moteurs de recherche ne conservent pas les informations de classement de page pour les réécritures temporaires. <br/>**[!UICONTROL Permanent (301)]**- Indique aux moteurs de recherche que la réécriture est permanente. Les moteurs de recherche conservent généralement les informations de classement de page pour les réécritures permanentes. |
| [!UICONTROL Description] | Décrit l’objectif de la réécriture à des fins de référence interne. |

{style="table-layout:auto"}
