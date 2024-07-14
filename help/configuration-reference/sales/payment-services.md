---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Vérifiez les paramètres de configuration dans la section [!UICONTROL Payment Services] de la page [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de l’administrateur Commerce.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: bf166c1debd7f10a4d988d231a1a47f32c4cea9e
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Les services de paiement offrent une solution de libre-service clé en main, notamment des tests d’environnement de test et une configuration simple, pour fournir un traitement de paiement robuste et sécurisé. Pour en savoir plus, consultez le [_Guide de l’utilisateur des services de paiement_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

Pour accéder aux paramètres de configuration des services de paiement, dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** et cliquez sur **[!UICONTROL Settings]**.

![ Paramètres des services de paiement ](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Pour utiliser la configuration héritée au lieu de [Paramètres](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html), voir [Configuration héritée](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Paramètres généraux](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|---|---|---|
| [!UICONTROL Enable] | site web | Activez ou désactivez [!DNL Payment Services] pour votre site web. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | vue de magasin | Définissez la méthode, ou l’environnement, de votre magasin. Options : [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | vue de magasin | Votre ID de marchand d’environnement de test, qui est généré automatiquement lors de l’intégration des environnements de test. |
| [!UICONTROL Production Merchant ID] | vue de magasin | Votre identifiant commercial de production, qui est généré automatiquement lors de l’intégration des environnements de test. |
| [!UICONTROL Soft Descriptor] | site web ou vue de magasin | Ajoutez un descripteur souple à vos sites web et aux vues des magasins qui fournit des informations sur les transactions des clients et délimite les marques, les magasins ou les lignes de produits. Le bouton d’activation/désactivation [!UICONTROL Use website] applique tout descripteur logiciel ajouté au niveau du site web. Le bouton d’activation/désactivation [!UICONTROL Use default] applique tout descripteur de type Soft ajouté comme valeur par défaut. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Paramètres des champs de carte de crédit](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|---|---|---|
| [!UICONTROL Title] | vue de magasin | Ajoutez le texte à afficher comme titre de cette option de paiement dans la vue Mode de paiement lors de l’extraction. |
| [!UICONTROL Payment Action] | site web | [action de paiement](payment-methods.md#payment-actions) pour le mode de paiement spécifié. Options : [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | site web | Activez ou désactivez l’ [authentification sécurisée 3DS](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). Options : [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | site web | Activez ou désactivez les champs de carte de crédit à afficher sur la page de paiement. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | vue de magasin | Activez ou désactivez la [valeur de carte de crédit](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | vue de magasin | Activez ou désactivez la possibilité de terminer les commandes pour les clients dans l’ [ administrateur à l’aide d’un mode de paiement Vault ](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | site web | Activez ou désactivez le mode de débogage. Options : [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![ Paramètres des boutons de paiement Paypal](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|---|---|---|
| [!UICONTROL Title] | vue de magasin | Ajoutez le texte à afficher comme titre pour cette option de paiement dans la vue Mode de paiement lors de l’extraction. |
| [!UICONTROL Payment Action] | site web | [action de paiement](payment-methods.md#payment-actions){target="_blank"} pour le mode de paiement spécifié. Options : [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | vue de magasin | Activez ou désactivez [!DNL PayPal Smart Buttons] sur la page de passage en caisse. Options : [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | vue de magasin | Activez ou désactivez [!DNL PayPal Smart Buttons] sur la page des détails du produit. Options : [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | vue de magasin | Activez ou désactivez [!DNL PayPal Smart Buttons] dans l’aperçu du mini-panier. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | vue de magasin | Activez ou désactivez [!DNL PayPal Smart Buttons] sur la page du panier. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | vue de magasin | Activez ou désactivez l’aspect de l’option de paiement ultérieur lorsque des boutons de paiement s’affichent. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | site web | Activez ou désactivez la messagerie Payer plus tard dans le panier, la page du produit, le mini-panier et pendant le flux de passage en caisse. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | vue de magasin | Activez ou désactivez l’option de paiement Venmo lorsque les boutons de paiement s’affichent. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | vue de magasin | Activez ou désactivez l’option Paiement Apple dans laquelle les boutons de paiement s’affichent. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | vue de magasin | Activez ou désactivez l’option de paiement par carte de crédit et de débit où des boutons de paiement s’affichent. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | site web | Activez ou désactivez le mode de débogage. Options : [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Paramètres de style des boutons de paiement Paypal](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Layout] | Affichage en magasin | Définissez le style de mise en page des boutons de paiement. Options : [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Affichage en magasin | Activez/désactivez tagline. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Affichage en magasin | Définissez la couleur des boutons de paiement. Options : [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Affichage en magasin | Définissez la forme des boutons de paiement. Options : [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Affichage en magasin | Définit si les boutons de paiement utilisent une hauteur par défaut. Options : [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Affichage en magasin | Définissez la hauteur des boutons de paiement. Valeur par défaut : aucune |
| [!UICONTROL Label] | Affichage en magasin | Définissez le libellé qui apparaît dans les boutons de paiement. Options : [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
