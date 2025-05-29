---
title: Identifiants de connexion et URL
description: Découvrez les URL Commerce et les informations d’identification de compte utilisées pour accéder à votre administrateur et à votre storefront.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Identifiants de connexion et URL

Avant de poursuivre l’installation et la configuration, assurez-vous de disposer des informations requises pour accéder à l’administrateur de votre boutique et de votre compte Commerce.

## URL de Storefront

L’adresse de votre [storefront](storefront.md) est généralement le domaine attribué à votre adresse IP. Certains magasins sont installés dans le répertoire racine ou le répertoire le plus élevé. D’autres sont installés dans un répertoire situé sous la racine. Le magasin peut résider dans un sous-domaine associé à un domaine principal. L’URL de votre boutique peut ressembler à l’une des suivantes :

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`

Si vous ne disposez pas encore d’un domaine, l’URL de votre boutique comprend une série de quatre nombres, séparés chacun par un point dans la notation _quad pointillé_.

## URL de l’administrateur

L’adresse de votre boutique [Admin](admin.md) est configurée lors de l’installation. L’adresse par défaut est identique à celle de votre boutique, mais avec `/admin` à la fin. Bien que les exemples de ce guide utilisent le répertoire par défaut, il est recommandé d’exécuter votre administrateur à partir d’un emplacement propre à votre magasin.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## compte [!DNL Commerce]

Votre compte [Commerce](commerce-account-create.md) permet d&#39;accéder à des informations sur vos produits et services, les paramètres de votre compte, l&#39;historique de facturation et les ressources d&#39;assistance. Pour accéder à votre compte, accédez au site Commerce principal et cliquez sur **[!UICONTROL My Account]** dans le coin supérieur droit.

## Compte client

Pendant que vous vous familiarisez avec le magasin, veillez à configurer un [compte client](../customers/account-dashboard.md) de test afin de pouvoir découvrir le magasin et le processus de passage en caisse du point de vue du client.

## Données d’exemple

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Adobe fournit un jeu de données d’exemple qui comprend un magasin d’exemple avec plus de 250 produits (dont environ 200 sont des produits configurables), des catégories, des règles de prix promotionnels, des pages CMS, des bannières, etc. Les exemples de données utilisent le thème _Luma_ sur le storefront. [L’installation de ces exemples de données](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=fr) est facultative, mais peut s’avérer utile pour tester et développer des personnalisations pour votre entreprise d’e-commerce.
