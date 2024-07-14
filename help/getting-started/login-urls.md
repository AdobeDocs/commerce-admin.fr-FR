---
title: Identifiants de connexion et URL
description: Découvrez les URL Commerce et les informations d’identification du compte utilisées pour accéder à votre administrateur et à votre vitrine.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Identifiants de connexion et URL

Avant de procéder à la configuration et à la configuration, assurez-vous de disposer des informations nécessaires pour accéder à l’administrateur de votre boutique et à votre compte Commerce.

## URL de storefront

L’adresse de votre [storefront](storefront.md) correspond généralement au domaine attribué à votre adresse IP. Certains magasins sont installés à la racine ou dans le répertoire le plus élevé. D’autres sont installés dans un répertoire sous la racine. Le magasin peut se trouver dans un sous-domaine associé à un domaine principal. L’URL de votre magasin peut se présenter comme suit :

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Si vous ne disposez pas encore d’un domaine, l’URL de votre magasin comprend une série de quatre nombres, chacun séparé par un point de la notation _quad pointillé_.

## URL d’administration

L’adresse de votre boutique [Admin](admin.md) est configurée pendant l’installation. L’adresse par défaut est la même que votre boutique, mais `/admin` à la fin. Bien que les exemples de ce guide utilisent le répertoire par défaut, il est recommandé d’exécuter l’administrateur à partir d’un emplacement propre à votre boutique.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## Compte [!DNL Commerce]

Votre [compte Commerce](commerce-account-create.md) permet d’accéder à des informations sur vos produits et services, les paramètres de compte, l’historique de facturation et les ressources d’assistance. Pour accéder à votre compte, accédez au site Commerce principal et cliquez sur **[!UICONTROL My Account]** dans le coin supérieur droit.

## Compte client

Pendant que vous découvrez le magasin, veillez à configurer un [compte client](../customers/account-dashboard.md) de test afin de pouvoir tester le processus de stockage et de passage en caisse du point de vue du client.

## Exemples de données

Adobe fournit un jeu de données d’exemple qui comprend un exemple de magasin avec plus de 250 produits (environ 200 d’entre eux sont des produits configurables), des catégories, des règles de prix promotionnel, des pages CMS, des bannières, etc. Les exemples de données utilisent le thème _Luma_ sur le storefront. [L’installation de ces données d’exemple](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) est facultative, mais peut s’avérer utile pour tester et développer des personnalisations pour votre entreprise d’e-commerce.
