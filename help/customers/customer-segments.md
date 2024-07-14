---
title: Segments de client
description: Les segments de clients vous permettent d’afficher dynamiquement le contenu et les promotions à des clients spécifiques.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Segments des clients

Les segments Clients vous permettent d’afficher dynamiquement le contenu et les promotions à des clients spécifiques, en fonction de différentes propriétés. L’adresse du client, l’historique des commandes et le contenu du panier sont quelques exemples. Vous pouvez optimiser les initiatives marketing basées sur des segments ciblés avec des règles de prix de panier. Vous pouvez également générer des rapports et exporter la liste des clients ciblés. Les informations sur les segments de clients étant constamment actualisées, les clients peuvent être associés et dissociés d’un segment lorsqu’ils font leurs achats dans votre boutique.

Pour mieux comprendre la différence entre les [groupes de clients](../customers/customer-groups.md) et les segments de clients, notez où ils sont utilisés :

|  | Segment de client | Groupe de clients |
|--- |--- |--- |
| Règle de prix du catalogue |  | ✔️ |
| Règle de prix du panier | ✔️ | ✔️ |
| Prix de niveau |  | ✔️ |
| Règle de produit associée | ✔️ |  |
| Bloc dynamique | ✔️ |  |
| Taux de récompense des exchanges |  | ✔️ |
| Autorisations de catégorie |  | ✔️ |
| Invitations |  | ✔️ |

{style="table-layout:auto"}

## Attributs de segment des clients

Les attributs de segment des clients sont définis d’une manière similaire aux règles de prix du panier et du catalogue. Pour qu’un attribut soit utilisé dans une condition de segment client, la _[!UICONTROL Use in Customer Segment]_[propriété](attribute-properties.md#) doit être définie sur `Yes`. Les conditions de segment client peuvent incorporer les types d’attributs suivants :

| Attribut | Description |
|---|---|
| `Customer Address Fields` | Vous pouvez définir n’importe quel champ d’adresse, tel que la ville ou le pays. Toute adresse du carnet d’adresses d’un client peut remplir ces conditions pour que le client corresponde. Vous pouvez également indiquer que seules les adresses de facturation ou de livraison par défaut peuvent être utilisées pour faire correspondre un client. Les attributs d’adresse du client sont disponibles uniquement pour les clients connectés à leurs comptes. |
| `Customer Information Fields` | Diverses informations sur les clients peuvent être définies, notamment le groupe client, le nom, l’adresse électronique, l’état d’abonnement au bulletin d’information et le solde du crédit de magasin. Les informations sur les clients ne sont disponibles que pour les clients connectés à leurs comptes. |
| `Cart Fields` | Les propriétés du panier peuvent être basées sur la quantité (éléments de ligne ou quantité totale) ou la valeur (total général, taxe et carte-cadeau) du contenu du panier. |
| `Products` | Vous pouvez référencer des produits qui se trouvent actuellement dans le panier ou la liste de souhaits, ou qui ont déjà été consultés ou commandés. Vous pouvez également définir une période au cours de laquelle elle s’est produite. Les produits sont définis à l’aide d’attributs de produit. |
| `Order Fields` | Les caractéristiques des commandes des commandes passées peuvent être définies en fonction de l’adresse de facturation/d’expédition de la commande, du montant total (ou moyen) ou de la quantité des commandes, ou du nombre total de commandes. Vous pouvez également définir une période pour le moment où elle s’est produite et l’état de la commande des commandes qui correspondent à ces conditions. Disponible uniquement pour les clients connectés. Les conditions définies pour les acheteurs qui ne sont pas connectés arrêtent de fonctionner lorsqu’ils se connectent. |

{style="table-layout:auto"}

Voir [Création et suppression de segments de clients](../customers/customer-segment-create.md) pour plus d’informations sur la définition de segments de clients.

## Livres électroniques

- **Segmentation des clients** — Procurez-vous le [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) pour découvrir comment augmenter les bénéfices et la satisfaction globale du client.
- **Tactiques de segmentation** — Procurez-vous le [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) pour améliorer le ciblage de vos messages et promotions afin de créer des conversations significatives avec vos clients.
