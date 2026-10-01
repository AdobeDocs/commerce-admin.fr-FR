---
title: Présentation de [!DNL Adobe Commerce B2B]
description: Découvrez comment utiliser les fonctionnalités intégrées B2B pour répondre à vos besoins pour les entreprises clientes.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
TQID: https://experienceleague.adobe.com/dt7QZnXH9yO6vMFJBIgt4g43XVfk6Da1gyXEMqqvJlo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 2%
---
# Présentation de [!DNL Adobe Commerce B2B]

Contrairement au modèle standard business-to-consumer, les fonctionnalités B2B (Business to Business) intégrées sont conçues pour répondre aux besoins des vendeurs (commerçants Adobe Commerce) qui ont des clients qui sont des entreprises. Il s’adapte aux entreprises dotées de structures organisationnelles complexes et à plusieurs utilisateurs ayant des rôles et des niveaux d’autorisation d’achat différents. Un client B2B type peut être le responsable d’un magasin de vente au détail ou un acheteur qui effectue des achats pour le compte d’une entreprise. Dans les deux cas, la transaction a lieu entre votre entreprise et la leur. Vous pouvez également vendre des produits directement au consommateur. [!DNL Adobe Commerce B2B] est une solution intégrée qui prend en charge les modèles B2B et B2C.

Grâce à l’[installation](install.md) et [activation](enable-basic-features.md) de l’extension B2B dans votre boutique Adobe Commerce, vous pouvez personnaliser l’expérience d’achat à l’aide de catalogues et de tarifs spécifiques aux clients, ainsi que de contenu et de promotions ciblés.

## Comptes d’entreprise

Le composant Compte d’entreprise est une entité clé du B2B sur laquelle toutes les autres fonctionnalités dépendent d’une manière ou d’une autre. Il permet de joindre plusieurs acheteurs appartenant à une seule société en un seul compte d’entreprise (ou compte d’entreprise). L’administrateur de l’entreprise peut créer une structure d’entreprise (divisions, subdivisions et utilisateurs) qui reflète le modèle opérationnel de l’entreprise et fournit différents rôles utilisateur et autorisations aux membres de l’entreprise. Cette structure permet à l’administrateur de la société de contrôler l’activité des utilisateurs pour le compte de la société : commande, devis, achats, accès aux informations de crédit ou au profil de la société, etc.

Depuis l’administrateur, l’administrateur du site Commerce peut configurer le fonctionnement de la société sur le site web. La configuration détermine les fonctionnalités B2B disponibles pour les utilisateurs de la société, notamment les modes de paiement, les niveaux de prix, la possibilité de négocier des prix à l&#39;aide de devis, la possibilité de créer des listes de demandes d&#39;approvisionnement, etc.

Pour plus d’informations, voir [Comptes société](account-companies.md).

>[!NOTE]
>
>Lorsque cette option est activée, votre boutique peut donner aux entreprises la possibilité de _Payer en compte_, ce qui signifie effectuer des achats sur une ligne de crédit d’entreprise. En tant que commerçant, vous pouvez allouer du crédit pour un compte d’entreprise et gérer les paramètres de crédit pour une entreprise, ainsi que le remboursement du crédit.

## Gestion d&#39;entreprise

La gestion d’entreprise aide les administrateurs commerçants à rationaliser l’administration et la gestion des organisations B2B avec des modèles opérationnels complexes.

À partir de l’administration, les utilisateurs disposant des autorisations appropriées peuvent créer un **[!UICONTROL Company Hierarchy]** qui reflète la structure organisationnelle d’une entreprise composée de plusieurs sociétés. Cette hiérarchie leur permet d’afficher et de gérer les entreprises en tant que groupe. Par exemple, l’administrateur peut désigner une société mère et affecter toutes les sociétés qui opèrent en tant que filiales de la société mère. Ensuite, l&#39;administrateur de la société parent peut afficher et gérer les comptes de société pour toutes les sociétés affectées.

Pour plus d&#39;informations, voir [Gestion des entreprises](manage-companies.md).

## Services pour Adobe Commerce

Les services pour Adobe Commerce sont des services hébergés qui fournissent des fonctionnalités étendues à Adobe Commerce et Magento Open Source. Les services suivants prennent en charge les workflows B2B :

