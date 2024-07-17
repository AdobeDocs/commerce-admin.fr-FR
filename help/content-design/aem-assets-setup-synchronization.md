---
title: Activation de la synchronisation des ressources
description: "Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets au service de moteur de règles Assets pour activer la synchronisation des ressources entre ces deux systèmes."
feature: CMS, Media
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 0%

---


# Configuration du service de synchronisation

Le service ARES (Asset Rules Engine Service) est un service multi-client qui intègre AEM Assets à Adobe Commerce. Ce service synchronise les ressources entre Adobe Commerce et Experience Manager. Le service ARES associe automatiquement les ressources d’AEM aux produits d’Adobe Commerce en fonction du SKU ou d’autres attributs clés. Elle garantit également que les dernières ressources et variations de produit sont toujours disponibles sur le site d’e-commerce.

Pour configurer le service, vous devez enregistrer votre ID de tenant à l’aide de l’API GraphQL ARES et sélectionner la règle correspondante pour synchroniser les ressources.

## Choisir une stratégie correspondante

L’intégration AEM Assets pour Commerce prend en charge deux stratégies correspondantes pour synchroniser des ressources entre Adobe Commerce et AEM Assets.

- **MatchBySku** : il s’agit de la règle de correspondance par défaut qui correspond aux ressources en fonction de l’unité de gestion des stocks (SKU) du produit. Le SKU est un identifiant unique pour chaque produit. Cette règle correspond au SKU des métadonnées de la ressource avec le SKU du produit Commerce pour s’assurer que les ressources sont associées aux produits appropriés.

- **ExternalMatcher** : cette règle de correspondance est destinée à des scénarios plus complexes ou à des besoins spécifiques qui nécessitent une logique de correspondance personnalisée. Pour utiliser cette règle, un code personnalisé doit être implémenté dans Adobe Developer App Builder afin de définir la manière dont les ressources sont mises en correspondance avec les produits.

Pour l’intégration initiale, utilisez la stratégie `MatchBySku`. Si nécessaire, vous pourrez modifier la stratégie correspondante ultérieurement.

## Enregistrement d’un client

>[!BEGINSHADEBOX]

**Condition préalable requise**

- [Le projet AEM Assets a été configuré avec les métadonnées Commerce requises pour mapper les ressources](aem-assets-configure-aem.md).

