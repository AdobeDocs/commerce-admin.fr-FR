---
title: Configuration  [!DNL Inventory Management]  options du produit
description: Découvrez comment configurer les options  [!DNL Inventory Management]  configuration du produit.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Configuration des options du produit [!DNL Inventory Management]

Ces configurations s’appliquent uniquement au produit modifié et remplacent toutes les configurations au niveau du site web global. Modifiez ces paramètres lors de la modification d’un produit via la section _[!UICONTROL Sources]_et la page_[!UICONTROL Advanced Inventory]_.

- Configurer les options du produit par source
- Configuration des options de produit pour l&#39;inventaire avancé

## Options du produit par source

Configurez les quantités et les paramètres supplémentaires par [source ajoutée](sources-add.md) pour le produit.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode d’édition.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Sources]** et configurez les paramètres du produit pour chaque source :

   - Saisissez un montant **[!UICONTROL Qty]** (quantité).

   - Définissez la **[!UICONTROL Source Item Status]** sur `In Stock` ou `Out of Stock`.

   - Pour modifier la case à cocher Notifier pour la quantité en dessous par source, décochez ou sélectionnez la case **[!UICONTROL Notify Quantity Use Default]**.

     Si cette option est désactivée, saisissez le montant du niveau de stock qui déclenche l&#39;avis de rupture de stock de l&#39;article. Le montant saisi est soustrait de la quantité vendable de l&#39;article au niveau du stock.

     `Select to use Default` - [!DNL Commerce] vérifie les paramètres de configuration des options d’inventaire avancé du produit.
     `Clear to Modify` - Saisissez une valeur pour la quantité à notifier, en remplaçant les paramètres avancés de configuration du stock et de la boutique.

   ![Section Sources pour un produit](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]**, puis **[!UICONTROL Save]**.

### Descriptions des champs

| Champ | Portée | Description |
|--|--|--|
| [!UICONTROL Source Code] | Global | Code unique d’une [source](sources-manage.md). |
| [!UICONTROL Name] | Global | Nom unique d’une source. |
| [!UICONTROL Status] | Global | Le produit est activé ou désactivé dans le catalogue. |
| [!UICONTROL Source Item Status] | Global | Détermine la disponibilité actuelle du produit. Options :<br />`In Stock` - Rend le produit disponible à l’achat.<br />`Out of Stock` - Sauf si les commandes en souffrance sont activées, empêche l&#39;achat du produit et supprime la liste du catalogue. |
| [!UICONTROL Qty] | Global | Montant du stock disponible pour chaque origine ou emplacement. |
| [!UICONTROL Notify Quantity] | Global | Montant de la _[!UICONTROL Notify for Quantity Below]_pour cette source spécifique si_[!UICONTROL Notify Quantity Use Default]_ n’est pas sélectionné. |
| [!UICONTROL Notify Quantity Use Default] | Global | Indique d’utiliser le paramètre par défaut pour les _[!UICONTROL Notify for Quantity Below]_dans la_[!UICONTROL Advanced Inventory]_ de produit ou le paramètre global dans la configuration du magasin. |

## Options de produit avancées

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode d’édition.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Sources]** et cliquez sur **[!UICONTROL Advanced Inventory]**.

