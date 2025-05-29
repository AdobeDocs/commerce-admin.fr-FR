---
title: Ventes et événements privés
description: Découvrez comment utiliser les ventes privées et d’autres événements de catalogue pour augmenter les ventes auprès de votre base de clients existante et générer du buzz et de nouveaux prospects.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Ventes et événements privés

{{ee-feature}}

Les ventes privées et d’autres événements de catalogue sont un excellent moyen d’utiliser votre base de clients existante pour générer du buzz et de nouveaux prospects, ou pour écouler l’excédent de stock. Vous pouvez créer des ventes à durée limitée, limiter les ventes à des membres spécifiques ou créer une page de vente privée autonome. Vous pouvez également définir des invitations et des détails d’événement. Augmentez la fidélité à la marque et générez un buzz en offrant à vos meilleurs clients le traitement VIP. Offrez un accès exclusif aux ventes des membres uniquement ou aux ventes privées pour accroître la fidélité à la marque. Vous pouvez également utiliser ces ventes pour liquider les marchandises excédentaires. Les groupes de clients sont utiles pour configurer ces types de membres uniquement et les ventes VIP.

![Exemple de storefront - événement sur la page d’accueil](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Composants de la gestion des événements

- **Catégories** - Chaque événement est associé à une [catégorie](../catalog/category-create.md) de votre catalogue.

- **Événements** - Les ventes d’événements sont basées sur une date de début et une date de fin. Vous pouvez utiliser un [compte à rebours](#event-ticker) pour afficher le temps restant.

- **Carrousel d’événement de catalogue** - Lorsque le [widget d’événement de catalogue](../content-design/widget-event-carousel.md) est activé dans la configuration, il peut être placé sur les pages de la boutique sous la forme d’une liste des événements ouverts et à venir, triés par date de fin. Si plusieurs événements ont la même date de fin, les événements sont triés en fonction de l’ordre spécifié dans la configuration.

- **[!UICONTROL Websites]** - Les autorisations de catégorie sont principalement basées sur [groupes de clients](../customers/customer-groups.md).

- **Autorisations de catégorie** - [Autorisations de catégorie](../catalog/category-permissions.md) vous donne un contrôle total sur les activités spécifiques qui peuvent avoir lieu dans une catégorie donnée.

- **Restrictions d’accès** - Empêche le public [d’accéder](event-configure.md#restrict-access) au site en le redirigeant vers une page de destination, une page de connexion ou une page d’enregistrement.

- **Invitations** - Les e-mails sont envoyés avec un lien pour créer un compte dans la boutique. Vous pouvez limiter la possibilité de créer un compte aux seules personnes qui reçoivent une [invitation](invitations.md).

- **Rapports des ventes privées** - Les [Rapports des ventes privées](../getting-started/private-sales-reports.md) fournissent des informations sur les invitations envoyées, les clients invités et les conversions.

## Indicateur d’événement

Le bloc de suivi affiche un compte à rebours pour les événements ouverts, avec les dates de début et de fin des événements à venir. Si un événement est clos, le ticker affiche les dates de début et de fin.

![Exemple de storefront - carrousel d’événement](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Si l’indicateur de page de catégorie est activé pour un événement, le bloc d’indicateur s’affiche en haut de la liste des catégories. Si l’indicateur de page de produit est activé, le bloc d’indicateur s’affiche également en haut de la page de produit de tout produit associé à la catégorie.

Le marqueur d’événement peut être activé lorsque vous [créez des événements](event-create.md).

![Exemple de storefront - barre latérale de l’événement](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