- [Installez et configurez l’intégration Experience Manager Assets dans Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Collecte des informations d’identification

Vous avez besoin des informations d’identification suivantes pour vous authentifier et connecter votre environnement de projet Commerce et votre environnement de projet AEM Assets aux services Commerce SaaS.

| Données requises | Source | Où le trouver |
| ---------- | ------ | ------------- |
| Clé API du compte Magento | Commerce | Fournissez la clé d’API publique pour l’environnement Commerce que vous utilisez, l’évaluation ou la production. Vous trouverez les clés d’API pour les environnements de production et d’évaluation sur la page [Configuration du connecteur de service Commerce](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) dans l’administrateur ou sur la page [!UICONTROL My Account] de la section [!UICONTROL API Portal]. |
| Identifiant de projet SaaS Commerce <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Administration de Commerce | Ces valeurs identifient l’environnement Commerce, l’espace de données SaaS et le projet auxquels se connecter. Les valeurs proviennent de la [ configuration de l’identifiant SaaS du connecteur Commerce Services ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId` et <br>`environmentId` | [Environnement de création AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Ouvrez la page AEM Sites et sélectionnez **[!UICONTROL Assets]**.  Copiez les ID de projet et d’environnement de l’URL :<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | Commerce storefront | [URL de base](../stores-purchase/store-urls.md) pour votre vitrine Commerce. |
| Informations d’identification OAuth pour l’accès aux API | Administration de Commerce | Vous pouvez trouver ces informations d’identification dans les paramètres de configuration de Commerce [ pour l’intégration d’Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release). |

## Enregistrer le client

Terminez l’enregistrement du client en envoyant une requête au service Assets Rule Engine pour ajouter des informations d’identification d’authentification et des identifiants de client. La requête inclut les informations d’identification et les identifiants de projet nécessaires pour établir les connexions entre le service, le projet Commerce et le projet Experience Manager Assets.

Envoyez la demande à l’aide d’un client GraphQL ou d’une cURL.

>[!BEGINTABS]

>[!TAB Requête GraphQL]

Utilisez un client GraphQL pour envoyer une requête de POST au point de terminaison de l’API `https://commerce.adobe.io/assets-integration/graphql`

**En-têtes requis**

Spécifiez les en-têtes HTTP suivants pour la requête :

- `x-api-key` : clé API de votre compte de Magento
- `magento-environment-Id` : identifiant SaaS
- `x-gw-signature` : JWT Token associé au MAGEID

**Requête :**

**Syntaxe**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**Exemple d’utilisation**

Enregistrez un client et sélectionnez la règle `matchBySku` pour mapper des ressources entre Adobe Commerce et le projet AEM Assets.

**Requête :**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Réponse**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB requête cURL]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Champs d’entrée

#### AemInput

Identifie l’instance AEM Assets pour le stockage des ressources Commerce. Vous pouvez obtenir ces informations à partir de la vue Mes programmes de Cloud Manager ou de l’URL de création de contenu.

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| `programId` | Chaîne ! | Identifiant unique de votre projet dans AEM Cloud Service |
| `environmentId` | Chaîne ! | Identifiant de l’environnement de projet que vous utilisez, tel que Production, Test ou Développement |

#### CommerceInput

Ce champ de saisie fournit les informations d’identification d’authentification OAuth pour l’accès de l’API au catalogue Commerce. Vous pouvez trouver ces informations d’identification dans les paramètres de configuration de Commerce [ pour l’intégration d’Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| `baseUrl` | Chaîne | [URL de base](../stores-purchase/store-urls.md) pour votre vitrine Commerce. |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Indique les informations d’identification pour accéder à l’instance Commerce. |
| `extensionVersion` | Chaîne | Facultatif. Version de l’intégration AEM Assets pour l’extension Commerce installée sur l’instance Commerce. |
| `version` | Chaîne | Facultatif. Version de l’application Commerce installée sur l’instance Commerce. |

#### CommerceCredentialsInput

Ce champ de saisie fournit les informations d’identification OAuth pour l’accès de l’API au catalogue Commerce. Vous pouvez trouver ces informations d’identification dans les paramètres de configuration de Commerce [ pour l’intégration d’Assets ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| `accessToken` | Chaîne ! | Jeton d’accès généré pour l’intégration Assets. |
| `accessTokenSecret` | Chaîne ! | Secret du jeton d’accès généré pour l’intégration Assets. |
| `consumerKey` | Chaîne ! | Clé de consommateur générée pour l’intégration Assets. |
| `consumerSecret` | Chaîne ! | Secret client généré pour l’intégration Assets. |

#### ExternalMatcherInput

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| assetToProductUrl | Chaîne ! | <!--Add field description--> |
| productToAssetUrl | Chaîne ! | <!--Add field description--> |
| informations | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | Informations d’identification pour accéder au projet App Builder pour l’intégration d’AEM Assets pour Commerce. |

#### ExternalMatcherCredentials

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| `oauthServerUrl` | Chaîne ! |    |
| `clientId` | Chaîne ! |      |
| `clientSecret` | Chaîne ! |    |
| `imsOrgId` | Chaîne ! | L’organisation IMS dans laquelle AEM Assets et Adobe Commerce sont configurés. |

#### MatchBySkuRuleInput

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| metadataField | Chaîne ! | Spécifiez le champ de métadonnées des ressources à utiliser pour la correspondance. Utiliser `commerce:skus` |

#### RuleInput

Indique la règle correspondante à utiliser pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | Sélectionne la règle externalMatcher pour la correspondance des ressources et spécifie les données requises pour l’utiliser. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | Sélectionne la règle MatchBySkuRule pour la correspondance des ressources et spécifie les données requises pour l’utiliser. |

#### RuleTypeInput

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| RuleType | enum | Indique une liste de règles de correspondance des ressources disponibles pour l’intégration AEM Assets pour Commerce. Les valeurs disponibles sont `matchBySKU` ou `externalMatcher`. |

#### TenantInput

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| `aem` | [AemInput!](#aeminput) | Identifie l’instance AEM Assets dans l’AEM Cloud Service dans laquelle vous stockez les ressources Commerce. |
| `commerce` | [CommerceInput!](#commerceinput) | Fournit des informations de projet Commerce et des informations d’identification pour l’accès à l’API |
| `enabled` | Booléen ! | Activez ou désactivez la synchronisation des ressources entre Adobe Commerce et AEM Assets. |
| `projectId` | Chaîne ! | L’identifiant de projet SaaS de la configuration de l’identifiant SaaS du [Connecteur de services Commerce](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [RuleInput!](#ruleinput) | Indique la règle correspondante à utiliser pour synchroniser les ressources entre Adobe Commerce et AEM Assets. Spécifiez `[matchBySkuRule](#matchbyskuruleinput)` ou `[externalMatcher](#externalmatcherinput)`. |

### Champs de sortie

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| data | [registerTenant] | Renvoie les informations d’enregistrement du client et les messages d’erreur provenant du serveur. |

#### RegisterTenantResponse

| Champ | Type de données | Description |
| ----- | --------- | ----------- |
| tenantId | Chaîne ! | Renvoie l’identifiant du client qui a été enregistré. Cet identifiant permet de s’assurer que les données de l’intégration AEM Assets pour Commerce sont stockées et récupérées à partir de l’espace de données SaaS associé à l’environnement Commerce. |
| userErrors | [[userError!]!](#usererror) | Renvoie les messages d’erreur générés par la requête. |

#### UserError

| Erreur | Description |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Cette erreur se produit si l’ID d’environnement spécifié dans l’en-tête `Magento-Environment-Id` n’est pas affecté au compte IMS. Cette erreur peut se produire car le compte IMS n’était pas connecté lorsque [Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) a été configuré pour l’instance Commerce. |
| `Client ID is invalid` | L&#39;en-tête `x-api-key` est incorrect. |
| `Client ID is missing` | L’en-tête `x-api-key` n’a pas été fourni. |
| `JWT is required` | L’en-tête `x-gw-signature` n’a pas été fourni. |
| `JWT is invalid` | L’en-tête `x-gw-signature` n’a pas été fourni. |
| `Tenant already exists` | Un client avec le `mageID` donné (extrait du jeton JWT) et `saasId` (fourni par l’en-tête `Magento-Environment-Id`) a déjà été enregistré. |
| `Unexpected error when connecting with AEM Assets` | Cette erreur se produit en raison de valeurs `programId` ou `environmentId` non valides ou inexistantes. |
| `Unable to connect with AEM Assets` | Cette erreur peut être motivée par deux raisons :<br>1. Le compte de ressource AEM est associé à un ID d’organisation IMS différent de celui fourni pour Adobe Commerce.<br>2. Les métadonnées `commerce:isCommerce` n’existent pas dans AEM Assets, ce qui indique qu’il n’y a aucune ressource approuvée à envoyer d’AEM Assets vers l’instance Commerce. |
| `Unexpected error when connecting with Commerce` | Cette erreur se produit lorsqu’un commerce `baseURL` non valide est fourni. |
| `Unable to connect with Commerce, unauthorized` | Des informations d’identification de commerce non valides ont été fournies, ce qui a entraîné un accès non autorisé. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | Le champ `Rule` contient une valeur incorrecte. Pour la requête RegisterTenant, les types de règles disponibles sont définis par l’énumération [RuleTypeInput](#ruletypeinput). |

## Activation de l’intégration Experience Manager Assets

Une fois le client enregistré, la dernière étape du processus d’intégration consiste à activer l’extension Experience Manager Assets Integration for Commerce dans l’administration.

1. Activez l’extension .

   1. Accédez à **Magasins** > Paramètres > **Configuration** > **Catalogue**.

   1. Ouvrez la configuration du catalogue en sélectionnant **[!UICONTROL Catalog]**.

   1. Développez **[!UICONTROL AEM Assets integration]**.

   1. Définissez **[!UICONTROL Integration enabled]** sur `yes`.

      ![Intégration AEM Assets pour la configuration d’administration Commerce](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
