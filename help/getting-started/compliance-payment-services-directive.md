---
title: Conformité à PSD2
description: Découvrez les exigences de la directive Services de paiement (PSD2) qui peuvent affecter votre boutique.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Conformité à PSD2

À compter du 14 septembre 2019, l’Union européenne exige que tous les commerçants de l’UE et du Royaume-Uni se conforment aux exigences de la [Strong Customer Authentication](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) de la directive sur les services de paiement (PSD2). Les commerçants de tous les autres pays sont encouragés à respecter le PSD2 comme une bonne pratique.

>[!NOTE]
>
>Cette rubrique est destinée uniquement à titre d’information et ne doit pas être interprétée comme un avis juridique. Pour déterminer si et comment votre entreprise doit se conformer à des obligations légales, consultez votre service juridique.

L’authentification forte du client est un composant clé de PSD2. Elle requiert deux des éléments suivants :

- Quelque chose dont seul le client dispose (mot de passe ou code PIN)
- Quelque chose que seul le client sait (jeton de sécurité unique généré par le sélecteur de téléphone ou de clé)
- Quelque chose que seul le client est (authentification biométrique telle qu’une empreinte ou une reconnaissance faciale)

Les banques européennes peuvent refuser des paiements qui ne répondent pas aux exigences. Cependant, les transactions à faible risque et à faible valeur peuvent toujours être acceptées, et les paiements ultérieurs dans un abonnement récurrent.

En raison de cette modification importante et pour s’assurer que les paiements client ne sont pas refusés, Adobe a introduit les modifications et recommandations suivantes pour les intégrations de paiement [!DNL Commerce] natives.

| Mode de paiement | Exigences de conformité |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Pour la plupart des solutions PayPal, aucune action n’est requise pour se conformer à PSD2, car les exigences sont gérées par PayPal. Pour plus d’informations sur des solutions spécifiques, consultez la note en haut de chaque rubrique de PayPal. |
| [Braintree](../stores-purchase/braintree.md) | À compter de la mise en place de l’extension installée dans la version 2.4.0, les exigences sont traitées dans le module de paiements de Braintree inclus et aucune action n’est requise pour se conformer au PSD2. <br /><br />**_Remarque :_**&#x200B;Pour vous conformer à PSD2 à l’aide de l’intégration principale dans les versions précédentes, effectuez l’une des opérations suivantes :<br/>- (recommandé) Installez l’extension officielle d’intégration des paiements de Braintree à partir de [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/> - Activez et configurez le mode de paiement du Braintree dans la configuration [!DNL Commerce].<br/><br/>Ces intégrations principales antérieures prennent en charge la vérification 3D Secure 2.0. Toutefois, les implémentations de Braintree qui s’exécutent sur le SDK JavaScript v2 ne prennent pas en charge 3D Secure 2.0. |
| Autre | Pour toutes les autres intégrations de paiement, vérifiez les extensions disponibles sur [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Demandez à votre fournisseur de paiement de recommander une solution pour répondre aux exigences du PSD 2. |

{style="table-layout:auto"}
