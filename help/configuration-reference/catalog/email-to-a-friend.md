---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Email to a Friend] de [!UICONTROL Catalog] &gt ; de l’administrateur Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '172'
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
