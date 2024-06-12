---
title: "[!DNL Audience Activation]"
description: Découvrez comment activer les audiences Real-Time CDP dans Adobe Commerce pour stimuler la personnalisation dans votre boutique.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: c9eb7f2b0b28f39ee9039be1e0fba4fe282ba7b3
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 0%

---

# [!DNL Audience Activation]

La variable [!DNL Audience Activation] l’extension vous permet d’activer les audiences Real-Time CDP dans Adobe Commerce pour créer des offres uniques dans le panier. Ces offres et incitations incluent des techniques courantes de marchandisage du commerce électronique, telles que _achat 2 obtenir 1 gratuit_, bannières à forte identification destinées à ce client et modification du prix des produits au moyen de diverses offres. Les audiences créées dans Real-Time CDP sont basées sur les données de divers systèmes d’entreprise, tels que le ERP (Enterprise Resource Planning), la gestion de la relation client (CRM), les points de vente et les systèmes marketing. Les informations sur les segments de clients étant constamment actualisées, les clients peuvent être associés et dissociés d’un segment lorsqu’ils font leurs achats dans votre boutique.

Vous pouvez activer les audiences dans un storefront Luma ou [headless](#headless-support) storefront. Dans un storefront Luma, les informations d’audience (appartenance à un segment) sont stockées dans un cookie côté Commerce. Dans un storefront sans interface utilisateur graphique, les informations d’audience sont transmises dans l’en-tête de l’API GraphQL sous la forme d’un paramètre nommé : `aep-segments-membership`.

## Notes de mise à jour

Cette section contient des informations sur les mises à jour apportées à l’extension d’Audience Activation et comprend :

![Nouveau](../assets/new.svg) - Nouvelles fonctionnalités
![Correction](../assets/fix.svg) - Correctifs et améliorations
![Bogue](../assets/bug.svg) - Problèmes connus

Voir [Versions à venir](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) pour en savoir plus sur les calendriers de publication et l’assistance.

Consultez la documentation destinée aux développeurs pour [découvrez la compatibilité des produits](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Mises à jour du service prises en charge

Ces notes de mise à jour décrivent les modifications et correctifs de fonctionnalités liés aux extensions utilisées par Audience Activation.

Mises à jour du service +++prises en charge

_15 août 2023_

![Correction](../assets/fix.svg) - Mise à jour de la [Tableau de bord Audiences Real-Time CDP](#real-time-cdp-audiences-dashboard) pour simplifier le filtrage.

_27 juin 2023_

![Correction](../assets/fix.svg) - Ajout de la prise en charge de PHP 8.2 dans le `magento/module-data-services-graphql` module.

_30 mai 2023_

![Nouveau](../assets/new.svg) - Mise à jour de la [Tableau de bord Audiences Real-Time CDP](#real-time-cdp-audiences-dashboard) pour inclure la possibilité de trier, rechercher et filtrer les audiences actives dans votre instance Adobe Commerce.

+++

### 2.2.0

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_12 juin 2024_

![Nouveau](../assets/new.svg) - Version GA pour [règles de produit connexes](../merchandising-promotions/product-related-rule-create.md) par les audiences.

### 2.1.1

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_4 avril 2024_

![Nouveau](../assets/new.svg) - Prise en charge de PHP 8.3.

### 2.2.0-beta1

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_16 février 2024_

![Nouveau](../assets/new.svg) - Si vous participez à la version bêta, assurez-vous que votre `composer.json` se présente comme suit au niveau racine : ` "minimum-stability": "beta"`.
![Nouveau](../assets/new.svg) - (**Beta**) Possibilité de créer des [règles de produit connexes](../merchandising-promotions/product-related-rule-create.md) par les audiences.

### 2.1.0

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_24 janvier 2024_

![Nouveau](../assets/new.svg) - Mise à jour de la [Tableau de bord Audiences Real-Time CDP](#real-time-cdp-audiences-dashboard) pour inclure les sites web qui contiennent les audiences et spécifier les blocs dynamiques et les règles de prix du panier configurés pour utiliser ces audiences.

### 2.0.1

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_16 novembre 2023_

![Correction](../assets/fix.svg) - Amélioration de la stabilité.

### 2.0.0

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_10 octobre 2023_

![Nouveau](../assets/new.svg) - Ajout de la prise en charge d’OAuth 2.0 lorsque vous [configure](#configure-the-extension) l’extension d’Audience Activation.
![Correction](../assets/fix.svg) - Amélioration de la stabilité.

### 1.2.0

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

_15 août 2023_

![Correction](../assets/fix.svg) - Mise à jour de la version des composants de l’interface utilisateur.

### 1.1.0

_30 mai 2023_

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

![Nouveau](../assets/new.svg) - Ajout de la prise en charge de [blocs dynamiques](#headless-support) dans une vitrine sans tête.

### 1.0.1

_11 mai 2023_

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

![Correction](../assets/fix.svg) - Correction d’un problème en raison duquel une règle de prix de bloc ou de panier dynamique n’était pas appliquée au storefront.
![Correction](../assets/fix.svg) - Correction d’un problème en raison duquel une installation non configurée de l’extension d’Audience Activation provoquait une erreur lorsqu’un commerçant tentait de créer ou de mettre à jour un bloc dynamique.

### 1.0.0

_31 mars 2023_

[!BADGE Compatibilité]{type=Informative tooltip="Compatibilité"}

![Nouveau](../assets/new.svg) - Version de disponibilité générale

## Implémentation

Les tâches suivantes s’appliquent aux mises en oeuvre de storefront sans interface et Luma. Pour activer les audiences dans Adobe Commerce, vous devez :

- Installation d’Adobe Commerce version 2.4.4 ou ultérieure
- [Activer](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce comme destination dans Real-Time CDP
- [Installer](#install-the-extension) la valeur [!DNL Audience Activation] dans Admin
- [Configurer](#configure-the-extension) la valeur [!DNL Audience Activation] dans Admin

### Installation de l’extension

Installez le [!DNL Audience Activation] de l’extension [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)ou exécutez la commande suivante :

```bash
composer require magento/audiences
```

### Configuration de l’extension

Après avoir installé la variable [!DNL Audience Activation] , vous devez vous connecter à votre administrateur Commerce et effectuer les opérations suivantes :

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Se connecter](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) à votre compte d’Adobe et sélectionnez l’ID d’organisation.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. Dans le **[!UICONTROL Datastream ID]** , collez l’identifiant de la banque de données que vous avez créée lorsque vous [activé](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce comme destination dans Real-Time CDP.

   Ce flux de données envoie des données de votre site web Commerce à Real-Time CDP pour déterminer si un acheteur appartient à une audience. Si vous n’avez pas encore créé de flux de données, [create](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) un en Experience Platform, [add](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) à la destination Commerce dans Real-Time CDP et au [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) dans Admin.

   >[!NOTE]
   >
   >Lorsque vous spécifiez un identifiant de flux de données, vous [l’associer à un site web spécifique](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) dans le [!DNL Data Connection] extension . Si votre boutique Commerce comporte plusieurs sites Web, [création d’une destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) pour chaque site web dans Real-Time CDP et utilisez un identifiant de flux de données différent pour chaque site.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Développer **[!UICONTROL Services]** et sélectionnez **[!UICONTROL [!DNL Data Connection]]**.

1. [Ajouter](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) informations de compte de service et d’identification.

## Où utiliser les audiences Real-Time CDP dans Commerce

Avec la variable [!DNL Audience Activation] extension activée, vous pouvez :

- [Créer une règle de prix de panier](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) tenus par les audiences
- [Créer un bloc dynamique](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) tenus par les audiences
- [Création d’une règle de produit associée](../merchandising-promotions/product-related-rule-create.md) tenus par les audiences

>[!TIP]
>
>Pour un cas d’utilisation complet de bout en bout sur l’exportation [!DNL Commerce] données à Real-Time CDP, création d’une audience, puis activation de cette audience vers [!DNL Commerce], voir [Création d’une audience dans Real-Time CDP à l’aide de [!DNL Commerce] données d’événement](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Tableau de bord des audiences Real-Time CDP

Vous pouvez afficher toutes les [active](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) audiences disponibles pour la personnalisation dans votre instance Adobe Commerce à l’aide de la variable **Audiences Real-Time CDP** tableau de bord.

Pour accéder au **Audiences Real-Time CDP** tableau de bord, accédez à la _Administration_ barre latérale, puis accédez à **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Tableau de bord des audiences Real-Time CDP](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Le tableau de bord contient les champs suivants :

| Colonne | Description |
|--- |--- |
| `Hide filters` | Permet d’afficher ou de masquer les filtres que vous pouvez appliquer au tableau de bord. Actuellement, le seul filtre que vous pouvez appliquer est `Last updated`. Ce filtre permet de sélectionner une période pour les audiences en fonction de la date de leur dernière mise à jour. |
| `Search` | Permet de rechercher des audiences actives dans votre instance Commerce. |
| `Name` | Nom donné à l’audience dans Real-Time CDP. |
| `Origin` | Indique d’où provient l’audience, par exemple : `Experience Platform`. |
| `Websites` | Indique les sites web configurés pour utiliser les audiences. |
| `Dynamic Blocks` | Indique les blocs dynamiques configurés pour utiliser les audiences. |
| `Cart Price Rules` | Indique les règles de prix du panier configurées pour utiliser les audiences. |
| `Related Product Rules` | Indique les règles de produit connexes configurées pour utiliser les audiences. |
| `Last updated` | Indique le moment où l’audience a été modifiée dans Real-Time CDP. |
| `Sync now` | Récupère les audiences nouvelles ou mises à jour de Real-Time CDP. |
| `Customize table` | Permet d’afficher ou de masquer le `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`, et `Last updated` colonnes. |

{style="table-layout:auto"}

## Prise en charge sans tête

Vous pouvez activer les audiences dans une instance Adobe Commerce sans interface utilisateur graphique, telle qu’AEM et PWA, pour afficher les règles de prix du panier, les règles de produit associées ou les blocs dynamiques en fonction des audiences.

### Règles de prix du panier et règles connexes sur les produits

Pour les règles de prix du panier et les règles de produit associées, un storefront sans interface communique avec l’Experience Platform via la variable [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). La structure fournit une API côté serveur implémentée à l’aide de GraphQL. Les informations d’audience, telles qu’un segment d’acheteur, sont transmises à Commerce par le biais d’un paramètre d’en-tête GraphQL nommé : `aep-segments-membership`.

L&#39;architecture globale est la suivante :

![Envoi de données d’un storefront sans affichage au serveur principal](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Après vous [install](#install-the-extension) et [configure](#configure-the-extension) Avec l’extension , le SDK Web Experience Platform contient les informations d’audience sous la forme d’adhésion au segment.

Pour capturer ces appartenances à des segments à partir du SDK, reportez-vous à cette section [extrait de code](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Une fois récupérés, vous pouvez transmettre ces segments à Commerce dans l’en-tête de GraphQL. Par exemple :

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Blocs dynamiques

Pour les blocs dynamiques, GraphQL `dynamicBlocks` Les requêtes peuvent contenir les `audience_id` attribut d’entrée. Si vous spécifiez une ou plusieurs `audience_id` dans une `dynamicBlocks` , elle renvoie une liste de blocs dynamiques affectés à ces audiences.

#### Exemple d’utilisation

La requête suivante renvoie tous les blocs dynamiques associés à plusieurs identifiants d’audience.

**Requête :**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Réponse :**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

En savoir plus sur les `dynamicBlocks` Requête GraphQL dans le [documentation destinée aux développeurs](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Récupération des audiences à l’aide du SDK Adobe Experience Platform Mobile

Vous pouvez récupérer les audiences Real-Time CDP à l’aide du SDK Adobe Experience Platform Mobile.

1. [Installer](#install-the-extension) l’extension d’Audience Activation.
1. [installation et configuration du SDK pour votre site Commerce mobile](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Le SDK Mobile Adobe Experience Platform pour iOS prend en charge iOS 11 ou version ultérieure.

Une fois la configuration terminée, utilisez les opérations du SDK mobile pour récupérer les données d’audience. Par exemple :

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Une fois les données récupérées, vous pouvez les utiliser pour créer des données en fonction de l’audience. [règles de prix du panier](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [blocs dynamiques](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) et  [règles de produit connexes](../merchandising-promotions/product-related-rule-create.md) dans l’application Commerce.

## Les audiences ne s’affichent pas dans Commerce

Si les audiences Real-Time CDP ne s’affichent pas dans Commerce, cela peut être dû à :

- Type d’authentification incorrect sélectionné dans la variable **Connexion aux données** page de configuration
- Privilèges insuffisants sur le jeton généré

Les deux sections suivantes expliquent comment résoudre l’un ou l’autre de ces cas.

### Type d’authentification incorrect sélectionné dans la configuration

1. Ouvrez votre instance Commerce.
1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Développer **[!UICONTROL Services]** et sélectionnez **[!UICONTROL [!DNL Data Connection]]**.
1. Assurez-vous que la méthode d’autorisation serveur à serveur spécifiée dans la variable **[!UICONTROL Authentication Type]** est correct. Adobe recommande d’utiliser **OAuth**. JWT a été abandonné. [En savoir plus](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Privilèges insuffisants sur le jeton généré

Ce problème peut être dû à des privilèges d’API insuffisants pour le jeton généré. Pour vous assurer que le jeton dispose des privilèges appropriés :

1. Identifiez l’administrateur système de Adobe Experience Platform de votre entreprise.
1. Recherchez le projet et les informations d’identification que vous utiliserez.
1. Identifiez l’adresse électronique du compte technique, par exemple : `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Demandez à l’administrateur système de lancer Adobe Experience Platform et d’accéder à **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. À l’aide de l’e-mail du compte technique ci-dessus, recherchez les informations d’identification à modifier.
1. Ouvrez les informations d’identification, puis sélectionnez **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Ajouter le rôle contenant **[!UICONTROL Manage destinations]** autorisation.
1. Cliquez sur **[!UICONTROL Save]**.
1. [Régénérer](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) le jeton d’accès dans la console.
1. Vérifiez que le jeton fournit une réponse valide à l’aide de la variable [API de connexions à Target](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
