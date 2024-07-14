---
title: Présentation de [!DNL Adobe Commerce B2B]
description: Découvrez comment utiliser les fonctionnalités intégrées B2B pour répondre à vos besoins pour les entreprises clientes.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: 8e4e070f41f7d3bf872e81c9805e7c24779b812d
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# Présentation de [!DNL Adobe Commerce B2B]

Contrairement au modèle standard &quot;business-to-consumer&quot;, les fonctionnalités intégrées B2B (Business to Business) sont conçues pour répondre aux besoins des vendeurs (marchands Adobe Commerce) qui ont des clients qui sont des entreprises. Il prend en charge les entreprises avec des structures organisationnelles complexes et plusieurs utilisateurs avec différents rôles et niveaux de permission d’achat. Un client B2B type peut être le gérant d’un magasin de détail ou un acheteur qui effectue des achats pour le compte d’une société. Dans les deux cas, la transaction a lieu entre votre entreprise et la leur. Vous pouvez également vendre des produits directement au consommateur. [!DNL Adobe Commerce B2B] est une solution intégrée qui prend en charge les modèles B2B et B2C.

Avec l’ [installation](install.md) et l’ [activation](enable-basic-features.md) de l’extension B2B dans votre boutique Adobe Commerce, l’expérience d’achat peut être personnalisée avec des catalogues et des prix spécifiques au client, ainsi qu’avec du contenu ciblé et des promotions.

## Comptes d’entreprise

Le composant Compte d’entreprise est une entité clé au sein de B2B sur laquelle dépendent d’une certaine manière toutes les autres fonctionnalités. Il permet de regrouper plusieurs acheteurs appartenant à une seule société dans un compte de société unique (ou compte d’entreprise). L’administrateur de l’entreprise peut créer une structure d’entreprise (divisions, subdivisions et utilisateurs) qui reflète le modèle opérationnel de l’entreprise et qui fournit différents rôles utilisateur et autorisations aux membres de l’entreprise. Cette structure permet à l’administrateur de la société de contrôler l’activité des utilisateurs pour le compte de la société : commande, citation, achat, accès aux informations de crédit ou au profil de la société, etc.

Depuis l’administrateur, l’administrateur du site Commerce peut configurer le fonctionnement de l’entreprise sur le site web. La configuration détermine les fonctionnalités B2B disponibles pour les utilisateurs de l’entreprise, notamment les méthodes de paiement, les niveaux de prix, la possibilité de négocier les prix à l’aide de devis, la possibilité de créer des listes de demandes d’acquisition, etc.

Pour plus d’informations, voir [Comptes d’entreprise](account-companies.md).

>[!NOTE]
>
>Lorsque cette option est activée, votre boutique peut offrir aux entreprises l’option _Payer sur le compte_, ce qui signifie effectuer des achats sur une ligne de crédit de l’entreprise. En tant que commerçant, vous pouvez allouer du crédit pour un compte de société et gérer les paramètres de crédit pour une société, ainsi que le remboursement du crédit.

## Gestion des entreprises

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme Beta"}

La gestion des entreprises permet aux administrateurs commerciaux de rationaliser l’administration et la gestion des organisations B2B à l’aide de modèles opérationnels complexes.

Depuis l’administrateur, les utilisateurs disposant des autorisations appropriées peuvent créer un **[!UICONTROL Company Hierarchy]** qui reflète la structure organisationnelle d’une entreprise composée de plusieurs entreprises. Cette hiérarchie leur permet d’afficher et de gérer les entreprises sous la forme d’un groupe. Par exemple, l’administrateur peut désigner une société mère et affecter toutes les sociétés qui fonctionnent comme des filiales de la société mère. Ensuite, l’administrateur de la société mère peut afficher et gérer les comptes de l’entreprise pour toutes les entreprises affectées.

Pour plus d’informations, voir [Gestion des entreprises](manage-companies.md).

## Services pour Adobe Commerce

Les services pour Adobe Commerce sont des services hébergés qui offrent des fonctionnalités étendues à Adobe Commerce et Magento Open Source. Les services qui prennent en charge les workflows B2B sont les suivants :

* [Service de catalogue](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Recherche en direct](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Recommendations de produit](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Catalogues partagés

Les catalogues partagés sont les niveaux de prix qui permettent de définir des prix personnalisés par produit pour différentes entreprises sur un ou plusieurs sites web. En utilisant des catalogues partagés, vous pouvez vendre des produits en appliquant différents niveaux de prix pour différents groupes de clients. La prise en charge des catalogues partagés n’est disponible que pour les magasins Commerce configurés pour prendre en charge les comptes d’entreprise.

Pour plus d’informations, voir [Utilisation de catalogues partagés](catalog-shared.md).

## Ordre rapide

Configurez la commande rapide pour réduire le processus de commande à plusieurs clics pour les clients connectés lorsqu’ils connaissent le nom ou le SKU des produits qu’ils souhaitent commander.

Pour plus d’informations, voir [Commandes rapides](quick-order.md).

## Devis négociables

Utilisez la fonction Devis pour lancer la négociation des prix entre un acheteur et un vendeur d’une société.

* Un acheteur autorisé peut lancer un devis à partir du panier.

* Un vendeur peut lancer un devis pour un acheteur auprès de l’administrateur.

Les acheteurs et les vendeurs utilisent le devis pour gérer le processus de négociation, comme l’ajout d’éléments, la mise à jour des quantités, la demande et l’application de remises, jusqu’à ce qu’ils parviennent à un accord. La grille _Guillemets_ de l’Admin répertorie chaque citation reçue et conserve un historique de la communication entre l’acheteur et le vendeur.

La prise en charge des devis négociables est disponible uniquement pour les magasins Commerce configurés pour prendre en charge les comptes d’entreprise.

Pour plus d’informations, voir [Guillemets négociables](quotes.md).

## Approbation des commandes d’achat

Lorsque les commandes d’achat sont activées pour un compte de société, toutes les commandes sont automatiquement créées en tant que commandes d’achat (PO). Les utilisateurs de l’entreprise disposant des autorisations requises peuvent créer, modifier et supprimer des PO qu’ils créent et des PO créés par des utilisateurs subordonnés. En fonction de leur rôle et de l’ordre, les utilisateurs de l’entreprise peuvent être soumis à plusieurs règles d’approbation.

Pour plus d’informations, voir [Commandes d’entreprises](purchase-order-flow.md).

## Listes de demandes

Les clients peuvent utiliser la liste des demandes d’achat pour gagner du temps lors de l’achat de produits fréquemment commandés, car ils peuvent ajouter des articles au panier directement à partir de la liste. Ils peuvent gérer plusieurs listes qui se concentrent sur des produits provenant de différents fournisseurs, acheteurs, équipes, campagnes ou tout autre élément qui simplifie leur workflow.

Pour plus d’informations, voir [Listes de demandes](requisition-lists.md).
