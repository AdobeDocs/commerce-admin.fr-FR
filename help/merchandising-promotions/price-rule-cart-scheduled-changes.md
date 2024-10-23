---
title: Modifications planifiées des règles de prix du panier
description: Découvrez comment appliquer les règles de prix du panier selon le calendrier dans le cadre d’une campagne et les regrouper avec d’autres modifications de contenu.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Modifications planifiées des règles de prix du panier

{{ee-feature}}

Les règles de prix du panier peuvent être appliquées au planning dans le cadre d’une campagne et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne en fonction des modifications planifiées apportées à une règle de prix ou appliquer les modifications à une campagne existante.

>[!NOTE]
>
>Les champs [!UICONTROL From] et [!UICONTROL To] ont été supprimés dans ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce et ne peuvent pas être modifiés directement sur la règle du prix du panier. Vous devez créer une mise à jour planifiée pour ces activations.

![ Règles de prix du panier - modifications planifiées](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées consécutivement. Cela signifie qu’une entité ne peut avoir qu’une seule mise à jour planifiée à un moment donné. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir simultanément différentes mises à jour planifiées pour différentes vues de magasin. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

Si plusieurs règles de prix sont exécutées dans la même campagne, le paramètre _[!UICONTROL Priority]_de la règle de prix détermine la règle qui prévaut. Pour en savoir plus, voir [Évaluation de contenu](../content-design/content-staging.md).

>[!NOTE]
>
>Si une campagne active est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une opération en double et de renseigner la date de fin nécessaire.

>[!NOTE]
>
>Si une campagne est liée à plusieurs règles de prix du panier, elle ne peut être modifiée que depuis le [tableau de bord de l’évaluation du contenu](../content-design/content-staging-dashboard.md).

Gardez à l’esprit les avertissements suivants :

- Si une campagne contenant une règle de prix est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Il est recommandé d’ajouter une date de fin lors de la création de la campagne ou de créer une version en double de la campagne existante et d’ajouter la date de fin au doublon, le cas échéant.
- Lorsque vous utilisez une mise à jour planifiée pour activer une règle de prix de panier avec une date de fin, veillez à définir la règle comme initialement désactivée. Les règles déjà actives ne respectent pas la date de fin.
- Les bons ne sont pas liés aux règles de prix du panier. Une mise à jour planifiée ne permet pas d’accéder aux champs _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_et_[!UICONTROL Uses per Customer]_ de l’onglet _[!UICONTROL Rule Information]_. De plus, tous les paramètres de l’onglet_[!UICONTROL Manage Coupon Codes]_ ne sont pas disponibles.

>[!IMPORTANT]
>
>Les campagnes **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** doivent être définies à l’aide du fuseau horaire d’ **_par défaut_** de l’administrateur, converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple de plusieurs sites web dans différents fuseaux horaires, mais que vous souhaitez lancer une campagne en fonction d’un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, et définir **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** convertis à partir de chaque fuseau horaire de site web local en fuseau horaire d’administration par défaut.
