---
title: Prix minimal annoncé
description: Découvrez comment utiliser la fonction de prix annoncé minimum (MAP) pour rester en conformité avec les exigences du fabricant avec des prix spéciaux.
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/DRNm0PPX81W4jzLnu7ALhJ1lQZYUpTcO6ojp1E50vto
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1143
ht-degree: 0%

---

# Prix minimal annoncé

Il est parfois interdit aux commerçants d&#39;afficher un prix inférieur au prix de détail suggéré par le fabricant. Le prix minimum annoncé (MAP) vous permet de rester en conformité avec les exigences du fabricant tout en offrant à vos clients un meilleur prix. Comme les exigences varient d’un fabricant à l’autre, vous pouvez configurer votre boutique pour empêcher l’affichage de votre prix réel sur les pages où il n’est pas autorisé.

La fonction MAP ajoute un lien dédié _Cliquez pour voir le prix_ au lieu du prix normal du produit. Si le prix de votre magasin est inférieur au prix minimum défini pour ce produit, il existe deux façons de gérer les informations de prix sur le storefront. La première est que le prix n&#39;est pas affiché. Si l&#39;acheteur clique sur le bouton _Cliquer pour connaître le prix_, le prix réel auquel vous vendez le produit devient visible. La deuxième méthode consiste à afficher le prix courant/de marché avec un trait barré pour souligner que votre prix est inférieur.

En outre, la fonction MAP vous permet de suggérer quelques améliorations. Par exemple, lorsqu’un client ajoute un tel produit au panier, il n’est pas redirigé vers le panier. À la place, des offres s’affichent pour permettre à l’acheteur de :

- Supprimer un article du panier (cela peut être fait si l&#39;acheteur souhaite simplement clarifier le prix et n&#39;a pas encore pris de décision d&#39;achat)

- Laissez-le dans leur panier et continuez à magasiner

- Passer en caisse

## Logique de mappage

Certains produits ont des prix qui dépendent d’une option sélectionnée, comme des options personnalisées ou des produits simples avec leurs propres SKU et leur propre gestion des stocks). Pour ces produits, la logique suivante est appliquée, en fonction du type de produit et de la définition du prix. Le prix réel est utilisé par la gestion des commandes, les outils de gestion des clients et les rapports.

## Utilisation de MAP avec des types de produits

| Type de produit | Description |
|--- |--- |
| [Simple](product-create-simple.md), [Virtuel](product-create-virtual.md) | Le prix réel n’apparaît pas automatiquement dans la liste de catalogues et les pages de produits, mais est inclus uniquement en fonction du paramètre [!UICONTROL Display Actual Price]. Les prix des options personnalisées s&#39;affichent normalement. |
| [Regroupé](product-create-grouped.md) | Les prix des produits simples associés n’apparaissent pas automatiquement dans la liste de catalogues et les pages de produits, mais sont inclus uniquement en fonction du paramètre [!UICONTROL Display Actual Price]. |
| [Configurable](product-create-configurable.md) | Le prix réel n’apparaît pas automatiquement dans la liste de catalogues et les pages de produits, mais est inclus uniquement en fonction du paramètre [!UICONTROL Display Actual Price]. Les prix des options apparaissent normalement. |
| [Offre groupée](product-create-bundle.md) (à prix fixe) | Le prix réel n’apparaît pas automatiquement sur les pages du catalogue, mais est inclus uniquement en fonction du paramètre [!UICONTROL Display Actual Price]. Les prix des articles groupés apparaissent normalement. MAP n’est pas disponible pour les produits groupés avec une tarification dynamique. |
| [Téléchargeable](product-create-downloadable.md) | Le prix réel n’apparaît pas automatiquement dans la liste de catalogues et les pages de produits, mais est inclus uniquement en fonction du paramètre [!UICONTROL Display Actual Price]. Le prix associé à chaque lien de téléchargement s’affiche normalement. |

{style="table-layout:auto"}

## Utilisation de MAP avec les paramètres de prix

