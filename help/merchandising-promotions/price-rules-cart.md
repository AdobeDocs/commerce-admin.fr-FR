---
title: Règles de prix du panier
description: Découvrez les règles de prix du panier qui appliquent des remises à des articles du panier selon un ensemble de conditions.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Règles de prix du panier

Les règles de prix du panier s’appliquent aux articles du panier, selon un ensemble de conditions. La remise peut être appliquée automatiquement lorsque les conditions sont remplies ou lorsque le client saisit un code de bon valide. Une fois appliquée, la remise apparaît dans le panier sous le sous-total. Une règle de prix de panier peut être utilisée selon les besoins pour une saison ou une promotion en modifiant son statut et sa plage de dates.

>[!NOTE]
>
>Si la règle du panier de coupon comporte des conditions qui spécifient les options de passage en caisse, telles que certains modes de livraison ou de paiement, les conditions ne sont remplies que lors du passage en caisse après sélection des méthodes de livraison/paiement spécifiques. Dans ce cas, le coupon peut être appliqué lors du passage en caisse de la dernière étape.

![Exemple de vitrine : coupon d’application de panier](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Accéder aux règles de prix du panier

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![Règle de prix du panier](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Si vous avez beaucoup de règles, utilisez les options de filtre en haut de chaque colonne pour rationaliser la liste et cliquez sur **[!UICONTROL Search]** pour appliquer les filtres.

1. Pour effacer toutes les options de filtre et afficher la liste complète, cliquez sur **[!UICONTROL Reset Filter]**.

1. Mettez à jour les propriétés d’une règle :

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page Informations sur la règle.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur la règle dans la liste pour afficher la page Informations sur la règle.

   Vous pouvez y modifier les paramètres de la règle (comme pour la création d’une règle).

## Filtrage des options par colonne

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Entrez du texte pour filtrer la liste en fonction d’un numéro d’ID de règle spécifique. |
| [!UICONTROL Rule] | Saisissez le texte pour filtrer la liste en fonction du nom de la règle défini lors de sa création. |
| [!UICONTROL Coupon Code] | Entrez du texte pour filtrer la liste en fonction du nom de code défini lors de la création de la règle. |
| [!UICONTROL Priority] | Champ de texte libre qui filtre la liste selon la priorité définie pour une règle. |
| [!UICONTROL Status] | Utilisez cette option pour filtrer la liste en fonction de l’état de la règle (`Active` ou `Inactive`). |
| [!UICONTROL Web Site] | Utilisez cette option pour filtrer la liste en fonction des sites web définis pour une règle. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page _[!UICONTROL Rule Information]_&#x200B;et mettre à jour les paramètres des règles (comme pour créer une règle). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (_[!UICONTROL To:]_&#x200B;et&#x200B;_[!UICONTROL From:]_) pour filtrer la liste en fonction de la date de début de la règle, telle que définie lors de la création de la règle. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (_[!UICONTROL To:]_&#x200B;et&#x200B;_[!UICONTROL From:]_) pour filtrer la liste en fonction de la date de fin de la règle, telle que définie lors de la création de la règle. |

{style="table-layout:auto"}

## Utilisation des audiences Real-Time CDP pour informer les règles de prix du panier

Découvrez comment [activer](../customers/audience-activation.md) les audiences Real-Time CDP dans votre instance Adobe Commerce pour informer les règles de prix du panier.
