---
title: Transfert d’un compte Adobe Commerce
description: Découvrez comment transférer un compte Adobe Commerce vers un nouveau propriétaire ou une nouvelle adresse e-mail, choisir le type de transfert approprié, vérifier les modifications apportées aux e-mails et contacter l’assistance.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Transfert d’un compte Adobe Commerce

À mesure que les responsabilités professionnelles changent, vous devrez peut-être transférer votre compte Adobe Commerce à un nouveau propriétaire ou à une autre adresse e-mail. Ce transfert nécessite une modification de l’adresse e-mail de l’utilisateur principal associée au compte.

Les informations suivantes décrivent le processus de transfert d’un compte Adobe Commerce (MAGEID). Elle n’inclut pas les modifications apportées à Adobe Commerce sur la propriété du projet d’infrastructure cloud ni la propriété du [!DNL New Relic]. Pour plus d’informations sur l’accès aux projets cloud, consultez [Gérer l’accès des utilisateurs](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) dans le guide _Commerce sur les infrastructures cloud_.

>[!IMPORTANT]
>
>Si le nouveau propriétaire du compte a acheté des extensions à l’aide de l’accès partagé, l’accès à ces extensions est perdu dès le début du transfert du compte.
>
>Avant de demander le transfert du compte, assurez-vous que le nouveau propriétaire récupère les ID de commande pour les achats sur [son [!DNL Commerce Marketplace] compte](https://commercemarketplace.adobe.com/sales/order/history/) et demande un remboursement à l’[[!DNL Commerce Marketplace] équipe](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Les achats d’extension ne peuvent pas être transférés vers un autre compte.

## Identification du type de transfert

Le processus de transfert de compte Adobe Commerce approprié dépend du statut du compte du propriétaire actuel et du nouveau propriétaire, et de si l’adresse e-mail du propriétaire actuel est toujours accessible. Par exemple, si le propriétaire actuel a quitté la société, vous devrez peut-être toujours accéder aux e-mails envoyés à cette adresse.

Les scénarios suivants décrivent les options de transfert disponibles en fonction de ces conditions.

| Type de transfert | Propriétaire actuel | Nouveau propriétaire |
| ------------- | ------------- | --------- |
| [Nouvel Adobe ID et modification des e-mails](#new-adobe-id-and-email-change) | A un MAGEID qui n’a pas été connecté à un Adobe ID | N’a pas de MAGEID et n’a pas d’Adobe ID. |
| [Modification des e-mails uniquement](#email-change) | Dispose d’un MAGEID connecté à un Adobe ID. | Dispose d’un Adobe ID, mais n’a pas de MAGEID connecté au compte. |
| [Changement de compte &#x200B;](#adobe-id-account-switch) | Dispose d’un MAGEID connecté à un Adobe ID. | Dispose d’un MAGEID et est connecté à un Adobe ID. |

{style="table-layout:auto"}

>[!NOTE]
>
>Comme Adobe Commerce continue à s’intégrer avec d’autres solutions Adobe, un compte Adobe Commerce (MAGEID) nécessite désormais une association avec un Adobe ID. Adobe ID utilise la même adresse e-mail que celle associée à votre compte [Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Vérifier une modification d’e-mail Adobe ID

Plusieurs chemins de transfert utilisent le même workflow de vérification sur [account.adobe.com](https://account.adobe.com/). Après avoir saisi l’adresse e-mail cible et cliqué sur **[!UICONTROL Change]**, procédez comme suit :

1. Ouvrez l’e-mail de vérification envoyé à l’adresse que vous avez saisie et recherchez le code de confirmation.

1. Saisissez le code de confirmation.

1. Cliquez sur **[!UICONTROL Verify]**.

## Nouvelle Adobe ID et modification d’e-mail

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et vérifiez que ce chemin d’accès correspond à votre situation :
>
>- Le propriétaire actuel fait toujours partie de l&#39;entreprise.
>- Le propriétaire actuel n&#39;a pas d&#39;Adobe ID ou a un Adobe ID qui n&#39;est pas connecté à son compte [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Le nouveau propriétaire ne dispose pas d’Adobe ID ni de compte Adobe Commerce.

Utilisez ce chemin d’accès lorsque le propriétaire actuel possède un MAGEID qui n’est pas encore lié à une Adobe ID. Le ou la propriétaire actuel(le) crée et lie d’abord une Adobe ID, puis modifie cette adresse e-mail Adobe ID en fonction de l’adresse e-mail du nouveau ou de la nouvelle propriétaire.

1. Accédez à la page [Connexion au compte &#x200B;](https://account.magento.com/customer/account/login/).

1. Cliquez sur **[!UICONTROL Sign in with Adobe ID]**.

1. Cliquez sur **[!UICONTROL Create an account]**.

1. Saisissez l&#39;adresse e-mail et le mot de passe du propriétaire actuel.

1. Cliquez sur **[!UICONTROL Continue]**.

   Cette étape permet de créer une Adobe ID et de la lier au compte Adobe Commerce courant (MAGEID). Avec ce lien de compte, le champ _[!UICONTROL Email]_&#x200B;est bloqué de toute modification. La configuration de l’adresse e-mail associée est gérée à partir du compte Adobe ID.

1. Accédez à [account.adobe.com](https://account.adobe.com/).

1. Cliquez sur **[!UICONTROL Change Email]**.

1. Saisissez l’adresse e-mail du nouveau propriétaire.

   Si la nouvelle adresse e-mail est déjà associée à un autre compte du système, elle ne peut pas être directement utilisée pour le transfert. Suivez plutôt le chemin d’accès du compte [&#128279;](#adobe-id-account-switch) et utilisez une [adresse e-mail temporaire](#change-to-a-temporary-account).

1. Suivez les [&#x200B; étapes de vérification par e-mail &#x200B;](#verify-an-adobe-id-email-change).

Une fois que le nouveau propriétaire a vérifié l’adresse e-mail, passez à la [Étapes finales](#final-steps) afin que l’assistance Adobe Commerce puisse mettre à jour les enregistrements de compte tels que le profil de [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## Modification d’e-mail uniquement {#email-change}

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et vérifiez que ce chemin d’accès correspond à votre situation :
>
>- Le propriétaire actuel fait toujours partie de l&#39;entreprise.
>- Le propriétaire actuel possède un Adobe ID connecté à son compte [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Le nouveau propriétaire a un Adobe ID qui n’est pas connecté à un compte Adobe Commerce.

Avant de commencer, notez que ce type de transfert entraîne pour le titulaire du compte actuel la perte d’accès à d’autres produits Adobe liés à cette Adobe ID.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail du nouveau propriétaire.

   Si la nouvelle adresse e-mail est déjà associée à un autre compte du système, elle ne peut pas être directement utilisée pour le transfert. Suivez plutôt le chemin d’accès du compte [&#128279;](#adobe-id-account-switch) et utilisez une [adresse e-mail temporaire](#change-to-a-temporary-account).

1. Suivez les [&#x200B; étapes de vérification par e-mail &#x200B;](#verify-an-adobe-id-email-change).

Une fois que le nouveau propriétaire a vérifié l’adresse e-mail, passez à la [Étapes finales](#final-steps) afin que l’assistance Adobe Commerce puisse mettre à jour les enregistrements de compte tels que le profil de [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Commutateur de compte Adobe ID

>[!IMPORTANT]
>
>Passez en revue les [types de transfert](#identify-your-transfer-type) et vérifiez que ce chemin d’accès correspond à votre situation :
>
>- Le propriétaire actuel ne fait plus partie de l’entreprise, mais les e-mails envoyés à l’adresse e-mail de l’entreprise du propriétaire actuel sont toujours accessibles, ou votre équipe informatique peut transférer ces e-mails à un contact autorisé.
>- Le propriétaire actuel possède un Adobe ID connecté à son compte [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Le nouveau propriétaire dispose d’une Adobe ID connectée à son compte Adobe Commerce.

Ce type de transfert utilise une adresse e-mail temporaire pour changer de propriétaire de compte lorsque le propriétaire actuel et le nouveau propriétaire possèdent tous deux des Adobe ID existants et que vous souhaitez conserver les deux Adobe ID. Pour effectuer le transfert de propriété, vous devez utiliser une adresse e-mail temporaire qui n’est pas associée à une Adobe ID.

### Passer à un compte temporaire

Pour associer l’Adobe ID du propriétaire actuel à une adresse e-mail temporaire, procédez comme suit. Vous devez avoir accès à cette adresse e-mail afin de pouvoir récupérer le code de confirmation.

>[!NOTE]
>
>Si vous ne pouvez pas accéder à l’adresse e-mail du propriétaire actuel, demandez à votre équipe informatique de configurer le transfert d’e-mail pour l’adresse e-mail du compte dans le système de messagerie de votre entreprise. Si le transfert d’e-mail ne peut pas être configuré, assurez-vous que le nouveau propriétaire du compte dispose d’une Adobe ID, puis [envoyez une demande d’assistance](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) avec tous les détails nécessaires pour lancer le transfert du compte.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez une adresse e-mail temporaire valide qui n’est pas utilisée par un Adobe ID.

1. Suivez les [&#x200B; étapes de vérification par e-mail &#x200B;](#verify-an-adobe-id-email-change).

1. Déconnectez-vous du compte Adobe.

### Nouvelles étapes de propriétaire

Une fois que le propriétaire actuel a effectué le transfert vers une adresse e-mail temporaire, le nouveau propriétaire doit effectuer les étapes suivantes pour remplacer son adresse e-mail Adobe ID par l’adresse e-mail d’origine du propriétaire actuel.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe.

1. Sous le nom de votre compte et votre avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail d’origine du propriétaire actuel.

1. Suivez les [&#x200B; étapes de vérification par e-mail &#x200B;](#verify-an-adobe-id-email-change).

1. Déconnectez-vous du compte Adobe.

### Étapes de suivi

Une fois que le nouveau propriétaire a configuré son Adobe ID avec l’adresse électronique d’origine du propriétaire actuel, procédez comme suit pour attribuer cette adresse électronique au nouveau propriétaire.

1. Accédez à [account.adobe.com](https://account.adobe.com/) et effectuez la connexion à Adobe à l’aide de l’adresse e-mail du [compte temporaire](#change-to-a-temporary-account).

1. Sous le nom du compte et son avatar, cliquez sur **[!UICONTROL Change Email]**.

1. Dans la boîte de dialogue, saisissez l’adresse e-mail du nouveau propriétaire.

1. Suivez les [&#x200B; étapes de vérification par e-mail &#x200B;](#verify-an-adobe-id-email-change).

Une fois que le nouveau propriétaire a vérifié l’adresse e-mail, passez à la [Étapes finales](#final-steps) afin que l’assistance Adobe Commerce puisse mettre à jour les enregistrements de compte tels que le profil de [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Dernières étapes

Effectuez ces étapes après avoir terminé le processus [Nouvelle Adobe ID et modification d’e-mail](#new-adobe-id-and-email-change), [Modification d’e-mail uniquement](#email-change) ou [Changement de compte Adobe ID](#adobe-id-account-switch).

1. En tant que nouveau propriétaire, [envoyez une demande d’assistance](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Insérez les détails suivants :

   - Adresse électronique du propriétaire du compte précédent
   - Adresse e-mail du nouveau propriétaire
   - Remarque : vous avez terminé un transfert de compte Adobe Commerce et mis à jour l’adresse e-mail Adobe ID

1. Patientez jusqu’à ce que la prise en charge d’Adobe Commerce confirme la mise à jour.

   L’assistance met également à jour les enregistrements associés, tels que l’adresse e-mail sur votre profil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

Une fois la demande terminée, le nouveau propriétaire peut se connecter au compte Adobe Commerce avec son Adobe ID. Le MAGEID reste l’identifiant des droits du compte.
