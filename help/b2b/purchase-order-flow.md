---
title: Commandes fournisseur pour les entreprises
description: Découvrez les workflows de bon de commande qui permettent aux entreprises de suivre et de contrôler les dépenses.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
TQID: https://experienceleague.adobe.com/YNQaayS05dNl3qUfoIUh2vqY3H3yTA32nt7rXmORF7A
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 947
ht-degree: 0%

---

# Commandes fournisseur pour les entreprises

Les bons de commande (PO) sont un moyen courant pour les entreprises de suivre et de contrôler les dépenses. [ Bon de commande ](../stores-purchase/purchase-order.md) est l’une des méthodes de paiement hors ligne standard prises en charge dans Adobe Commerce et Magento Open Source. Lorsque B2B d’Adobe Commerce est installé et que l’option [_Activer les commandes_](account-company-manage.md#advanced-settings) est activée pour un compte d’entreprise, toutes les commandes sont automatiquement créées en tant que commandes. Les utilisateurs de la société disposant des [autorisations](account-company-roles-permissions.md) requises peuvent créer, modifier et supprimer les ordres d&#39;achat qu&#39;ils créent ainsi que les ordres d&#39;achat créés par des utilisateurs subordonnés.

## Flux de commande fournisseur

En fonction de leur rôle et de la commande, les utilisateurs de l’entreprise peuvent être soumis à plusieurs règles de validation. Et selon que vous utilisez des méthodes de paiement en ligne ou hors ligne, le flux est légèrement différent. Les administrateurs d&#39;entreprise peuvent créer des commandes automatiquement, en contournant les règles d&#39;approbation. Le stockage des détails de paiement en ligne pendant le processus d&#39;approbation posant un risque de sécurité, ces détails sont ajoutés après approbation, puis la commande fournisseur est convertie en commande réelle.

![Flux de commande fournisseur](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Une commande ne peut pas être passée si un ou plusieurs produits de la commande fournisseur sont actuellement désactivés ou en rupture de stock.

Le workflow de bon de commande d’une entreprise peut varier de plusieurs façons :

- Si aucune règle d&#39;approbation n&#39;est définie, les commandes fournisseur peuvent être passées et la commande traitée directement.

  >[!NOTE]
  >
  >Par défaut, un message `Purchase order has been submitted for approval` s’affiche toujours pour les utilisateurs et utilisatrices de l’entreprise, même si aucune règle de validation n’est définie. Lorsqu’aucun processus d’approbation n’est requis, les utilisateurs de l’entreprise reçoivent automatiquement un e-mail les informant que la commande a été créée et approuvée.

- Si les règles d’approbation sont définies par l’administrateur de l’entreprise, les utilisateurs passent par le processus d’approbation.
- Si plusieurs règles d&#39;approbation s&#39;appliquent à une commande fournisseur, tous les approbateurs requis uniques doivent l&#39;approuver.
- Les détails de paiement hors ligne sont saisis lors de la création de la commande fournisseur.
- Les détails de paiement en ligne sont saisis une fois la commande fournisseur approuvée.

>[!NOTE]
>
>Les commandes fournisseur créent un _instantané_ des prix d&#39;article, des remises et des prix d&#39;expédition au moment où la commande a été créée. Si le prix d&#39;un article change après la création de la commande, le prix d&#39;origine est utilisé.

### Exemple de workflow de base

Les entreprises utilisent les commandes pour contrôler les achats que les employés peuvent effectuer pour le compte de l&#39;entreprise et configurent souvent des règles d&#39;approbation pour appliquer les directives de l&#39;entreprise. Selon les règles d’approbation, plusieurs personnes peuvent être amenées à approuver la commande.

1. L’utilisateur crée une commande pour des marchandises d’une valeur de 25 000 $.
1. Leur responsable doit approuver.
1. Comme la commande est supérieure à 10 000 $, le vice-président doit également l&#39;approuver.
1. Selon le mode de paiement, après les approbations, la commande est automatiquement convertie en commande ou l&#39;utilisateur revient pour saisir les détails du paiement.

### Règles d&#39;approbation

Les règles d’approbation sont utilisées pour contrôler les dépenses en fonction des directives de l’entreprise. Voici quelques exemples de règles de validation :

- Toute commande de plus de 100 $ nécessite l&#39;approbation de votre gestionnaire.
- Toute commande supérieure à 1 000 $ nécessite l&#39;approbation de votre gestionnaire et de l&#39;administrateur de l&#39;entreprise.
- Toute commande comportant plus de 30 SKU uniques doit être approuvée par l’administrateur de l’entreprise.

Une fois ces règles en place pour une entreprise, un utilisateur de l’entreprise peut terminer la commande immédiatement lorsque celle-ci est inférieure à 100 $. Pour en savoir plus sur la définition des règles d&#39;approbation, voir [ Règles d&#39;approbation ](account-dashboard-approval-rules.md).

### Types d’utilisateurs et d’utilisatrices du magasin

Le workflow de bon de commande peut également être différent selon la personne qui effectue l’achat.

- Un employé régulier peut être soumis à toutes les règles d&#39;approbation
- Un gestionnaire pourrait avoir plus de pouvoir d&#39;achat et aurait des règles d&#39;approbation différentes
- Les administrateurs de l’entreprise peuvent contourner toutes les règles d’approbation et laisser leurs bons de commande être exécutés automatiquement.

Tous ces facteurs peuvent avoir une influence sur le processus exact de passage en caisse.

## [!UICONTROL My Purchase Orders]

Lorsque les commandes fournisseur sont activées pour une société, l’élément **[!UICONTROL My Purchase Orders]** s’affiche dans le panneau de gauche pour les clients connectés à un compte utilisateur de société. Trois onglets fournissent différentes listes de bons de commande et fonctions :

- **[!UICONTROL My Purchase Orders]** : commandes créées par le client.
- **[!UICONTROL Company Purchase Orders]** : commandes passées par des utilisateurs subordonnés au sein de la société (dépend de la structure et des rôles de la société).
- **[!UICONTROL Requires My Approval]** : (visible pour les approbateurs désignés) commandes en attente d&#39;approbation par le client. Le compteur indique le nombre de commandes en attente d&#39;approbation.

![Mes commandes fournisseur](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Pour plus d’informations sur les fonctions de bon de commande prises en charge disponibles pour les utilisateurs de la société sur le storefront, voir [Mes bons de commande](account-dashboard-my-purchase-orders.md).

## Modes de paiement hors ligne et en ligne

Les workflows peuvent varier en fonction du mode de paiement. Pour en savoir plus sur les modes de paiement Adobe Commerce, consultez [Modes de paiement](../stores-purchase/payments.md) dans le _Guide de l’expérience client et d’achat_.

>[!IMPORTANT]
>
>Les commandes fournisseur doivent utiliser une expérience de passage en caisse _In-Context_. Les extractions _hors contexte_ ne sont pas prises en charge, car elles contournent le flux d’extraction normal. En règle générale, _In-Context_ signifie que le client reste sur votre site commercial pour terminer le processus. _hors contexte_ désigne le moment où le client est redirigé vers un autre site pour effectuer l’achat.

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
- Paiement à la livraison
- Virements bancaires
- Crédit de la boutique
