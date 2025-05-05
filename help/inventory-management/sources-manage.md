---
title: Gestion des sources d’inventaire
description: Découvrez les sources et comment elles définissent les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes, ou où les services sont disponibles.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Gestion des sources

Les sources sont les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes ou où les services sont disponibles. Il peut s’agir d’entrepôts, de magasins en briques et de mortiers, de centres de distribution, de lieux de ramassage et d’expéditeurs. Vous allouez les quantités d&#39;inventaire à ces sources, et [!DNL Commerce] agrège automatiquement le total des produits commercialisables de vos stocks. Pour les grandes entreprises, ajoutez plusieurs sources pour tous vos emplacements : dans différents emplacements géographiques par pays et par continent, emplacements dans une ville, en fonction du type d’inventaire, même en fonction des services.

Il est recommandé de fournir des emplacements géographiques spécifiques lors de la création d’une source. Cela permet à l’ _algorithme de priorité de distance_ de comparer l’emplacement de l’adresse de destination de livraison avec les emplacements source disponibles afin de déterminer la source la plus proche pour accomplir les chargements. Vous pouvez utiliser des cartes Google ou des calculs hors ligne qui utilisent des codes géographiques. Pour plus d’informations sur cet _algorithme de priorité des distances_, voir [ Configuration de l’algorithme de priorité des distances](distance-priority-algorithm.md).

Commencez par un _Source par défaut_ que vous pouvez mettre à jour mais pas désactiver. Cette source est utilisée par les marchands à source unique et pour la migration de produits. Vous avez toujours besoin d’une source par défaut.

- **Informations sur l’emplacement** - Chaque source inclut le nom, le pays, l’adresse physique de l’emplacement et un point de contact.
- **Activation des ressources** - Vous pouvez activer et désactiver des sources selon vos besoins. N’activez une source que si elle accepte et exécute des commandes et des commandes en arrière-plan.
- **Inventaire disponible** - Attribuez et mettez à jour les quantités d’inventaire pour chaque source via la page de produits. Les quantités d&#39;inventaire sont calculées, fournies et réservées via le mapping source et stock.

Le diagramme suivant illustre les sources pour un marchand de vélos qui vend un vélo tout-terrain, disponible pour les stocks et accessible par l&#39;ASS pour les envois.

![Exemple de diagramme de sources](assets/diagram-sources.png){width="600" zoomable="yes"}

Tous les magasins commencent par une Source par défaut qui doit rester activée :

- Tous les nouveaux produits importés dans [!DNL Commerce] nécessitent une source et un stock, automatiquement attribués pour un accès immédiat à [!DNL Inventory Management].
- Les marchands à source unique utilisent le Source par défaut comme point unique de l’emplacement du stock et des envois.

## Modifier les sources

Vous pouvez mettre à jour le nom, l’adresse, l’emplacement GPS et les informations sur le point de contact. Le code de la source est une valeur protégée, agissant comme un identifiant unique associant la source à vos quantités et stocks de produits.

Si vous modifiez le Source par défaut, vous pouvez modifier toutes les configurations, à l’exception du nom et du code. Il est recommandé que les marchands à source unique ajoutent des informations correspondant à leur emplacement.

La page _[!UICONTROL Manage Sources]_&#x200B;répertorie tous les emplacements d’inventaire et toutes les installations d’exécution disponibles. Vous pouvez ajouter de nouvelles sources d’inventaire et modifier des emplacements existants.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Pour ajouter un emplacement d’inventaire, voir [Ajout d’un nouveau Source](sources-add.md).

1. Recherchez la source d’inventaire et ouvrez-la en mode _Édition_ .

1. Mettez à jour les informations et enregistrez les modifications.

   ![Gérer les sources](assets/inventory-sources.png){width="600" zoomable="yes"}

## Barre de boutons

| Bouton | Description |
|--|--|
| [!UICONTROL Add New Source] | Ouvre le nouveau formulaire Source utilisé pour saisir une nouvelle source d’inventaire, une nouvelle fonctionnalité d’exécution ou un nouvel emplacement. |

## Gestion des descriptions des colonnes de sources

| Colonne | Description |
|--|--|
| [!UICONTROL Code] | Code alphanumérique unique utilisé par le système pour identifier la source de l’inventaire. |
| [!UICONTROL Name] | Nom unique qui identifie la source de stock pour les utilisateurs administrateurs. |
| [!UICONTROL Is Enabled] | Indique si la source d’inventaire est active et disponible à utiliser. |
| [!UICONTROL Pickup Location] | Indique si la source est active comme emplacement de récupération pour la [diffusion en magasin](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Cliquez sur **[!UICONTROL Edit]** pour ouvrir l’enregistrement de source de stock en mode d’édition. |

## Autres colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Latitude] | Indique la coordonnée de latitude de la source d’inventaire pour le GPS. Saisissez la valeur sous la forme d’un nombre, précédé d’un signe plus ou moins, si nécessaire. Le symbole du diplôme et les lettres ne sont pas autorisés. Par exemple : `32.7555` |
| [!UICONTROL State/Province] | État ou province où se trouve la source. |
| [!UICONTROL Postcode] | Code postal de la source. |
| [!UICONTROL Email] | Adresse électronique du contact principal. |
| [!UICONTROL Longitude] | Indique la coordonnée de longitude la source d’inventaire pour le GPS. Saisissez la valeur sous la forme d’un nombre, précédé d’un signe plus ou moins, si nécessaire. Le symbole du diplôme et les lettres ne sont pas autorisés. Par exemple : Longitude -97.3308 |
| [!UICONTROL City] | Ville où se trouve la source. |
| [!UICONTROL Phone] | Numéro de téléphone du contact principal. |
| [!UICONTROL Country] | Pays où se trouve la source. |
| [!UICONTROL Street] | Adresse postale de la source. |
| [!UICONTROL Fax] | l&#39;indicatif régional et le numéro de fax du contact principal. |
