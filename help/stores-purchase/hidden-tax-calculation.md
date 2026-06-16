---
title: Calcul des taxes cachées
description: Découvrez comment configurer un calcul de taxe masquée lorsqu'une remise est associée à une taxe.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
TQID: https://experienceleague.adobe.com/KkluEZ6WopfZzfFvnd0XA93av21JP0mxXBS4A4czvA0
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 1%

---

# Calcul des taxes cachées

_Taxe cachée_ est le montant de TVA dont dispose un montant de remise. Elle est non nulle lorsque toutes ces conditions sont vraies :

- Les prix du catalogue incluent la taxe
- Le taux de TVA n&#39;est pas nul
- Il y a une réduction

Lorsqu’une remise est associée à une taxe, Commerce calcule une _taxe masquée_ qui est ajoutée en retour pour calculer le prix réduit.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Exemple

1. Prix complet de l&#39;article, avec taxe incluse : 100 $
1. TVA à : 20%
1. Remise de 10% appliquée sur le prix de l&#39;article hors taxes :

### Résultat attendu non valide

- Prix de l&#39;article hors taxe sans remise=100 USD
- Prix de l&#39;article sans remise=100/1.2=83.33 USD
- Remise=83,33 \ *0,1=8,33 USD
- Taxe=(83,33-8,33) \ *0,2=**15 USD (non valide)**
- Total de la commande hors taxe=83,33-8,33=**75 USD (non valide)**
- Total de la commande incluant la taxe=75+15=**90 USD (non valide)**

### Résultat réel valide dans le panier

![Calcul de la taxe cachée dans le panier](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Calculs valides

1. Le prix complet de l&#39;article sans taxes est : 100 $ / 1,2 = **$83.33**

1. Le montant de TVA sur le prix total de l’article est de 100 $ à 83,33 $ = 16,67 $

   _Peut également être calculé comme suit : $100 \ * (1 - 1/1.2)._

1. Remise de 10% sur 83,33 $ est : **8,33 $** (lorsque vous ne réduisez pas la taxe)

1. Prix réduit de l&#39;article avec taxe : $100 - $8.33 = $91.67

   >[!NOTE]
   >
   >Cette équation illustre la perception du client quant à la façon dont les remises sont appliquées.

1. Prix réduit de l&#39;article sans taxes : 91,67 $ / 1,2 = 76,39 $

1. Le montant de TVA sur le prix réduit est : 91,67 $ - 76,39 $ = 15,28 $ **(valide)**

   _Peut également être calculé comme suit : 91,67 $ \ * (1 - 1/1,2)._

1. La taxe cachée ou _Rémunération de taxe sur remise_ est la différence entre le montant de la TVA du prix complet et le prix actualisé : 16,67 $ - 15,28 $ = 1,39 **$**

   _Une autre façon de voir les choses : la taxe cachée est le montant de TVA porté dans la remise de 8,33 $ : 8,33 $ \* (1 - 1/1,2)._

1. Comment le client comprend habituellement le prix réduit (total de la commande) :

   _Prix complet de l&#39;article, taxes comprises **moins**le montant de la remise : 100 $ - 8,33 $ = 91,67 $_

1. **Comment Commerce calcule le prix réduit** (voir plus haut pour la formule) :

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
