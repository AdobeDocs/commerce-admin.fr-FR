---
title: Modifications planifiées des règles de prix du panier
description: Découvrez comment appliquer les règles de prix du panier selon le calendrier dans le cadre d’une campagne et les regrouper avec d’autres modifications de contenu.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Modifications planifiées des règles de prix du panier

{{ee-feature}}

Les règles de prix du panier peuvent être appliquées au planning dans le cadre d’une campagne et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne en fonction des modifications planifiées apportées à une règle de prix ou appliquer les modifications à une campagne existante.

![Règles de prix du panier - modifications planifiées](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées consécutivement. Cela signifie qu’une entité ne peut avoir qu’une seule mise à jour planifiée à un moment donné. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir simultanément différentes mises à jour planifiées pour différentes vues de magasin. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

Si plusieurs règles de prix sont en cours d’exécution dans la même campagne, la variable _[!UICONTROL Priority]_la définition de la règle de prix détermine la règle qui prévaut. Pour en savoir plus, voir [Évaluation du contenu](../content-design/content-staging.md).

Gardez à l’esprit les avertissements suivants :

- Si une campagne contenant une règle de prix est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Il est recommandé d’ajouter une date de fin lors de la création de la campagne ou de créer une version en double de la campagne existante et d’ajouter la date de fin au doublon, le cas échéant.
- Lorsque vous utilisez une mise à jour planifiée pour activer une règle de prix de panier avec une date de fin, veillez à définir la règle comme initialement désactivée. Les règles déjà actives ne respectent pas la date de fin.
- Les bons ne sont pas liés aux règles de prix du panier. Une mise à jour planifiée ne permet pas d’accéder au _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, et_[!UICONTROL Uses per Customer]_ dans le champ _[!UICONTROL Rule Information]_. En outre, tous les paramètres de la variable_[!UICONTROL Manage Coupon Codes]_ ne sont pas disponibles.

>[!IMPORTANT]
>
>Campagne **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** doit être défini à l’aide de la variable **_default_** Fuseau horaire de l’administrateur, converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple de plusieurs sites web dans différents fuseaux horaires, mais que vous souhaitez lancer une campagne en fonction d’un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, puis définir **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** converti de chaque fuseau horaire de site web local en fuseau horaire d’administration par défaut.
