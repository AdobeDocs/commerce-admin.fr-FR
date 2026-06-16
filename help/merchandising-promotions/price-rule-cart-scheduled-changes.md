---
title: Modifications planifiées pour les règles de prix de panier
description: Découvrez comment appliquer les règles de prix de panier selon le calendrier dans le cadre d’une campagne et regroupées avec d’autres modifications de contenu.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/S4sSXY-SSMabdW-rkaqr-cMexe0q1-k6AbTNvb7pR14
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 0%

---

# Modifications planifiées pour les règles de prix de panier

{{ee-feature}}

Les règles de prix du panier peuvent être appliquées selon le calendrier dans le cadre d’une campagne et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne basée sur les modifications planifiées apportées à une règle de prix ou appliquer les modifications à une campagne existante.

>[!NOTE]
>
>Les champs [!UICONTROL From] et [!UICONTROL To] ont été supprimés dans ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce et ne peuvent pas être modifiés directement dans la règle de prix du panier. Vous devez créer une mise à jour planifiée pour ces activations.

![Règles de prix du panier - modifications planifiées](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées de manière consécutive. Cela signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à un moment donné. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir différentes mises à jour planifiées pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut, et non de la mise à jour planifiée précédente.

Si plusieurs règles de prix sont exécutées dans la même campagne, le paramètre _[!UICONTROL Priority]_de la règle de prix détermine quelle règle est prioritaire. Pour en savoir plus, voir [Évaluation du contenu](../content-design/content-staging.md).

>[!NOTE]
>
>Si une campagne active est initialement créée sans date de fin, la campagne ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une campagne en double et de saisir la date de fin nécessaire.

>[!NOTE]
>
>Si une campagne est liée à plusieurs règles de prix de panier, elle ne peut être modifiée qu’à partir du [Tableau de bord d’évaluation de contenu](../content-design/content-staging-dashboard.md).

Gardez à l’esprit les avertissements suivants :

- Si une campagne qui comprend une règle de prix est initialement créée sans date de fin, la campagne ne peut pas être modifiée ultérieurement pour inclure une date de fin. Il est recommandé d’ajouter une date de fin au moment de la création de la campagne ou de créer une version en double de la campagne existante et d’ajouter la date de fin au doublon, si nécessaire.
- Lors de l’utilisation d’une mise à jour planifiée pour activer une règle de prix de panier avec une date de fin, veillez à définir la règle comme initialement désactivée. Les règles déjà actives ne respectent pas la date de fin.
- Les coupons ne sont pas liés aux règles de prix du panier. Une mise à jour planifiée ne permet pas d’accéder aux champs _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_et_[!UICONTROL Uses per Customer]_ de l’onglet _[!UICONTROL Rule Information]_. En outre, tous les paramètres de l’onglet_[!UICONTROL Manage Coupon Codes]_ ne sont pas disponibles.

>[!IMPORTANT]
>
>Les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** de Campaign doivent être définis à l’aide du fuseau horaire **_par défaut_** Admin , converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple où plusieurs sites web se trouvent dans des fuseaux horaires différents et où vous souhaitez démarrer une campagne selon un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, et définir les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** convertis de chaque fuseau horaire local du site web sur le fuseau horaire de l’administrateur par défaut.
