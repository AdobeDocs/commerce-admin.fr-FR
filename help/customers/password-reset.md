---
title: Réinitialisation des mots de passe des clients
description: Les clients réinitialisent généralement leurs mots de passe à partir du storefront, mais un administrateur de magasin peut initialiser une réinitialisation de mot de passe ou une connexion forcée de l’administrateur.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Réinitialisation des mots de passe des clients

Les clients réinitialisent généralement leurs mots de passe à partir du storefront en cliquant sur _[!UICONTROL Forgot Your Password?]_. Cependant, l’administrateur du magasin peut réinitialiser un mot de passe ou établir une connexion forcée à partir de l’administrateur.

| Fonction | Description |
| --- | --- |
| Réinitialiser le mot de passe | Un courrier électronique de réinitialisation de mot de passe est envoyé directement au compte de messagerie du client. L’administrateur du magasin ne peut pas accéder au mot de passe du client. |
| Forcer la connexion | Révoque les jetons d’accès OAuth associés au compte client. Cela ne peut être utilisé qu’avec les comptes client auxquels des jetons OAuth ont été attribués, dans le cadre d’une API Web. [integration](../systems/integrations.md). Pour en savoir plus, voir [Authentification basée sur OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) dans la documentation destinée aux développeurs. <br/><br/>Les comptes clients standard créés à partir du storefront ou de l’administrateur n’ont pas de jetons OAuth. |

{style="table-layout:auto"}

## Réinitialisation d’un mot de passe à partir du storefront

1. Sur la page de connexion, le client clique sur **[!UICONTROL Forgot Your Password?]**.

1. Lorsque vous y êtes invité, la fonction **[!UICONTROL Email Address]** qui est associé à leur compte et aux clics **[!UICONTROL Reset My Password]**.

   ![Mot de passe oublié](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Si l’adresse électronique saisie correspond à celle associée au compte, le client reçoit un courrier électronique de confirmation de réinitialisation de mot de passe contenant un lien pour réinitialiser son mot de passe.

1. Lorsque l&#39;email arrive, le client clique sur la variable _réinitialisation du mot de passe_ et entre leurs **[!UICONTROL New Password]** lorsque vous y êtes invité.

1. Le saisir à nouveau pour confirmer et cliquer **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Le nouveau mot de passe doit comporter au moins six caractères, sans espaces. Lorsqu’ils reçoivent la confirmation que le mot de passe est mis à jour, ils peuvent utiliser le nouveau mot de passe pour se connecter à leur compte. Par défaut, la variable _réinitialisation du mot de passe_ est valide pendant 24 heures.

## Réinitialisation d’un mot de passe à partir de l’administrateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le compte client dans la grille, puis cliquez sur **[!UICONTROL Edit]** dans le _Action_ colonne .

1. Dans l’ensemble d’options situé en haut de la page, cliquez sur **[!UICONTROL Reset Password]**.

   Le nombre de demandes de réinitialisation de mot de passe autorisées dans l’heure est défini dans la variable [configuration](../configuration-reference/customers/customer-configuration.md) rubrique.

## Révocation des jetons OAuth d’un client

>[!IMPORTANT]
>
>Ne procédez pas à moins que vous ne maîtrisiez parfaitement l’authentification de l’API.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le compte client dans la grille, puis cliquez sur **[!UICONTROL Edit]** dans le _Action_ colonne .

1. Dans l’ensemble d’options situé en haut de la page, cliquez sur **[!UICONTROL Force Sign In]**.

1. Lorsque vous y êtes invité, cliquez sur **OK**.
