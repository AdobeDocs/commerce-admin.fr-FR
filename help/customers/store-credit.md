---
title: Crédit de la boutique
description: Le crédit en magasin est un montant qui est restauré sur un compte client et qui peut être utilisé pour payer des achats ou des remboursements en espèces.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Crédit de la boutique

{{ee-feature}}

Le crédit de la boutique est un montant qui est restauré sur un compte client. Les clients peuvent utiliser leur crédit de magasin pour payer leurs achats et les administrateurs peuvent utiliser le crédit de magasin pour les remboursements en espèces. Les soldes de carte cadeau peuvent être crédités sur le compte du client, au lieu d&#39;utiliser le code de carte cadeau pour les achats futurs.

Une fois la commande payée et facturée, elle peut être remboursée, en tout ou en partie, en [émettant un avoir](../stores-purchase/credit-memo-create.md). Un avoir diffère d&#39;un remboursement, car le montant du crédit est restauré sur le compte du client où il peut être utilisé pour des achats futurs. Parfois, un remboursement peut être effectué au moment où un avoir est émis et appliqué au solde du crédit de la boutique du client. Le montant du crédit de magasin disponible dans le compte du client est spécifié dans la configuration.

>[!NOTE]
>
>Le mode de paiement [_Passage en caisse du sous-total zéro_](../stores-purchase/zero-subtotal-checkout.md) doit être activé si le crédit du magasin couvre le total de la commande.

## Workflow Stocker le crédit

1. **Connexion client** - Le client se connecte au compte avant de commencer le processus de passage en caisse.

1. **Utiliser le magasin** - Crédit Pendant l’étape [!UICONTROL _Vérification et paiements_] du processus de passage en caisse, le client sélectionne [!UICONTROL _Utiliser le crédit du magasin_] comme option de paiement. Le solde disponible est affiché entre parenthèses. Si le solde disponible est supérieur au total général, les autres modes de paiement ne s&#39;affichent plus.

1. **Crédit appliqué à la commande** - Le montant du crédit de magasin appliqué à la commande s’affiche avec les totaux de la commande et est soustrait du total général.

1. **Solde client ajusté** - Le solde disponible du client est ajusté lorsque la commande est passée.
