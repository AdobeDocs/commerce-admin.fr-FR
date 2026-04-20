---
title: Configurer  [!DNL Inventory Management]  commandes en souffrance
description: Découvrez comment configurer les commandes en souffrance pour prendre en charge la vente de produits en rupture de stock.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 837da039e03db94014056fbb4e945c47fa37b7c1
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Configurer les reliquats de [!DNL Inventory Management]

Les reliquats permettent à votre magasin de continuer à vendre des produits une fois que la quantité a atteint zéro ou est effectivement en rupture de stock. Lorsqu’une commande client est une commande en souffrance, les fonds sont autorisés et saisis immédiatement, le statut de traitement de la commande ne change pas et l’expédition reste en attente jusqu’à ce que le stock soit disponible.

Selon votre magasin et vos ventes, vous pouvez activer ou désactiver les commandes en souffrance aux niveaux suivants :

- **[!UICONTROL Global]** - Tous les produits de votre catalogue au niveau du site

- **[!UICONTROL Product]** - Paramètres de remplacement des produits spécifiques pour le site, la source et le stock

## Présentation des paramètres de backorder

Il est vivement recommandé de configurer des seuils et des paramètres spécifiques pour prendre en charge au mieux les commandes en souffrance.

### Seuil de rupture de stock

Utilisez une valeur négative pour ce seuil afin de définir la quantité maximale de produits pouvant faire l&#39;objet d&#39;une mise en reliquat avant que le produit ne soit réellement considéré comme en rupture de stock. Ce montant s&#39;ajoute à la quantité commercialisable. La valeur définie au niveau du produit remplace toute valeur définie au niveau global.

La formule de la quantité vendable est `(Quantity - (Out-of-Stock Threshold))`.

Voici un exemple :

- Quantité : 25
- Notifier pour la quantité ci-dessous : 10
- Seulement X Seuil Gauche : 5
- Seuil de rupture de stock : -50

La quantité commercialisable pour ce produit est `75 (25 - (-50))`.

![Exemple de quantité commercialisable avant l&#39;activation des reliquats](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Exemple de quantité vendable après les reliquats activés](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Lorsque les clients achètent les 25 produits disponibles, de nouvelles commandes sont entrées en tant que reliquats. Comme la quantité vendable du produit est réduite à 5 (70 articles ont été vendus), la page _Produit_ affiche un message `Only 5 left` sur le storefront. Lorsque la quantité vendable atteint `0`, le produit s&#39;affiche comme `Out of Stock` dans le storefront.

>[!NOTE]
>
>Lorsqu&#39;un client passe une commande à l&#39;aide de _[!UICONTROL backorder qty]_, [!DNL Inventory Management] soustrait automatiquement la quantité de la quantité vendable. Si une commande n&#39;est pas expédiée et est annulée, la quantité revient à la quantité vendable virtuelle agrégée. La **_quantité de commande annulée n&#39;est affectée à aucune des origines_**, mais est renvoyée au nombre total de produits disponibles à la vente (colonne&#x200B;_[!UICONTROL Salable Quantity]_ de la grille des produits).

<!--
### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). 
-->

### Statut des stocks

Le statut des produits doit être défini sur `In Stock` lors de l&#39;activation des commandes en souffrance. Vous pouvez définir cette valeur à partir de la page _Product_. Pour les commerçants multi-sources, vous devez avoir au moins une source marquée comme `In Stock`. Accédez au statut et définissez-le via la page _Produit_ et la grille _Sources_ qui lui est affectée.

## Configurer les commandes en souffrance globalement

Ces étapes permettent d’activer les commandes en souffrance pour tous les produits au niveau du site.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Définissez **[!UICONTROL Store View]** sur `Default Config`.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Par **[!UICONTROL Backorders]**, décochez la case **[!UICONTROL Use system value]** et sélectionnez une option :

   | Option | Description |
   | -- | -- |
   | `No Backorders` | Pour ne pas accepter de commandes en souffrance lorsque le produit est en rupture de stock. |
   | `Allow Qty Below 0` | Pour accepter les reliquats lorsque la quantité est inférieure à zéro. |
   | `Allow Qty Below 0 and Notify Customer` | Accepter les commandes en souffrance lorsque la quantité est inférieure à zéro et informer le client que la commande peut toujours être passée. |

1. Par **[!UICONTROL Out-of-Stock Threshold]**, décochez la case **[!UICONTROL Use system value]** et saisissez un montant différent.

   | Valeur | Description |
   | -- | -- |
   | Montant positif | Lorsque Commandes en souffrance est désactivé, saisissez une valeur positive. |
   | Zéro | Lorsque les reliquats sont activés, la saisie de `0` permet de créer un nombre infini de reliquats. |
   | Montant négatif | Lorsque les commandes en souffrance sont activées, il est recommandé de saisir une valeur négative. Le montant est ajouté à la quantité vendable. Par exemple, saisissez `-50` pour autoriser les commandes jusqu&#39;à ce montant. |

1. Cliquez sur **[!UICONTROL Save Config]**.

## Configuration des reliquats d’un produit

Les configurations au niveau du produit remplacent les configurations globales. Vous pouvez configurer les reliquats au niveau du produit pour remplacer les paramètres au niveau du magasin global ou de la source. Par exemple, votre magasin peut prendre en charge les commandes en souffrance dans le monde entier. Avec les paramètres du produit, vous pouvez désactiver les commandes en souffrance ou modifier le seuil de rupture de stock sans affecter d’autres produits et sources.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode **[!UICONTROL Edit]** et faites défiler la page vers le bas jusqu’à la zone _[!UICONTROL Sources]_.

   Pour les produits configurés sans [!DNL Inventory Management], l’onglet n’apparaît pas. Le bouton `Advanced Inventory` s’affiche sous le champ _[!UICONTROL Quantity]_.

1. Cliquez sur **[!UICONTROL Advanced Inventory]**.

   Cette action affiche une page de configurations spécifiques au produit. Tout paramètre répertorié comme `global` affiche le paramètre global actuel du magasin.

1. Par **[!UICONTROL Backorders]**, décochez la case **[!UICONTROL Use Config Setting]** et sélectionnez une option :

   | Option | Description |
   | -- | -- |
   | `No Backorders` | Pour ne pas accepter de commandes en souffrance lorsque le produit est en rupture de stock. |
   | `Allow Qty Below 0` | Pour accepter les reliquats lorsque la quantité est inférieure à zéro. |
   | `Allow Qty Below 0 and Notify Customer` | Accepter les commandes en souffrance lorsque la quantité est inférieure à zéro et informer le client que la commande peut toujours être passée. |

1. Par **[!UICONTROL Out-of-Stock Threshold]**, décochez la case **[!UICONTROL Use Config Setting]** et saisissez un montant :

   | Valeur | Description |
   | -- | -- |
   | Montant positif | Lorsque Commandes en souffrance est désactivé, saisissez une valeur positive. |
   | Zéro | Lorsque les reliquats sont activés, la saisie de `0` permet de créer un nombre infini de reliquats. |
   | Montant négatif | Lorsque les commandes en souffrance sont activées, il est recommandé de saisir une valeur négative. Le montant est ajouté à la quantité vendable. Par exemple, saisissez `-50` pour autoriser les commandes jusqu&#39;à ce montant. |

   ![Inventaire avancé configuré pour les reliquats](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Done]**, puis sur **[!UICONTROL Save]**.
