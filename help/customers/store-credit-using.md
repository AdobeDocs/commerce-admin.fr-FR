---
title: Appliquer le crédit du magasin
description: Les administrateurs de boutique peuvent appliquer un crédit de boutique à un achat.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 321
ht-degree: 0%

---

# Appliquer le crédit du magasin

{{ee-feature}}

Les administrateurs de boutique peuvent afficher le solde et l’historique du crédit à partir du compte client et appliquer également le crédit de boutique à un achat.

![Solde et historique de crédit client](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Afficher le solde créditeur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL Edit]**.

1. Faites défiler _[!UICONTROL Customer View]_&#x200B;page et affichez les **[!UICONTROL Store Credit Balance]**&#x200B;en bas.

![Solde créditeur de la boutique](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Mettre à jour le solde créditeur du magasin

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > _Opérations_ > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Store Credit]**.

1. Choisissez le site web (storefront) que vous souhaitez associer au solde.

1. Par **[!UICONTROL Update Balance]**, saisissez la nouvelle valeur.

1. Pour avertir le client de la mise à jour du solde, cochez la case **[!UICONTROL Notify Customer by Email]** et choisissez la vue du magasin dans **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Saisissez un **[!UICONTROL Comment]** sur la modification.

1. Une fois les mises à jour terminées, cliquez sur **[!UICONTROL Save and Continue Edit]** ou **[!UICONTROL Save Customer]**.

Le solde mis à jour doit être affiché en **[!UICONTROL Balance History]**.

## Appliquer un solde créditeur à une commande en tant qu&#39;administrateur de magasin

En tant qu’administrateur de magasin, vous pouvez effectuer différentes opérations pour le compte d’un client, notamment envoyer des commandes. Lorsque vous [créez une commande](../stores-purchase/customer-account-create-order.md), vous pouvez appliquer un solde créditeur de la boutique dû au client. Le solde disponible s&#39;affiche dans la section _Informations sur le paiement et l&#39;expédition_. Cochez la case **[!UICONTROL Use Store Credit]** pour appliquer le solde ou une partie du solde si le total de la commande est inférieur.

![Appliquer le solde créditeur du magasin à la commande](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Appliquer le crédit du magasin lors du passage en caisse

S&#39;il existe un solde créditeur pour le site, le client peut appliquer un crédit de magasin au solde de la commande avant de passer la commande sur le storefront.

1. Le client consulte le montant du crédit de magasin disponible.

   Lors de l’étape _Révision et paiements_, le montant disponible s’affiche sous _[!UICONTROL Store Credit]_.

1. Pour appliquer le montant à la commande, cliquez sur **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Le total de la commande est recalculé et le montant du crédit de magasin appliqué apparaît dans le _[!UICONTROL Order Summary]_.

   ![Solde créditeur de magasin appliqué à la commande](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Lorsque vous êtes prêt, cliquez sur **[!UICONTROL Place Order]**.
