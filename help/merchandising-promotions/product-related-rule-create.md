---
title: Création d’une règle de produit associée
description: Découvrez comment créer une règle de produit associée qui peut être déclenchée pour afficher les produits associés, les ventes incitatives et les ventes croisées.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: cea943cd7f4d148c885fbd113c3bc08bfdf63ea0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Création d’une règle de produit associée

{{ee-feature}}

Le processus de création d’une règle de produit associée est similaire à la configuration d’une règle de prix. Tout d’abord, vous définissez les conditions à remplir, puis choisissez les produits à afficher. À tout moment, plusieurs règles actives peuvent être déclenchées pour afficher les produits associés, les ventes incitatives et les ventes croisées. La priorité de chaque règle détermine l’ordre dans lequel le bloc de produits s’affiche sur la page.

>[!NOTE]
>
>Pour qu’un attribut soit utilisé dans une règle ciblée, la propriété [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) doit être définie sur `Yes`.

>[!NOTE]
>
>La valeur de portée `All Store Views` est toujours utilisée pour les conditions [!UICONTROL Products to Match] et [!UICONTROL Products to Display] de tous les attributs de produit. Cela s’applique également lorsque les attributs de produit ont des valeurs différentes pour différents sites web et vues de magasin.

## Création d’une règle de produit associée

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Rule]**.

   ![Règle de produits associés - information](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Complétez le **[!UICONTROL Rule Information]** comme suit :

   - Saisissez un **[!UICONTROL Rule Name]** pour identifier la règle lorsque vous utilisez l’administrateur.

   - Pour **[!UICONTROL Priority]**, saisissez un nombre qui détermine l’ordre dans lequel les résultats apparaissent sur la page lorsque les résultats d’autres règles ciblent le même emplacement. Le nombre `1` est la priorité absolue.

   - Pour activer la règle, définissez **[!UICONTROL Status]** sur `Active`.

   - Définissez **[!UICONTROL Apply To]** sur l’une des options suivantes :

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Si la règle doit être active pendant une période spécifique, saisissez les dates **[!UICONTROL From]** et **[!UICONTROL To]**.

   - Pour **[!UICONTROL Result Limit]**, saisissez le nombre d&#39;enregistrements à afficher dans la liste des résultats. Le nombre maximal est 20.

   - Si la règle s’applique à un [segment client](../customers/customer-segments.md) spécifique, définissez **[!UICONTROL Customer Segments]** sur `Specified` et sélectionnez le segment client dans la liste.

   - Si la règle s’applique à une [audience Real-Time CDP](../customers/audience-activation.md) spécifique, définissez **[!UICONTROL Real-Time CDP Audience]** sur `Specified` et sélectionnez l’audience Real-Time CDP dans la liste. Cette fonctionnalité est en version bêta. Si vous souhaitez rejoindre le programme bêta, envoyez une demande à [dataconnection@adobe.com](mailto:dataconnection@adobe.com).

     ![Règle de produits associés - Audience Real-Time CDP](./assets/rtcdp-related-products.png){width="500"}

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Products to Match]** et créez les conditions comme vous le feriez pour une [règle de prix de catalogue](price-rules-catalog.md).

   ![Règle de produits associés - produits à faire correspondre](./assets/catalog-related-products-match.png){width="500"}

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Products to Display]** et créez les conditions de résultats comme vous le feriez pour une [règle de prix du catalogue](price-rules-catalog.md).

   ![Règle de produits associés - produits à afficher](./assets/catalog-related-products-to-display.png){width="500"}

   Renseignez la condition pour décrire les produits que vous souhaitez inclure dans les résultats affichés.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Suppression d’une règle de produit associée

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Recherchez la règle de produit associée que vous souhaitez supprimer.

1. Cliquez sur la règle pour ouvrir la page de détails.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Démonstration des règles de produit associées

Regardez cette vidéo pour en savoir plus sur la création de règles de produit connexes :

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Rule Name] | Nom qui identifie la règle à des fins d’utilisation interne. |
| [!UICONTROL Priority] | Détermine la séquence dans laquelle les résultats de la règle apparaissent lorsqu’ils sont affichés avec d’autres ensembles de résultats qui ciblent le même emplacement sur la page. La valeur peut être définie sur n’importe quel nombre, avec la priorité la plus élevée de 1. Par exemple, s’il existe plusieurs règles de vente incitative qui s’appliquent, celle qui a la priorité la plus élevée apparaît avant les autres. L’ordre de tri des produits dans chaque ensemble de résultats est aléatoire. Les produits de vente incitative, de vente croisée et associés configurés manuellement apparaissent toujours sur la page avant toute promotion de produits basée sur des règles. |
| [!UICONTROL Status] | Contrôle l’état actif de la règle. Options : `Active` / `Inactive` |
| [!UICONTROL Apply To] | Identifie le type de relation de produit associé à la règle. Options : `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Si la règle est active pendant une période donnée, ce paramètre détermine la première date à laquelle elle est active. |
| [!UICONTROL To Date] | Si la règle est active pendant une période donnée, ce paramètre détermine la dernière date à laquelle elle est active. |
| [!UICONTROL Result Limit] | Détermine le nombre de produits qui apparaissent simultanément dans les résultats. Le nombre maximal est 20. Si d’autres résultats correspondants sont trouvés, les produits font pivoter le bloc à chaque actualisation de la page. |
| [!UICONTROL Customer Segments] | Identifie les segments de clients auxquels s’applique la règle. Options : `All` / `Specified` |

{style="table-layout:auto"}
