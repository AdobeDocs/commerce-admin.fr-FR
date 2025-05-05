---
title: Achat et rachat de cartes-cadeaux
description: Découvrez le cycle de vie achat-remboursement des cartes-cadeaux lorsque vous incluez des cartes-cadeaux dans votre catalogue de magasins.
exl-id: ecaa39aa-f504-4bfd-874b-12b44093c2a9
feature: Products, Gift
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Achat et rachat de cartes-cadeaux

{{ee-feature}}

Les cartes-cadeaux sont consommées dans le panier de la même manière qu’un coupon est appliqué à une commande. Pendant le passage en caisse, l’acheteur saisit le code de carte-cadeau pour appliquer un montant de la carte-cadeau à l’achat. Les titulaires d’une carte cadeau qui disposent d’un compte client peuvent vérifier l’état et le solde restant dans le tableau de bord de leur compte. Vous pouvez utiliser des cartes-cadeaux simples et multiples pour payer tout ou partie d’une commande.

Le code de carte-cadeau appliqué peut être affiché en ouvrant la commande dans l’ _Admin_, ce qui vous permet de récupérer le code pour le placer sur une carte-cadeau physique, si nécessaire. Si une commande de carte-cadeau est annulée ou remboursée, vous devez annuler manuellement le compte de carte-cadeau associé. Vous pouvez supprimer entièrement le compte ou le désactiver.

![Détail de carte-cadeau dans le panier](./assets/storefront-gift-card-order-customer-account.png){width="700" zoomable="yes"}

Par exemple, un client qui fait ses achats dans la boutique de démonstration Luma peut acheter une carte-cadeau virtuelle ou physique.

**Carte cadeau virtuelle** - Une carte cadeau virtuelle Luma est envoyée par courrier électronique avec un message facultatif au destinataire. Elle peut être consommée sur n’importe lequel des sites web de la famille Luma et n’expire jamais.

**Carte-cadeau physique** - Une carte-cadeau Luma est emballée dans un courrier électronique d’art personnalisé et envoyée gratuitement au destinataire. Il peut être produit à l’avance, étiqueté avec des codes uniques et consommé en magasin, par téléphone ou sur n’importe quel site Web de la famille Luma. Elle n’expire jamais.

**Carte-cadeau combinée** - Une carte-cadeau combinée possède les caractéristiques d’une carte-cadeau virtuelle et physique. Une carte cadeau Luma est envoyée au destinataire par courrier électronique. L’adresse électronique et l’adresse de livraison sont requises lors de l’achat de la carte-cadeau. Elle n’expire jamais.

## Cycle de vie de la carte cadeau

1. **Le client détermine la valeur de la carte-cadeau**.

   Le client détermine la valeur de la carte-cadeau à partir de la page du produit. Selon la configuration, il existe un champ de prix fixe, une liste d’options de prix, ou les deux. Tous les montants apparaissent dans la devise utilisée dans le magasin.

1. **Le client complète les informations de carte-cadeau**.

   Pour une carte-cadeau physique, le client saisit le **nom de l’expéditeur** et le **nom du destinataire**. Pour les cartes-cadeaux virtuelles ou combinées, le client saisit également les **Email de l’expéditeur** et **Email du destinataire**. Si le client est connecté, le nom de l’expéditeur (et l’adresse électronique de l’expéditeur, le cas échéant) est automatiquement renseigné à partir de son compte. Selon le paramétrage, le client peut également saisir un message à l&#39;intention du destinataire.

1. **Le client termine le passage en caisse**.

   La carte de cadeau apparaît sous forme d’article dans le panier avec le détail qui indique le nom de l’expéditeur, du destinataire et du message, le cas échéant. Le montant associé à la carte-cadeau est converti dans la devise de base de la boutique lorsqu’elle est ajoutée au panier.

1. **Le client reçoit la confirmation de la commande**.

   L’acheteur de la carte-cadeau peut cliquer sur le lien de la confirmation pour effectuer le suivi de la commande depuis le tableau de bord de son compte.

