---
title: Ordre de tri des totaux de paiement
description: Découvrez le total de passage en caisse affiché et comment configurer l’ordre de tri des totaux de passage en caisse dans le résumé de la commande.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Ordre de tri des totaux de paiement

Lors de la révision de la commande, le total apparaît au bas de la commande, avec les éventuels ajustements pour les remises, les frais d’expédition, le crédit de magasin et les taxes. L’ordre de chaque élément détermine la séquence des calculs et est défini dans la configuration par un nombre attribué à chaque élément. Par exemple, le sous-total est le premier élément de la section et se voit attribuer une valeur de 10. Le total général apparaît en dernier et reçoit une valeur de 100. Une valeur est affectée à tous les autres éléments de la section des totaux entre ces valeurs.

![Le résumé de la commande affiche le total du passage en caisse](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Pour configurer l’ordre de tri des totaux de passage en caisse :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Checkout Totals Sort Order]** .

   ![Options de totaux de passage en caisse numérotées pour déterminer l’ordre de tri](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Ordre de tri des totaux de passage en caisse](../configuration-reference/sales/sales.md#checkout-totals-sort-order) dans le _Guide de référence de configuration_.

1. Si le paramètre est défini pour une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Pour déterminer la commande dans la section _Totaux_, modifiez le numéro attribué à chaque élément.

   Plus la valeur est faible, plus son emplacement dans la liste est précoce. Dans la configuration par défaut, le sous-total (`10`) est le premier et le total général (`100`) est le dernier.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour effectuer ces modifications.

1. Cliquez sur **[!UICONTROL Save Config]**.
