---
title: Transfert d’un compte Commerce
description: Découvrez comment transférer votre compte Commerce à un autre propriétaire ou adresse électronique.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 00994f506056bf5504df758a44a7cd56f590750d
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Transfert d’un compte Commerce

À mesure que les responsabilités commerciales changent, vous devrez peut-être transférer la propriété de votre compte Commerce existant à un nouveau propriétaire ou à une autre adresse électronique. Ce transfert nécessite une modification de l’e-mail de l’utilisateur principal associé au compte.

Les informations suivantes décrivent le processus de transfert d’un compte Commerce (MAGEID). Elle n’inclut pas de modifications concernant la propriété du compte Cloud (projet Cloud ou New Relic). Pour plus d’informations sur l’accès aux projets cloud, voir [Gestion de l’accès des utilisateurs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) dans le _Guide de l’infrastructure de Commerce on Cloud_.

## Identifier votre type de transfert

La manière dont vous effectuez ce transfert dépend de l’un des scénarios suivants qui décrit votre situation en tant que propriétaire actuel du compte et du nouveau propriétaire (adresse électronique) à qui vous souhaitez transférer le compte :

| Type de transfert | Propriétaire actuel | Nouveau propriétaire |
| ------------- | ------------- | --------- |
| [Nouvelle modification Adobe ID et email](#new-adobe-id-and-email-change) | Comporte un MAGEID **_non connecté_** avec un compte de connexion d’Adobe. | Ne possède pas de MAGEID et n’est pas connecté à un compte de connexion d’Adobe. |
| [Modification de l’email](#email-change) | Dispose d’un MAGEID **_connecté_** avec un compte de connexion Adobe sans aucun autre produit/service d’Adobe associé. | Ne possède pas de MAGEID et n’est pas connecté à un compte de connexion d’Adobe. |
| [Bouton Adobe ID](#adobe-id-account-switch) | Dispose d’un MAGEID **_connecté_** avec un compte de connexion Adobe sans aucun autre produit/service d’Adobe associé. | Possède un MAGEID et est connecté à un compte de connexion d’Adobe sans aucun autre produit/service d’Adobe associé. |

{style="table-layout:auto"}

>[!NOTE]
>
>Comme Adobe Commerce continue de s’intégrer à d’autres solutions d’Adobe, un compte Commerce (MAGEID) nécessite désormais une association avec une connexion d’Adobe. Cette Adobe ID utilise la même adresse électronique que celle connectée à votre compte Commerce.

## Nouvelle modification d’Adobe ID et du courrier électronique

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de respecter les conditions préalables de cette séquence d’étapes.

Ce type de transfert nécessite d’abord de créer une Adobe ID associée, puis de remplacer ce compte par l’adresse électronique du nouveau propriétaire.

1. Accédez à votre [compte Commerce](https://account.magento.com/customer/account/login/).

1. Cliquez sur **[!UICONTROL Sign in with Adobe ID]**.

1. Cliquez sur **[!UICONTROL Create an account]**.

1. Saisissez l&#39;adresse email du propriétaire actuel et un mot de passe.

1. Cliquez sur **[!UICONTROL Continue]**.

   Cela crée une Adobe ID et la lie au compte Commerce actif (MAGEID). Avec ce lien de compte, le champ _[!UICONTROL Email]_est bloqué pour toutes les modifications. L’adresse électronique associée est gérée par le compte Adobe ID.

1. Accédez à [account.adobe.com](https://account.adobe.com/).

1. Cliquez sur **[!UICONTROL Change Email]**.

1. Saisissez l’adresse électronique du nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette opération génère un email de vérification envoyé à la nouvelle adresse email. L’email contient un code de confirmation qui est requis pour effectuer le changement d’adresse email.

1. Saisissez le code de confirmation envoyé à la nouvelle adresse email.

1. Cliquez sur **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Modification des emails

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de respecter les conditions préalables de cette séquence d’étapes.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et terminez la connexion à l’Adobe.

1. Sous le nom de votre compte et l’avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse électronique du nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette opération génère un email de vérification envoyé à la nouvelle adresse email. L’email contient un code de confirmation qui est requis pour effectuer le changement d’adresse email.

1. Saisissez le code de confirmation envoyé à la nouvelle adresse email.

1. Cliquez sur **[!UICONTROL Verify]**.

## Changement de compte Adobe ID

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de respecter les conditions préalables de cette séquence d’étapes.

Dans le cas où le propriétaire actuel et le nouveau propriétaire ont des identifiants d’Adobe existants, les deux comptes doivent rester, mais les adresses électroniques doivent être échangées entre eux. Cela nécessite l’utilisation d’une adresse électronique _temporaire_ valide, mais non associée à et à Adobe ID.

### Modification d’un compte temporaire

Le propriétaire actuel effectue ces étapes pour associer son Adobe ID à une autre adresse électronique temporaire.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et terminez la connexion à l’Adobe.

1. Sous le nom de votre compte et l’avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez une adresse électronique temporaire valide qui n’est pas utilisée par Adobe ID.

   Vous devez avoir accès à l&#39;adresse email pour pouvoir récupérer l&#39;email avec le code de confirmation.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette opération génère un courrier électronique de vérification envoyé à l’adresse électronique temporaire. L’email contient un code de confirmation qui est requis pour effectuer le changement d’adresse email.

1. Saisissez le code de confirmation envoyé à l&#39;adresse email temporaire.

1. Cliquez sur **[!UICONTROL Verify]**.

1. Déconnectez-vous du compte Adobe.

### Nouvelles étapes du propriétaire

Une fois que le propriétaire actuel a terminé le transfert vers une adresse électronique temporaire, procédez comme suit pour modifier votre compte et le transférer vers le propriétaire actuel.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et terminez la connexion à l’Adobe.

1. Sous le nom de votre compte et l’avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse électronique d’origine du propriétaire actuel.

1. Cliquez sur **[!UICONTROL Change]**.

   Un courrier électronique de vérification est alors envoyé à cette adresse. L’email contient un code de confirmation qui est requis pour effectuer le changement d’adresse email.

1. Saisissez le code de confirmation envoyé au propriétaire actuel.

1. Cliquez sur **[!UICONTROL Verify]**.

1. Déconnectez-vous du compte Adobe.

### Étapes de suivi

Une fois que le nouveau propriétaire a transféré son compte d’Adobe au propriétaire actuel (maintenant précédent), procédez comme suit pour transférer la propriété.

1. Accédez à [account.adobe.com](https://account.adobe.com/) (premier compte utilisé dans la série d’étapes) et terminez la connexion à l’Adobe.

   Cette connexion nécessite l’utilisation de l’adresse électronique temporaire.

1. Sous le nom du compte et l’avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse électronique du nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Change]**.

   Un courrier électronique de vérification est alors envoyé à cette adresse. L’email contient un code de confirmation qui est requis pour effectuer le changement d’adresse email.

1. Saisissez le code de confirmation envoyé au nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Verify]**.

1. **Envoyez une demande d’assistance** pour informer l’équipe d’assistance que vous avez mis à jour l’adresse électronique du propriétaire du compte. Incluez l’adresse électronique du propriétaire précédent du compte dans votre requête.

D’autres étapes doivent être effectuées par l’assistance, telles que la mise à jour de l’adresse électronique sur votre profil [Commerce Marketplace](https://commercemarketplace.adobe.com/).