* [Service de catalogue](https://experienceleague.adobe.com/fr/docs/commerce/catalog-service/guide-overview)
* [Recherche en direct](https://experienceleague.adobe.com/fr/docs/commerce/live-search/overview)
* [Recommandations de produit](https://experienceleague.adobe.com/fr/docs/commerce/product-recommendations/guide-overview)
* [Connecteur Adobe Commerce Optimizer](https://experienceleague.adobe.com/fr/docs/commerce/aco-optimizer-connector/overview)

Le [!DNL Adobe Commerce Optimizer Connector] synchronise les données de catalogue et de prix d’Adobe Commerce dans [!DNL Adobe Commerce Optimizer] pour alimenter la découverte de produits, les recommandations et les vitrines découplées pilotées par l’IA, tandis qu’Adobe Commerce reste le système d’enregistrement.

>[!NOTE]
>
>Pour les commerçants B2B, le [!DNL Adobe Commerce Optimizer Connector for B2B] synchronise automatiquement vos catalogues partagés dans [!DNL Adobe Commerce Optimizer] en tant que vues de catalogue protégées, sécurisées par des clés d’accès restreintes, de sorte que l’assortiment de produits et les prix spécifiques au contrat restent synchronisés entre les deux systèmes.

Pour plus d’informations, consultez le [[!DNL Adobe Commerce Optimizer Connector]  Guide d’intégration &#x200B;](https://experienceleague.adobe.com/fr/docs/commerce/aco-optimizer-connector/overview).

## Catalogues partagés

Les catalogues partagés sont les niveaux de prix qui permettent de définir des prix personnalisés par produit pour différentes sociétés sur un ou plusieurs sites web. En utilisant des catalogues partagés, vous pouvez vendre des produits en appliquant différents niveaux de tarification à différents groupes de clients. La prise en charge des catalogues partagés est disponible uniquement pour les magasins Commerce configurés pour prendre en charge les comptes d’entreprise.

Pour plus d’informations, voir [&#x200B; Utilisation de catalogues partagés &#x200B;](catalog-shared.md).

>[!NOTE]
>
>Si l’extension [!DNL Adobe Commerce Optimizer Connector for B2B] est installée, chaque catalogue partagé personnalisé est également projeté en [!DNL Adobe Commerce Optimizer] sous la forme d’une ou de plusieurs vues de catalogue, une par vue de magasin dans le catalogue partagé. Pour plus d’informations, consultez les sections [Gérer la configuration des vues du catalogue](catalog-views-manage.md) et [Surveillance de l’état de synchronisation des vues du catalogue](/help/systems/catalog-view-sync-status.md).

## Commande rapide

Configurez Commande rapide pour réduire le processus de commande à plusieurs clics pour les clients connectés lorsqu’ils connaissent le nom du produit ou le SKU des produits qu’ils souhaitent commander.

Pour plus d&#39;informations, voir [Commandes rapides](quick-order.md).

## Devis Négociables

Utilisez la fonction Devis pour lancer la négociation des prix entre un acheteur et un vendeur de la société.

* Un acheteur autorisé peut lancer un devis à partir du panier.

* Un vendeur peut lancer un devis pour un acheteur auprès de l&#39;administrateur.

Les acheteurs et les vendeurs utilisent le devis pour gérer le processus de négociation (comme l&#39;ajout d&#39;articles, la mise à jour des quantités, la demande et l&#39;application de remises) jusqu&#39;à ce qu&#39;ils parviennent à un accord. La grille _Devis_ de l&#39;administrateur répertorie chaque devis reçu et conserve un historique de la communication entre l&#39;acheteur et le vendeur.

La prise en charge des devis négociables n’est disponible que pour les magasins Commerce configurés pour prendre en charge les comptes d’entreprise.

Pour plus d&#39;informations, voir [Devis négociables](quotes.md).

## Approbations de commande fournisseur

Lorsque les commandes sont activées pour un compte de société, toutes les commandes sont automatiquement créées en tant que commandes. Les utilisateurs de la société disposant des autorisations requises peuvent créer, modifier et supprimer les ordres d&#39;achat qu&#39;ils créent ainsi que les ordres d&#39;achat créés par des utilisateurs subordonnés. En fonction de leur rôle et de la commande, les utilisateurs de l’entreprise peuvent être soumis à plusieurs règles de validation.

Pour plus d&#39;informations, voir [Commandes pour les sociétés](purchase-order-flow.md).

## Listes de demandes d&#39;approvisionnement

Les clients peuvent utiliser la liste de demandes d&#39;approvisionnement pour gagner du temps lors de l&#39;achat de produits fréquemment commandés, car ils peuvent ajouter des articles au panier directement à partir de la liste. Ils peuvent gérer plusieurs listes axées sur les produits de différents fournisseurs, acheteurs, équipes, campagnes ou toute autre activité qui simplifie leur workflow.

Pour plus d&#39;informations, voir [Listes de demandes](requisition-lists.md).
