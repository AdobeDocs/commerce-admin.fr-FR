---
title: Commande par SKU
description: Découvrez comment configurer votre boutique pour prendre en charge la commande par SKU à titre de commodité pour vos clients.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Commande par SKU

{{ee-feature}}

Un &quot;SKU&quot; est une &quot;unité de gestion des stocks&quot;. Les SKU aident généralement les vendeurs en ligne à identifier les caractéristiques de produits les plus importantes, telles que : taille, couleur, prix et matière. Les ID de produit diffèrent des SKU :

- `Product ID` est une série séquentielle de nombres qui est utilisée en interne pour identifier les produits et qui n’est pas disponible pour les clients.
- Le `SKU` est généré par le vendeur, normalement en fonction du nom du produit et des attributs pour le marketing ou le suivi interne. Par exemple : T-shirt bleu, coton, taille moyenne : T-COT-MED-BL. Le SKU peut être modifié par le vendeur si nécessaire.

Normalement, un SKU comprend un ensemble d’abréviations indiquant les caractéristiques de distinction du produit. La longueur maximale du SKU est de 64 caractères. Les SKU sont importants pour assurer un suivi et une gestion efficaces des stocks. Par conséquent, leur configuration est essentielle pour le commerce électronique.

_Commande par SKU_ est un [widget](../content-design/widgets.md) qui peut être affiché dans le magasin à titre de commodité pour tous les clients ou mis à la disposition des seuls acheteurs dans des groupes de clients spécifiques. Les acheteurs peuvent saisir le SKU et les informations de quantité directement dans le bloc Commande par SKU ou charger un fichier csv à partir de leur compte client. Quelle que soit la configuration, la commande par SKU est toujours disponible pour les administrateurs de magasin.

![Commande par SKU dans le storefront](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Configuration de la commande par SKU

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Order by SKU Settings]** .

1. Définissez **[!UICONTROL Enable Order by SKU on my Account in Storefront]** sur l’une des options suivantes :

   - `Yes, for Everyone` - Le bloc Commande par SKU est disponible dans le magasin pour chaque acheteur.
   - `Yes, for Specified Customer Groups` - La commande par SKU est disponible uniquement pour les membres d’un groupe de clients spécifique, tel que `Wholesale`.
   - `No` - Le bloc Commande par SKU n’apparaît pas dans le storefront et la page Commande par SKU n’est pas disponible dans le compte client.

   ![Paramètres de commande par SKU](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B uniquement) _&#x200B;**Pour activer la fonction Classer par SKU, désactivez la fonction Ordre rapide :**&#x200B;_

1. Accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL B2B Features]**

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL B2B Features]** .

1. Définissez **[!UICONTROL Enable Quick Order]** sur `No`.

   La [&#x200B; fonction Commande rapide](../b2b/quick-order.md) permet aux clients et aux invités d’effectuer rapidement des commandes en fonction du SKU ou du nom du produit.

## Expérience Storefront

Lorsque la fonctionnalité est configurée pour le magasin, les clients peuvent commander par SKU à partir de n’importe quelle page qui comprend le widget _Commande par SKU_ ou à partir du tableau de bord de leur compte.

### Commande par SKU du bloc de page

1. Dans le bloc _Order by SKU_ , le client saisit les **[!UICONTROL SKU]** et **[!UICONTROL Qty]** de l’article à commander.

1. Pour ajouter un autre élément, cliquez sur **[!UICONTROL Add Row]** et répétez le processus.

1. Clics **[!UICONTROL Add to Cart]**.

### Commande par SKU d’un compte client

1. Depuis le storefront, le client se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Order by SKU]**.

1. Ajoute des éléments individuels en fonction des préférences :

   _&#x200B;**Ajoute chaque élément par SKU :**&#x200B;_

   - Entrez les **[!UICONTROL SKU]** et **[!UICONTROL Qty]** de l’élément à commander.

   - Pour ajouter d’autres éléments selon les besoins, cliquez sur _Ajouter une ligne_ ![Bouton représentant le signe plus](../assets/button-add-item.png) et répète pour autant d’éléments que nécessaire.

   - Clics **[!UICONTROL Add to Cart]**.

   _&#x200B;**Télécharge un fichier CSV de plusieurs éléments :**&#x200B;_

   - Prépare un fichier [&#x200B; de données d’importation CSV](../systems/data-csv.md) (valeur séparée par des virgules) qui comprend des colonnes pour `SKU` et `Qty`.

   ![SKU à importer](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Pour charger le fichier CSV, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier à télécharger.

   - Clics **[!UICONTROL Add to Cart]**.

   Si l’un des produits comporte des options supplémentaires, le client est invité à s’intéresser au produit depuis le panier.

   ![Le produit nécessite de l’attention](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >S’il existe des SKU en double, les quantités sont combinées en une ligne dans le panier. Le client peut modifier la quantité de n’importe quel article et cliquer sur **[!UICONTROL Update Shopping Cart]** pour recalculer les totaux.

