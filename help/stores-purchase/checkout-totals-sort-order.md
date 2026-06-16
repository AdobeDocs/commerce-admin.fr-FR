---
title: Ordre de tri des totaux de passage en caisse
description: Découvrez le total de passage en caisse affiché et comment configurer l’ordre de tri des totaux de passage en caisse dans le résumé de la commande.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg
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
source-wordcount: 257
ht-degree: 0%

---

# Ordre de tri des totaux de passage en caisse

Lors de la révision de la commande, le total s’affiche au bas de la commande, avec les ajustements liés aux remises, aux frais d’expédition, au crédit de la boutique et à la taxe. L&#39;ordre de chaque article détermine l&#39;ordre des calculs et est défini dans la configuration par un numéro attribué à chaque article. Par exemple, le sous-total est le premier élément de la section et se voit attribuer la valeur 10. Le total général apparaît en dernier et se voit attribuer une valeur de 100. Une valeur est attribuée à tous les autres éléments de la section des totaux entre ces valeurs.

![Le récapitulatif de la commande affiche le total du passage en caisse](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Pour configurer l’ordre de tri des totaux de passage en caisse:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Checkout Totals Sort Order]** .

   ![Les options de passage en caisse sont numérotées afin de déterminer l’ordre de tri](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Ordre de tri des totaux de passage en caisse](../configuration-reference/sales/sales.md#checkout-totals-sort-order) dans le _Guide de référence de configuration_.

1. Si le paramètre concerne une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Pour déterminer l&#39;ordre dans la section _Totaux_, modifiez le numéro attribué à chaque élément.

   Plus la valeur est faible, plus son emplacement dans la liste est précoce. Dans la configuration par défaut, le sous-total (`10`) est le premier et le total général (`100`) est le dernier.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour effectuer ces modifications.

1. Cliquez sur **[!UICONTROL Save Config]**.
