---
title: '[!UICONTROL Customers] > [!UICONTROL Gift Registry]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Gift Registry] de [!UICONTROL Customers] &gt ; de l’administrateur Commerce.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/STCCRRp71FXvz-09LFiYKhJnsbdF8wokfdIa2Ij6-9A
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 346
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Pour obtenir des informations détaillées sur l&#39;utilisation de ces paramètres pour activer les chèques-cadeaux pour les clients de votre boutique, consultez [Configurer les chèques-cadeaux](../../merchandising-promotions/gift-registry-configure.md). Pour plus d&#39;informations sur l&#39;inclusion de la recherche de registre des cadeaux sur le storefront, voir [Ajouter une recherche de registre des cadeaux](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Options générales](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Affichage de la boutique | Détermine si des registres cadeaux sont disponibles. Options : <br/>**`Yes`**- Active les registres de cadeaux pour la vue de magasin sélectionnée. L&#39;onglet Registre des cadeaux s&#39;affiche dans le tableau de bord du compte des clients enregistrés.<br/>**`No`** - Les registres de cadeaux ne sont pas disponibles pour la vue de la boutique. |
| [!UICONTROL Maximum Registrants] | Affichage de la boutique | Définit le nombre de personnes qu&#39;un client peut ajouter à un registre des cadeaux. Le client partage le registre des cadeaux avec chaque inscrit. Dans le storefront, le bouton _Ajouter un inscrit_ est disponible pour les clients jusqu’à ce que le nombre maximal soit atteint. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Notification du propriétaire](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Template] | Affichage de la boutique | Détermine le modèle utilisé pour l&#39;e-mail de notification du propriétaire envoyé lors de la création d&#39;un registre des cadeaux. Modèle par défaut : notification du propriétaire du registre des cadeaux |
| [!UICONTROL Email Sender] | Affichage de la boutique | Identifie le [contact de la boutique](../../getting-started/store-details.md#store-email-addresses) qui s&#39;affiche comme expéditeur de l&#39;e-mail de notification du propriétaire du registre des cadeaux. Valeur par défaut : `General Contact` |

{style="table-layout:auto"}

## Partage du registre des cadeaux

![Partage du registre des cadeaux](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Template] | Affichage de la boutique | Détermine le modèle utilisé pour l&#39;e-mail de partage du registre des cadeaux envoyé lors de la création d&#39;un registre des cadeaux. Lorsque le propriétaire clique sur _Partager le registre des cadeaux_, l’e-mail est envoyé à chaque destinataire. Modèle par défaut : `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Affichage de la boutique | Identifie le [&#x200B; contact de la boutique](../../getting-started/store-details.md#store-email-addresses) qui s’affiche comme expéditeur de l’e-mail de partage du registre des cadeaux. Valeur par défaut : `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Affichage de la boutique | Nombre maximal de messages de notification par e-mail de partage du registre des cadeaux pouvant être envoyés simultanément. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Mise à jour du registre des cadeaux](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Template] | Affichage de la boutique | Détermine le modèle utilisé pour l&#39;e-mail de mise à jour du registre des cadeaux envoyé au propriétaire du registre des cadeaux lorsqu&#39;un achat est effectué à partir du registre des cadeaux. La mise à jour inclut des informations sur l&#39;article et la quantité achetée, mais n&#39;inclut pas le nom de la personne qui a passé la commande. Modèle par défaut : `Gift Registry Update` |
| [!UICONTROL Email Sender] | Affichage de la boutique | Identifie le [&#x200B; contact de la boutique](../../getting-started/store-details.md#store-email-addresses) qui s&#39;affiche comme expéditeur de l&#39;e-mail de mise à jour du registre des cadeaux. Valeur par défaut : `General Contact` |

{style="table-layout:auto"}
