---
title: Règles de prix du panier
description: Découvrez les règles de prix de panier qui appliquent des remises aux articles du panier en fonction d’un ensemble de conditions.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/i3G3iGuomU0cjy3aX9eynyzAtpCgQxeEFAyRUdUUu44
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 0%

---

# Règles de prix du panier

Les règles de prix de panier appliquent des remises aux articles du panier, en fonction d’un ensemble de conditions. La remise peut être appliquée automatiquement lorsque les conditions sont remplies ou lorsque le client saisit un code de coupon valide. Lorsqu’elle est appliquée, la remise apparaît dans le panier sous le sous-total . Une règle de prix de panier peut être utilisée selon les besoins pour une saison ou une promotion en modifiant son statut et sa période.

>[!NOTE]
>
>Si la règle de panier de coupons comporte des conditions qui spécifient des options de passage en caisse, telles que certains modes d’expédition ou de paiement, les conditions ne sont remplies que lors du passage en caisse une fois les modes d’expédition/de paiement spécifiques sélectionnés. Dans ce cas, le coupon peut être appliqué lors du passage en caisse à la dernière étape.

![Exemple de storefront - appliquer un bon de réduction au panier](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Accéder aux règles de prix de panier

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![ Règle de prix du panier ](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Si vous disposez de nombreuses règles, utilisez les options de filtre en haut de chaque colonne pour rationaliser la liste, puis cliquez sur **[!UICONTROL Search]** pour appliquer les filtres.

1. Pour effacer toutes les options de filtrage et afficher la liste complète, cliquez sur **[!UICONTROL Reset Filter]**.

1. Mettez à jour les propriétés d’une règle :

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page Informations sur la règle.

   - ![](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur la règle dans la liste pour afficher la page Informations sur la règle.

   Vous pouvez y modifier les paramètres de la règle (comme pour la création d’une règle).

## Filtrer les options par colonne

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Saisissez du texte pour filtrer la liste pour un numéro d’ID de règle spécifique. |
| [!UICONTROL Rule] | Saisissez du texte pour filtrer la liste en fonction du nom de règle défini lors de la création de la règle. |
| [!UICONTROL Coupon Code] | Saisissez du texte pour filtrer la liste en fonction du nom de code défini lors de la création de la règle. |
| [!UICONTROL Priority] | Champ de texte libre qui filtre la liste en fonction de la priorité définie pour une règle. |
| [!UICONTROL Status] | Utilisez cette option pour filtrer la liste en fonction du statut de la règle (`Active` ou `Inactive`). |
| [!UICONTROL Web Site] | Utilisez cette option pour filtrer la liste en fonction des sites web définis pour une règle. |
| [!UICONTROL Action] | ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page _[!UICONTROL Rule Information]_et mettre à jour les paramètres des règles (comme pour la création d’une règle). |
| [!UICONTROL Start] | ![](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (_[!UICONTROL To:]_et_[!UICONTROL From:]_) pour filtrer la liste en fonction de la date de début de la règle telle que définie lors de la création de la règle. |
| [!UICONTROL End] | ![](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (_[!UICONTROL To:]_et_[!UICONTROL From:]_) pour filtrer la liste en fonction de la date de fin de la règle telle que définie lors de la création de la règle. |

{style="table-layout:auto"}

## Utilisation des audiences Real-Time CDP pour informer les règles de prix de panier

Découvrez comment [activer](../customers/audience-activation.md) les audiences Real-Time CDP dans votre instance Adobe Commerce pour informer les règles de prix de panier.
