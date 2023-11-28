---
title: Gestion des sources d’inventaire
description: Découvrez les sources et comment elles définissent les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes, ou où les services sont disponibles.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Gestion des sources

Les sources sont les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes ou où les services sont disponibles. Il peut s’agir d’entrepôts, de magasins en briques et de mortiers, de centres de distribution, de lieux de ramassage et d’expéditeurs. Vous allouez les quantités d’inventaire à ces sources, et [!DNL Commerce] agrège automatiquement le total des produits vendables de vos stocks. Pour les grandes entreprises, ajoutez plusieurs sources pour tous vos emplacements : dans différents emplacements géographiques par pays et par continent, emplacements dans une ville, en fonction du type d’inventaire, même en fonction des services.

Il est recommandé de fournir des emplacements géographiques spécifiques lors de la création d’une source. Cela permet à la variable _Algorithme de priorité des distances_ pour comparer l’emplacement de l’adresse de destination de livraison avec les emplacements de source disponibles afin de déterminer la source la plus proche pour effectuer les envois. Vous pouvez utiliser des cartes Google ou des calculs hors ligne qui utilisent des codes géographiques. Pour plus d’informations à ce sujet _Algorithme de priorité des distances_, voir [Configuration de l’algorithme de priorité des distances](distance-priority-algorithm.md).

Commencer par un _Source par défaut_ que vous pouvez mettre à jour, mais pas désactiver. Cette source est utilisée par les marchands à source unique et pour la migration de produits. Vous avez toujours besoin d’une source par défaut.

- **Informations sur l’emplacement** - Chaque source comprend le nom, le pays, l’adresse physique de l’emplacement et un point de contact.
- **Activation des ressources** - Vous pouvez activer et désactiver les sources selon vos besoins. N’activez une source que si elle accepte et exécute des commandes et des commandes en arrière-plan.
- **Inventaire disponible** - Attribuez et mettez à jour les quantités d’inventaire pour chaque source via la page de produits. Les quantités d&#39;inventaire sont calculées, fournies et réservées via le mapping source et stock.

Le diagramme suivant illustre les sources pour un marchand de vélos qui vend un vélo tout-terrain, disponible pour les stocks et accessible par l&#39;ASS pour les envois.

![Schéma des sources d’exemple](assets/diagram-sources.png){width="600" zoomable="yes"}

Tous les magasins commencent par une source par défaut qui doit rester activée :

- Tous les nouveaux produits importés dans [!DNL Commerce] nécessitent une source et un stock, automatiquement affectés pour un accès immédiat à [!DNL Inventory Management].
- Les marchands à source unique utilisent la source par défaut comme point unique de l’emplacement du stock et des envois.

## Modifier les sources

Vous pouvez mettre à jour le nom, l’adresse, l’emplacement GPS et les informations sur le point de contact. Le code de la source est une valeur protégée, agissant comme un identifiant unique associant la source à vos quantités et stocks de produits.

Si vous modifiez la source par défaut, vous pouvez modifier toutes les configurations, à l’exception du nom et du code. Il est recommandé que les marchands à source unique ajoutent des informations correspondant à leur emplacement.

La variable _[!UICONTROL Manage Sources]_répertorie tous les emplacements d’inventaire et les installations d’exécution disponibles. Vous pouvez ajouter de nouvelles sources d’inventaire et modifier des emplacements existants.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Pour ajouter un emplacement de stock, voir [Ajout d’une nouvelle source](sources-add.md).

1. Recherchez la source d’inventaire et ouvrez-la dans _Modifier_ mode .

1. Mettez à jour les informations et enregistrez les modifications.

   ![Gérer les sources](assets/inventory-sources.png){width="600" zoomable="yes"}

## Barre de boutons

| Bouton | Description |
|--|--|
| [!UICONTROL Add New Source] | Ouvre le formulaire Nouvelle source utilisé pour saisir une nouvelle source d’inventaire, une nouvelle fonctionnalité d’exécution ou un nouvel emplacement. |

## Gestion des descriptions des colonnes de sources

| Colonne | Description |
|--|--|
| [!UICONTROL Code] | Code alphanumérique unique utilisé par le système pour identifier la source de l’inventaire. |
| [!UICONTROL Name] | Nom unique qui identifie la source de stock pour les utilisateurs administrateurs. |
| [!UICONTROL Is Enabled] | Indique si la source d’inventaire est active et disponible à utiliser. |
| [!UICONTROL Pickup Location] | Indique si la source est active en tant qu’emplacement de récupération pour [diffusion en magasin](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Cliquer **[!UICONTROL Edit]** ouvre l’enregistrement source de stock en mode d’édition. |

## Autres colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Latitude] | Indique la coordonnée de latitude de la source d’inventaire pour le GPS. Saisissez la valeur sous la forme d’un nombre, précédé d’un signe plus ou moins, si nécessaire. Le symbole du diplôme et les lettres ne sont pas autorisés. Par exemple: `32.7555` |
| [!UICONTROL State/Province] | État ou province où se trouve la source. |
| [!UICONTROL Postcode] | Code postal de la source. |
| [!UICONTROL Email] | Adresse électronique du contact principal. |
| [!UICONTROL Longitude] | Indique la coordonnée de longitude la source d’inventaire pour le GPS. Saisissez la valeur sous la forme d’un nombre, précédé d’un signe plus ou moins, si nécessaire. Le symbole du diplôme et les lettres ne sont pas autorisés. Par exemple : Longitude -97.3308 |
| [!UICONTROL City] | Ville où se trouve la source. |
| [!UICONTROL Phone] | Numéro de téléphone du contact principal. |
| [!UICONTROL Country] | Pays où se trouve la source. |
| [!UICONTROL Street] | Adresse postale de la source. |
| [!UICONTROL Fax] | l&#39;indicatif régional et le numéro de fax du contact principal. |
