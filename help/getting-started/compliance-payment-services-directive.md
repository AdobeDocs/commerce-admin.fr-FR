---
title: Conformité à PSD2
description: Découvrez les exigences de la directive sur les services de paiement (PSD2) qui peuvent affecter votre boutique.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# Conformité à PSD2

À compter du 14 septembre 2019, l&#39;Union européenne exige que tous les commerçants de l&#39;UE et du Royaume-Uni se conforment aux exigences [authentification forte des clients](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) de la directive sur les services de paiement (PSD2). Les commerçants de tous les autres pays sont encouragés à se conformer à PSD2 en tant que bonne pratique.

>[!NOTE]
>
>Cette rubrique est uniquement fournie à titre d’information et ne doit pas être interprétée comme un avis juridique. Pour déterminer si votre entreprise devrait se conformer à des obligations légales et, le cas échéant, comment, consultez votre conseiller juridique.

L’authentification forte du client est un composant essentiel de PSD2 et requiert deux des éléments suivants :

- Élément dont seul le client dispose (mot de passe ou code confidentiel)
- Ce que seul le client sait (jeton de sécurité unique généré par le téléphone ou le porte-clés)
- Élément dont seul le client est capable (authentification biométrique, par exemple par empreinte digitale ou reconnaissance faciale)

Les banques européennes peuvent refuser des paiements qui ne répondent pas aux exigences. Cependant, les transactions à faible risque et à faible valeur peuvent toujours être acceptées, et les paiements ultérieurs dans un abonnement récurrent.

En raison de ce changement important et pour s’assurer que les paiements des clients ne sont pas refusés, Adobe a introduit les modifications et recommandations suivantes pour les intégrations de paiements natives [!DNL Commerce].

| Mode de paiement | Exigences de conformité |
|--- |--- |
| [ PayPal ](../stores-purchase/paypal.md) | Pour la plupart des solutions PayPal, aucune action n&#39;est nécessaire pour se conformer à PSD2, car les exigences sont gérées par PayPal. Pour plus d&#39;informations sur des solutions spécifiques, consultez la remarque en haut de chaque rubrique PayPal. |
| [](../stores-purchase/braintree.md) | À partir du passage à l’extension installée dans la version 2.4.0, les exigences sont gérées dans le module Braintree Payments inclus et aucune action n’est requise pour se conformer à PSD2. <br /><br />**_Note:_** Pour vous conformer à PSD2 en utilisant l’intégration principale dans les versions précédentes, effectuez l’une des opérations suivantes :<br/>- (Recommandé) Installez l’extension d’intégration de paiement Braintree officielle à partir de [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Activez et configurez le mode de paiement Braintree dans la configuration [!DNL Commerce].<br/><br/>Ces intégrations principales antérieures prennent en charge la vérification 3D Secure 2.0. Toutefois, les implémentations de Braintree qui s’exécutent sur JavaScript SDK v2 ne prennent pas en charge 3D Secure 2.0. |
| Autres frais | Pour toutes les autres intégrations de paiement, vérifiez les extensions disponibles sur [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Demandez à votre fournisseur de services de paiement de vous recommander une solution pour répondre aux exigences de PSD2. |

{style="table-layout:auto"}
