---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce avec packages B2B

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B utilise le compositeur pour gérer les packages PHP.

Le fichier `composer.json` déclare la liste des packages, tandis que le fichier `composer.lock` stocke une liste complète des packages (une version complète de chaque package et de ses dépendances) utilisés pour créer une installation d’Adobe Commerce B2B.

La documentation de référence suivante est générée à partir du fichier `composer.lock` et couvre les packages requis inclus dans Adobe Commerce B2B 1.5.2.

## Dépendances

`magento/extension-b2b 1.5.2` possède les dépendances suivantes :

- magento/framework : >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base : 1.5.2
- [magento/module-b2b](https://developer.adobe.com/commerce/php/module-reference/module-b2b/) : 100.5.2
- [devis-négociable-module/magento](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/) : 100.5.1
- [magento/module-bundle-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/) : 100.5.1
- [magento/module-bundle-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/) : 1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/) : 100.5.1
- [magento/module-checkout-address-search-négociable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/) : 100.5.1
- [magento/module-checkout-agreement-négociable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/) : 100.5.1
- [magento/module-checkout-agreement-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/) : 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/) : 102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/) : 1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/) : 100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/) : 1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/) : 1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/) : 1.5.2
- [devis-négociable-magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/) : 1.5.1
- [magento/module-company-négociable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/) : 1.5.1
- [magento/module-company-pay](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/) : 100.5.1
- [prix magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/) : 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/) : 1.5.2
- [relation magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/) : 1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/) : 1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/) : 1.5.1
- [devis-négociable-configurable-magento/module](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/) : 100.5.1
- [magento/module-configurable-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/) : 100.5.1
- [magento/module-configurable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/) : 1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/) : 100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/) : 1.5.1
- [magento/module-downloadable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/) : 1.5.1
- [devis-négociable-carte-cadeau-magento/module](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/) : 100.5.1
- [liste-de-demande-de-carte-cadeau/module-magento](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/) : 100.5.1
- [magento/module-gift-card-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/) : 1.5.1
- [magento/module-gift-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/) : 100.5.1
- [magento/module-grouped-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/) : 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/) : 100.5.1
- [devis-négociable-module/magento](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/) : 101.0.2
- [magento/module-négociable-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/) : 1.5.1
- [magento/module-négociable-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/) : 1.5.2
- [magento/module-négociable-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/) : 1.5.1
- [magento/module-négociable-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/) : 1.5.1
- [magento/module-négociable-quote-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/) : 1.5.1
- [magento/module-négociable-quote-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/) : 1.5.1
- [magento/module-négociable-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/) : 100.5.1
- [modèle-devis-négociable-module/magento](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/) : 1.5.2
- [magento/module-négociable-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/) : 1.5.2
- [magento/module-négociable-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/) : 1.5.1
- [magento/module-négociable-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/) : 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/) : 100.5.2
- [devis-négociable-magento/module-paypal](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/) : 1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/) : 1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/) : 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/) : 1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/) : 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/) : 1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/) : 100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/) : 1.5.1
- [magento/module-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/) : 100.5.2
- [magento/module-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/) : 1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/) : 100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/) : 1.5.1
- magento/security-package-b2b : 1.0.6

## Licences tierces

### Apache-2.0, LGPL-2.1-uniquement

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Client PHP pour OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque d’API Adobe Stock</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>Bibliothèque</td>
    <td>AWS Common Runtime pour PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>Bibliothèque</td>
    <td>AWS SDK for PHP - Utilisez Amazon Web Services dans votre projet PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api">open-telemetry/api</a>
    </td>
    <td>Bibliothèque</td>
    <td>API pour OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context">télémétrie/contexte ouvert</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentation du contexte pour OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>Métapaquet</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Port PHP du processeur LESS</td>
  </tr>
  </tbody>
</table>

