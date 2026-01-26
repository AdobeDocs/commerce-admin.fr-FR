---
title: Conformité au CCPA
description: Découvrez le California Consumer Privacy Act (CCPA), qui étend les droits des consommateurs californiens quant à la manière dont leurs informations personnelles sont collectées, stockées et utilisées.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2252'
ht-degree: 0%

---

# Conformité au CCPA

>[!NOTE]
>
>Ces informations font partie d’une série de rubriques destinées à aider les commerçants et les développeurs Adobe Commerce à comprendre les implications de la Loi sur la protection de la vie privée des consommateurs de Californie. L&#39;information est basée sur le texte de la loi. Pour confirmer si le CCPA s&#39;applique à votre entreprise, consultez votre avocat.

Le [&#x200B; California Consumer Privacy Act &#x200B;](https://oag.ca.gov/privacy/ccpa) (CCPA) élargit les droits des consommateurs californiens quant à la manière dont leurs informations personnelles sont collectées, stockées et utilisées. Elle met l&#39;accent sur la protection des consommateurs contre la vente ou l&#39;échange non autorisé de leurs renseignements personnels. Le CCPA a été adopté en 2018 et est entré en vigueur le 1er janvier 2020.

Le CCPA accorde aux consommateurs les nouveaux droits suivants :

- **Droit de savoir** les catégories d&#39;informations personnelles les concernant qui sont collectées, utilisées, partagées ou vendues au cours des 12 derniers mois.
- **Droit de suppression** certains types d&#39;informations personnelles détenues par une entreprise et/ou ses fournisseurs de services.
- **Droit d’opposition** à la vente de leurs informations personnelles.
- **Droit à la non-discrimination** en termes de prix ou de service pour avoir exercé un droit à la vie privée en vertu du CCPA.

Aux fins du CCPA, les renseignements personnels dans ce contexte sont définis comme :

>Information qui identifie, se rapporte à, décrit, est susceptible d&#39;être associée à, ou pourrait raisonnablement être liée, directement ou indirectement, à un consommateur ou à un ménage particulier. (Article 1798.140)

À cet égard, elle couvre certains éléments de données qui ne peuvent pas être considérés comme des données personnelles dans le contexte d’autres lois ou règlements. Les commerçants devraient en tenir compte lorsqu&#39;ils déterminent s&#39;ils doivent se conformer à la loi et de quelle manière.

Le CCPA exige également des entreprises qu&#39;elles fournissent une _sécurité raisonnable_ et inclut des dispositions élargies en matière de protection des données pour les consommateurs, y compris le droit de poursuivre une action en justice en cas d&#39;atteinte à la protection des données.

Consultez votre service juridique pour déterminer si et comment vous devez vous conformer aux exigences de la CCPA qui peuvent s&#39;appliquer à vous et à votre entreprise. Cela comprend les nouvelles exigences en matière d&#39;avis, de droit d&#39;opposition et de tenue de documents que les entreprises doivent mettre en œuvre conformément à la loi.

## Exigences de l’entreprise

Le CCPA s&#39;applique aux entreprises à but lucratif qui font des affaires en Californie et qui remplissent l&#39;une des conditions suivantes :

- ont un revenu annuel brut de plus de 25 millions de dollars;
- Acheter, recevoir ou vendre les informations personnelles de 100 000 personnes ou plus résidant en Californie, ménages ou appareils
- 50 % ou plus de leurs revenus annuels proviennent de la vente des informations personnelles des Californiens.

## Guide de conformité au CCPA

Cette section fournit un aperçu général des étapes requises pour que les commerçants se conforment aux réglementations de confidentialité telles que le California Consumer Privacy Act (CCPA).

### RGPD et CCPA

Si votre entreprise est tenue de se conformer à la fois au [Règlement général sur la protection des données](compliance-gdpr.md) (RGPD) et au CCPA, vous pouvez utiliser une partie du travail de votre programme de conformité au RGPD pour le CCPA. Bien que le règlement présente certaines similitudes, quelques différences incluent :

- La définition des renseignements personnels diffère selon les règlements.
- Le RGPD exige des consommateurs qu’ils s’inscrivent avant que leurs données personnelles ne puissent être utilisées à certaines fins ; le CCPA leur donne le droit de se désinscrire.
- Le CCPA a des exigences supplémentaires en matière d’inventaire et de mappage des données.
- Les règlements ont des exigences différentes en matière de politique de confidentialité.

Les entreprises qui se conforment au RGPD peuvent avoir des obligations supplémentaires en vertu du CCPA. Pour en savoir plus, consultez la fiche d&#39;information [CCPA](https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf){:target="_blank"}.

### Feuille de route de conformité

Un effort coordonné est nécessaire pour élaborer et mettre en œuvre un plan de conformité. Utilisez cette feuille de route comme guide pour mobiliser les ressources et hiérarchiser les tâches afin d’avancer sur plusieurs fronts. Le processus est essentiellement le même pour toutes les installations [!DNL Commerce], à l’exception de :

- **Adobe Commerce sur les infrastructures cloud** : les commerçants dont les magasins sont hébergés sur Adobe [infrastructure cloud](https://www.adobe.com/commerce/magento.html){:target="_blank"} peuvent demander de l’aide à leur gestionnaire de compte technique Adobe Commerce ou au service clientèle pour répondre aux demandes des consommateurs.

- **On-Premise** : les commerçants disposant d’installations on-premise d’Adobe Commerce ou de Magento Open Source doivent développer leurs propres processus et outils pour répondre aux demandes des consommateurs liées aux réglementations de confidentialité et les gérer.

#### Étape 1 : constituer une équipe transversale pour veiller au respect de la réglementation

Réunissez une équipe qui représente les rôles fonctionnels suivants dans votre entreprise et planifiez une session de formation pour les mettre au courant de la législation. Ensuite, affectez les tâches requises aux parties prenantes par rôle.

- Stratégie et opérations de l’entreprise
- Mentions légales
- Technologie De L&#39;Information
- Expérience utilisateur
- Service à la clientèle
- Support Administratif

Du point de vue commercial, vous devez déterminer si votre entreprise étend ces mesures de protection de la vie privée aux consommateurs californiens uniquement ou si elle les met à la disposition de tous les consommateurs, où qu’ils se trouvent.

#### Étape 2 : faire l&#39;inventaire de vos propriétés numériques

**Parties prenantes :** de la technologie de l&#39;information, soutien juridique et administratif

Faites l’inventaire de vos propriétés numériques, y compris toutes les intégrations et qui a accès à vos données client.

1. Déterminez quelles informations personnelles publiques et privées sont collectées sur vos sites web et applications mobiles. Par exemple, une base de données Commerce standard stocke les types d’informations personnelles publiques et privées suivants :

   - **Public** : Listes de souhaits, avis produits

   - **Privé** : Informations Sur Le Client, Informations Sur La Commande, Points De Récompense, Registre Des Cadeaux, Carnet D’Adresses, Crédit En Boutique, Modes De Paiement, Accords De Facturation, Abonnements À Des Newsletters, Invitations.

     Si votre installation [!DNL Commerce] a été personnalisée, des informations personnelles supplémentaires peuvent être collectées. Les informations personnelles peuvent également se trouver dans des [cookies](./compliance-cookie-law.md), balises et autres technologies qui collectent des informations.

1. Identifiez les parties avec lesquelles vous partagez des données. La liste devrait inclure les fournisseurs de services et les tiers. Les tiers comprennent les réseaux publicitaires, les fournisseurs de services Internet, les fournisseurs d’analyse de données, les entités gouvernementales, les systèmes d’exploitation et les plateformes, les réseaux sociaux et les revendeurs de données client qui ne collectent pas directement les informations personnelles de vos clients.

   - **Fournisseurs de services** : entités qui ont accès à vos données client à des fins commerciales et fournissent des services en votre nom. Par exemple, Adobe est un fournisseur de services, tout comme certains développeurs de personnalisations, d’extensions et de services.

     Vérifiez les paramètres par défaut de Google Universal Analytics, de Google Tag Manager (et de tout autre service de données que vous utilisez) et apportez les modifications nécessaires pour vous conformer à la réglementation. Pour en savoir plus, consultez [Paramètres de confidentialité de Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Autres tiers** : entités avec lesquelles vous partagez ou vendez des données des consommateurs. Par exemple, vous pouvez partager des données client avec un réseau publicitaire en échange de publicité.

#### Étape 3 : cartographier le parcours client et le processus de collecte de données dans vos magasins

**Parties Prenantes :** Expérience Utilisateur, Technologie De L’Information, Support Administratif

1. Identifiez chaque point du [parcours client] où les informations personnelles sont collectées, ainsi que le type d’informations collectées à chaque étape.

   Les visiteurs et visiteuses de votre site doivent être avertis à l’avance ou au point de collecte des données. Par exemple, un magasin sans intégrations personnalisées collecte des informations personnelles lors de la création d’un compte client et lors du passage en caisse. Si votre magasin comporte des intégrations personnalisées, il se peut qu’il y ait des éléments de données et des attributs supplémentaires à identifier.

1. Consultez les rubriques suivantes pour les diagrammes de flux de données applicables et les mappages d’entités de base de données pour chaque version :

   - [Référence des informations personnelles (2.x)](https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html)
   - [Référence des informations personnelles (1.x)](https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html)

   ![diagramme](./assets/privacy-frontend-diagram.svg)

#### Étape 4 : Établir des procédures et des mécanismes pour répondre aux demandes des clients

**Parties prenantes :** du service client, technologie de l’information, expérience utilisateur, support administratif

Du point de vue de la gestion des données, chaque demande de renseignements personnels implique les parties suivantes :

- **Titulaires de données** (consommateurs) : en vertu du CCPA, toute personne en Californie qui fournit des informations personnelles pour effectuer un achat et/ou gérer un compte client peut soumettre une demande d’accès ou de suppression de ses données personnelles.

- **Entités agissant en tant qu&#39;Entreprises dans le cadre du CCPA** (Marques) : [!DNL Commerce] commerçants collectent et stockent les informations personnelles de leurs clients et invités qui effectuent des achats dans leurs magasins.

- **Responsable du traitement des données** (fournisseurs de technologie) : Adobe Commerce et Magento Open Source agissent en tant que responsables du traitement des données personnelles stockées dans le cadre des services fournis aux commerçants. En tant que sous-traitant, Adobe traite les données personnelles conformément à l’autorisation et aux instructions du commerçant, conformément au contrat de licence.

Les commerçants sont tenus de faire ce qui suit :

1. Identifiez les parties impliquées dans la demande d’accès au titulaire de données (DSAR) et vérifiez l’identité de toute personne qui demande à connaître, à exclure ou à supprimer. Cela s’applique à une personne qui possède un compte client protégé par mot de passe ou qui effectue ses achats dans votre magasin en tant qu’invité.

1. Divulguer et fournir des informations à un consommateur en réponse à sa demande de droits dans les 45 jours suivant la réception d&#39;une demande vérifiable du consommateur, sauf si cela n&#39;est pas possible. (La loi prévoit certaines autres exigences pour qu&#39;une entreprise maintienne sa conformité en cas de retard pouvant aller jusqu&#39;à 45 jours supplémentaires).

   Les commerçants doivent répondre à chaque DSAR dans les 45 jours, à compter du jour où la demande est reçue. Si nécessaire, les commerçants peuvent prendre jusqu&#39;à 45 jours de plus pour répondre, pour un total maximal de 90 jours à compter du jour où la demande est reçue. Pour ce faire, le commerçant doit aviser le client pour lui expliquer la raison du retard.

1. Développez un mécanisme pour présenter les notifications requises dans votre magasin et collecter les réponses des consommateurs.

1. Établissez des procédures de réponse et documentez chacune des demandes suivantes :

   - **Demandes d&#39;information** - Les visiteurs de votre boutique doivent être informés de tout arrangement que vous devez vendre ou partager leurs informations personnelles avec des tiers, et être autorisés à se désinscrire. Les détails de votre utilisation des informations personnelles et les parties avec lesquelles vous partagez ou vendez des données peuvent être conservés dans votre politique de confidentialité.

   - **Demandes de désinscription** - Si des données personnelles sont vendues ou transférées à des tiers en échange d&#39;une contrepartie précieuse, le CCPA exige un lien _Ne pas vendre mes informations_ à chaque point où elles sont collectées. D’autres contrôles de saisie activés par l’utilisateur, tels que les cases à cocher et les boutons, peuvent être utilisés dans les communications par e-mail, les paramètres de préférences du site web ou dans les formulaires de site web au moment de la collecte de données pour que les particuliers puissent soumettre une demande de désinscription valide.

   - **Demandes de suppression**

      - Les commerçants dont les magasins sont hébergés sur Adobe Commerce Cloud doivent contacter l’assistance Adobe pour obtenir de l’aide sur la suppression des informations personnelles. Pour plus d’informations, contactez votre gestionnaire de compte technique Adobe ou le service clientèle.
      - Les commerçants qui exécutent des installations d’Adobe Commerce ou de Magento Open Source on-premise doivent mettre en œuvre leur propre processus et script pour supprimer les informations personnelles sur demande.

#### Étape 5 : rédiger le contenu des notifications client requises

**Parties prenantes :** juridique, service client, expérience utilisateur, technologie de l’information, support administratif

1. En partenariat avec votre service juridique, déterminez les types d’avis qui doivent être ajoutés à votre site Web pour respecter les obligations du CCPA.

   - **Avis de collecte** : avis donné au plus tard au moment où les renseignements personnels sont recueillis auprès du consommateur. L&#39;avis devrait être rédigé en langage simple et être facile à comprendre pour le citoyen moyen. L’avis doit être visible et fourni dans une ou plusieurs langues du contenu de votre site web.

   - **Avis de droit d’opposition** : avis informant les consommateurs de leur droit d’opposition à la vente de leurs informations personnelles.

   - **Avis d’incitation financière** : avis expliquant chaque incitation financière, prix ou différence de service que votre entreprise reçoit en échange d’informations personnelles.

   - **Comment soumettre une demande de collecte et d’utilisation de renseignements personnels** : Instructions aux particuliers pour présenter une demande de divulgation des renseignements personnels que vous avez recueillis sur la personne, y compris :

      - Informations personnelles spécifiques que vous avez collectées sur le consommateur
      - Catégories d’informations personnelles que vous avez collectées sur le consommateur
      - Catégories de sources auprès desquelles les renseignements personnels sont recueillis
      - Catégories de renseignements personnels sur le consommateur que vous avez vendus ou divulgués à des fins commerciales
      - Catégories de tiers auxquels les renseignements personnels ont été vendus ou divulgués à des fins commerciales
      - Les raisons pour lesquelles votre entreprise recueille ou vend des renseignements personnels

1. Envoyez le contenu à l’équipe et, si possible, à votre service juridique pour révision.

1. Déterminez où les avis apparaissent, comment ils fonctionnent (pour chaque visite, lors de l’authentification ou lors d’un clic publicitaire), ainsi que leur position et leur format par rapport aux autres contenus.

1. Transmettez le contenu approuvé à votre équipe de développement.

#### Étape 6 : Revoir vos ententes avec les fournisseurs de services

**Parties Prenantes :** Soutien Juridique Et Administratif

Examinez et, au besoin, mettez à jour tous les contrats des fournisseurs de services pour refléter les exigences du CCPA.

#### Étape 7 : mettre à jour votre politique de confidentialité

**Parties Prenantes :** Soutien Juridique Et Administratif

Examinez votre politique de confidentialité actuelle et déterminez quelles informations supplémentaires sont nécessaires, le cas échéant.

- **Utilisation des renseignements personnels** : Vous devez divulguer les renseignements personnels recueillis et tout incitatif financier que vous recevez en échange de la vente de vos renseignements personnels. Il est également nécessaire que vous expliquiez comment l&#39;incitation est autorisée en vertu de la CCPA, et comment la valeur des renseignements personnels est calculée.

- **Âge du consentement** : Si vous collectez ou utilisez des informations personnelles sur des mineurs, vous pouvez être soumis aux exigences suivantes :

   - **Mineurs &lt; 13 ans** : une autorisation parentale est requise pour que les mineurs de moins de 13 ans puissent s&#39;inscrire à la vente de leurs informations personnelles.

   - **Mineurs âgés de 13 à &lt; 16 ans** : Les mineurs âgés d&#39;au moins 13 ans et de moins de 16 ans peuvent choisir de vendre leurs renseignements personnels, à condition que l&#39;entreprise établisse un processus raisonnable pour documenter l&#39;action. Le processus doit être décrit dans la [politique de confidentialité](privacy-policy.md) de l&#39;entreprise. Lorsqu&#39;une entreprise reçoit des demandes de mineurs de cette tranche d&#39;âge, elle doit les informer de leur droit de retrait ultérieur et leur expliquer comment procéder.

  >[!IMPORTANT]
  >
  >Les commerçants n&#39;ont pas le droit de stocker les données personnelles des enfants sur [!DNL Commerce] plate-forme ou systèmes. S’il existe des raisons de croire que les données collectées appartiennent à une personne mineure, elles doivent être supprimées immédiatement d’une plateforme [!DNL Commerce] afin d’éviter toute violation des termes du contrat de licence Adobe.

#### Étape 8 : documenter toutes les procédures connexes et tenir des dossiers

**Parties prenantes :** du service client, du support administratif

Pendant les 24 mois suivant la réception de chaque demande de droits individuels, conservez un dossier de la demande et de la réponse de votre entreprise.
