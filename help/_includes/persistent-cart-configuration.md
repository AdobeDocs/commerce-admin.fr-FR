---
title: Référence de configuration du panier persistant
description: Contenu réutilisable pour la référence de configuration du panier persistant.
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%
---

# [!UICONTROL General Options]

![Options générales](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| Champ | [Portée](/help/getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Site internet | Détermine si la fonctionnalité de persistance est activée. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site internet | Définit la durée de vie du cookie persistant en secondes. La valeur maximale autorisée est de 34560000 secondes (400 jours). Il s’agit d’une limitation de la durée de vie maximale recommandée des cookies. |
| [!UICONTROL Enable "Remember Me"] | Site internet | Définit si la case à cocher _Mémoriser mon nom_ s’affiche sur les pages de connexion et d’enregistrement du magasin. Options : <br/>**`Yes`**- Affiche la case _Mémorisez-moi_.<br/>**`No`** : n’affiche pas la case à cocher _Mémoriser mon nom_ et le cookie persistant est utilisé uniquement pour les clients qui l’ont déjà. |
| [!UICONTROL "Remember Me" Default Value] | Site internet | Définit l’état par défaut de la case à cocher _Mémoriser mon_. |
| [!UICONTROL Clear Persistence on Log Out] | Site internet | Définit si le cookie persistant est supprimé lorsqu’un client du magasin se déconnecte. Quelle que soit la manière dont cette option est configurée, si un client ne se déconnecte pas, mais que le cookie de session expire, le cookie persistant est toujours utilisé. |
| [!UICONTROL Persist Shopping Cart] | Site internet | Définit si l’utilisation du cookie persistant donne accès aux données du panier du compte correspondant. Options : <br/>**`Yes`**&#x200B;ou **`No`**. |
| [!UICONTROL Persist Wish List] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si le statut des listes de souhaits des clients est conservé lorsque la session se termine. Options : <br/>**`Yes`**- Le contenu de la liste de souhaits est enregistré à la fin de la session.<br/>**`No`** - La liste de souhaits n’est pas enregistrée à la fin de la session. |
| [!UICONTROL Persist Recently Ordered Items] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si le statut des éléments récemment commandés est enregistré à la fin de la session. Options : <br/>**`Yes`**&#x200B;ou **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’état des produits actuellement comparés est conservé lorsque la session se termine. Options : <br/>**`Yes`**&#x200B;ou **`No`**. |
| [!UICONTROL Persist Comparison History] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si l’historique de comparaison est conservé à la fin de la session. Options : <br/>**`Yes`**&#x200B;ou **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si le statut des produits récemment consultés est conservé lorsque la session se termine. Options : <br/>**`Yes`**&#x200B;ou **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site internet | ![](/help/assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si le statut des critères d’appartenance à un groupe et de segmentation des clients est conservé lorsque la session se termine. Options : <br/>**`Yes`**- L’état des données d’appartenance à un groupe et de segmentation du client est enregistré à la fin de la session.<br/>**`No`** - L’état des données d’appartenance à un groupe et de segmentation du client n’est pas enregistré à la fin de la session. |

{style="table-layout:auto"}
