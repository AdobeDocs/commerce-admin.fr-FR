---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Email to a Friend] de [!UICONTROL Catalog] &gt ; de l’administrateur Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Modèles d’e-mail](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage de la boutique | Active le processus qui permet aux clients d’envoyer des e-mails à leurs amis à propos des produits de votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Select Email Template] | Affichage de la boutique | Identifie le modèle d’e-mail utilisé pour les messages générés par la fonction _Envoyer un e-mail à un ami_. Modèle par défaut : `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Affichage de la boutique | Détermine si l’expéditeur doit être un client enregistré pour envoyer un e-mail à propos d’un produit à des amis. Options : `Yes` / `No` |
| [!UICONTROL Max Recipients] | Affichage de la boutique | Limite le nombre de personnes qui peuvent figurer sur la liste de distribution pour un seul e-mail. |
| [!UICONTROL Max Products Sent in 1  Hour] | Affichage de la boutique | Limite le nombre de produits qui peuvent être partagés par un seul utilisateur sur une période d’une heure. |
| [!UICONTROL Limit Sending By] | Affichage de la boutique | Détermine la méthode utilisée pour identifier l’expéditeur. Les options incluent : <br/>**`IP Address`**- (recommandé) identifie l’expéditeur à l’aide de l’adresse IP de l’ordinateur utilisé pour envoyer les e-mails de produit.<br/>**`Cookie (unsafe)`** - Identifie l’expéditeur à l’aide d’un cookie de navigateur. Cette méthode n’est pas sécurisée, car l’utilisateur ou l’utilisatrice peut supprimer le cookie pour éviter la restriction. |

{style="table-layout:auto"}
