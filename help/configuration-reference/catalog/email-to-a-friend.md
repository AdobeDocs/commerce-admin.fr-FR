---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] de l’administrateur Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Modèles de courrier électronique](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage en magasin | Active le processus qui permet aux clients d’envoyer des courriers électroniques à leurs amis concernant les produits de votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Select Email Template] | Affichage en magasin | Identifie le modèle de courrier électronique utilisé pour les messages générés par la fonction _Email a Friend_. Modèle par défaut : `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Affichage en magasin | Détermine si l’expéditeur doit être un client enregistré pour envoyer un courrier électronique concernant un produit à ses amis. Options : `Yes` / `No` |
| [!UICONTROL Max Recipients] | Affichage en magasin | Limite le nombre de personnes qui peuvent se trouver sur la liste de distribution pour un seul email. |
| [!UICONTROL Max Products Sent in 1  Hour] | Affichage en magasin | Limite le nombre de produits qui peuvent être partagés par un utilisateur unique sur une période d’une heure. |
| [!UICONTROL Limit Sending By] | Affichage en magasin | Détermine la méthode utilisée pour identifier l’expéditeur. Les options incluent : <br/>**`IP Address`**- (Recommandé) Identifie l’expéditeur selon l’adresse IP de l’ordinateur qui est utilisé pour envoyer les emails du produit.<br/>**`Cookie (unsafe)`** - Identifie l’expéditeur par un cookie de navigateur. Cette méthode n’est pas sécurisée, car l’utilisateur peut supprimer le cookie pour éviter la restriction. |

{style="table-layout:auto"}