1. **Le destinataire reçoit la carte-cadeau**.

   Pour les cartes-cadeaux virtuelles ou combinées, le destinataire reçoit un email avec le code de carte-cadeau, le nom de l’expéditeur et le message, le cas échéant. Si plusieurs cartes-cadeaux sont achetées dans une seule commande et que le type est virtuel ou combiné, tous les codes de cartes-cadeaux correspondants sont envoyés au destinataire dans un seul e-mail. Les cartes de cadeaux physiques peuvent être expédiées directement au destinataire ou au client, qui peut ensuite lui remettre personnellement la carte de cadeau.

1. **Le destinataire applique une carte-cadeau à l’achat**.

   Le destinataire achète un article dans votre boutique et applique le code de carte-cadeau lors du passage en caisse. Chaque fois qu’une carte-cadeau est appliquée lors du passage en caisse, le montant apparaît dans le bloc de totaux de la commande et est soustrait du total général. Le solde total de chaque carte-cadeau est soustrait du total du panier. Si plusieurs cartes-cadeaux sont utilisées à des fins d’achat, elles sont appliquées dans un ordre croissant, en commençant par la carte dont le solde restant est le plus petit, jusqu’à ce que toutes les cartes soient appliquées ou que le total général soit nul. Lorsque le total général atteint zéro, le dernier compte de carte-cadeau appliqué au panier reçoit une déduction partielle. Les cartes qui n’ont pas été appliquées au panier ne reçoivent pas de déduction du solde. Les montants sont déduits des comptes de carte-cadeau uniquement après la commande.

## Expérience Storefront

Fonctionnement des cartes-cadeaux sur la vitrine :

- Le code de carte-cadeau peut être appliqué dans le panier ou lors du passage en caisse pour couvrir le montant total de la commande.

- Dans le catalogue, une carte-cadeau est présentée comme un type de produit distinct.

- Le code de carte-cadeau est activé après la facturation de la commande. Si la commande n’est pas payée, le client destinataire ne peut pas utiliser la carte cadeau.

- Les comptes des codes cadeau sont créés pour effectuer le suivi du solde d’un bon spécifique. Un administrateur de magasin peut régler manuellement le solde.

Le client destinataire peut utiliser la section _[!UICONTROL Gift Card]_&#x200B;du tableau de bord de son compte pour vérifier le solde de son [compte de carte-cadeau](product-gift-card-accounts.md) et échanger des cartes-cadeaux pour le [crédit de boutique](../customers/store-credit-using.md).

![Carte cadeau](./assets/account-dashboard-gift-card.png){width="700" zoomable="yes"}

### Vérifier l’état et le solde de la carte-cadeau

1. Depuis le storefront, le client se connecte et ouvre sa page de compte client.

1. Le client ouvre la page **[!UICONTROL Gift Card]** et saisit le code de carte-cadeau.

1. Le client clique sur **[!UICONTROL Check status and balance]**.

![Balance des cartes-cadeaux](./assets/gift-balance.png){width="700" zoomable="yes"}

Le solde de la carte cadeau s’affiche.

### Activation de la carte cadeau

1. Sur la page _[!UICONTROL Gift Card]_, le client saisit le code de carte-cadeau.

1. Le client clique sur **[!UICONTROL Redeem Gift Card]**.

![Message concernant l&#39;activation réussie de la carte-cadeau](./assets/gift-redeemed-balance.png){width="700" zoomable="yes"}

Le montant de la carte cadeau est activé et ajouté au solde total du crédit de la boutique.

![Solde du crédit de magasin](./assets/store-credit.png){width="700" zoomable="yes"}

Toutes les opérations relatives au solde des cartes-cadeaux sont disponibles sur la page _[!UICONTROL Store Credit]_.

### Appliquer une carte-cadeau lors du passage en caisse

Si la carte-cadeau n’est pas remboursable, un client peut appliquer le code de carte-cadeau lors du passage en caisse.

1. Au cours de l’étape _Révision et paiements_, le client clique sur **[!UICONTROL Apply Gift Card]**.

1. Entrez le code de la carte-cadeau, puis cliquez sur **[!UICONTROL Apply]**.

   La remise doit être répercutée dans le _[!UICONTROL Order Summary]_.

1. Cliquez sur **[!UICONTROL Place Order]** pour finaliser la commande.