### BSD-2-Clause

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">code-qr/bacon</a>
    </td>
    <td>Bibliothèque</td>
    <td>BaconQrCode est un générateur de code QR pour PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">dasprid/enum</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentation de l’énumération PHP 7.1</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">webimpress/safe-writer</a>
    </td>
    <td>Bibliothèque</td>
    <td>Outil pour écrire des fichiers en toute sécurité, pour éviter les conditions de concurrence</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colinmollenhour/cache-backend-file</a>
    </td>
    <td>Magento-module</td>
    <td>Le serveur principal Zend_Cache_Backend_File de stock présente des performances extrêmement faibles pour le nettoyage par balises, ce qui le rend inutilisable à mesure que le nombre d’éléments mis en cache augmente. Ce serveur principal effectue de nombreuses modifications, ce qui améliore considérablement les performances, en particulier pour le nettoyage des balises.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colinmollenhour/php-redis-session-abstract</a>
    </td>
    <td>Bibliothèque</td>
    <td>Gestionnaire de sessions basé sur Redis avec verrouillage optimiste</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une implémentation PHP de Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">firebase/php-jwt</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une simple bibliothèque pour coder et décoder les jetons web JSON (JWT) en PHP. Doit être conforme à la spécification actuelle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>Bibliothèque</td>
    <td>Générer et valider des CAPTCHA à l’aide de puces, d’images, de ReCaptcha, etc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code </a>
    </td>
    <td>Bibliothèque</td>
    <td>Extensions de l'API PHP Reflection, analyse de code statique et génération de code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>Bibliothèque</td>
    <td>fournit une interface utilisateur basée sur une propriété d’objet imbriqué pour accéder à ces données de configuration dans le code de l’application</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di">laminas/laminas-di</a>
    </td>
    <td>Bibliothèque</td>
    <td>Injection de dépendance automatisée pour conteneurs PSR-11</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper">laminas/laminas-escaper</a>
    </td>
    <td>Bibliothèque</td>
    <td>Échappement sécurisé et sécurisé d’HTML, des attributs HTML, de JavaScript, de CSS et des URL</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager">laminas/laminas-eventmanager</a>
    </td>
    <td>Bibliothèque</td>
    <td>Déclencher et écouter des événements dans une application PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed">laminas/laminas-feed</a>
    </td>
    <td>Bibliothèque</td>
    <td>fournit des fonctionnalités pour créer et utiliser des flux RSS et Atom</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter">laminas/laminas-filter</a>
    </td>
    <td>Bibliothèque</td>
    <td>Filtrer et normaliser les données et les fichiers par programmation</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit une interface facile pour exécuter des requêtes HTTP (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n">laminas-i18n</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournissez des traductions pour votre application, et filtrez et validez les valeurs internationalisées</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>Bibliothèque</td>
    <td>fournit des méthodes pratiques pour sérialiser PHP natif en JSON et décoder JSON en PHP natif</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader">laminas/laminas-loader</a>
    </td>
    <td>Bibliothèque</td>
    <td>Stratégies de chargement automatique et de chargement du plug-in</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager">laminas/laminas-modulemanager</a>
    </td>
    <td>Bibliothèque</td>
    <td>Système d'application modulaire pour applications laminas-mvc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc">laminas/laminas-mvc</a>
    </td>
    <td>Bibliothèque</td>
    <td>Couche MVC pilotée par les événements de Laminas, y compris les applications, contrôleurs et modules externes MVC</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit une mise en œuvre légère et flexible de la liste de contrôle d’accès (ACL) pour la gestion des privilèges</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-recaptcha</a>
    </td>
    <td>Bibliothèque</td>
    <td>wrapper OOP pour le service web ReCaptcha</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">laminas/laminas-router</a>
    </td>
    <td>Bibliothèque</td>
    <td>Système de routage flexible pour applications HTTP et console</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">laminas/laminas-server</a>
    </td>
    <td>Bibliothèque</td>
    <td>Créer des serveurs RPC basés sur la réflexion</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager">laminas/laminas-servicemanager</a>
    </td>
    <td>Bibliothèque</td>
    <td>Récipient D'Injection De Dépendance À Commande D'Usine</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">session laminas/laminas</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface orientée objet pour les sessions PHP et le stockage</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap">laminas/laminas-soap</a>
    </td>
    <td>Bibliothèque</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib">laminas/laminas-stdlib</a>
    </td>
    <td>Bibliothèque</td>
    <td>Extensions SPL, utilitaires de tableau, gestionnaires d’erreur, etc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text">laminas/laminas-text</a>
    </td>
    <td>Bibliothèque</td>
    <td>Création de figlets et de tableaux textuels</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator">laminas-translator</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interfaces pour le composant Translator de laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri">laminas/laminas-uri</a>
    </td>
    <td>Bibliothèque</td>
    <td>Un composant qui aide à la manipulation et à la validation des URI (Uniform Resource Identifiers)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator </a>
    </td>
    <td>Bibliothèque</td>
    <td>Classes de validation pour un large éventail de domaines et possibilité d’enchaîner des validateurs pour créer des critères de validation complexes</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view">laminas/laminas-view</a>
    </td>
    <td>Bibliothèque</td>
    <td>Calque de vue flexible prenant en charge et fournissant plusieurs calques de vue, assistants, etc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentation simple et rapide des énumérations avec PHP natif</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>Bibliothèque</td>
    <td>Un analyseur PHP écrit en PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha"> phpfui/recaptcha </a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque cliente pour Google reCAPTCHA pour PHP 8.4 et versions ultérieures</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jshrink</a>
    </td>
    <td>Bibliothèque</td>
    <td>Javascript Minifier intégré en PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port">tubalmartin/cssmin</a>
    </td>
    <td>Bibliothèque</td>
    <td>Un port PHP du compresseur CSS YUI</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause-Modification

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colinmollenhour/cache-backend-redis</a>
    </td>
    <td>Magento-module</td>
    <td>Serveur principal Zend_Cache utilisant Redis avec prise en charge complète des balises.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">paragonie/sodium_compat</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentation Pure PHP de libsodium ; utilise l'extension PHP si elle existe</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1-ou-version ultérieure

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlpurifier</a>
    </td>
    <td>Bibliothèque</td>
    <td>Filtre HTML conforme aux standards écrit en PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>Bibliothèque</td>
    <td>Anciennement videlalvaro/php-amalplib.  Cette bibliothèque est une implémentation pure de PHP du protocole AMQP. Il a été testé contre RabbitMQ.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">braintree/braintree_php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque cliente PHP Braintree</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math">brique/mathématiques</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque arithmétique de précision arbitraire</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une alternative puissante à var_export(), qui peut exporter des fermetures et des objets sans __set_state()</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">christian-riesen/base32</a>
    </td>
    <td>Bibliothèque</td>
    <td>Codeur/décodeur Base32 selon RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis">colinmollenhour/credis</a>
    </td>
    <td>Bibliothèque</td>
    <td>Credis est une interface légère du magasin clé-valeur Redis qui enveloppe la bibliothèque phpredis lorsqu’elle est disponible pour de meilleures performances.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">compositeur/ca-bundle</a>
    </td>
    <td>Bibliothèque</td>
    <td>Vous permet de trouver un chemin d’accès au lot d’autorité de certification système et inclut un secours au lot d’autorité de certification Mozilla.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">compositeur/class-map-generator</a>
    </td>
    <td>Bibliothèque</td>
    <td>Utilitaires pour scanner le code PHP et générer des cartes de classes.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">compositeur</a>
    </td>
    <td>Bibliothèque</td>
    <td>Le compositeur vous aide à déclarer, gérer et installer des dépendances de projets PHP. Cela garantit que vous disposez de la pile appropriée partout.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">compositeur/minificateur-métadonnées</a>
    </td>
    <td>Bibliothèque</td>
    <td>Petite bibliothèque utilitaire qui gère la minimisation et l’extension des métadonnées.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">compositeur/pcre</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque d’encapsulation PCRE qui propose des remplacements preg_* sécurisés par le type.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">compositeur/semver</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque de serveurs qui propose des utilitaires, une analyse et une validation des contraintes de version.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">compositeur/spdx-licences</a>
    </td>
    <td>Bibliothèque</td>
    <td>Liste des licences SPDX et bibliothèque de validation.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">compositeur/xdebug-handler</a>
    </td>
    <td>Bibliothèque</td>
    <td>Redémarre un processus sans Xdebug.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer">doctrine/lexer</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque d'analyseurs PHP Doctrine Lexer qui peut être utilisée dans les analyseurs descendants récursifs.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une bibliothèque pour valider les e-mails par rapport à plusieurs RFC</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php">élastique/transport</a>
    </td>
    <td>Bibliothèque</td>
    <td>Transport HTTP Bibliothèque PHP pour les produits Elastic</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>Bibliothèque</td>
    <td>Client PHP pour Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>Bibliothèque</td>
    <td>Code QR Android</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>Bibliothèque</td>
    <td>Branchement de guzzle/ruisseaux (abandonné) à utiliser avec elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>Bibliothèque</td>
    <td>Branchement de guzzle/RingPHP (abandonné) à utiliser avec elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>Bibliothèque</td>
    <td>Guzzle est une bibliothèque cliente HTTP PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promesses</a>
    </td>
    <td>Bibliothèque</td>
    <td>Guzzle promet une bibliothèque</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentation du message PSR-7 qui fournit également des méthodes d’utilitaire courantes</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">justinrainbow/json-schema</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque permettant de valider un schéma json.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">league/flysystem</a>
    </td>
    <td>Bibliothèque</td>
    <td>Abstraction de stockage de fichier pour PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">league/flysystem-aws-s3-v3</a>
    </td>
    <td>Bibliothèque</td>
    <td>Adaptateur de système de fichiers AWS S3 pour Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">league/flysystem-local</a>
    </td>
    <td>Bibliothèque</td>
    <td>Adaptateur de système de fichiers local pour Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">league/mime-type-detection</a>
    </td>
    <td>Bibliothèque</td>
    <td>Détection de type MIME pour Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog">monologue/monologue</a>
    </td>
    <td>Bibliothèque</td>
    <td>Envoie vos journaux à des fichiers, des sockets, des boîtes de réception, des bases de données et divers services web</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Spécifier de manière déclarative comment extraire des éléments d’un document JSON</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>Bibliothèque</td>
    <td>Implémentations à temps constant du codage RFC 4648 (Base-64, Base-32, Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>Bibliothèque</td>
    <td>PHP 5.x polyfill pour random_bytes() et random_int() de PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier">pelago/emogrifier</a>
    </td>
    <td>Bibliothèque</td>
    <td>Convertit les styles CSS en attributs de style intégrés dans votre code HTML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-plugin</td>
    <td>Recherche et installation des implémentations PSR-7, PSR-17, PSR-18 et HTTPlug</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>Bibliothèque</td>
    <td>HTTPlug, l’abstraction du client HTTP pour PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">php-http/promise</a>
    </td>
    <td>Bibliothèque</td>
    <td>Promesse utilisée pour les requêtes HTTP asynchrones</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>Bibliothèque</td>
    <td>Convertissez les sélecteurs CSS en requêtes XPath.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>Bibliothèque</td>
    <td>API DOM moderne.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fonctions d’accesseur et de mutateur de propriété.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclib/mcrypt_compat</a>
    </td>
    <td>Bibliothèque</td>
    <td>Extension PHP 5.x-8.x polyfill pour mcrypt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclib/phpseclib</a>
    </td>
    <td>Bibliothèque</td>
    <td>Bibliothèque de communications sécurisé PHP - Implémentations Pure-PHP de RSA, AES, SSH2, SFTP, X.509, etc.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">psr/cache</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface commune pour la mise en cache des bibliothèques</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">psr/horloge</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface commune pour la lecture de l'horloge.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">psr/container</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface de conteneur commun (PHP FIG PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">psr/event-dispatcher</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interfaces standard pour la gestion des événements.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">psr/http-client</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface commune pour les clients HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">psr/http-factory</a>
    </td>
    <td>Bibliothèque</td>
    <td>PSR-17 : interfaces communes pour les usines de messages HTTP PSR-7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">psr/http-message</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface commune pour les messages HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">psr/log</a>
    </td>
    <td>Bibliothèque</td>
    <td>Interface commune pour les bibliothèques de journalisation</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getallheaders</a>
    </td>
    <td>Bibliothèque</td>
    <td>Un polyfill pour les en-têtes getall.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection">ramsey/collection</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une bibliothèque PHP pour représenter et manipuler les collections.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid">ramsey/uuid</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une bibliothèque PHP pour générer et travailler avec des identifiants universels uniques (UUID).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">react/promise</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une implémentation légère de CommonJS Promises/A pour PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>Bibliothèque</td>
    <td>Analyseur pour les fichiers CSS écrits en PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>Bibliothèque</td>
    <td>JSON Linter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>Bibliothèque</td>
    <td>Utilitaires de format de fichier PHAR, pour quand PHP vous pharine</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">seld/signal-handler</a>
    </td>
    <td>Bibliothèque</td>
    <td>Gestionnaire de signaux Unix simple qui échoue silencieusement lorsque les signaux ne sont pas pris en charge pour un développement simple sur plusieurs plateformes</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>Bibliothèque</td>
    <td>AES Key Wrap pour PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>Bibliothèque</td>
    <td>Une bibliothèque PHP pour générer des mots de passe à usage unique selon RFC 4226 (algorithme HOTP) et RFC 6238 (algorithme TOTP) et compatible avec Google Authenticator</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>Bibliothèque</td>
    <td>Un framework PHP pour la gestion des infrastructures à clé publique. Il comprend des certificats de clé publique X.509, des certificats d’attribut, des demandes de certification et la validation du chemin de certification.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet de rechercher, charger, combiner, remplir automatiquement et valider des valeurs de configuration de tout type</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console"> symfony/console </a>
    </td>
    <td>Bibliothèque</td>
    <td>Facilite la création d’interfaces de ligne de commande belles et testables</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>Bibliothèque</td>
    <td>Convertit les sélecteurs CSS en expressions XPath</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection"> symfony/dependency-injection </a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet de normaliser et de centraliser la façon dont les objets sont construits dans votre application</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">symfony/deprecation-constraints</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fonction générique et convention pour déclencher des avis d’obsolescence</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit des outils pour gérer les erreurs et faciliter le débogage du code PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit des outils qui permettent aux composants de votre application de communiquer entre eux en distribuant des événements et en les écoutant</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-constraints</a>
    </td>
    <td>Bibliothèque</td>
    <td>Abstractions génériques liées à l’événement de répartition</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/filesystem</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit des utilitaires de base pour le système de fichiers</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>Bibliothèque</td>
    <td>Recherche des fichiers et répertoires via une interface intuitive et fluide</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit des méthodes puissantes pour récupérer des ressources HTTP de manière synchrone ou asynchrone</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-constraints</a>
    </td>
    <td>Bibliothèque</td>
    <td>Abstractions génériques liées aux clients HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>Bibliothèque</td>
    <td>Définit un calque orienté objet pour la spécification HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit un processus structuré pour convertir une requête en réponse</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet d'accéder aux données de localisation de la bibliothèque ICU</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet d’envoyer des e-mails</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet de manipuler des messages MIME</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-ctype</a>
    </td>
    <td>Bibliothèque</td>
    <td>Polyfill symfony pour les fonctions ctype</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill pour les fonctions grapheme_* d'intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill pour les fonctions idn_to_ascii et idn_to_utf8 d’intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill pour la classe Normalizer d’intl et fonctions associées</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>Bibliothèque</td>
    <td>Polyfill Symfony pour l’extension Mbstring</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill rétroportage de quelques fonctionnalités PHP 7.3+ pour abaisser les versions PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill rétroportage de quelques fonctionnalités PHP 8.0+ pour abaisser les versions PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill rétroportage de quelques fonctionnalités PHP 8.1+ pour abaisser les versions PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill rétroportage de quelques fonctionnalités PHP 8.2+ pour abaisser les versions PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>Bibliothèque</td>
    <td>Symfony polyfill rétroportage de quelques fonctionnalités PHP 8.3+ pour abaisser les versions PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>Bibliothèque</td>
    <td>Exécute les commandes dans les sous-processus</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/service-constraints</a>
    </td>
    <td>Bibliothèque</td>
    <td>Abstractions génériques liées aux services d’écriture</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symfony/string</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit une API orientée objet aux chaînes et traite de manière unifiée les octets, les points de code UTF-8 et les clusters de graphème</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>Bibliothèque</td>
    <td>Fournit des mécanismes pour parcourir toute variable PHP arbitraire</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-exporter</a>
    </td>
    <td>Bibliothèque</td>
    <td>Permet d'exporter n'importe quelle structure de données PHP sérialisable en code PHP brut</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>Bibliothèque</td>
    <td>Charge et vide les fichiers YAML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">Web-token/jwt-framework</a>
    </td>
    <td>Symfony-bundle</td>
    <td>Bibliothèque de signature et de chiffrement d’objet JSON pour le bundle PHP et Symfony.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>Bibliothèque</td>
    <td>Port PHP de l’implémentation de référence de GraphQL</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-chèque-cadeau-compte
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-reward
    </td>
    <td>Magento2-module</td>
    <td>S.O.</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>Bibliothèque</td>
    <td>Encodeur CBOR pour PHP</td>
  </tr>
  </tbody>
</table>

### Propriétaire

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### exclusif

<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Magento2-module</td>
    <td>Branchement du module Magento Braintree 2.2.0 de Gene Commerce pour PayPal.</td>
  </tr>
  </tbody>
</table>
