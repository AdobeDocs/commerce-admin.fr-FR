---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] de l’administrateur Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] a été développé par [!DNL Visa] pour promouvoir des transactions en ligne sécurisées. Exemples [!DNL 3-D Secure] les solutions créées par les réseaux de cartes sont vérifiées par [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], et [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] est un chef de file mondial de l’authentification des transactions numériques et une filiale à part entière de [!DNL Visa].

[!DNL 3-D Secure] La version 2.0 prend en charge de nombreuses améliorations, notamment des méthodes d’authentification avancées et un flux d’authentification, ainsi qu’un meilleur partage des données entre le commerçant et l’émetteur.

>[!NOTE]
>
>La variable [Braintree](../../stores-purchase/braintree.md) la passerelle de paiement prend également en charge [!DNL 3-D Secure] vérification.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Environment] | Site Web | Indique le mode de fonctionnement de votre [!DNL CardinalCommerce] compte . Si vous exécutez dans un environnement de test, sélectionnez &quot;Environnement de test&quot;. Options : environnement de test/production (par défaut) |
| [!UICONTROL Org Unit ID] | Site Web | L’ID d’unité de l’organisation de votre [!DNL CardinalCommerce] compte marchand. |
| [!UICONTROL API Key] | Site Web | La clé API de votre [!DNL CardinalCommerce] compte marchand. |
| [!UICONTROL API Identifier] | Site Web | L’identifiant API de votre [!DNL CardinalCommerce] compte marchand. |
| [!UICONTROL Debug] | Site Web | Options : `Yes` / `No` |

{style="table-layout:auto"}
