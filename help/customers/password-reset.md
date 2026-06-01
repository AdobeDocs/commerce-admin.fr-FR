---
title: Réinitialiser les mots de passe client
description: Les clients réinitialisent généralement leurs mots de passe à partir du storefront, mais un administrateur de magasin peut lancer une réinitialisation de mot de passe ou une connexion forcée à partir de l’administrateur.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Réinitialiser les mots de passe client

Les clients réinitialisent généralement leurs mots de passe à partir du storefront en cliquant sur _[!UICONTROL Forgot Your Password?]_. Cependant, l’administrateur du magasin peut déclencher une réinitialisation du mot de passe ou une connexion forcée à partir de l’administrateur.

| Fonction | Description |
| --- | --- |
| Réinitialiser le mot de passe | Un e-mail de réinitialisation de mot de passe est envoyé directement au compte de messagerie du client. L’administrateur du magasin ne peut pas accéder au mot de passe du client. |
| Forcer la connexion | Révoque les jetons d’accès OAuth associés au compte client. Cela ne peut être utilisé qu’avec des comptes client auxquels des jetons OAuth ont été attribués dans le cadre d’une API web [intégration](../systems/integrations.md). Pour en savoir plus, consultez la section [Authentification basée sur OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) dans la documentation du développeur. <br/><br/>Les comptes clients standard créés à partir du storefront ou de l’administrateur ne disposent pas de jetons OAuth. |

{style="table-layout:auto"}

## Réinitialiser un mot de passe à partir du storefront

1. Sur la page de connexion, le client clique sur **[!UICONTROL Forgot Your Password?]**.

1. Lorsque vous y êtes invité, saisissez le **[!UICONTROL Email Address]** associé à son compte et clique sur **[!UICONTROL Reset My Password]**.

   ![Mot de passe oublié](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Si l’adresse e-mail saisie correspond à celle associée au compte, le client reçoit un e-mail de confirmation de réinitialisation du mot de passe contenant un lien lui permettant de réinitialiser son mot de passe.

1. Lorsque l’e-mail arrive, le client clique sur le lien _Réinitialiser le mot de passe_ et saisit son **[!UICONTROL New Password]** à l’invite.

1. Le saisit à nouveau pour confirmer et clique sur **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Le nouveau mot de passe doit comporter au moins six caractères sans espaces. Lorsqu’ils reçoivent la confirmation que le mot de passe est mis à jour, ils peuvent utiliser le nouveau mot de passe pour se connecter à leur compte. Par défaut, le lien _réinitialiser le mot de passe_ est valide pendant 24 heures.

## Réinitialiser un mot de passe à partir de l’administrateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le compte client dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _Action_.

1. Dans l’ensemble d’options en haut de la page, cliquez sur **[!UICONTROL Reset Password]**.

   Le nombre de demandes de réinitialisation de mot de passe autorisées dans l’heure est défini dans la rubrique [configuration](../configuration-reference/customers/customer-configuration.md).

## Révoquer les jetons OAuth d’un client

>[!IMPORTANT]
>
>Ne continuez pas sauf si vous avez une compréhension complète de l’authentification de l’API.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le compte client dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _Action_.

1. Dans l’ensemble d’options en haut de la page, cliquez sur **[!UICONTROL Force Sign In]**.

1. Lorsque vous êtes invité à confirmer, cliquez sur **OK**.
