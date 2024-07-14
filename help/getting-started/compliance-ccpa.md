---
title: Conformité au CCPA
description: Découvrez le California Consumer Privacy Act (CCPA), qui étend les droits des consommateurs en Californie pour déterminer comment leurs informations personnelles sont collectées, stockées et utilisées.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2256'
ht-degree: 0%

---

# Conformité au CCPA

>[!NOTE]
>
>Ces informations font partie d’une série de rubriques destinées à aider les marchands et les développeurs Adobe Commerce à comprendre les implications du California Consumer Privacy Act. L&#39;information est basée sur le texte de la loi. Pour confirmer si le CCPA s’applique à votre entreprise, contactez votre avocat.

Le [California Consumer Privacy Act][5] (CCPA) étend les droits des consommateurs en Californie pour déterminer comment leurs informations personnelles sont collectées, stockées et utilisées. Elle met l’accent sur la protection des consommateurs contre la vente ou l’exchange non autorisé ou leurs informations personnelles. La CCPA a été adoptée en 2018 et est entrée en vigueur le 1er janvier 2020.

Le CCPA accorde aux consommateurs les nouveaux droits suivants :

- **Droit de connaître** les catégories d&#39;informations personnelles les concernant qui sont collectées, utilisées, partagées ou vendues au cours des 12 derniers mois.
- **Droit de suppression** de certains types d&#39;informations personnelles détenues par une entreprise et/ou ses fournisseurs de services.
- **Droit d&#39;opposition** à la vente de leurs informations personnelles.
- **Droit à la non-discrimination** en termes de prix ou de service pour avoir exercé un droit à la vie privée en vertu de la CCPA.

Aux fins de la CCPA, les informations personnelles dans ce contexte sont définies comme suit :

>Les informations qui identifient, se rapportent à, décrivent, peuvent être associées ou pourraient raisonnablement être liées, directement ou indirectement, à un consommateur ou à un ménage particulier. (Section 1798.140)

À cet égard, il couvre certains éléments de données qui ne peuvent pas être considérés comme des données personnelles dans le cadre d’autres lois ou réglementations. Les commerçants doivent garder cela à l&#39;esprit lorsqu&#39;ils déterminent s&#39;ils doivent se conformer à la loi et comment.

Le CCPA exige également que les entreprises assurent une _sécurité raisonnable_ et inclut des dispositions de protection des données étendues pour les consommateurs, y compris le droit de poursuivre une action en justice en cas de violation des données.

Consultez votre service juridique pour déterminer si et comment vous devriez vous conformer aux exigences du CCPA qui peuvent s’appliquer à vous et à votre entreprise. Cela inclut les nouvelles exigences en matière de notification, d’opt-out et d’enregistrement que les entreprises doivent mettre en oeuvre conformément à la loi.

## Exigences commerciales

Le CCPA s’applique aux entreprises à but lucratif qui font des affaires en Californie et qui répondent à l’une des exigences suivantes :

- ont un revenu annuel brut de plus de 25 millions de dollars ;
- Achetez, recevez ou vendez les informations personnelles de 100 000 résidents, ménages ou appareils californiens ou plus.
- Dérivez 50 % ou plus de leurs revenus annuels à la vente des informations personnelles des résidents de Californie.

## Guide de conformité CCPA

Cette section décrit de manière approfondie les étapes nécessaires pour que les marchands se conforment aux réglementations de confidentialité, telles que la California Consumer Privacy Act (CCPA).

### RGPD et CCPA

Si votre entreprise est tenue de se conformer au [ Règlement général sur la protection des données ](compliance-gdpr.md) (RGPD) et à la CCPA, vous pouvez utiliser une partie du travail effectué dans le cadre de votre programme de conformité au RGPD pour le CCPA. Bien que la réglementation présente certaines similitudes, quelques différences incluent :

- La définition des informations personnelles diffère pour chaque réglementation.
- Le RGPD exige que les consommateurs s’inscrivent avant que leurs données personnelles ne puissent être utilisées à certaines fins ; le CCPA accorde aux consommateurs le droit de s’exclure.
- Le CCPA a des exigences supplémentaires en matière d’inventaire et de mappage des données.
- Les règlements ont des exigences de politique de confidentialité différentes.

Les entreprises qui se conforment au RGPD pourraient avoir des obligations supplémentaires en vertu de la CCPA. Pour en savoir plus, consultez la [fiche d’information CCPA][3]{:target=&quot;_blank&quot;}.

