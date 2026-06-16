---
title: Segments clients
description: Les segments de clients vous permettent d’afficher de manière dynamique du contenu et des promotions à des clients spécifiques.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
TQID: https://experienceleague.adobe.com/K10qvsYlYebR6fJG8-QNI5qrqwjE-Sn-kSxzfiuoXdo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Segments de clients

Les segments de clients vous permettent d’afficher de manière dynamique du contenu et des promotions à des clients spécifiques, en fonction de diverses propriétés. Voici quelques exemples : adresse du client, historique des commandes et contenu du panier. Vous pouvez optimiser les initiatives marketing en fonction de segments ciblés avec les règles de prix des paniers. Vous pouvez également générer des rapports et exporter la liste des clients et clientes ciblés. Comme les informations sur les segments de clients sont constamment actualisées, les clients peuvent être associés et dissociés d’un segment lorsqu’ils font leurs achats dans votre boutique.

Pour mieux comprendre la différence entre les [groupes de clients](../customers/customer-groups.md) et les segments de clients, notez où ils sont utilisés :

|  | Segment client | Groupe de clients |
|--- |--- |--- |
| Règle de prix de catalogue |  | ✔️ |
| Règle de prix du panier | ✔️ | ✔️ |
| Prix de niveau |  | ✔️ |
| Règle de produit associé | ✔️ |  |
| Bloc dynamique | ✔️ |  |
| Taux de change de récompense |  | ✔️ |
| Autorisations de catégorie |  | ✔️ |
| Invitations |  | ✔️ |

{style="table-layout:auto"}

## Attributs de segment des clients

Les attributs de segment des clients sont définis de la même manière que les règles de prix de panier et de catalogue. Pour qu’un attribut soit utilisé dans une condition de segment client, la _[!UICONTROL Use in Customer Segment]_[propriété](attribute-properties.md#) doit être définie sur `Yes`. Les conditions de segment client peuvent incorporer les types d’attributs suivants :

| Attribut | Description |
|---|---|
| `Customer Address Fields` | Vous pouvez définir n’importe quel champ d’adresse, tel que la ville ou le pays. Toute adresse figurant dans le carnet d&#39;adresses d&#39;un client peut répondre à ces conditions afin que le client puisse les faire correspondre. Vous pouvez également indiquer que seules les adresses de facturation ou d’expédition par défaut peuvent être utilisées pour correspondre à un client. Les attributs d’adresse du client ne sont disponibles que pour les clients connectés à leurs comptes. |
| `Customer Information Fields` | Diverses informations sur le client peuvent être définies, notamment le groupe de clients, le nom, l’adresse e-mail, le statut d’abonnement à la newsletter et le solde du crédit de la boutique. Les informations sur les clients ne sont disponibles que pour les clients qui sont connectés à leurs comptes. |
| `Cart Fields` | Les propriétés du panier peuvent être basées sur la quantité (lignes ou quantité totale) ou la valeur (total général, taxe et carte cadeau, par exemple) du contenu du panier. |
| `Products` | Vous pouvez référencer des produits qui se trouvent actuellement dans le panier ou la liste de souhaits, ou qui ont été précédemment consultés ou commandés. Vous pouvez également définir une période au cours de laquelle l’événement s’est produit. Les produits sont définis à l’aide d’attributs de produit. |
| `Order Fields` | Les caractéristiques des commandes passées peuvent être définies en fonction de l’adresse de facturation/d’expédition de la commande, du montant total (ou moyen) ou de la quantité des commandes, ou du nombre total de commandes. Vous pouvez également définir une période pour laquelle elle s’est produite et le statut des commandes correspondant à ces conditions. Disponible uniquement pour les clients et clientes connectés. Les conditions définies pour les acheteurs qui ne sont pas connectés ne fonctionnent plus lorsqu’ils se connectent. |

{style="table-layout:auto"}

Voir [Créer et supprimer des segments clients](../customers/customer-segment-create.md) pour plus d’informations sur la définition des segments clients.

## Livres électroniques

- **Segmentation de la clientèle** — Obtenez le [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) pour découvrir comment augmenter les bénéfices et la satisfaction globale de la clientèle.
- **Tactiques de segmentation** — Obtenez le [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) pour améliorer le ciblage de vos messages et promotions afin de créer des conversations significatives avec vos clients.
