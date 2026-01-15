---
title: Tarification par niveau
description: Découvrez comment utiliser la tarification de niveau pour offrir une remise sur la quantité à partir d’une liste de produits ou d’une page produit.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Tarification par niveau

La tarification de niveau vous permet d’offrir une remise sur la quantité à partir d’une liste de produits ou d’une page de produits dans le storefront. La remise peut être appliquée à une vue de magasin spécifique, à un groupe de clients ou à un catalogue partagé.

Si vous avez de nombreux produits à mettre à jour, il est plus efficace d’importer les modifications de prix de niveau plutôt que de les saisir individuellement. Pour plus d&#39;informations, voir [Importer les prix de niveau](../systems/data-import-price-tier.md).

![Hiérarchiser le prix sur une page produit de storefront](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

La page Produit calcule la remise sur quantité et affiche un message tel que :

`Buy 6 for $5.95 each and save 15%`

Les prix dans le storefront ont la priorité de la quantité la plus élevée à la quantité la plus faible. Si vous avez un prix de niveau pour la quantité `5` et un pour `10`, et qu&#39;un client ajoute cinq, six, sept, huit ou neuf articles au panier, il reçoit le prix réduit pour la quantité `5` niveau. Lorsque le client ajoute le dixième article, le prix réduit spécifié pour la quantité `10` niveau remplace le niveau pour une quantité de `5`, et le prix réduit pour `10` s&#39;applique.

## Ajouter un niveau de prix pour un produit

1. Ouvrez le produit en mode d’édition.

1. Sous le champ _[!UICONTROL Price]_, cliquez sur **[!UICONTROL Advanced Pricing]**.

1. Dans la section _[!UICONTROL Tier Price]_, cliquez sur **[!UICONTROL Add]**.

   Si vous créez un niveau de plusieurs prix, cliquez sur **[!UICONTROL Add]** pour chaque niveau supplémentaire afin de pouvoir travailler sur tous les niveaux en même temps. Chaque niveau du groupe a le même site web et le même groupe de clients ou l’affectation de catalogue partagée, mais une quantité et un prix différents.

## Configurer le niveau de prix

1. Si votre boutique comporte plusieurs sites web, choisissez le **[!UICONTROL Website]** auquel s’applique la tarification de niveau .

1. Si nécessaire, limitez la disponibilité du niveau tarifaire en sélectionnant le **[!UICONTROL Customer Group]** ou le **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) Disponible avec [Adobe Commerce B2B](./b2b/../introduction.md) uniquement).

