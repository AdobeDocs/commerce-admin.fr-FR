---
title: Segments clients dans les règles de prix
description: Découvrez comment associer des segments de clients à une règle de prix de panier afin de pouvoir définir des promotions ciblées pour votre boutique.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Segments clients dans les règles de prix

{{ee-feature}}

Un segment client peut être utilisé pour les promotions ciblées en l’associant à une [règle de prix de panier](../merchandising-promotions/price-rules-cart.md).

![Règle de prix du panier - segment client ciblé](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**Pour associer un segment à une règle de prix de panier :**&#x200B;_

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Ouvrez une règle nouvelle ou existante :

   * Pour utiliser une nouvelle règle, cliquez sur **[!UICONTROL Add New Rule]** dans le coin supérieur droit.
   * Pour utiliser une règle existante, cliquez sur la règle dans la liste pour l’ouvrir en mode d’édition.

1. Faites défiler vers le bas et développez la section **[!UICONTROL Conditions]** .

1. Ajoutez la condition .

   * Cliquez sur l’icône _Ajouter_ (![Icône de liste](../assets/icon-add-green-circle.png)), qui affiche la liste des conditions. Choisissez ensuite **[!UICONTROL Customer Segment]**.

   ![Règle de prix du panier - Ajouter une condition de segment client](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Par défaut, la condition est définie pour rechercher une condition correspondante. Si nécessaire, cliquez sur le lien **[!UICONTROL matches]** et définissez l’opérateur sur l’une des options suivantes :

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Opérateur de condition](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Pour cibler un segment spécifique, cliquez sur le lien Plus de **...** pour afficher des options supplémentaires. Cliquez ensuite sur l’icône _Sélecteur_ (![Icône de liste](../assets/icon-list-chooser.png)) pour afficher la liste des segments clients.

1. Dans la liste, cochez la case de chaque segment que vous souhaitez cibler avec la condition.

   ![Règle de prix du panier - liste du sélecteur de conditions](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Select]** pour placer les segments de clients sélectionnés dans la condition.

1. Complétez le reste de la règle de prix selon vos besoins.

1. Cliquez ensuite sur **[!UICONTROL Save]**.
