---
title: Calcul des taxes masquées
description: Découvrez comment configurer un calcul de taxe masqué en cas de remise incluant une taxe.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Calcul des taxes masquées

_Taxe cachée_ est le montant de la TVA qui correspond à un montant de remise. Elle est non nulle lorsque toutes ces conditions sont vraies :

- Les prix du catalogue incluent les taxes
- Le taux de TVA n&#39;est pas nul
- Il y a une remise

Lorsqu’une remise est incorporée à la taxe, Commerce calcule une _taxe masquée_ qui est ajoutée pour calculer le prix escompté.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Exemple

1. Prix complet de l&#39;article, taxe comprise : 100 $
1. TVA à : 20 %
1. Remise de 10 % appliquée sur les produits hors taxes :

### Résultat attendu non valide

- Prix de l&#39;article après taxe sans remise=100 USD
- Prix de l&#39;article avant taxe sans remise=100/1.2=83,33 USD
- Discount=83,33 \ *0,1=8,33 USD
- Tax=(83.33-8.33) \ *0.2=**15 USD (non valide)**
- Total des commandes Taxe d’exclusion=83.33-8.33=**75 USD (non valide)**
- Total de la commande incluant la taxe=75+15=**90 USD (non valide)**

### Résultat réel valide dans le panier

![Calcul de la taxe masquée dans le panier](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Calculs valides

1. Le prix complet de l&#39;article sans taxes est : $100 / 1.2 = **$83.33**

1. Le montant de la TVA sur le prix de l&#39;article complet est : $100 - $83.33 = $16.67

   _Peut également être calculé comme suit : $100 \ * (1 - 1/1.2)._

1. La remise de 10 % sur 83,33 $ est : **$8.33** (lorsque vous ne réduisez pas la taxe)

1. Prix actualisé de l’article taxé : 100 $ à 8,33 $ = 91,67 $

   >[!NOTE]
   >
   >Cette équation illustre la perception par le client de la manière dont les remises sont appliquées.

1. Prix actualisé de l&#39;article sans taxes : 91,67 $ / 1,2 = 76,39 $

1. Le montant de la TVA sur le prix réduit est : $91.67 - $76.39 = **$15.28 (valide)**

   _Peut également être calculé comme suit : $91.67 \ * (1 - 1/1.2)._

1. Taxe masquée ou _Rémunération fiscale de rabais_ est la différence entre le montant de la TVA du prix complet et le prix actualisé : 16,67 $ - 15,28 $ = **$1,39**

   _Autre façon de voir les choses : la taxe cachée est le montant de la TVA reporté dans la remise de 8,33 $ : 8,33 $ \* (1 - 1/1.2)._

1. Comment le client comprend habituellement le prix réduit (total de la commande) :

   _Prix complet de l&#39;article, taxes comprises **inférieur**au montant de remise : 100 $ à 8,33 $ = 91,67 $_

1. **Comment Commerce calcule le prix escompté** (voir plus haut pour la formule) :

   _$83.33 - 8.33 + 15.28 + 1.39 =**$91.67***_
