---
title: Règles de prix de catalogue
description: Découvrez les règles de prix de catalogue qui peuvent être utilisées pour proposer des produits aux acheteurs à un prix réduit basé sur un ensemble de conditions définies.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/JZE2DF0tp-XOsKjxo-WaQiwA3Y-FrM4TI5qq-Nze-qo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 468
ht-degree: 0%

---

# Règles de prix de catalogue

Les règles de prix de catalogue peuvent être utilisées pour proposer des produits aux acheteurs à un prix réduit, en fonction d’un ensemble de conditions définies. Les règles de prix de catalogue n’utilisent pas de [codes coupon](price-rules-cart-coupon.md), car elles sont déclenchées avant le placement d’un produit dans le panier.

Par exemple, vous pouvez définir et définir les conditions d&#39;une règle de prix qui, lorsqu&#39;elle est remplie, affiche automatiquement les produits avec un prix spécial ou promotionnel. Les propriétés de règle définies peuvent inclure des groupes de clients, des catégories de produits, un montant ou un pourcentage de remise, la couleur du produit, la taille du produit ou n’importe quel attribut de produit configuré dans votre boutique. Vous pouvez définir des dates de début et de fin pour une règle de prix qui démarrent et arrêtent automatiquement une promotion aux dates que vous définissez dans la règle. Les propriétés d’une règle enregistrée peuvent être mises à jour ou modifiées selon les besoins.

- ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Vous pouvez également lier une règle définie à un [bloc dynamique](../content-design/dynamic-blocks.md) afin de promouvoir l’événement ou le produit dans votre boutique.

- ![](../assets/open-source.svg) (Magento Open Source uniquement) Pour les promotions récurrentes, vous pouvez définir manuellement une règle enregistrée sur le statut _Actif_ ou _Inactif_ chaque fois que vous souhaitez exécuter la promotion.

## Accéder aux règles de prix de catalogue

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Règles de prix de catalogue](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Mettez à jour les propriétés d’une règle :

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page _Informations sur les règles_.

   - ![](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur la règle dans la liste pour afficher la page Informations sur la règle.

   Vous pouvez y modifier les paramètres de la règle (comme pour la [création d’une règle](price-rules-catalog-create.md)).

## Options de filtre

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Saisissez du texte pour filtrer la liste pour un numéro d’ID de règle spécifique. |
| [!UICONTROL Rule] | Saisissez du texte pour filtrer la liste en fonction du nom de règle défini lors de la création de la règle. |
| [!UICONTROL Priority] | ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Saisissez du texte dans ce champ pour filtrer la liste selon la priorité définie pour une règle. |
| [!UICONTROL Web Site] | ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez cette option pour filtrer la liste en fonction des sites web définis pour une règle. |
| [!UICONTROL Action] | ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher les informations de la règle et mettre à jour les paramètres de la règle (comme pour la création d’une règle). |
| [!UICONTROL Start] | ![](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (Vers : et De :) pour filtrer la liste en fonction de la date de début de la règle telle que définie lors de la création de la règle. |
| [!UICONTROL End] | ![](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez les champs de calendrier dynamique (Vers : et De :) pour filtrer la liste en fonction de la date de fin de la règle telle que définie lors de la création de la règle. |
| [!UICONTROL Status] | ![](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez cette option pour filtrer la liste en fonction du statut de la règle (`Active` ou `Inactive`). |

{style="table-layout:auto"}