### Feuille de route de la conformité

Un effort coordonné est nécessaire pour élaborer et mettre en oeuvre un plan de conformité. Utilisez cette feuille de route comme guide de mobilisation des ressources et de hiérarchisation des tâches afin de pouvoir avancer sur plusieurs fronts. Le processus est essentiellement le même pour toutes les installations [!DNL Commerce], à l’exception suivante :

- **Adobe Commerce sur l’infrastructure cloud** : les commerçants avec des magasins hébergés sur l’Adobe [infrastructure cloud][4]{:target=&quot;_blank&quot;} peuvent demander de l’aide à leur gestionnaire de compte technique Adobe Commerce ou à l’assistance clientèle pour répondre aux demandes des clients.

- **On-Premise** : les commerçants disposant d’installations on-premise d’Adobe Commerce ou d’un Magento Open Source doivent développer leurs propres processus et outils pour répondre et gérer les demandes des clients en rapport avec les réglementations de confidentialité.

#### Étape 1 : assemblez une équipe interfonctionnelle pour répondre à la conformité aux réglementations

Regroupez une équipe qui représente les rôles fonctionnels suivants dans votre entreprise et planifiez une session de formation afin de les mettre à jour rapidement la législation. Ensuite, attribuez les tâches requises aux parties prenantes par rôle.

- Stratégie commerciale et opérations
- Mentions légales
- Technologie de l&#39;information
- Expérience utilisateur
- Service client
- Assistance administrative

Du point de vue commercial, vous devez déterminer si votre entreprise étend ces mesures de protection de la vie privée uniquement aux consommateurs de Californie, ou les met à la disposition de tous les consommateurs, quel que soit leur lieu d’implantation.

#### Étape 2 : inventaire de vos propriétés numériques

**Parties prenantes :** Technologie de l’information, assistance juridique, assistance administrative

Faites l’inventaire de vos propriétés numériques, y compris toutes les intégrations et les personnes ayant accès aux données de vos clients.

1. Déterminez quelles informations personnelles publiques et privées sont collectées sur vos sites web et applications mobiles. Par exemple, une base de données Commerce standard stocke les types d’informations personnelles publiques et privées suivants :

   - **Public** : Listes de souhaits, révisions de produits

   - **Privé** : Informations sur le client, informations sur la commande, points de récompense, registre des cadeaux, carnet d’adresses, crédit de magasin, méthodes de paiement, accords de facturation, abonnements à la newsletter, invitations.

     Si votre installation [!DNL Commerce] a été personnalisée, des informations personnelles supplémentaires peuvent être collectées. Les informations personnelles peuvent également résider dans les [cookies](./compliance-cookie-law.md), balises et autres technologies qui collectent des informations.

