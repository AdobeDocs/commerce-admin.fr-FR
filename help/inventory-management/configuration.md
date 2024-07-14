---
title: "Configure [!DNL Inventory Management]"
description: Découvrez la configuration des options  [!DNL Inventory Management] qui déterminent la disponibilité de la source, les produits storefront et l'expédition des commandes.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configurer [!DNL Inventory Management]

Le module [!DNL Inventory Management] prend en charge les paramètres de configuration de stock au niveau du produit et global et fournit également des paramètres supplémentaires qui affectent la disponibilité de la source, les produits storefront et l’expédition de commandes. Les paramètres de configuration s’appliquent à :

- L’ensemble du catalogue : accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Ensuite, développez **[!UICONTROL Catalog]**dans le panneau de gauche et sélectionnez **[!UICONTROL Inventory]**.

- Produits spécifiques : accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Ouvrez ensuite le produit en mode d’édition et cliquez sur **[!UICONTROL Advanced Inventory]** dans la section _[!UICONTROL Sources]_.

Votre catalogue peut être configuré pour afficher les données d’inventaire dans votre vitrine, gérer les paniers actifs, etc. Affichez la disponibilité de chaque article sous la forme _En stock_ ou _En rupture de stock_ et l’inventaire disponible lorsque le stock est faible.

Le seuil de rupture de stock indique à quel moment un produit doit être réorganisé, soustrait de la quantité vendable d’un stock et peut être défini pour prendre en charge les commandes en arrière-plan activées ou désactivées. Autoriser les commandes en arrière-plan pour votre magasin, en définissant une quantité maximale de commandes pour tous les produits ou des produits spécifiques.

Vous pouvez également utiliser le seuil de disponibilité du stock pour gérer les produits à forte demande. Si vous souhaitez capturer de nouveaux clients, plutôt que de les vendre à des acheteurs en grande quantité, vous pouvez définir une quantité maximale afin d’empêcher un seul acheteur de retirer l’intégralité de votre stock.

![Exemple en stock, seulement 1 à gauche](assets/storefront-stock-options-1-left.png)

## Options de configuration

[!DNL Commerce] magasins et produits prennent en charge les configurations suivantes pour la gestion des produits, des stocks, des notifications, etc. [!DNL Commerce] fournit des paramètres de configuration supplémentaires pour les actions en masse et l’algorithme Priorité de distance.

| Option | Description |
|--|--|
| [!UICONTROL Manage Stock] | Permet à [!DNL Commerce] de gérer tous les stocks. Défini si le contrôle d’inventaire est utilisé pour ce produit ou tous les produits dans [!DNL Commerce]. Affiche d’autres options lorsqu’elles sont définies sur `Yes`. |
| [!UICONTROL Only X left Threshold] | Définit une quantité à avertir lorsqu’un montant spécifique est laissé disponible à l’achat. Ce montant est suivi au niveau des stocks. |
| [!UICONTROL Out-of-Stock Threshold] | Votre stock de sécurité, Quantité pour déclencher une notification d’rupture de stock et atténuer le risque de rupture de stock. Cette valeur affecte les commandes en arrière-plan. Options : <br />**[!UICONTROL No Backorders]**: n’accepte pas les commandes en arrière-plan lorsque le produit est en rupture de stock.<br />**[!UICONTROL Allow Qty Below 0]** : accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro, mais avertit les clients que les commandes peuvent toujours être passées.<br /><br />**[!UICONTROL Backorders disabled]** : il est recommandé de saisir une valeur positive supérieure à 0, par exemple 5 ou 25. <br/>**[!UICONTROL Backorders enabled]**: entrez un seuil négatif pour la quantité maximale de commandes en arrière-plan autorisées, par exemple -5 ou -25. Une valeur de 0 agit comme un stock infini. Une valeur positive est ignorée et traitée comme 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Définit la quantité minimale du produit qui peut être acheté dans une seule commande. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Définit la quantité maximale de produits pouvant être achetés dans une seule commande. |
| [!UICONTROL Qty Uses Decimals] | Permet des nombres décimaux au lieu de nombres entiers pour la quantité d’un produit. Ce paramètre est utile pour les produits vendus en poids, volume ou longueur. Spécifié sur le niveau de Source, calculé sur le niveau Stock en fonction des sources affectées. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Détermine si des parties d’un produit peuvent être expédiées séparément. Cette option est visible lorsque **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Indique si les commandes en arrière-plan sont autorisées. Spécifié sur le niveau de Source, calculé sur le niveau Stock en fonction des sources affectées. S’il est activé pour autoriser les commandes en arrière-plan, il est recommandé de définir une valeur négative pour le seuil d’rupture de stock (voir [Configuration des commandes en arrière-plan](backorders.md)). Options : <br />**[!UICONTROL No Backorders]**: n’accepte pas les commandes en arrière-plan lorsque le produit est en rupture de stock.<br />**[!UICONTROL Allow Qty Below 0]** : accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro, mais avertit les clients que les commandes peuvent toujours être passées. |
| [!UICONTROL Notify for Quantity Below] | Définit la quantité qui déclenche une notification Quantité en dessous , en avertissement de stock faible. Ce montant est déduit de la Quantité vendable, et non de la Quantité d’inventaire. |
| [!UICONTROL Enable Qty Increments] | Détermine si le produit peut être vendu en quantité par incréments. Si cette option est activée, saisissez la quantité de produits à acheter dans une étape incrémentielle. Les incréments définissent le nombre d’articles de produit qui doivent être achetés en tant que produit unique et enfant de produits configurables, regroupés et regroupés. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] n’utilise pas cette valeur. Lorsque vous réalisez un retour ou une note de crédit, la quantité du produit est automatiquement renvoyée à la quantité source affectée. Voir [Configuration des options de produit](product-options.md). |

## Restauration de la configuration et héritage

Les configurations remplacent ou s’appliquent dans le chemin d’héritage suivant : la section _[!UICONTROL Sources]_du produit remplace la configuration globale du magasin_[!UICONTROL Inventory]_ par le produit _[!UICONTROL Advanced Options]_.

Lorsque [!DNL Commerce] recherche des paramètres personnalisés à appliquer, il suit l’ordre suivant :

1. Vérifie les paramètres personnalisés au niveau du produit dans la section _[!UICONTROL Sources]_. Quelques paramètres sont disponibles.

1. Vérifie les paramètres du produit _[!UICONTROL Advanced Inventory]_.

1. Si `Use Config Settings` est sélectionné pour les paramètres du produit, il recherche une valeur dans la page de configuration globale de magasin _Inventory_.

Par exemple, vous pouvez configurer les commandes en arrière-plan différemment dans votre boutique avec une configuration similaire à celle-ci :

- _Globally :_ Activez les commandes en arrière-plan pour le magasin, définissez le Seuil d’absence de stock sur `-50`

- _Produit :_ Désactivez les commandes en arrière-plan pour un produit spécifique, définissez le seuil d’rupture de stock sur `10`
