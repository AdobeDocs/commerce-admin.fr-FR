---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Gift Cards] de [!UICONTROL Sales] &gt ; de l’administrateur Commerce.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/J-VH-mdaM7HrMRHJMNmmbBPggm1hjtHHWTh3q-5en0w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d9ced453-36f4-4eb5-b2f3-1d593e32476b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Paramètres d’e-mail de la carte cadeau](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Affichage de la boutique | Identifie le [&#x200B; contact de la boutique &#x200B;](../../getting-started/store-details.md#store-email-addresses) qui s’affiche comme expéditeur de l’e-mail de notification de carte cadeau. Valeur par défaut : `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Affichage de la boutique | Détermine le [modèle](../../systems/email-templates.md) utilisé pour l’e-mail de notification de carte cadeau. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Paramètres généraux de la carte cadeau](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Détermine si le détenteur de la carte cadeau peut utiliser sa valeur contre de l&#39;argent. Options : `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Détermine le nombre de jours de validité de la carte. Si rien n’est indiqué, la carte n’expire pas. <br/><br/>**_Important:_** à certains endroits, il est illégal de définir des données d’expiration sur les cartes-cadeaux. Vérifiez vos lois locales avant de fixer une durée de vie pour vos cartes-cadeaux. |
| [!UICONTROL Allow Gift Message] | Affichage de la boutique | Détermine si l’option permettant d’inclure un message cadeau est disponible pour les clients qui achètent une carte cadeau. Options : `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Affichage de la boutique | Détermine le nombre maximal de caractères autorisés dans un message de carte cadeau. Valeur par défaut : 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Détermine si un compte de carte cadeau est généré lorsqu’un client passe une commande ou lorsque la commande est facturée. Options : `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-mail envoyé à partir de la gestion de compte de carte cadeau](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Affichage de la boutique | Identifie le [&#x200B; contact de la boutique &#x200B;](../../getting-started/store-details.md#store-email-addresses) qui s’affiche comme expéditeur de l’e-mail de carte cadeau. Valeur par défaut : `General Contact` |
| [!UICONTROL Gift Card Template] | Affichage de la boutique | Détermine le [modèle](../../systems/email-templates.md) utilisé pour l’e-mail de carte cadeau. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Paramètres généraux du compte de carte-cadeau](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Détermine la longueur du code de carte cadeau. |
| [!UICONTROL Code Format] | Global | Détermine le format du code de carte cadeau. Options : `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Définit tout préfixe ajouté au début du code. |
| [!UICONTROL Code Suffix] | Global | Définit tout suffixe ajouté à la fin du code. |
| [!UICONTROL Dash Every X Characters] | Global | Si vous souhaitez inclure des tirets dans le code, détermine le nombre de caractères entre chaque tiret. |
| [!UICONTROL New Pool Size] | Global | Détermine la taille du nouveau pool de code à générer. |
| [!UICONTROL Low Code Pool Threshold] | Global | Détermine le nombre d&#39;enregistrements dans le pool de code qui déclenche une alerte indiquant que le pool doit être réapprovisionné. |
| [!UICONTROL Generate] | Global | Cliquez pour générer la liste des codes de carte cadeau. |

{style="table-layout:auto"}
