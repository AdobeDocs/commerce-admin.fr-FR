---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] de l’administrateur Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [Panier persistant](../../stores-purchase/cart-persistent.md) permet de conserver les articles non achetés qui restent dans le panier et de les enregistrer pendant une période configurée dans _Durée de vie de la persistance_. Les cookies doivent être autorisés dans le navigateur du client pour utiliser le panier persistant.

## [!UICONTROL General Options]

![Options générales](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Site Web | Détermine si la persistance est activée. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site Web | Définit la durée de vie du cookie persistant en secondes. Valeur maximale autorisée : 3153600000 secondes (100 ans). |
| [!UICONTROL Enable "Remember Me"] | Site Web | Définit si la variable _Mémoriser_ s’affiche sur les pages de connexion et d’enregistrement du magasin. Options : <br/>**`Yes`**- Affiche la variable _Mémoriser_ .<br/>**`No`** - N’affiche pas la variable _Mémoriser_ et le cookie persistant est utilisé uniquement pour les clients qui l’ont déjà. |
| [!UICONTROL "Remember Me" Default Value] | Site Web | Définit l’état par défaut de la variable _Mémoriser_ . |
| [!UICONTROL Clear Persistence on Log Out] | Site Web | Définit si le cookie persistant est supprimé lorsqu’un client de magasin se déconnecte. Quelle que soit la configuration, si un client ne se déconnecte pas mais que le cookie de session expire, le cookie persistant est toujours utilisé. |
| [!UICONTROL Persist Shopping Cart] | Site Web | Définit si l’utilisation du cookie persistant donne accès aux données du panier du compte correspondant. Options : <br/>**`Yes`**- Le contenu du panier est enregistré une fois la session terminée.<br/>**`No`** - Le contenu du panier n’est pas enregistré une fois la session terminée. |
| [!UICONTROL Persist Wish List] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des listes de souhaits des clients est conservé lorsque la session se termine. Options : <br/>**`Yes`**- Le contenu de la liste de souhaits est enregistré à la fin de la session.<br/>**`No`** - La liste de souhaits n’est pas enregistrée à la fin de la session. |
| [!UICONTROL Persist Recently Ordered Items] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des éléments récemment commandés est conservé lorsque la session se termine. Options : <br/>**`Yes`**- L’état des éléments récemment commandés est enregistré lorsque la session se termine.<br/>**`No`** - L’état des éléments récemment triés n’est pas enregistré lorsque la session se termine. |
| [!UICONTROL Persist Currently Compared Products] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des produits actuellement comparés est conservé lorsque la session se termine. Options : <br/>**`Yes`**- L’état des produits actuellement comparés est enregistré à la fin de la session.<br/>**`No`** - L’état des produits actuellement comparés n’est pas enregistré à la fin de la session. |
| [!UICONTROL Persist Comparison History] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’historique de comparaison de l’état est conservé lorsque la session se termine. Options : <br/>**`Yes`**- L’historique de l’état de comparaison est enregistré à la fin de la session.<br/>**`No`** - L’historique de l’état de comparaison n’est pas enregistré à la fin de la session. |
| [!UICONTROL Persist Recently Viewed Products] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des produits récemment consultés est conservé lorsque la session se termine. Options : <br/>**`Yes`**- L’état des produits récemment consultés est enregistré à la fin de la session.<br/>**`No`** - L’état des produits récemment consultés n’est pas enregistré à la fin de la session. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si les critères d’appartenance et de segmentation de l’état des clients sont conservés à la fin de la session. Options : <br/>**`Yes`**- L’état de l’appartenance au groupe du client et les données de segmentation sont enregistrés à la fin de la session.<br/>**`No`** - L’état de l’appartenance au groupe du client et les données de segmentation ne sont pas enregistrés à la fin de la session. |

{style="table-layout:auto"}
