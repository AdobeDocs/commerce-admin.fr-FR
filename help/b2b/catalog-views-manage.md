---
title: Gérer la configuration de la vue Catalogue
description: Découvrez comment passer en revue les vues de catalogue Adobe Commerce Optimizer créées pour les catalogues partagés B2B et attribuer les clés d’accès restreintes qui les protègent.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: f9f21f675d5c608547db790f33d1aa9be90a36eb
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# Gestion de la configuration de la vue de catalogue

Une fois l’extension [!DNL Adobe Commerce Optimizer Connector for B2B] installée, la page Vues du catalogue répertorie les [!DNL Adobe Commerce Optimizer] [projections des vues du catalogue](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"} créées pour le catalogue partagé personnalisé.  Une _projection_ est la vue de catalogue créée lorsque le connecteur synchronise les données de catalogue partagées avec [!DNL Adobe Commerce Optimizer]. Le connecteur crée une projection distincte pour chaque vue de magasin du catalogue partagé, de sorte qu’un catalogue partagé puisse avoir plusieurs vues de catalogue. Dans les expériences storefront, ces vues de catalogue sont accessibles uniquement aux sociétés affectées au catalogue partagé associé.

Supposons, par exemple, qu’Acme Industrial soit affecté à un catalogue partagé, EU Business, qui appartient au site web de l’UE. Ce site Web propose deux affichages de magasin :

- `English (UK)`

- `German (Germany)`

Le connecteur projette le catalogue partagé en deux vues de catalogue [!DNL Adobe Commerce Optimizer] :

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

L’entreprise a des vues de catalogue en anglais et en allemand, mais une seule affectation de catalogue partagée. Chaque vue de magasin affiche les données de la vue de catalogue correspondante.

Les deux vues de catalogue peuvent partager le même catalogue de prix lorsqu’elles utilisent le même site web et la même portée de tarification du groupe de clients.

## Authentification de la vue Catalogue

Le connecteur protège les vues de catalogue avec des clés d’accès restreintes. Adobe Commerce utilise la clé privée pour signer un jeton d’accès pour un acheteur autorisé. Avant de renvoyer des données de catalogue protégées, [!DNL Adobe Commerce Optimizer] valide le jeton par rapport à la clé publique correspondante associée à la vue de catalogue demandée.

Pour configurer la durée de vie du jeton ou désactiver l’émission du jeton, voir [Services > Vue Catalogue ACO](/help/configuration-reference/services/aco-catalog-view.md).

Vous pouvez examiner ces vues de catalogue et gérer leurs clés affectées à partir de l’onglet _[!UICONTROL Catalog Views]_du catalogue partagé ou de la section_[!UICONTROL Catalog Views]_ de l’entreprise associée ; les deux répertorient les mêmes vues de catalogue et les mêmes affectations de clés actuelles. Consultez [Modifier les clés d’accès restreint](#edit-restricted-access-keys) pour connaître le chemin de navigation exact à partir de chaque emplacement.

Pour surveiller la synchronisation des données de catalogue partagées avec [!DNL Adobe Commerce Optimizer], consultez [Surveillance de l’état de synchronisation des vues du catalogue](/help/systems/catalog-view-sync-status.md).

## Référence des vues de catalogue

{{$include /help/_includes/catalog-views-reference-table.md}}

## Modifier les clés d’accès restreintes

{{$include /help/_includes/edit-restricted-access-keys.md}}

Pour plus d’informations, voir [Gestion des clés d’accès restreint](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Projection de catalogue partagé B2B](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [Services > Vue Catalogue ACO](/help/configuration-reference/services/aco-catalog-view.md)
> - [Surveillance du statut de synchronisation de la vue Catalogue](/help/systems/catalog-view-sync-status.md)
> - [Gérer les catalogues partagés](catalog-shared-manage.md)
> - [Gestion des comptes d’entreprise](account-company-manage.md)