| Paramétrage des prix | Description |
|--- |--- |
| Prix principal | Lorsque MAP est appliqué au prix principal, les prix des options, des articles groupés et des produits associés (qui ajoutent ou soustraient du prix principal) apparaissent normalement. |
| Prix du produit associé | Si un produit n’a pas de prix principal et que son prix est dérivé des prix de produit associés (comme dans un produit groupé), les paramètres MAP des produits associés sont appliqués. |
| [MSRP](product-price-minimum-advertised.md) | Si le prix de détail suggéré par le fabricant (PDSF) d&#39;un produit du panier est spécifié, le prix n&#39;est pas biffé. |
| [Prix de niveau](product-price-tier.md) | Si la tarification de niveau est définie, le message de tarification de niveau ne s’affiche pas dans le catalogue. Sur la page des produits, une notification s’affiche indiquant que le prix peut être inférieur lors d’une commande supérieure à une certaine quantité, mais la remise s’affiche en pourcentages uniquement. Pour les produits associés d’un produit regroupé, les remises ne s’affichent pas sur la page du produit. Le prix du niveau s’affiche en fonction du paramètre Afficher le prix réel . |
| [Prix spécial](product-price-special.md) | Si le prix spécial est spécifié, il est affiché en fonction du paramètre Afficher le prix réel. |

## Configuration du MAPPAGE

La fonction Prix minimum annoncé (MAP) n’est pas activée par défaut. Si vous souhaitez ajouter cette fonctionnalité à votre boutique, vous devez l’activer et configurer les paramètres MAP pour vos produits. Les paramètres MAP peuvent être appliqués à tous les produits de votre catalogue ou configurés pour des produits spécifiques. Lorsque MAP est activé globalement, tous les prix des produits du storefront sont masqués. Il existe différentes options de configuration que vous pouvez utiliser pour rester en conformité avec les termes de votre accord avec le fabricant, tout en offrant à vos clients un meilleur prix.

![Le Prix Réel Apparaît « Par Gestes »](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

Au niveau global, vous pouvez activer ou désactiver MAP, l&#39;appliquer à tous les produits, définir comment le prix réel est affiché. Vous pouvez également modifier le texte des messages associés et des conseils d’informations qui apparaissent dans le magasin.

Lorsque MAP est activé, les paramètres de MAP au niveau du produit sont disponibles. Vous pouvez appliquer le MAP à un produit individuel en saisissant le MSRP et en choisissant comment vous souhaitez que le prix réel apparaisse dans le magasin. Les paramètres MAP au niveau du produit remplacent les paramètres MAP globaux.

![Cliquer pour voir le prix](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### Étape 1 : activer MAP pour la vue de magasin

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Le cas échéant, définissez **[!UICONTROL Store View]** dans le coin supérieur droit de la vue où la configuration s’applique.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _[!UICONTROL Minimum Advertised Price]_.

1. Si nécessaire, définissez **Activer MAP** sur `Yes`.

   ![Configuration de MAP](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options de configuration, voir [_Prix minimum annoncé_](../configuration-reference/sales/sales.md#minimum-advertised-price) dans la _Référence de configuration_.

### Étape 2 : Configurer les paramètres MAP

Utilisez l’une des méthodes suivantes pour configurer les paramètres MAP :

#### Méthode 1 : configurer MAP pour tous les produits

1. Pour déterminer quand et où vous souhaitez que le prix réel soit visible pour les clients, procédez comme suit :

   - Pour modifier la valeur par défaut, désélectionnez la case **[!UICONTROL Use system value]**.

   - Définissez **Afficher le prix réel** sur l’une des options suivantes :
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. Saisissez le texte qui doit apparaître dans le **[!UICONTROL Default Popup Text Message]**.

1. Saisissez toute explication supplémentaire que vous souhaitez afficher dans le **[!UICONTROL Default "What's This" Text Message]**.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

#### Méthode 2 : configuration de MAP pour un seul produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. Ouvrez le produit en mode **[!UICONTROL Edit]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced Settings]** et choisissez **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >Les champs [!UICONTROL Manufacturer's Suggested Retail Price] et [!UICONTROL Display Actual Price] s’affichent uniquement lorsque [Prix minimum annoncé](../configuration-reference/sales/sales.md#minimum-advertised-price) est activé dans la configuration.

1. Saisissez le **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP).

   Dans cet exemple, le prix du produit est de 54,00 $ et le PDSF est de 59,95.

   ![Prix de détail suggéré par le fabricant](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Display Actual Price]** sur l’une des options suivantes :

   - `Use config` - (par défaut) Applique les paramètres d’affichage tels que [configurés](../configuration-reference/sales/sales.md#minimum-advertised-price) pour le magasin. |
   - `On Gesture` : affiche le prix réel du produit dans une fenêtre contextuelle lorsque le client clique sur le _Cliquer pour voir le prix_ ou _Qu’est-ce que c’est ?_ lien.
   - `In Cart` - Affiche le prix réel du produit dans le panier.
   - `Before Order Confirmation` - Affiche le prix réel du produit à la fin du processus de passage en caisse, juste avant la confirmation de la commande.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!UICONTROL Save]**.
