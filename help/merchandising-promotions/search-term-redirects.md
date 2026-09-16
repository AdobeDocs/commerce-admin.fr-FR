---
title: Redirections à terme de recherche et routage de storefront
description: Découvrez comment choisir les redirections de termes de recherche, les réécritures d’URL, les règles de recherche en direct ou le routage storefront par déploiement pour Adobe Commerce et Edge Delivery Services.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# Redirections de termes de recherche et routage de storefront

Les redirections par terme de recherche, les redirections d’URL et le marchandisage de recherche résolvent différents problèmes. Utilisez ce guide pour choisir la fonctionnalité appropriée pour la recherche [!DNL Adobe Commerce] standard, la [!DNL Live Search] et les [!DNL Commerce Storefront] optimisés par [!DNL Edge Delivery Services].

## Présentation des types de redirection

Ces fonctionnalités diffèrent selon ce qui déclenche le comportement et ce que l’acheteur voit :

* Une **redirection de terme de recherche** envoie un acheteur qui saisit un terme de recherche spécifique vers une page désignée.

* Une **redirection d’URL** envoie une demande d’ancienne URL à une nouvelle URL, généralement avec une réponse HTTP 301 ou 302. La barre d’adresse du navigateur est remplacée par la nouvelle URL.

* **Le marchandisage de recherche** modifie les produits qui apparaissent ou leur ordre dans les résultats de recherche sans modifier l’URL demandée.

* Une **réécriture d’URL** mappe une URL à une autre sur le serveur. L’outil de réécriture d’URL [!DNL Adobe Commerce] crée une redirection permanente (301) pour l’ancienne URL. Pour plus d’informations, voir [Réécritures d’URL](url-rewrite.md).

## Choisir une fonctionnalité de routage

Suivez les conseils suivants pour identifier la fonctionnalité qui correspond à vos besoins :

