---
title: Commandes fournisseur pour les entreprises
description: Découvrez les workflows de bon de commande qui permettent aux entreprises de suivre et de contrôler les dépenses.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: 4b34645377102e890779059e57c61cf23f71f34c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Commandes fournisseur pour les entreprises

Les bons de commande sont un moyen courant pour les entreprises de suivre et de contrôler les dépenses. [Bon de commande](../stores-purchase/purchase-order.md) est l’une des méthodes de paiement hors ligne standard prises en charge dans Adobe Commerce et Magento Open Source. Lorsque le B2B d’Adobe Commerce est installé et [_Activer les commandes fournisseur_](account-company-manage.md#advanced-settings) est activé pour un compte d’entreprise. Toutes les commandes sont automatiquement créées en tant que commandes (PO). Utilisateurs de l’entreprise avec les [autorisations](account-company-roles-permissions.md) peut créer, modifier et supprimer des ordres d&#39;achat qu&#39;il crée et des ordres d&#39;achat créés par des utilisateurs subordonnés.

## Flux de commande fournisseur

En fonction de leur rôle et de la commande, les utilisateurs de l’entreprise peuvent être soumis à plusieurs règles de validation. Et selon que vous utilisez des méthodes de paiement en ligne ou hors ligne, le flux est légèrement différent. Les administrateurs d’entreprise peuvent créer des commandes automatiquement, en contournant les règles d’approbation. Le stockage des détails de paiement en ligne pendant le processus d&#39;approbation posant un risque de sécurité, ces détails sont ajoutés après approbation, puis la commande fournisseur est convertie en commande réelle.

![Flux de commande fournisseur](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Une commande ne peut pas être passée si un ou plusieurs produits de la commande fournisseur sont actuellement désactivés ou en rupture de stock.

Le workflow de bon de commande d’une société peut varier de plusieurs façons :

- Si aucune règle d&#39;approbation n&#39;est définie, les commandes fournisseur peuvent être passées et la commande traitée directement.

  >[!NOTE]
  >
  >Par défaut, une `Purchase order has been submitted for approval` Le message est toujours affiché pour les utilisateurs de l’entreprise, même si aucune règle de validation n’est définie. Lorsqu’aucun processus d’approbation n’est requis, les utilisateurs de l’entreprise reçoivent automatiquement un e-mail les informant que la commande a été créée et approuvée.

- Si les règles d’approbation sont définies par l’administrateur de l’entreprise, les utilisateurs passent par le processus d’approbation.
- Les détails de paiement hors ligne sont saisis lors de la création de la commande fournisseur.
- Les détails du paiement en ligne sont saisis une fois la commande fournisseur approuvée.

>[!NOTE]
>
>Les bons de commande créent un _instantané_ des prix d&#39;article, remises et prix d&#39;expédition au moment de la création de la commande. Si le prix d&#39;un article change après la création de la commande, le prix d&#39;origine est utilisé.

### Exemple de workflow de base

Les entreprises utilisent les commandes pour contrôler ce que les employés peuvent acheter pour le compte de l&#39;entreprise et configurent souvent des règles d&#39;approbation pour appliquer les directives de l&#39;entreprise. Selon les règles d’approbation, plusieurs personnes peuvent être amenées à approuver la commande.

1. L’utilisateur crée une commande pour des marchandises d’une valeur de 25 000 $.
1. Leur responsable doit approuver.
1. Étant donné que la commande est supérieure à 10 000 $, le vice-président doit également approuver.
1. En fonction du mode de paiement, après les approbations, la commande est automatiquement convertie en commande ou l&#39;utilisateur renvoie pour saisir les détails du paiement.

### Règles d&#39;approbation

Les règles d’approbation sont utilisées pour contrôler les dépenses en fonction des directives de l’entreprise. Voici quelques exemples de règles de validation :

- Toute commande de plus de 100 $ nécessite l&#39;approbation de votre gestionnaire.
- Toute commande supérieure à 1 000 $ nécessite l&#39;approbation de votre gestionnaire et de l&#39;administrateur de l&#39;entreprise.
- Toute commande comportant plus de 30 SKU uniques doit être approuvée par l’administrateur de l’entreprise.

Une fois ces règles en place pour une entreprise, un utilisateur de l’entreprise peut passer la commande immédiatement lorsque celle-ci est inférieure à 100 $. Pour en savoir plus sur la définition des règles d&#39;approbation, voir [Règles d&#39;approbation](account-dashboard-approval-rules.md)

### Types d’utilisateurs et d’utilisatrices du magasin

Le workflow de bon de commande peut également être différent selon la personne qui effectue l’achat.

- Un employé régulier peut être soumis à toutes les règles d&#39;approbation
- Un gestionnaire pourrait avoir plus de pouvoir d&#39;achat et aurait des règles d&#39;approbation différentes
- Les administrateurs de l’entreprise peuvent contourner toutes les règles d’approbation et laisser leurs commandes fournisseur être exécutées automatiquement.

Tous ces facteurs peuvent avoir une influence sur le processus exact de passage en caisse.

## [!UICONTROL My Purchase Orders]

Lorsque les commandes fournisseur sont activées pour une société, la **[!UICONTROL My Purchase Orders]** élément s’affiche dans le panneau de gauche pour les clients connectés à un compte utilisateur d’entreprise. Trois onglets fournissent différentes listes de bons de commande et fonctions :

- **[!UICONTROL My Purchase Orders]**: commandes d’achat créées par le client.
- **[!UICONTROL Company Purchase Orders]**: commandes effectuées par des utilisateurs subordonnés au sein de l’entreprise (dépend de la structure et des rôles de l’entreprise).
- **[!UICONTROL Requires My Approval]**: (visible pour les approbateurs désignés) commandes en attente d&#39;approbation par le client. Le compteur indique le nombre de commandes en attente d&#39;approbation.

![Mes commandes](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Pour plus d’informations sur les fonctions de bon de commande prises en charge disponibles pour les utilisateurs de la société sur le storefront, voir [Mes commandes](account-dashboard-my-purchase-orders.md).

## Modes de paiement hors ligne et en ligne

Les workflows peuvent varier en fonction du mode de paiement. Pour en savoir plus sur les modes de paiement Adobe Commerce, voir [Modes de paiement](../stores-purchase/payments.md) dans le _Guide de l’expérience d’achat et de vente_.

>[!IMPORTANT]
>
>Les commandes fournisseur doivent utiliser une _In-Context_ expérience de passage en caisse. _Hors contexte_ les passages en caisse ne sont pas pris en charge, car ils contournent le flux de passage en caisse normal. En général, _In-Context_ signifie que le client reste sur votre site de commerce pour terminer le processus. _Hors contexte_ est le moment où le client est redirigé vers un autre site pour terminer l’achat.

### Paiements en ligne

Pour des raisons de sécurité, les boutiques en ligne ne souhaitent généralement pas collecter les informations de carte de crédit de la boutique en attendant la fin du processus d’approbation. Par conséquent, si une option de paiement en ligne est sélectionnée, le créateur de la commande fournisseur revient au magasin après approbation, saisit les détails de paiement et termine la commande. Voici quelques exemples de paiements en ligne :

- Cartes de crédit/débit
- PayPal
- Braintree

>[!IMPORTANT]
>
>L’utilisation de cartes-cadeaux, de points de crédit ou de récompense en magasin avec des méthodes de paiement en ligne pour les bons de commande n’est pas prise en charge. L’activation de ces fonctionnalités avec les paiements en ligne peut entraîner un comportement inattendu. Il est recommandé de désactiver les cartes-cadeaux, les crédits en magasin et les points de récompense lorsque les paiements en ligne sont activés pour les bons de commande.

### Paiements hors ligne

Comme les méthodes de paiement hors ligne, telles qu’un mandat, sont gérées en dehors du site web, elles sont plus sûres. Les commandes fournisseur avec paiements hors ligne peuvent être traitées automatiquement, après tout processus d&#39;approbation.

Voici quelques exemples de paiements hors ligne :

- Chèque/Mandat
- Paiement sur le compte
- Contre remboursement
- Virements bancaires
- Crédit de la boutique