1. Pour activer le [contrôle des stocks](enable.md) pour votre catalogue, définissez **[!UICONTROL Manage Stock]** sur `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] paramètres des produits enfants remplacent ceux d’un produit configurable.

   ![Inventaire avancé d&#39;un produit](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Saisissez un montant pour le **[!UICONTROL Out-of-Stock Threshold]** :

   | Valeur | Description |
   | ----- | ----- |
   | Montant positif | Lorsque l’option _[!UICONTROL Backorders]_est désactivée, saisissez une valeur positive. |
   | Zéro | Lorsque l’option _[!UICONTROL Backorders]_est activée, la saisie de `0` permet un nombre infini de reliquats. |
   | Montant négatif | Lorsque _[!UICONTROL Backorders]_est activé, il est recommandé de saisir une valeur négative. Le montant est ajouté à la quantité vendable. Par exemple, saisissez `-50` pour autoriser les commandes jusqu&#39;à ce montant. |

1. Saisissez le **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Saisissez le **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Définissez **[!UICONTROL Qty uses Decimals]** sur `Yes` si les clients peuvent utiliser une valeur décimale plutôt qu&#39;un nombre entier lors de la saisie de la quantité commandée.

1. Définissez **[!UICONTROL Allow Multiple Boxes for Shipping]** sur `Yes` si le produit peut être vendu séparément, dans de nombreuses boîtes. Cette option est visible lorsque **[!UICONTROL Qty Uses Decimals]** est défini sur `Yes` uniquement.

1. Définissez **[!UICONTROL Backorders]** sur l’une des options suivantes :

   | Option | Description |
   | ----- | ----- |
   | `No Backorders` | Pour ne pas accepter de commandes en souffrance lorsque le produit est en rupture de stock. |
   | `Allow Qty Below 0` | Pour accepter les reliquats lorsque la quantité est inférieure à zéro. |
   | `Allow Qty Below 0 and Notify Customer` | Accepter les commandes en souffrance lorsque la quantité est inférieure à zéro et informer le client que la commande peut toujours être passée. |

   Pour plus d&#39;informations, voir [Configuration des reliquats](backorders.md).

1. Pour activer les incréments de quantité pour le produit, définissez **[!UICONTROL Enable Qty Increments]** sur `Yes` et saisissez le numéro des articles qui doivent être achetés pour répondre au besoin dans le champ **[!UICONTROL Qty Increments]**.

   Par exemple, un article vendu par incréments de six peut être acheté en quantités de 6, 12, 18, etc.

   **[!UICONTROL Qty Increments]** champ définit le nombre d’articles de produit qui doivent être achetés en tant que produit unique, et en tant qu’enfant de produits configurables, groupés et groupés.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!UICONTROL Save]**.

### Descriptions des champs

| Champ | Portée | Description |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Détermine si le contrôle de stock est utilisé pour gérer ce produit dans votre catalogue. Définissez pour activer ou désactiver toutes les fonctionnalités [!DNL Inventory Management]. Lorsque vous effectuez un retour ou un avoir, la quantité de produit est automatiquement renvoyée à la quantité d&#39;origine affectée. Il peut être préférable de désactiver ce système si vous utilisez un système ERP tiers. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Détermine le niveau de stock auquel un produit est considéré comme en rupture de stock. Options:<br />Valeur positive - Lorsque les reliquats sont désactivés, saisissez un montant positif.<br />Zéro (0) - Lorsque les reliquats sont activés, la saisie de zéro permet d’obtenir un nombre infini de reliquats.<br />Valeur négative - Lorsque les reliquats sont activés, il est recommandé de saisir un montant négatif. Le montant est ajouté à la quantité vendable. Par exemple, saisissez `-50` pour autoriser les commandes jusqu&#39;à ce montant. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Détermine le nombre minimum de produits pouvant être achetés dans une seule commande. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Détermine le nombre maximal de produits pouvant être achetés dans une seule commande. |
| [!UICONTROL Qty Uses Decimals] | Global | Détermine si les clients peuvent utiliser une valeur décimale plutôt qu&#39;un nombre entier lors de la saisie de la quantité commandée. Options:<br />`Yes` - Permet de saisir des valeurs sous la forme de décimales plutôt que de nombres entiers. Les décimales conviennent aux produits vendus en poids, en volume ou en longueur.<br />`No` - Nécessite que les valeurs de quantité soient saisies sous forme de nombres entiers. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Détermine si des parties du produit peuvent être expédiées séparément. Cette option est visible lorsque **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Détermine comment les reliquats sont gérés. Les reliquats ne modifient pas le statut de traitement de la commande. Les fonds sont toujours autorisés ou saisis immédiatement lorsque la commande est passée, que le produit soit en stock ou non. Les produits sont expédiés au fur et à mesure de leur disponibilité. Lorsque cette option est activée, il est recommandé de saisir un montant négatif pour le seuil de rupture de stock. Options : <br/>`No Backorders` - N’accepte pas les reliquats lorsque le produit est en rupture de stock.<br />`Allow Qty Below 0` - Accepte les reliquats lorsque la quantité est inférieure à zéro.<br />`Allow Qty Below 0 and Notify Customer` - Accepte les commandes en souffrance lorsque la quantité est inférieure à zéro, mais informe les clients que des commandes peuvent toujours être passées. |
| [!UICONTROL Enable Qty Increments] | Global | Détermine si le produit peut être vendu par incréments de quantité. Les incréments définissent le nombre d’articles à acheter en tant que produit unique, et en tant qu’enfant de produits configurables, groupés et groupés. |

>[!NOTE]
>
>Une configuration de produit simple remplace les configurations de produit configurables pour un produit spécifique.
