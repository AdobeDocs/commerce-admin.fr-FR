---
title: Outils de site Google
description: Découvrez les intégrations d’outils Google que vous pouvez utiliser pour optimiser votre contenu, analyser votre trafic et connecter votre catalogue aux agrégateurs d’achats et aux places de marché.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Outils de site Google

La configuration de votre boutique est intégrée aux outils Google suivants pour vous aider à optimiser votre contenu, à analyser votre trafic et à connecter votre catalogue aux agrégateurs d’achats et aux places de marché.

- [Google Analytics](google-analytics.md) - Utilisez _Google Universal Analytics_ pour définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions d’applications mobiles et hors ligne et l’accès aux mises à jour en cours.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez Google Tag Manager pour gérer les nombreuses balises liées aux événements de campagne marketing.

- [Google AdWords](google-adwords.md) - Créez une campagne Google AdWords et suivez les conversions pour votre boutique.

{{gtag-api-note}}

## Paramètres de confidentialité de Google

Si votre entreprise doit se conformer aux réglementations de confidentialité telles que le [RGPD](../getting-started/compliance-gdpr.md) ou le [CCPA](../getting-started/compliance-ccpa.md), modifiez les paramètres par défaut des outils Google pour répondre aux exigences en matière de confidentialité. Suivez ces étapes pour vous assurer que votre utilisation des données client reste conforme.

### Étape 1 : mettre à jour les paramètres de Google

1. [Connectez-vous][1]{: target="_blank"} au compte Google Analytics de votre entreprise.

1. Dans la partie inférieure de la barre latérale gauche, choisissez **[!UICONTROL Admin]**, puis accédez au compte à modifier (le cas échéant).

1. Dans la colonne **[!UICONTROL Account]**, cliquez sur **[!UICONTROL Account Settings]**.

1. Désactivez le partage de données afin de répondre aux exigences de la réglementation en matière de confidentialité.

   Les paramètres par défaut de Google Analytics partagent les données de votre société avec Google et d’autres utilisateurs. Pour désactiver le partage de données, désélectionnez la case pour sélectionner les paramètres suivants :

   - Produits et services Google
   - Benchmarking
   - Support technique
   - Spécialistes des comptes

1. Acceptez la _modification relative au traitement des données_.

   Les termes de traitement des données Google Ads décrivent le traitement des données par Google et les mesures qu’il prend pour assurer la sécurité des données pour les entreprises soumises au RGPD. Un registre de vos personnes morales et de vos coordonnées est également conservé avec la modification. Pour [en savoir plus][2]{: target="_blank"}, cliquez sur le lien contenu dans le message en haut de la page.

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

Pour en savoir plus, consultez [Référence des champs Analytics.js][3]{: target="_blank"} dans l’aide de Google.

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

Pour en savoir plus, voir [Anonymisation d’IP dans Analytics][4] dans l’aide de Google.

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

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
