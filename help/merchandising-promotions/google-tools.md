---
title: Outils de site Google
description: Découvrez les intégrations d’outils Google que vous pouvez utiliser pour optimiser votre contenu, analyser votre trafic et connecter votre catalogue aux agrégateurs d’achats et aux places de marché.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/P-IniOyLDfDk8oe1v9ysmRV6yC7IWpxUBaFF--2YMCg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 0%

---

# Outils de site Google

La configuration de votre boutique est intégrée aux outils Google suivants pour vous aider à optimiser votre contenu, à analyser votre trafic et à connecter votre catalogue aux agrégateurs d’achats et aux places de marché.

- [&#128279;](google-analytics.md) - Utilisez _Google Universal Analytics_ pour définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions d’applications mobiles et hors ligne et l’accès aux mises à jour en cours.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez Google Tag Manager pour gérer les nombreuses balises liées aux événements de campagne marketing.

- [Google AdWords](google-adwords.md) - Créez une campagne Google AdWords et suivez les conversions pour votre boutique.

{{gtag-api-note}}

## Paramètres de confidentialité de Google

Si votre entreprise doit se conformer aux réglementations de confidentialité telles que le [RGPD](../getting-started/compliance-gdpr.md) ou le [CCPA](../getting-started/compliance-ccpa.md), modifiez les paramètres par défaut des outils Google pour répondre aux exigences en matière de confidentialité. Suivez ces étapes pour vous assurer que votre utilisation des données client reste conforme.

### Étape 1 : mettre à jour les paramètres de Google

1. [Connectez-vous](https://www.google.com/analytics/){: target="_blank"} au compte Google Analytics de votre entreprise.

1. Dans la partie inférieure de la barre latérale gauche, choisissez **[!UICONTROL Admin]**, puis accédez au compte à modifier (le cas échéant).

1. Dans la colonne **[!UICONTROL Account]**, cliquez sur **[!UICONTROL Account Settings]**.

1. Désactivez le partage de données afin de répondre aux exigences de la réglementation en matière de confidentialité.

   Les paramètres par défaut de Google Analytics partagent les données de votre société avec Google et d’autres utilisateurs. Pour désactiver le partage de données, désélectionnez la case pour sélectionner les paramètres suivants :

   - Produits et services Google
   - Benchmarking
   - Support technique
   - Spécialistes des comptes

1. Acceptez la _modification relative au traitement des données_.

   Les termes de traitement des données Google Ads décrivent le traitement des données par Google et les mesures qu’il prend pour assurer la sécurité des données pour les entreprises soumises au RGPD. Un registre de vos personnes morales et de vos coordonnées est également conservé avec la modification. Pour [en savoir plus](https://support.google.com/analytics/answer/3379636){: target="_blank"}, cliquez sur le lien contenu dans le message en haut de la page.

   - Faites défiler la page vers le bas pour **[!UICONTROL Data Processing Amendment]**.
   - Cliquez sur **[!UICONTROL Review Amendment]** pour lire les _conditions de traitement des données Google Ads_.
   - Cliquez sur **[!UICONTROL Accept]**.
   - Cliquez sur **[!UICONTROL Save]**.

1. Renseignez les détails de l&#39;_Administration DPA_.

   - Cliquez sur **[!UICONTROL Manage DPA Details]** pour ouvrir une page d&#39;administration DPA dans laquelle vous pouvez modifier les contacts et les entités juridiques de votre entreprise.

   - Dans la section **[!UICONTROL Legal Entities]**, cliquez sur l’icône _Modifier_ ( ![icône de modification de Google](./assets/google-icon-edit.png) ) et ajoutez un ou plusieurs noms enregistrés pour votre organisation. Cliquez ensuite sur **[!UICONTROL Save]**.

   - Dans la section **Contacts**, cliquez sur l’icône _Ajouter_ ( ![icône d’ajout Google](./assets/google-icon-add.png) ) et saisissez les informations du premier contact. Cochez ensuite la case de chaque rôle applicable et cliquez sur **[!UICONTROL Add]**.

      - Contact Principal - (Adresse e-mail de notification) Contact auquel les notifications sont envoyées.
      - Délégué à la protection des données - (le cas échéant) Personne désignée pour faciliter le respect de la réglementation en matière de confidentialité.
      - Représentant de l&#39;Espace économique européen (EEE) - (Le cas échéant) Personne qui représente des clients en dehors de l&#39;UE concernant leurs obligations en vertu du RGPD.

     Répétez l’opération pour ajouter un autre contact, le cas échéant.

### Étape 2 : modifier vos bibliothèques JS Google

Google prend en charge trois bibliothèques JavaScript pour mesurer l’utilisation du site web, en fonction du produit Google : `gtag.js`, `analytics.js` et `ga.js`. Pour répondre aux exigences de confidentialité, le code standard peut être modifié comme suit :

#### Anonymisation des adresses IP

Pour rendre anonymes les adresses IP utilisées par **_Google Universal Analytics_**, ajoutez le fragment de code suivant à la bibliothèque `analytics.js` sur votre serveur web :

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Pour en savoir plus, consultez [Référence des champs Analytics.js](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"} dans l’aide de Google.

Si vous utilisez l’ancienne bibliothèque `ga.js`, ajoutez le fragment de code suivant :

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Pour rendre anonymes les adresses IP utilisées par **_Google Tag Manager_**, définissez le paramètre `anonymize_ip` sur `true` dans la bibliothèque `gtag.js` de votre serveur web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Pour en savoir plus, voir [Anonymisation d’IP dans Analytics](https://support.google.com/analytics/answer/2763052) dans l’aide de Google.

#### Forcer SSL

Pour forcer la transmission de toutes les données Google sur une couche de socket sécurisée (SSL), ajoutez le fragment de code suivant à la bibliothèque `analytics.js` sur votre serveur web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Étape 3 : mettre à jour votre politique de confidentialité

Mettez à jour votre [politique de confidentialité](../getting-started/privacy-policy.md) pour indiquer que votre entreprise :

- Utilise Google Analytics
- Masque les adresses IP pour masquer les informations personnelles
- A désactivé le partage de données Google
- N’utilise pas d’autres services Google avec les cookies Google Analytics
