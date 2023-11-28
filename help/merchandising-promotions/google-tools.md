---
title: Outils du site Google
description: Découvrez les intégrations d’outils Google que vous pouvez utiliser pour optimiser votre contenu, analyser votre trafic et connecter votre catalogue aux agrégateurs d’achats et aux marchés.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Outils du site Google

La configuration de votre magasin est intégrée aux outils Google suivants pour vous aider à optimiser votre contenu, à analyser votre trafic et à connecter votre catalogue aux agrégateurs d’achats et aux marchés.

- [Google Analytics](google-analytics.md) - Utilisation _Google Universal Analytics_ pour définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions avec les applications mobiles et hors ligne, ainsi que l’accès aux mises à jour en cours.

- [Expériences de contenu Google](google-content-experiments.md) - Configurez un test A/B pour les produits, les catégories ou les pages de contenu à l’aide des expériences de contenu Google Analytics.

- [Gestionnaire de balises de Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez Google Tag Manager pour gérer les nombreuses balises liées aux événements de campagne marketing.

- [Google AdWords](google-adwords.md) - Créez une campagne Google AdWords et effectuez le suivi des conversions pour votre magasin.

{{gtag-api-note}}

## Paramètres de confidentialité de Google

Si votre entreprise est tenue de se conformer aux réglementations de confidentialité, telles que [RGPD](../getting-started/compliance-gdpr.md) ou [CCPA](../getting-started/compliance-ccpa.md), modifiez les paramètres par défaut des outils Google pour répondre aux exigences de confidentialité. Suivez ces étapes pour vous assurer que votre utilisation des données client reste conforme.

### Étape 1 : mise à jour des paramètres Google

1. [Se connecter][1]{ : target=&quot;_blank&quot;} pour accéder au compte Google Analytics de votre société.

1. Dans la partie inférieure de la barre latérale gauche, choisissez **[!UICONTROL Admin]**, puis accédez au compte à modifier (le cas échéant).

1. Dans le **[!UICONTROL Account]** colonne, cliquez sur **[!UICONTROL Account Settings]**.

1. Désactivez le partage de données afin de répondre aux exigences de la réglementation sur la confidentialité.

   Les paramètres par défaut des Google Analytics partagent les données de votre société avec Google et d’autres tiers. Pour désactiver le partage des données, décochez la case de sélection pour les paramètres suivants :

   - Produits et services Google
   - Évaluation
   - Support technique
   - Spécialistes des comptes

1. Acceptez la variable _Modification du traitement des données_.

   Les termes de traitement des données de Google Ads décrivent comment Google traite les données et les mesures qu’il prend pour garantir la sécurité des données pour les entreprises soumises au RGPD. Un enregistrement de vos entités juridiques et de vos coordonnées est également conservé avec la modification. À [en savoir plus][2]{: target=&quot;_blank&quot;}, cliquez sur le lien dans le message en haut de la page.

   - Faites défiler la page vers le bas pour **[!UICONTROL Data Processing Amendment]**.
   - Cliquez sur **[!UICONTROL Review Amendment]** pour lire le _Termes de traitement des données de Google Ads_.
   - Cliquez sur **[!UICONTROL Accept]**.
   - Cliquez sur **[!UICONTROL Save]**.

1. Procédez comme suit : _Administration des DPA_ détails.

   - Cliquez sur **[!UICONTROL Manage DPA Details]** pour ouvrir une page d’administration DPA dans laquelle vous pouvez modifier les contacts et les entités juridiques de votre entreprise.

   - Dans le **[!UICONTROL Legal Entities]** , cliquez sur le bouton _Modifier_ ( ![Icône Modifier Google](./assets/google-icon-edit.png) ) et ajoutez un ou plusieurs noms enregistrés pour votre organisation. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   - Dans le **Contacts** , cliquez sur le bouton _Ajouter_ ( ![Icône Ajouter Google](./assets/google-icon-add.png) ) et saisissez les informations du premier contact. Ensuite, cochez la case de chaque rôle applicable et cliquez sur **[!UICONTROL Add]**.

      - Contact Principal - (adresse électronique de notification) Contact à qui les avis sont envoyés.
      - Délégué à la protection des données - (le cas échéant) La personne désignée pour faciliter la conformité à la réglementation sur la protection des données.
      - Représentant de l’Espace économique européen (EEE) - (le cas échéant) La personne qui représente les clients en dehors de l’UE concernant leurs obligations en vertu du RGPD.

     Répétez l&#39;opération pour ajouter un autre contact, le cas échéant.

### Étape 2 : modification des bibliothèques JS Google

Google prend en charge trois bibliothèques JavaScript pour mesurer l’utilisation du site web, en fonction du produit Google : `gtag.js`, `analytics.js`, et `ga.js`. Pour répondre aux exigences de confidentialité, le code standard peut être modifié comme suit :

#### Anonymiser les adresses IP

Pour anonymiser les adresses IP utilisées par **_Google Universal Analytics_**, ajoutez le fragment de code suivant au `analytics.js` bibliothèque sur votre serveur web :

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Pour en savoir plus, voir la section [Référence du champ Analytics.js][3]{: target=&quot;_blank&quot;} dans l’aide de Google.

Si vous utilisez l’ancien `ga.js` , ajoutez le fragment de code suivant :

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Pour anonymiser les adresses IP utilisées par **_Gestionnaire de balises de Google_**, définissez la variable `anonymize_ip` du paramètre `true` dans le `gtag.js` sur votre serveur web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Pour en savoir plus, voir [Analyse des adresses IP dans Analytics][4] dans l’aide de Google.

#### Forcer SSL

Pour forcer la transmission de toutes les données Google sur une couche de socket sécurisée (SSL), ajoutez le fragment de code suivant au `analytics.js` sur votre serveur web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Étape 3 : mise à jour de votre politique de confidentialité

Mettez à jour votre [politique de confidentialité](../getting-started/privacy-policy.md) pour indiquer à votre société :

- Utilise des Google Analytics
- Masque les adresses IP pour masquer les informations personnelles.
- A désactivé le partage de données Google
- N’utilise pas d’autres services Google avec les cookies Google Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
