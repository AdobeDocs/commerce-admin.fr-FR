---
title: Transfert d’un compte Commerce
description: Découvrez comment transférer votre compte Commerce vers un autre propriétaire ou une autre adresse e-mail.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: b66fd3fad065f78726eb368b5ba06f0f61174356
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 1%

---

# Transfert d’un compte Commerce

À mesure que les responsabilités professionnelles changent, vous devrez peut-être transférer votre compte Commerce à un nouveau propriétaire ou à une autre adresse e-mail. Ce transfert nécessite une modification de l’adresse e-mail de l’utilisateur principal associée au compte.

Les informations suivantes décrivent le processus de transfert d’un compte Commerce (MAGEID). Elle n’inclut pas les modifications relatives à la propriété du compte cloud (projet cloud ou New Relic). Pour plus d’informations sur l’accès aux projets cloud, consultez [Gérer l’accès des utilisateurs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) dans le guide _Commerce sur les infrastructures cloud_.

>[!IMPORTANT]
>
>Si le nouveau titulaire du compte a acheté des extensions à l’aide de l’accès partagé, l’accès à ces extensions est perdu dès que le processus de transfert de compte a été lancé. Avant de demander le transfert du compte, assurez-vous que le nouveau propriétaire récupère les ID de commande pour les achats auprès de [son compte Marketplace](https://commercemarketplace.adobe.com/sales/order/history/) et demande un remboursement pour ces extensions à l’équipe [Marketplace](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Il n’est pas possible de transférer les achats d’extensions vers un autre compte.

## Identification du type de transfert

Le type de transfert de compte Commerce dépend des identifiants du compte Commerce disponibles pour le propriétaire actuel et le nouveau propriétaire. Les scénarios suivants décrivent les différents types de transfert en fonction de ces informations d’identification.

| Type de transfert | Propriétaire actuel | Nouveau propriétaire |
| ------------- | ------------- | --------- |
| [Nouvel Adobe ID et modification des e-mails](#new-adobe-id-and-email-change) | possède un MAGEID **_non connecté_** avec un compte de connexion Adobe ; | Ne possède pas de MAGEID et n’est pas connecté à un compte de connexion Adobe. |
| [Modification de l’e-mail](#email-change) | Dispose d’un MAGEID **_connecté_** avec un compte de connexion Adobe. | Ne possède pas de MAGEID et n’est pas connecté à un compte de connexion Adobe. |
| [Commutateur Adobe ID](#adobe-id-account-switch) | Dispose d’un MAGEID **_connecté_** avec un compte de connexion Adobe. | Dispose d’un MAGEID et est connecté à un compte de connexion Adobe. |

{style="table-layout:auto"}

>[!NOTE]
>
>Comme Adobe Commerce continue à s’intégrer avec d’autres solutions Adobe, un compte Commerce (MAGEID) nécessite désormais une association avec un identifiant Adobe. Cette Adobe ID utilise la même adresse e-mail que celle associée à votre compte Commerce.

## Nouvelle Adobe ID et modification d’e-mail

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de remplir les conditions préalables pour cette séquence d’étapes.

Ce type de transfert nécessite de créer d’abord une Adobe ID associée, puis de modifier ce compte en fonction de l’adresse e-mail du nouveau propriétaire.

1. Accédez à votre compte [Commerce](https://account.magento.com/customer/account/login/).

1. Cliquez sur **[!UICONTROL Sign in with Adobe ID]**.

1. Cliquez sur **[!UICONTROL Create an account]**.

1. Saisissez l’adresse e-mail du propriétaire actuel et un mot de passe.

1. Cliquez sur **[!UICONTROL Continue]**.

   Cette étape permet de créer une Adobe ID et de la lier au compte Commerce courant (MAGEID). Avec ce lien de compte, le champ _[!UICONTROL Email]_&#x200B;est bloqué de toute modification. La configuration de l’adresse e-mail associée est gérée à partir du compte Adobe ID.

1. Accédez à [account.adobe.com](https://account.adobe.com/).

1. Cliquez sur **[!UICONTROL Change Email]**.

1. Saisissez l’adresse e-mail du nouveau propriétaire.

   Si la nouvelle adresse e-mail est déjà associée à un autre compte du système, elle ne peut pas être directement utilisée pour le transfert. Le processus nécessite plutôt l’utilisation d’une [adresse e-mail temporaire](#change-to-a-temporary-account) pour faciliter le changement.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette étape génère un email de vérification envoyé à la nouvelle adresse email. L’e-mail contient un code de confirmation qui est requis pour terminer le changement d’adresse e-mail.

1. Saisissez le code de confirmation envoyé à la nouvelle adresse e-mail.

1. Cliquez sur **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Modification d’e-mail

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de remplir les conditions préalables pour cette séquence d’étapes.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail du nouveau propriétaire.

   Si la nouvelle adresse e-mail est déjà associée à un autre compte du système, elle ne peut pas être directement utilisée pour le transfert. Le processus nécessite plutôt l’utilisation d’une [adresse e-mail temporaire](#change-to-a-temporary-account) pour faciliter le changement.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette étape génère un email de vérification envoyé à la nouvelle adresse email. L’e-mail contient un code de confirmation qui est requis pour terminer le changement d’adresse e-mail.

1. Saisissez le code de confirmation envoyé à la nouvelle adresse e-mail.

1. Cliquez sur **[!UICONTROL Verify]**.

## Commutateur de compte Adobe ID

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et assurez-vous de remplir les conditions préalables pour cette séquence d’étapes.

Si le propriétaire actuel et le nouveau propriétaire possèdent des identifiants Adobe existants, les deux comptes doivent rester ouverts, mais il est nécessaire de changer d’adresse e-mail. Cela nécessite l’utilisation d’une adresse e-mail _temporaire_ valide, mais qui n’est pas associée à une Adobe ID.

### Passer à un compte temporaire

Le propriétaire actuel effectue ces étapes pour associer son Adobe ID à une autre adresse e-mail temporaire.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez une adresse e-mail temporaire valide qui n’est pas utilisée par un Adobe ID.

   Vous devez avoir accès à l’adresse e-mail afin de pouvoir récupérer l’e-mail avec le code de confirmation.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette étape génère un e-mail de vérification envoyé à l’adresse e-mail temporaire. L’e-mail contient un code de confirmation qui est requis pour terminer le changement d’adresse e-mail.

1. Saisissez le code de confirmation envoyé à l’adresse e-mail temporaire.

1. Cliquez sur **[!UICONTROL Verify]**.

1. Déconnectez-vous du compte Adobe.

### Nouvelles étapes de propriétaire

Une fois que le propriétaire actuel a terminé le transfert vers une adresse électronique temporaire, le nouveau propriétaire doit effectuer les étapes suivantes pour modifier la configuration de son compte afin de pointer vers l&#39;adresse électronique d&#39;origine du propriétaire actuel.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail d’origine du propriétaire actuel.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette étape génère un e-mail de vérification envoyé à l&#39;adresse e-mail d&#39;origine du propriétaire actuel. L’e-mail contient un code de confirmation qui est requis pour terminer le changement d’adresse e-mail.

1. Saisissez le code de confirmation envoyé à l&#39;adresse e-mail d&#39;origine du propriétaire actuel.

1. Cliquez sur **[!UICONTROL Verify]**.

1. Déconnectez-vous du compte Adobe.

### Étapes de suivi

Une fois que le nouveau propriétaire a configuré son compte Adobe avec l’adresse électronique d’origine du propriétaire actuel (maintenant précédent), procédez comme suit pour transférer la propriété.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe à l’aide de l’adresse e-mail du [compte temporaire](#change-to-a-temporary-account).

1. Sous le nom du compte et son avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail du nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Change]**.

   Cette étape génère un e-mail de vérification envoyé à l’adresse e-mail du nouveau propriétaire. L’e-mail contient un code de confirmation qui est requis pour terminer le changement d’adresse e-mail.

1. Saisissez le code de confirmation envoyé à l&#39;adresse e-mail du nouveau propriétaire.

1. Cliquez sur **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Envoyez une demande d’assistance pour informer l’équipe d’assistance que vous avez mis à jour l’adresse e-mail du propriétaire du compte. L’équipe doit effectuer des étapes supplémentaires pour terminer la mise à jour, comme mettre à jour l’adresse e-mail sur votre profil [Commerce Marketplace](https://commercemarketplace.adobe.com/). Incluez l’adresse e-mail du propriétaire du compte précédent dans votre demande.
