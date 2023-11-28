---
title: Appliquer le crédit de magasin
description: Les administrateurs de magasin peuvent appliquer un crédit de magasin à un achat.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Appliquer le crédit de magasin

{{ee-feature}}

Les administrateurs de magasin peuvent afficher le solde et l’historique du crédit du compte client, ainsi que appliquer le crédit de magasin à un achat.

![Solde et historique du crédit client](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Afficher le solde du crédit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trouvez le client dans la grille.

1. Dans le _Action_ colonne, cliquez sur **[!UICONTROL Edit]**.

1. Défilement _[!UICONTROL Customer View]_et affichez le **[!UICONTROL Store Credit Balance]**en bas.

![Solde du crédit de la boutique](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Mettre à jour le solde du crédit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > _Opérations_ > **[!UICONTROL All Customers]**.

1. Trouvez le client dans la grille.

1. Dans le _Action_ colonne, cliquez sur **[!UICONTROL Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Store Credit]**.

1. Sélectionnez le site web (storefront) à associer au solde.

1. Pour **[!UICONTROL Update Balance]**, saisissez la nouvelle valeur.

1. Pour informer le client de la mise à jour du solde, sélectionnez l’option **[!UICONTROL Notify Customer by Email]** et sélectionnez la vue de magasin à partir de **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Saisissez un **[!UICONTROL Comment]** à propos de la modification.

1. Une fois les mises à jour terminées, cliquez sur **[!UICONTROL Save and Continue Edit]** ou **[!UICONTROL Save Customer]**.

Le solde mis à jour doit être affiché dans la section **[!UICONTROL Balance History]**.

## Application d’un solde de crédit à une commande en tant qu’administrateur de magasin

En tant qu’administrateur de magasin, vous pouvez effectuer diverses opérations pour le compte d’un client, y compris envoyer des commandes. Lorsque vous [création d’une commande](../stores-purchase/customer-account-create-order.md), vous pouvez appliquer un solde de crédit de boutique dû au client. Le solde disponible s’affiche dans la _Informations de paiement et d’expédition_ . Sélectionnez la variable **[!UICONTROL Use Store Credit]** pour appliquer le solde ou une partie du solde si le total de la commande est inférieur.

![Application du solde du crédit de la boutique à la commande](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Application d’un crédit de magasin lors du passage en caisse

S’il existe un solde créatif pour le site, le client peut appliquer un crédit de magasin au solde de la commande avant de passer la commande sur le storefront.

1. Le client affiche le montant du crédit de magasin disponible.

   Durant : _Révision et paiements_ , le montant disponible apparaît sous _[!UICONTROL Store Credit]_.

1. Pour appliquer le montant à la commande, cliquez sur **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Le total de la commande est recalculé et le montant du crédit de magasin appliqué apparaît dans la variable _[!UICONTROL Order Summary]_.

   ![Solde du crédit de magasin appliqué à la commande](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Une fois prêt, cliquez sur **[!UICONTROL Place Order]**.
