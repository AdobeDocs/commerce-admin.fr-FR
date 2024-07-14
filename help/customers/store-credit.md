---
title: Crédit de la boutique
description: Le crédit de magasin est un montant restauré dans un compte client et qui peut être utilisé pour payer des achats ou des remboursements en espèces.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Crédit de la boutique

{{ee-feature}}

Le crédit de magasin est un montant restauré dans un compte client. Les clients peuvent utiliser leur crédit de boutique pour payer les achats, et les administrateurs peuvent utiliser le crédit de magasin pour les remboursements en espèces. Les soldes des cartes-cadeaux peuvent être crédités au compte du client, au lieu d’utiliser le code de carte-cadeau pour les achats futurs.

Une fois qu’une commande est payée et facturée, la commande, ou une partie de celle-ci, peut être remboursée en [émettant un avoir](../stores-purchase/credit-memo-create.md). Une note de crédit diffère d’un remboursement, car le montant du crédit est restauré sur le compte du client, où il peut être utilisé pour de futurs achats. Parfois, un remboursement peut être effectué au moment de l’émission d’une note de crédit et appliqué au crédit de la balance des stocks du client. Le montant du crédit de magasin disponible dans le compte du client est spécifié dans la configuration.

>[!NOTE]
>
>Le mode de paiement [_Zero Subtotal Checkout_](../stores-purchase/zero-subtotal-checkout.md) doit être activé si le crédit de magasin couvre le total de la commande.

## Workflow de crédit de magasin

1. **Connexion client** - Le client se connecte à son compte avant de commencer le processus de passage en caisse.

1. **Utiliser la boutique** - Crédit Pendant l’étape [!UICONTROL _Révision et paiements_] du processus de passage en caisse, le client sélectionne l’option de paiement [!UICONTROL _Utiliser le crédit de la boutique_]. Le solde disponible s’affiche entre parenthèses. Si le solde disponible est supérieur au total général, les autres modes de paiement ne sont plus affichés.

1. **Crédit appliqué à la commande** : le montant du crédit de magasin appliqué à la commande apparaît avec les totaux de la commande et est soustrait du total général.

1. **Solde client ajusté** - Le solde disponible du client est ajusté lors de la commande.
