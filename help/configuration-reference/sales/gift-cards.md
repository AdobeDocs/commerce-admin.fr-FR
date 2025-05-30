---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] de l’administrateur Commerce.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Paramètres de courrier électronique Carte cadeau](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Affichage en magasin | Identifie le [contact de boutique](../../getting-started/store-details.md#store-email-addresses) qui apparaît comme expéditeur de l’e-mail de notification de carte-cadeau. Valeur par défaut : `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Affichage en magasin | Détermine le [modèle](../../systems/email-templates.md) utilisé pour l’e-mail de notification de carte-cadeau. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Paramètres généraux de carte-cadeau](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Détermine si le détenteur de la carte-cadeau peut rembourser sa valeur en espèces. Options : `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Détermine le nombre de jours de validité de la carte. Si rien n’est indiqué, la carte n’expire pas. <br/><br/>**_Important :_**&#x200B;Dans certains endroits, il est illégal de définir une donnée d’expiration sur les cartes-cadeaux. Vérifiez vos lois locales avant de définir une durée de vie pour vos cartes-cadeaux. |
| [!UICONTROL Allow Gift Message] | Affichage en magasin | Détermine si l’option permettant d’inclure un message cadeau est disponible pour les clients qui achètent une carte cadeau. Options : `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Affichage en magasin | Détermine le nombre maximal de caractères autorisés dans un message de carte cadeau. Valeur par défaut : 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Détermine si un compte de carte cadeau est généré lorsqu’un client passe une commande ou lorsque la commande est facturée. Options : `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![ Courrier électronique envoyé à partir de la gestion de compte de carte cadeau ](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Affichage en magasin | Identifie le [contact de boutique](../../getting-started/store-details.md#store-email-addresses) qui apparaît comme expéditeur de l’e-mail de carte-cadeau. Valeur par défaut : `General Contact` |
| [!UICONTROL Gift Card Template] | Affichage en magasin | Détermine le [modèle](../../systems/email-templates.md) utilisé pour l’e-mail de carte-cadeau. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Paramètres généraux du compte de carte-cadeau](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Détermine la longueur du code de carte cadeau. |
| [!UICONTROL Code Format] | Global | Détermine le format du code de carte cadeau. Options : `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Définit tout préfixe ajouté au début du code. |
| [!UICONTROL Code Suffix] | Global | Définit tout suffixe ajouté à la fin du code. |
| [!UICONTROL Dash Every X Characters] | Global | Si vous souhaitez inclure des tirets dans le code, détermine le nombre de caractères entre chaque tiret. |
| [!UICONTROL New Pool Size] | Global | Détermine la taille du nouveau pool de code à générer. |
| [!UICONTROL Low Code Pool Threshold] | Global | Détermine le nombre d’enregistrements dans le pool de code qui déclenche une alerte indiquant que le pool doit être réapprovisionné. |
| [!UICONTROL Generate] | Global | Cliquez sur pour générer la liste des codes de carte-cadeau. |

{style="table-layout:auto"}