1. Identifiez les parties avec lesquelles vous partagez des données. La liste doit inclure les fournisseurs de services et les tiers. Les tiers incluent les réseaux publicitaires, les fournisseurs d’accès à Internet, les fournisseurs d’analyse de données, les entités gouvernementales, les systèmes d’exploitation et les plateformes, les réseaux sociaux et les revendeurs de données des consommateurs qui ne collectent pas directement des informations personnelles de vos clients.

   - **Fournisseurs de services** : entités qui ont accès à vos données clients à des fins commerciales et qui fournissent des services en votre nom. Par exemple, Adobe est un fournisseur de services, tout comme certains développeurs de personnalisations, d’extensions et de services.

     Vérifiez les paramètres par défaut de Google Universal Analytics, de Google Tag Manager et de tous les autres services de données que vous utilisez, et apportez les modifications nécessaires pour vous conformer à la réglementation. Pour en savoir plus, voir [Paramètres de confidentialité de Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Autres tiers** : entités avec lesquelles vous partagez ou vendez des données de consommateur. Par exemple, vous pouvez partager des données sur les consommateurs avec un réseau publicitaire dans exchange pour la publicité.

#### Étape 3 : mappez le parcours client et le processus de collecte de données dans vos magasins

**Parties prenantes :** expérience utilisateur, technologie de l’information, assistance administrative

1. Identifiez chaque point du [parcours client] où les informations personnelles sont collectées et le type d’informations collectées à chaque étape.

   Les visiteurs de votre site doivent être avertis au préalable ou au moment de la collecte des données. Par exemple, un magasin sans intégration personnalisée collecte des informations personnelles lors de la création d’un compte client et lors de l’extraction. Si votre magasin comporte des intégrations personnalisées, il peut y avoir des éléments de données et des attributs supplémentaires à identifier.

1. Reportez-vous aux rubriques suivantes pour connaître les diagrammes de flux de données applicables et les mappages d’entités de base de données pour chaque version :

   - [Référence des informations personnelles (2.x)][1]
   - [Référence des informations personnelles (1.x)][2]

   ![diagramme](./assets/privacy-frontend-diagram.svg)

#### Étape 4 : établir des procédures et des mécanismes pour répondre aux demandes des clients

**Parties prenantes :** Service client, technologie de l’information, expérience utilisateur, assistance administrative

Du point de vue de la gestion des données, chaque demande d’informations personnelles implique les parties suivantes :

- **Sujets de données** (Consommateurs) : dans le cadre de la CCPA, toute personne en Californie qui fournit des informations personnelles pour effectuer un achat et/ou pour gérer un compte client peut envoyer une demande d’accès ou de suppression de ses données personnelles.

- **Entités agissant comme entreprises dans le cadre de la CCPA** (Marques) : [!DNL Commerce] les marchands collectent et stockent des informations personnelles sur leurs clients et invités qui effectuent des achats dans leurs magasins.

- **Responsable du traitement des données** (Fournisseurs de technologie) : Adobe Commerce et Magento Open Source agissent comme responsables du traitement des données personnelles stockées dans le cadre des services fournis aux commerçants. En tant qu’entité de traitement, Adobe traite les données personnelles conformément aux autorisations et aux instructions du marchand, conformément au contrat de licence.

Les commerçants sont responsables de ce qui suit :

1. Identifiez les parties impliquées dans la demande d’accès aux titulaires de données (DSAR) et vérifiez l’identité de toute personne qui demande à connaître, exclure ou supprimer. Cela s’applique à une personne qui dispose d’un compte client protégé par mot de passe ou qui fait ses achats dans votre boutique en tant qu’invité.

1. Communiquer et diffuser des informations à un consommateur en réponse à sa demande de droits dans les 45 jours suivant la réception d’une demande vérifiable du consommateur, sauf si cela n’est pas possible. (La loi comporte d&#39;autres exigences pour qu&#39;une entreprise puisse se conformer aux dispositions de la loi en cas de délais pouvant aller jusqu&#39;à 45 jours supplémentaires).

   Les marchands doivent répondre à chaque demande dans les 45 jours, à partir du jour de réception de la demande. Au besoin, les commerçants peuvent mettre jusqu’à 45 jours de plus pour répondre, pour un total maximal de 90 jours à compter du jour de réception de la demande. Pour ce faire, le marchand doit informer le client de la raison du retard.

1. Développez un mécanisme pour présenter les notifications requises dans votre magasin et collecter les réponses des consommateurs.

1. Créez des procédures de réponse et documentez chacune des demandes suivantes :

   - **Requêtes à connaître** - Les visiteurs de votre boutique doivent être informés de tout arrangement que vous devez prendre pour vendre ou partager leurs informations personnelles avec des tiers et être autorisés à se désabonner. Les détails de votre utilisation des informations personnelles et des parties avec lesquelles vous partagez ou vendez des données peuvent être conservés dans votre politique de confidentialité.

   - **Demandes d’opposition** - Si des données personnelles sont vendues ou transférées à des tiers dans l’exchange à des fins utiles, le CCPA requiert un lien _Ne pas vendre mes informations_ à chaque point où elles sont collectées. D’autres contrôles d’entrée activés par l’utilisateur, tels que des cases à cocher et des boutons, peuvent être utilisés dans les communications par e-mail, les paramètres de préférence de site web ou dans les formulaires de site web au moment de la collecte des données pour que les individus puissent envoyer une demande d’exclusion valide.

   - **Demandes de suppression**

      - Les commerçants dont les magasins sont hébergés sur Adobe Commerce Cloud doivent contacter l’assistance Adobe pour obtenir de l’aide sur la suppression des informations personnelles. Pour plus d’informations, contactez votre gestionnaire de compte technique d’Adobe ou le service clientèle.
      - Les commerçants qui exécutent des installations d’Adobe Commerce ou de Magento Open Source on-premise doivent mettre en oeuvre leur propre processus et script pour supprimer des informations personnelles sur demande.

#### Étape 5 : Ecrire le contenu des notifications client requises

**Parties prenantes :** juridique, service client, expérience utilisateur, technologie de l’information, assistance administrative

1. En partenariat avec votre service juridique, déterminez les types d’avis qui doivent être ajoutés à votre site web pour respecter les obligations du CCPA.

   - **Avis de collecte** : avis donné au moment ou avant la collecte des informations personnelles auprès du consommateur. L&#39;avis doit être rédigé en langage clair et être facile à comprendre pour la personne moyenne. L’avis doit être visible et fourni dans une ou plusieurs langues que le contenu de votre site web.

   - **Avis de droit d’opposition** : avis informant les consommateurs de leur droit d’opposition à la vente de leurs informations personnelles.

   - **Avis d’incitation financière** : avis expliquant chaque différence financière d’incitation, de prix ou de service que votre entreprise reçoit en exchange pour des informations personnelles.

   - **Comment envoyer une demande de collecte et d’utilisation des informations personnelles** : instructions pour les individus de soumettre une demande de divulgation des informations personnelles que vous avez collectées sur la personne, notamment :

      - Informations personnelles spécifiques que vous avez collectées sur le consommateur
      - Catégories d’informations personnelles que vous avez collectées sur le consommateur
      - Catégories de sources à partir desquelles les informations personnelles sont collectées
      - Catégories d’informations personnelles sur le consommateur que vous avez vendu ou divulgué à des fins commerciales
      - Catégories de tiers auxquels les informations personnelles ont été vendues ou divulguées à des fins commerciales
      - Raisons pour lesquelles votre entreprise collecte et/ou vend des informations personnelles

1. Envoyez le contenu à l’équipe et, si possible, votre service juridique pour examen.

1. Déterminez où apparaissent les avis, leur mode de fonctionnement (pour chaque visite, lors de l’authentification ou lors d’un clic publicitaire), ainsi que leur position et leur format par rapport à d’autres contenus.

1. Transmettez le contenu approuvé à votre équipe de développement.

#### Étape 6 : consultez vos contrats avec les prestataires

**Parties prenantes :** Assistance juridique, assistance administrative

Examinez et, au besoin, mettez à jour tous les contrats de fournisseur de services afin de tenir compte des exigences de la CCPA.

#### Étape 7 : mise à jour de votre politique de confidentialité

**Parties prenantes :** Assistance juridique, assistance administrative

Examinez votre politique actuelle en matière de confidentialité et réfléchissez à ce qui, le cas échéant, est nécessaire pour d’autres divulgations.

- **Utilisation des informations personnelles** : vous devez divulguer les informations personnelles collectées, ainsi que les incitations financières que vous recevez en exchange de la vente des informations personnelles. Vous devez également expliquer comment l’incitation est autorisée en vertu de la CCPA et comment la valeur des informations personnelles est calculée.

- **Âge du consentement** : si vous collectez ou utilisez des informations personnelles sur les mineurs, vous pouvez être soumis aux exigences suivantes :

   - **Mineurs &lt; 13** : une autorisation parentale est requise pour que les mineurs de moins de 13 ans souscrivent à la vente de leurs informations personnelles.

   - **Minors 13 to &lt; 16** : les mineurs de moins de 13 ans et de moins de 16 ans peuvent souscrire à la vente de leurs informations personnelles, à condition que l&#39;entreprise établisse un processus raisonnable pour documenter l&#39;action. Le processus doit être décrit dans la [politique de confidentialité](privacy-policy.md) de la société. Lorsqu&#39;une entreprise reçoit des demandes de la part de mineurs de cette tranche d&#39;âge, elle doit les informer de leur droit de se désinscrire plus tard et expliquer comment le faire.

  >[!IMPORTANT]
  >
  >Il est interdit aux commerçants de stocker les données personnelles des enfants sur la plateforme ou les systèmes [!DNL Commerce]. S’il y a des raisons de croire que les données collectées appartiennent à un mineur, elles doivent être supprimées immédiatement d’une plateforme [!DNL Commerce] afin d’éviter toute violation des conditions de licence d’Adobe.

#### Etape 8 : documenter toutes les procédures associées et conserver les enregistrements

**Parties prenantes :** Service client, assistance administrative

Pendant les 24 mois qui suivent la réception de chaque demande de droits, conservez un enregistrement de la demande et de la réponse de votre société.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
