---
title: Segments de client dans les règles de prix
description: Découvrez comment associer des segments de clients à une règle de prix de panier afin que vous puissiez définir des promotions ciblées pour votre boutique.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Segments de client dans les règles de prix

{{ee-feature}}

Un segment de client peut être utilisé pour les promotions ciblées en l’associant à une [règle de prix du panier](../merchandising-promotions/price-rules-cart.md).

![Règle de prix du panier - segment client ciblé](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**Pour associer un segment à une règle de prix de panier :**&#x200B;_

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Ouvrez une règle nouvelle ou existante :

   * Pour utiliser une nouvelle règle, cliquez sur **[!UICONTROL Add New Rule]** dans le coin supérieur droit.
   * Pour utiliser une règle existante, cliquez sur la règle dans la liste pour l’ouvrir en mode d’édition.

1. Faites défiler l’écran vers le bas et développez la section **[!UICONTROL Conditions]**.

1. Ajoutez la condition .

   * Cliquez sur l’icône _Ajouter_ (![Icône Liste](../assets/icon-add-green-circle.png)), qui affiche la liste des conditions. Sélectionnez ensuite **[!UICONTROL Customer Segment]**.

   ![Règle de prix du panier - ajouter une condition de segment client](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Par défaut, la condition est définie pour trouver une condition correspondante. Si nécessaire, cliquez sur le lien **[!UICONTROL matches]** et remplacez l’opérateur par l’un des éléments suivants :

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Opérateur de condition](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Pour cibler un segment spécifique, cliquez sur le lien Plus **...** pour afficher d’autres options. Cliquez ensuite sur l’icône _Programme de sélection_ (![Icône Liste](../assets/icon-list-chooser.png)) pour afficher la liste des segments de clients.

1. Dans la liste, cochez la case de chaque segment que vous souhaitez cibler avec la condition .

   ![Règle de prix du panier - liste de sélection de conditions](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Select]** pour placer les segments de clients sélectionnés dans la condition.

1. Effectuez le reste de la règle de prix selon vos besoins.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.
