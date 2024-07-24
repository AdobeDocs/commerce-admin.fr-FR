---
title: Référence de configuration du panier persistant
description: Contenu réutilisable pour la référence de configuration du panier persistant.
source-git-commit: d23cb0d63409e533cf950d8d14514d9f9157fd05
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Options générales](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Champ | [Portée](/help/getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Site Web | Détermine si la fonction de persistance est activée. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site Web | Définit la durée de vie du cookie persistant en secondes. La valeur maximale autorisée est de 34560000 secondes (400 jours). Il s’agit d’une limitation de la durée de vie maximale recommandée pour les cookies. |
| [!UICONTROL Enable "Remember Me"] | Site Web | Définit si la case à cocher _Mémoriser_ s’affiche sur les pages de connexion et d’enregistrement du magasin. Options : <br/>**`Yes`**- Affiche la case à cocher _Mémoriser_ .<br/>**`No`** - N’affiche pas la case à cocher _Mémoriser_ et le cookie persistant est utilisé uniquement pour les clients qui l’ont déjà. |
| [!UICONTROL "Remember Me" Default Value] | Site Web | Définit l’état par défaut de la case à cocher _Mémoriser_ . |
| [!UICONTROL Clear Persistence on Log Out] | Site Web | Définit si le cookie persistant est supprimé lorsqu’un client de magasin se déconnecte. Quelle que soit la configuration de cette option, si un client ne se déconnecte pas mais que le cookie de session expire, le cookie persistant est toujours utilisé. |
| [!UICONTROL Persist Shopping Cart] | Site Web | Définit si l’utilisation du cookie persistant donne accès aux données du panier du compte correspondant. Options : <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Wish List] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des listes de souhaits des clients est conservé lorsque la session se termine. Options : <br/>**`Yes`**- Le contenu de la liste de souhaits est enregistré à la fin de la session.<br/>**`No`** - La liste de souhaits n’est pas enregistrée à la fin de la session. |
| [!UICONTROL Persist Recently Ordered Items] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des éléments récemment commandés est enregistré à la fin de la session. Options : <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des produits actuellement comparés est conservé lorsque la session se termine. Options : <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Comparison History] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’historique de comparaison de l’état est conservé lorsque la session se termine. Options : <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des produits récemment consultés est conservé lorsque la session se termine. Options : <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si les critères d’appartenance et de segmentation de l’état des clients sont conservés à la fin de la session. Options : <br/>**`Yes`**- L’état de l’appartenance au groupe du client et les données de segmentation sont enregistrés à la fin de la session.<br/>**`No`** - L’état de l’appartenance au groupe du client et les données de segmentation ne sont pas enregistrés à la fin de la session. |

{style="table-layout:auto"}