1. Par **[!UICONTROL Qty]**, saisissez la quantité qui doit être commandée pour recevoir la remise.

   - **Méthode 1 :** Entrez le prix sous la forme d&#39;un montant fixe

     Définissez **[!UICONTROL Price]** sur `Fixed` et saisissez le prix ajusté pour une unité à ce niveau.

     ![Prix de niveau en tant que montant fixe](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Entrez le prix en pourcentage

     Définissez **[!UICONTROL Price]** sur `Discount` et saisissez le prix réduit en pourcentage du prix de base du produit.

     Par exemple, pour une remise de 15 %, saisissez le nombre `15`. (Le prix est enregistré avec deux décimales, par exemple `15.00`.)

     >[!NOTE]
     >
     >Pour obtenir le prix réduit, le pourcentage défini est calculé par rapport à la valeur définie dans le champ _[!UICONTROL Price]_, et non dans le champ&#x200B;_[!UICONTROL Special Price]_ .

     ![Prix de niveau en pourcentage](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Terminer la configuration des prix

1. Pour ajouter un autre ensemble de niveaux de tarification pour un autre site web ou groupe de clients, répétez les étapes précédentes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Le prix du produit **_final_** est calculé comme étant le prix pertinent **_minimum_** selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit ne sont _pas_ affectées par les règles Prix du groupe, Prix de niveau, Prix spécial ou Prix catalogue.

## Activer la tarification de niveau pour les règles de prix de catalogue

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

[!BADGE &#x200B; Sandbox &#x200B;]{type=Caution tooltip="Les éléments répertoriés ne sont actuellement disponibles que dans les environnements Sandbox. Adobe commence par rendre les nouvelles versions disponibles dans les environnements Sandbox afin que vous disposiez du temps nécessaire pour tester les modifications à venir avant que la version ne soit disponible dans les environnements de production."}

Dans les versions précédentes de Commerce, la tarification de niveau ne pouvait pas être utilisée conjointement avec les règles de prix de catalogue. Les règles de catalogue ont ignoré la configuration du prix de niveau et ont calculé les remises uniquement à partir du prix de base d’origine. Avec Adobe Commerce as a Cloud Service, vous pouvez désormais choisir d’inclure la tarification de niveau dans le calcul des règles de prix de catalogue.

Pour activer cette fonctionnalité :

1. Accédez à **[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]** et définissez le champ **[!UICONTROL Apply Catalog Price Rule on Grouped Price]** sur **[!UICONTROL Yes]**.

   ![Activer la tarification de niveau pour les règles de prix de catalogue](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. Définissez un prix de niveau avec une quantité de `1` pour chaque groupe de clients ou catalogue partagé spécifique (tel que `Wholesale`, `Retail` ou groupe défini par le commerçant) que vous souhaitez cibler avec des règles de prix de catalogue. Le groupe de clients `ALL GROUPS` et `Default` catalogue partagé ne peuvent pas être utilisés à cet effet. La tarification de niveau n&#39;est activée pour aucun groupe pour lequel aucun prix de niveau n&#39;est défini avec une quantité de `1`.

1. Définissez des prix de niveau supplémentaire avec des quantités supérieures à `1` selon les besoins. Ces prix de niveau supplémentaire seront appliqués comme d’habitude lorsque le client ajoute des quantités supplémentaires du produit dans le panier. Les règles de prix de catalogue ne s’appliqueront pas à ces prix de niveau supplémentaire.

Pour illustrer le fonctionnement de la tarification de niveau avec les règles de prix de catalogue lors de l’achat d’un seul produit, prenons l’exemple suivant :

- Le prix de base standard d&#39;un produit est de 100 USD.
- Un prix de niveau est défini pour le groupe de clients `Wholesale` avec une quantité de `1` et un prix fixe de 90 USD.
- Une règle de prix catalogue offre une remise de 10 % pour le groupe de clients `Wholesale`.

Lorsque la tarification de niveau est activée pour les règles de prix de catalogue, le système utilise le flux suivant pour calculer le prix final :

1. Avant que le client ne se connecte, le prix du produit s’affiche à 100 USD (le prix de base standard).

1. Une fois que le client s’est connecté en tant que membre du groupe `Wholesale`, le prix du produit est ajusté à 90 USD (prix de niveau pour le groupe `Wholesale`).

1. La règle de prix catalogue est appliquée, offrant une remise de 10 % sur le prix de niveau de 90 USD, ce qui donne un prix final de 81 USD.

Le tableau suivant résume les calculs de prix lorsque la tarification de niveau est activée pour les règles de prix de catalogue et qu&#39;une règle de prix de catalogue offre une remise de 10 % pour tous les groupes de clients :

Produit : Prix standard 100 $ (achat d&#39;un seul article)

| Groupe de clients | Prix De Niveau (Qté=1) | Nouveau prix de base | Prix final |
|---|---|---|---|
| TOUS LES GROUPES | Non configuré | 100 $ | 100 $ - 10 % = 90 $ |
| Commerce de gros | Fixe : 85 $ | 85 $ | 85 $ - 10 % = 76,50 $ |
| Retailer | Remise de 20 % | 80 $ | 80 $ - 10 % = 72 $ |
| VIP | Remise de 15 % | 85 $ | 85 $ - 10 % = 76,50 $ |