| Exigence | Fonctionnalité recommandée |
| --- | --- |
| Envoi d’une requête spécifique à partir de la recherche [!DNL Adobe Commerce] standard vers une page | Configurez un terme de recherche dans [Gérer les termes de recherche](../catalog/search-terms.md), lorsque cela est pris en charge. |
| Modifier le classement ou la visibilité des produits dans les résultats de recherche | Utilisez [!DNL Live Search] [synonymes](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-admin/synonyms/synonyms) ou [règles de marchandisage](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Rediriger une ancienne URL de produit, de catégorie ou de CMS | Utilisez l’outil Commerce [Réécriture d’URL](url-rewrite.md) lorsqu’il s’applique à votre déploiement. |
| Rediriger un chemin [!DNL Edge Delivery Services] | Utilisez le routage storefront ou CDN. |
| Conserver les URL héritées après une migration de storefront | Créez et testez un mappage de redirection d’URL hérité vers nouveau. |

## Recherche Commerce standard

Avec la recherche catalogue standard, vous pouvez configurer un terme de recherche pour ouvrir une page de contenu, une page de catégorie, une page de produit ou une page externe dans laquelle le déploiement prend en charge cette fonctionnalité. Utilisez-la lorsqu’une requête saisie par l’acheteur, telle que `gift cards` ou `returns`, doit ouvrir une campagne ou une page d’information.

Pour créer ou mettre à jour ce type de redirection, voir [Gérer les termes de recherche](../catalog/search-terms.md). La configuration des termes de recherche est distincte de l’outil de réécriture d’URL, car le déclencheur est la requête de l’acheteur et non une URL existante.

>[!NOTE]
>
>Vérifiez que le storefront utilise la recherche catalogue standard et prend en charge les redirections natives des termes de recherche. Le comportement et la configuration disponible peuvent différer pour [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] ou un storefront découplé.

## Redirections et réécritures d’URL

Utilisez une réécriture d’URL lorsque la source est une URL existante plutôt qu’un terme de recherche saisi par l’acheteur. La redirection est un exemple courant :

* Une ancienne URL de produit vers une nouvelle URL de produit.

* Une URL de catégorie retirée vers une URL de catégorie de remplacement.

* Une URL de page CMS obsolète vers une nouvelle URL de page de contenu.

Pour les déploiements qui prennent en charge l’outil de réécriture d’URL, accédez à **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** pour créer la redirection. Pour obtenir des conseils détaillés, voir [Réécritures d’URL](url-rewrite.md).

>[!NOTE]
>
>La rubrique [Réécritures d’URL](url-rewrite.md) s’applique uniquement à PaaS. Pour un storefront [!DNL Adobe Commerce as a Cloud Service] ou [!DNL Edge Delivery Services], utilisez plutôt le guide de routage pour ce storefront.

## Recherche en direct

[!DNL Live Search] remplace l’expérience de recherche storefront par défaut et fournit des fonctionnalités telles que des synonymes, des facettes et des règles de marchandisage.

Utilisez [!DNL Live Search] lorsque vous devez modifier la pertinence de la recherche, le classement des produits ou la visibilité des produits. Utilisez des synonymes lorsque différents mots doivent renvoyer des produits similaires. Utilisez des règles de marchandisage lorsque les produits doivent être boostés, enterrés ou classés différemment.

[!DNL Live Search] comportement de recherche ne doit pas être traité comme un remplacement de liste déroulante pour chaque configuration native de terme de recherche Commerce. Lorsqu’une requête doit accéder à une page de contenu ou de campagne, implémentez la redirection dans le calque de storefront ou de routage Edge qui reçoit la requête. Pour plus d’informations, voir la [[!DNL Live Search] documentation](https://experienceleague.adobe.com/fr/docs/commerce/live-search/overview).

## Edge Delivery Services

Pour un storefront alimenté par [!DNL Edge Delivery Services], gérez les redirections dans le storefront ou la couche de routage Edge. Ne supposez pas que l’URL d’administration [!DNL Adobe Commerce] réécrit le contrôle de chaque requête.

Lorsque vous utilisez la création de documents, conservez les mappages de redirection dans la configuration de redirection du site. Pour les redirections qui doivent s’exécuter avant qu’une requête n’atteigne l’origine, utilisez la configuration CDN ou Edge appropriée. Pour obtenir des conseils relatifs à l’optimisation du moteur de recherche, voir [Directives relatives à l’optimisation du moteur de recherche pour Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=fr).

## Migrer depuis Luma

Traiter la migration de redirection comme faisant partie de la migration du storefront. Préservez le parcours du client et l’intention d’optimisation du moteur de recherche, puis implémentez à nouveau le routage pour le storefront cible.

Avant de basculer le trafic vers le nouveau storefront :

1. Exportez et inventoriez les URL Luma et les pages de destination de termes de recherche existantes.

1. Classez chaque élément en tant que redirection de terme de recherche, redirection d’URL ou règle de marchandisage.

1. Mappez chaque URL héritée à son nouveau chemin de storefront.

1. Implémentez chaque redirection au niveau de la couche qui reçoit la requête.

1. Testez les codes d’état, les paramètres de requête, les URL canoniques, les chemins d’accès aux paramètres régionaux et les boucles de redirection.

1. Surveillez les journaux et les analyses après le lancement à la recherche d’URL héritées non résolues.

## Résolution des problèmes de redirection

Utilisez les contrôles suivants lorsqu’une redirection ne se comporte pas comme prévu dans les vues de recherche, de routage de storefront et de magasin [!DNL Adobe Commerce].

| Problème | Éléments à vérifier |
| --- | --- |
| Un terme de recherche ne redirige pas | Vérifiez que le storefront utilise la recherche catalogue standard, que la requête de recherche correspond au terme configuré et que le terme de recherche est affecté à l’affichage correct du magasin. Si [!DNL Live Search] est activé, vérifiez que la redirection est implémentée dans la couche storefront ou edge. |
| Une redirection fonctionne sur Luma, mais pas sur Edge Delivery Services | Vérifiez que la redirection est configurée dans le storefront [!DNL Edge Delivery Services] ou la couche de routage CDN. [!DNL Adobe Commerce] Les réécritures d’URL d’administration peuvent ne pas recevoir la demande. |
| La recherche en direct renvoie les résultats au lieu de les rediriger | Utilisez des règles de [!DNL Live Search] pour le classement et la visibilité des produits. Pour accéder à une page de contenu ou de campagne, configurez la redirection dans le calque storefront ou edge. |
| Une redirection fonctionne dans une vue de magasin, mais pas dans une autre | Vérifiez la vue de magasin affectée au terme de recherche ou à la règle d’URL. Testez le chemin d’accès au paramètre régional complet et la requête dans chaque vue de magasin affectée. |

## Plus d’aide sur cette rubrique

* [Présentation de l’optimisation pour les moteurs de recherche et bonnes pratiques](seo-overview.md)

* [Quelle est la devanture ?](../getting-started/storefront.md)

* [Gestion des termes de recherche](../catalog/search-terms.md)

* [Réécritures d’URL](url-rewrite.md)
