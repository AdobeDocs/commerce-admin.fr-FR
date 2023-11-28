---
title: '[!DNL B2B for Adobe Commerce] notes de mise à jour'
description: Pour plus d’informations sur les modifications apportées à la variable [!DNL B2B for Adobe Commerce] versions d’extension.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 1123cf4b257a83a61914c378104c43e952512e7d
workflow-type: tm+mt
source-wordcount: '6937'
ht-degree: 0%

---

# [!DNL B2B for Adobe Commerce] notes de mise à jour

Ces notes de mise à jour relatives à l’extension B2B capturent les ajouts et les correctifs ajoutés par Adobe au cours d’un cycle de publication, notamment :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités
![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

>[!NOTE]
>
>Voir [Disponibilité du produit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) pour plus d’informations sur les versions de l’extension Commerce B2B prises en charge pour les versions Adobe Commerce disponibles.

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*13 novembre 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

La version bêta B2B 1.5.0 comprend de nouvelles fonctionnalités, des améliorations de qualité et des correctifs.

![Nouveau](../assets/new.svg) Les améliorations apportées aux guillemets permettent aux acheteurs et aux vendeurs de gérer plus efficacement les devis et les négociations de devis.

- **Enregistrer la citation en tant que brouillon**<!--B2B-2566-->: lors de la création d’un [demande de devis](quote-request.md) dans le panier, les acheteurs peuvent désormais enregistrer le devis en tant que brouillon en sélectionnant **[!UICONTROL Save as Draft]** sur le [!UICONTROL Request a Quote] formulaire.

  Le projet de citation n’a pas de date d’expiration. Les acheteurs peuvent consulter et mettre à jour les versions préliminaires des guillemets [!UICONTROL My Quotes] du tableau de bord de leur compte.

- **Renommer la citation**<!--B2B-2596-->: les acheteurs peuvent désormais modifier un nom de guillemet à partir du [Détails des citations](account-dashboard-my-quotes.md#quote-actions) en sélectionnant **[!UICONTROL Rename]** . Cette option est disponible pour les acheteurs autorisés lorsqu’ils modifient le devis. Les événements de changement de nom sont enregistrés dans le journal de l’historique des citations.

- **Dupliquer la citation**<!--B2B-2701-->: les acheteurs et les vendeurs peuvent désormais créer un nouveau guillemet en copiant un guillemet existant. Une copie est créée à partir de la vue Détails de la citation en sélectionnant  **[!UICONTROL Create Copy]** sur le [Mode Détails des citations](quote-price-negotiation.md#button-bar) dans l’ administrateur ou le [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Verrouillage de remise d’article**<!--B2B-2597-->: lors de la négociation de devis, les vendeurs peuvent utiliser le verrouillage de remise sur article pour plus de flexibilité lors de l’application de remises. Par exemple, un Vendeur peut appliquer une réduction spéciale sur un article et verrouiller l’article pour éviter toute remise supplémentaire. Lorsqu’un article est verrouillé, le prix de l’article ne peut pas être mis à jour lorsqu’une remise de niveau citation est appliquée. Voir [Lancer un devis pour un acheteur](sales-rep-initiates-quote.md).

![Nouveau ](../assets/new.svg)**Gestion des entreprises**<!--B2B-2901-->: les commerçants peuvent désormais afficher et gérer les entreprises Adobe Commerce sous la forme d’organisations hiérarchiques en attribuant des sociétés à des sociétés mères désignées. Une fois qu’une société est affectée à un parent, l’administrateur de la société mère peut gérer le compte de la société. Seuls les utilisateurs administrateurs autorisés peuvent ajouter et gérer des affectations d’entreprise. Pour plus d’informations, voir [Gérer la hiérarchie de l’entreprise](assign-companies.md).

- Sur la page Entreprises, une nouvelle **[!UICONTROL Company Type]** identifie les sociétés parents et enfants. Les vendeurs peuvent filtrer la vue d’entreprise par type d’entreprise et gérer les entreprises à l’aide d’éléments de ligne ou d’actions en bloc.

- Les vendeurs peuvent ajouter et gérer des affectations d’entreprise à partir du nouveau **[!UICONTROL Company Hierarchy]** de la section [!UICONTROL Company Account] page.

- Les développeurs d’API peuvent utiliser le nouveau point d’entrée de l’API REST Relations de l’entreprise `/V1/company/{parentId}/relations` pour créer, afficher et supprimer des affectations d’entreprise. Voir [Gestion des objets d’entreprise](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) dans le *Guide du développeur de l’API web*.

![Correction d’un problème](../assets/fix.svg)<!--ACP2E-1984-->Les marchands cliquent sur le bouton **[!UICONTROL Print]** dans la vue détaillée des guillemets de l’administrateur, vous êtes désormais invité à enregistrer le guillemet en tant que PDF. Auparavant, les marchands étaient redirigés vers une page qui contenait les détails des guillemets.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1742-->Auparavant, lors de l’envoi d’un devis client avec 0 pourcentage et changement de quantité, l’administrateur générait une exception, mais enregistrait la quantité. Une fois ce correctif appliqué, pour la variable `0 percentage` une exception appropriée avec un message sera générée.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1742-->Lors de la négociation d’un devis, un vendeur peut désormais définir une `0%` escompte dans le champ de remise sur devis négociée et renvoyer le devis à l’acheteur. Auparavant, si le vendeur avait effectué une remise de 0 % et l’avait renvoyé à l’acheteur, l’administrateur avait renvoyé une `Exception occurred during quote sending` message d’erreur.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-2097-->La validation ReCaptcha fonctionne désormais correctement pendant le processus de passage en caisse pour un guillemet B2B lorsque ReCaptcha V3 est configuré pour le passage en caisse du magasin. Auparavant, la validation échouait avec une `recaptcha validation failed, please try again` message d’erreur.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1825-->Les commandes ne peuvent plus être passées par un utilisateur associé à la société après le blocage de celle-ci. Auparavant, un utilisateur associé à la société pouvait passer des commandes lorsque la société était bloquée.

![Correction d’un problème](../assets/fix.svg)<!--ACP2E-1933-->Les administrateurs d’entreprise peuvent désormais ajouter des utilisateurs d’entreprise à partir du storefront. Auparavant, Commerce consignait une erreur lorsqu’un utilisateur administrateur tentait d’ajouter un nouvel utilisateur : `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2

*10 octobre 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

La version B2B v1.4.2 comprend des améliorations de qualité et des correctifs.

![Correction d’un problème](../assets/fix.svg) <!--B2B-2897-->Si un vendeur crée un devis d’acheteur qui inclut un SKU de produit non disponible dans le catalogue partagé associé à la société acheteuse, le système affiche le message d’erreur. `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Le Vendeur ne peut pas enregistrer le devis tant qu’il n’a pas supprimé le produit qui n’est pas disponible. Auparavant, le guillemet était enregistré avec le SKU non disponible inclus et le guillemet ne se chargeait pas sur le storefront.

## B2B v1.4.1

*7 août 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible avec Adobe Commerce 2.4.7-beta1.

La version B2B v1.4.1 comprend des améliorations de qualité et des correctifs de bogues.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1825-->Les commandes ne peuvent plus être passées par un utilisateur associé à la société après le blocage de celle-ci. Auparavant, un utilisateur associé à la société pouvait passer des commandes lorsque la société était bloquée.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1943-->L’état des produits en arrière-plan s’affiche désormais correctement sur le storefront. Auparavant, les produits disponibles pour l’expédition étaient incorrectement identifiés comme des commandes en souffrance.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1862-->Si le formulaire d’enregistrement de l’entreprise contient un attribut de type de fichier client, le fichier transféré au cours du processus d’enregistrement est désormais inclus dans les informations de compte de l’administrateur de l’entreprise après la création de l’entreprise. Auparavant, la pièce jointe était manquante.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1793-->Le sélecteur d’échantillon d’un produit configurable s’affiche désormais comme prévu dans la page de configuration des éléments de la liste des demandes d’acquisition. Auparavant, le sélecteur d’échantillons s’affichait sous forme de champ déroulant dans la page de configuration des éléments de la liste de demandes d’acquisition.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1968-->Lors de l’utilisation de la variable [Requête GraphQL d’entreprise](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) pour renvoyer les détails de la société, les résultats sont désormais renvoyés avec succès sans erreur.

## B2B v1.4.0

*13 juin 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible avec Adobe Commerce 2.4.7-beta1

Cette version comprend de nouvelles fonctionnalités et améliorations pour les guillemets négociables B2B et plusieurs correctifs de bogues.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec Adobe Commerce 2.4.7-beta1.

![Nouveau](../assets/new.svg) **Guillemets lancés par le vendeur**: les vendeurs peuvent désormais lancer un devis pour un acheteur directement à partir du devis et des grilles client dans l’administrateur. Cette fonctionnalité simplifie le processus de devis et réduit la complexité pour les clients. Si un client n’a pas lancé de commande, un vendeur peut rapidement créer un devis au nom du client et lancer le processus de négociation. Auparavant, les devis ne pouvaient être créés que depuis la vitrine par l’acheteur ou par un vendeur connecté en tant que client.

![Nouveau](../assets/new.svg) **Remises sur article et négociation**—<!--B2B-2440--> Dans un guillemet, les acheteurs et les vendeurs B2B peuvent désormais négocier au niveau des articles de ligne, en appliquant des rabais et en échangeant des notes jusqu’à ce qu’un accord soit trouvé. La création et les mises à jour des notes sont incluses dans l’élément de ligne et dans l’historique des guillemets pour suivre la communication. Auparavant, les acheteurs et les vendeurs pouvaient uniquement échanger des notes et appliquer des remises au niveau des devis.

![Correction d’un problème](../assets/fix.svg) Adobe Commerce affiche désormais les détails corrects lors du paiement lorsque l’option Commandes est activée et qu’un devis virtuel créé avec l’option de paiement PayPal a été sélectionné. Auparavant, les totaux s’affichaient comme nuls sous ces conditions.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1504--> Les erreurs de validation ne se produisent plus lorsque vous essayez d’enregistrer une société dont la limite de crédit dépasse 999. Auparavant, pour les limites de crédit de l’entreprise supérieures à 999, Adobe Commerce insérait un séparateur de virgule, ce qui provoquait une erreur de validation qui empêchait l’enregistrement des mises à jour.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1474-->  L’adresse de livraison sélectionnée reste inchangée lorsque vous passez une commande avec un devis négociable. Auparavant, lors de la commande, l’adresse de livraison sélectionnée était remplacée par l’adresse de livraison par défaut.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1429--> Dans les paramètres de configuration de magasin des fonctionnalités B2B, la variable **[!UICONTROL Enable Shared Catalog direct products price assigning]** est maintenant désactivé automatiquement. Sur le storefront, il est masqué lorsque la variable **[!UICONTROL Enable Company]** paramètre ou **[!UICONTROL Enable Shared Catalog]** est défini sur **[!UICONTROL No]**.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1683--> Lors de la création d’un compte d’entreprise à partir du storefront, Commerce valide désormais l’adresse électronique avant de traiter l’enregistrement de l’entreprise. Si l’adresse électronique n’est pas valide, l’opération échoue et aucune mise à jour de compte n’est traitée. Auparavant, un compte client était créé même si la demande de création d’un compte de société échouait en raison d’une adresse électronique incorrecte.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1664--> Les SKU de produit qui incluent des guillemets doubles dans le catalogue partagé et la structure de prix ne provoquent plus d’erreurs dans l’administrateur.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1498--> Mise à jour de la configuration de vernis pour l’application Commerce afin d’empêcher les utilisateurs invités de voir les données d’autres groupes de clients.

### Problème connu

Si vous installez ou mettez à niveau B2B 1.4.0 sur [Adobe Commerce version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), l’erreur suivante se produit :

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Vous pouvez résoudre ce problème en ajoutant des dépendances manuelles pour le package de sécurité B2B en ajoutant des dépendances manuelles pour le package de sécurité B2B avec une [balise de stabilité](https://getcomposer.org/doc/04-schema.md#package-links). Pour obtenir des instructions, voir [Base de connaissances Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 mars 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Publication de la version 1.3.5-p2 B2B pour prendre en charge la compatibilité avec Adobe Commerce 2.4.6-p2.

![Nouveau](../assets/new.svg) Publication de la version 1.3.5-p1 de B2B afin de prendre en charge la compatibilité avec Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Après la mise à niveau de Commerce de la version 2.4.6 vers la version [dernière version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), veillez à effectuer la mise à jour vers la version de correctif B2B 1.3.5 prise en charge. Vous pouvez également mettre à niveau l’extension B2B de la version 1.3.5 vers la version 1.4.0 ou ultérieure pour bénéficier des dernières fonctionnalités.

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.6.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce affiche désormais les détails corrects lors du paiement lorsque l’option Commandes est activée et qu’un devis virtuel créé avec l’option de paiement PayPal a été sélectionné. Auparavant, les totaux s’affichaient comme nuls sous ces conditions.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-609--> La liste des groupes de clients pour la variable **Autoriser la catégorie de navigation** ne contient plus de groupes de clients liés à des catalogues partagés.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1244--> L’attribut client Numéro de TVA/Taxe fonctionne désormais comme prévu avec les comptes d’administrateur de la société sur l’administrateur et le storefront. Les attributs Taxe/TVA personnalisés ne sont plus nécessaires pour créer un compte d’entreprise. Auparavant, lorsqu’un commerçant créait un compte de société avec un attribut Taxe/TVA personnalisé, Adobe Commerce envoyait une erreur de validation sur le storefront et l’administrateur.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1236--> La désactivation de la fonctionnalité de catalogue partagé sur une plage spécifique fonctionne désormais correctement. Auparavant, Adobe Commerce définissait une plage non valide lorsqu’un commerçant enregistrait la configuration de catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1203--> Les utilisateurs administrateurs peuvent désormais enregistrer des valeurs d’attributs personnalisés pour les utilisateurs de l’entreprise. Auparavant, les attributs personnalisés du client pour les utilisateurs de l’entreprise ne pouvaient pas être enregistrés.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1221--> Les problèmes de performances sont résolus grâce à la validation des autorisations de l’entreprise fournies par GraphQL lorsque de nombreuses autorisations de l’entreprise sont déjà attribuées.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce ne renvoie plus d’erreur sur la page du panier lorsque la commande rapide est utilisée pour ajouter un produit à une quantité qui dépasse l’inventaire disponible.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1090--> Les performances de `SELECT` les opérations d’autorisations d’entreprise ont été améliorées.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-2456--> Les requêtes de catégorie renvoient désormais les prix des produits en fonction des paramètres de configuration du magasin lorsqu’aucune autorisation de catégorie n’est explicitement définie sur la catégorie interrogée.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-6829--> La variable **[!UICONTROL Place Order]** fonctionne désormais comme prévu lorsque vous effectuez un achat avec une demande de devis approuvée. Problèmes liés au devis négociable `negotiableQuoteCheckoutSessionPlugin` ont été résolus.

## B2B v1.3.4

*9 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce n’envoie plus de notifications par courrier électronique chaque fois qu’une entreprise existante est mise à jour par un appel API. Les emails sont désormais envoyés uniquement lors de la création d’une société.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce calcule désormais correctement le total général d’un guillemet négociable lorsque la variable **[!UICONTROL Enable Cross Border Trade]** le paramètre de calcul des taxes est activé.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-322-->Les produits configurables sont désormais déplacés vers la dernière position de la liste de produits après la mise à jour du stock lors de la **[!UICONTROL Move out of stock to the bottom]** est activé. Une nouvelle requête de base de données personnalisée est implémentée pour s’assurer que l’ordre de tri des index Elasticsearch respecte désormais l’ordre de tri activé par l’administrateur. Auparavant, les produits configurables et leurs produits enfants n’étaient pas déplacés vers le bas de la liste lorsque ce paramètre était activé.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-308-->Le message électronique de bon de commande honore désormais le paramètre d’envoi des emails de chaque site web dans un déploiement multisite. Un contrôle pour la variable **[!UICONTROL Disable Email Communications]** est ajouté à la logique personnalisée pour les files d’attente d’e-mail. Auparavant, Adobe Commerce ne respectait pas le paramètre d’envoi des emails pour le site web secondaire.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-302-->Le titre du champ SKU de la page Commande rapide est modifié pour plus de clarté.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce affiche désormais un message d’erreur plus informatif lorsqu’un acheteur entre dans un SKU non valide dans la variable **Saisissez le SKU ou le nom du produit** champ .

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1753-->La variable **[!UICONTROL Account Created in]** pour un administrateur de société conserve désormais sa valeur comme prévu une fois que vous avez enregistré la société.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-722 -->La variable `customer` La requête ne renvoie plus de résultats vides lorsqu’elle récupère les listes de demandes filtrées par `uid`.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-210 -->Ajout d’un module externe avant l’événement `collectQuoteTotals` appelez pour vous assurer que les crédits de magasin ne sont appliqués qu’une seule fois.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-665 -->Les clients sont désormais redirigés vers la page de connexion lorsque leur compte est supprimé par un administrateur de l’Admin. Auparavant, Adobe Commerce renvoyait une erreur. Le module externe (`SessionPlugin`), le bloc de code se trouve maintenant à l’intérieur de la balise `try…catch` bloque. Auparavant, ce code n’était pas encapsulé dans le bloc générique de gestion des exceptions.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-661 --> Sur la page Ordre rapide en mode mobile, appuyez sur **Entrée** après avoir saisi un nom de produit ou un SKU valide, l’acheteur passe au champ suivant comme prévu.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-607 -->Le nom de la société est maintenant visible comme prévu dans les sections des adresses de facturation et de livraison du workflow de passage en caisse.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-375 -->Le crédit de magasin n’est désormais plus disponible lorsque la variable **[!UICONTROL Zero Subtotal Checkout]** le mode de paiement est désactivé. Auparavant, la case à cocher Stocker le crédit n’était pas fonctionnelle lors du placement de la commande par l’administrateur. L’application n’a pas passé la commande avec le crédit de magasin et a affiché cette erreur : `The requested Payment Method is not available`.

## B2B v1.3.3

*9 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.4.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41985--> Le temps nécessaire à la mise à niveau d’Adobe Commerce 2.3.x vers Adobe Commerce 2.4.x dans les déploiements comportant plus de 100 000 rôles d’entreprise a été considérablement réduit.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42153--> Le POST `V1/order/:orderId/invoice` prend désormais en charge la création de factures partielles lorsque la variable **[!UICONTROL Payment on Account]** le mode de paiement est activé. Auparavant, Adobe Commerce générait cette erreur : `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Correction d’un problème](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro fonctionne désormais comme prévu avec les guillemets négociables B2B lorsque le panier du client contient d’autres produits. Adobe Commerce traite désormais la commande avec succès et envoie un courrier électronique au client comme prévu. Auparavant, Adobe Commerce envoyait une erreur irrécupérable et un email de confirmation au client qui contenait zéro valeur.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41819--> La pagination s’affiche désormais correctement sur la page des résultats de recherche de catalogue après l’exclusion de certains produits du catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42886--> Les attributs personnalisés du client sont désormais enregistrés comme prévu lors de la création ou de l’enregistrement d’un utilisateur de l’entreprise dans l’administrateur.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42927--> La variable **[!UICONTROL Submit]** sur le formulaire Créer une entreprise , cette option est désormais désactivée en un seul clic pour empêcher plusieurs envois de formulaire. Auparavant, vous pouviez envoyer ce formulaire plusieurs fois en cliquant plusieurs fois sur ce bouton, ce qui générait une erreur.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce n’affiche plus le lien de réorganisation sur le storefront lorsqu’un acheteur se connecte à un magasin pour lequel les commandes ont été désactivées.

![Correction d’un problème](../assets/fix.svg) <!--- MC-43115--> La recherche dans les commandes rapides par SKU n’est désormais pas sensible à la casse lorsque le catalogue partagé est activé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42203--> Vous pouvez désormais mettre à jour un fichier pour un attribut du client lors de la création d’une société. Auparavant, lorsque vous tentiez de créer une société avec une pièce jointe de type `File`, Adobe Commerce n’a pas créé l’entreprise et a consigné cette erreur dans le journal des exceptions : `Something went wrong while saving file`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42242--> Vous pouvez désormais créer une société avec un compte client doté d’un attribut personnalisé avec un (`File`) ou (`Image`). Auparavant, si le compte disposait de l’une de ces options personnalisables, le chargeur de page de modification de l’entreprise ne se résolvait pas, ce qui empêchait la modification des détails de l’entreprise.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42268--> La variable `products` la requête renvoie désormais une valeur exacte. `total_count` lorsque le catalogue partagé est activé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42203-->  Vous pouvez désormais mettre à jour un fichier pour un attribut du client lors de la création d’une société. Auparavant, lorsque vous tentiez de créer une société avec une pièce jointe de type `File`, Adobe Commerce n’a pas créé l’entreprise et a consigné cette erreur dans le journal des exceptions : `Something went wrong while saving file`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-43178--> La variable _Configuration de l’entreprise_ et _Créer une entreprise_ les pages fonctionnent désormais comme prévu une fois que vous avez désactivé un mode de livraison en ligne. Une vérification a été ajoutée pour empêcher le traitement des modules d’expédition désactivés. Auparavant, Adobe Commerce affichait cette erreur : `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42214--> La variable _Catégorie_ affiche désormais des données de produit cohérentes lors de la génération des autorisations lors de l’indexation partielle. Un nouvel indexeur partiel pour les autorisations d’annuaire a été ajouté à ce processus. Auparavant, les données affichées pendant l’exécution de l’indexeur étaient incorrectes.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42567--> La variable `categoryList` query renvoie désormais le nombre correct de produits lorsque des autorisations de catalogue sont utilisées et que des produits sont affectés à un catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42528--> La variable `categoryList` la requête respecte désormais les autorisations de catégorie et renvoie uniquement les catégories autorisées. Auparavant, elle renvoyait toutes les catégories affectées et non affectées.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42399--> La variable `rest/V1/company/{id}` request now renvoie `is_purchase_order_enabled` des valeurs d’attribut, comme prévu.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-128--> Les attributs du client personnalisés s’affichent désormais comme prévu dans la variable _Administrateur de société_ .

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-130--> Le bloc Ma liste de souhaits de la page Mon compte s’affiche désormais comme prévu pour les administrateurs d’entreprise et les utilisateurs d’entreprise.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-133--> Les erreurs de commande rapide ne s’affichent plus dans le panier. Auparavant, Adobe Commerce affichait cette erreur dans le panier lorsque le SKU était introuvable dans le catalogue :  `The SKU was not found in the catalog`.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-194--> Les opérations d’enregistrement de catalogue partagées ont été optimisées pour s’exécuter plus rapidement. Auparavant, l’enregistrement d’un catalogue partagé avec de nombreux groupes de clients pouvait prendre plusieurs minutes.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce supprime désormais toutes les autorisations de sous-catégorie de la `sharedcatalog_category_permissions` lorsque la catégorie parent est supprimée. Auparavant, seules les données de catégorie parente étaient supprimées.

## B2B v1.3.2

*29 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.3.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce envoie désormais avec succès des emails de mise à jour concernant des guillemets négociables expirés. Auparavant, lorsqu’un guillemet négociable expirait, Adobe Commerce n’envoyait pas d’emails de mise à jour.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce envoie désormais avec succès des courriers électroniques de mise à jour concernant l’expiration prochaine et les guillemets négociables expirés lorsqu’un `cron` est manquante.

### Société

![Correction d’un problème](../assets/fix.svg) <!--- MC-41542--> Le champ déroulant Créer un compte d’entreprise - Pays ne répertorie plus les valeurs d’option vides. Auparavant, les deux premières valeurs d’option et le code de pays `AN` étaient vides.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41260--> Cliquez sur le bouton **[!UICONTROL Return]** pour une commande créée par un utilisateur de la société, redirige désormais un utilisateur administrateur vers la page Créer un retour , comme prévu. Auparavant, l’administrateur était redirigé vers la page Historique des commandes .

![Correction d’un problème](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce n’échoue plus avec une erreur de mémoire insuffisante lors de l’exécution de la variable `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` durant `bin/magento setup:upgrade`. Auparavant, Adobe Commerce n’utilisait pas la taille du lot pour la collecte lors de l’initialisation des autorisations, mais chargeait plutôt une collection de tous les rôles de l’entreprise.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40551--> Les utilisateurs de l’entreprise peuvent désormais modifier et mettre à jour les valeurs d’attributs personnalisés du client. Auparavant, ces attributs n’étaient pas correctement liés au formulaire utilisateur de création et de modification. Un utilisateur de la société peut saisir des valeurs d’attribut différentes, mais Adobe Commerce n’a pas enregistré ces valeurs correctement.

![Correction d’un problème](../assets/fix.svg) <!--- MC-32653--> L’arborescence des ressources pour les autorisations de rôle d’entreprise peut désormais être traduite comme prévu. Auparavant, l’arborescence des autorisations n’était pas traduite même si des fichiers de traduction valides étaient présents.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce enregistre désormais les valeurs d’attributs du client personnalisées pour les utilisateurs B2B comme prévu. Auparavant, la création d’un compte de société contenant des attributs client personnalisés déclenchait une erreur de modèle, et Adobe Commerce ne chargeait pas le formulaire avec succès. Ajout d’un argument à la mise en page de `company_create_account` a résolu ce problème.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41721--> Les filtres utilisateur de l’entreprise tels que Afficher tous les utilisateurs, Afficher les utilisateurs actifs et Afficher les utilisateurs inactifs fonctionnent désormais comme prévu. Auparavant, le filtrage des actions sur la page utilisateur de l’entreprise provoquait une erreur JavaScript.

### Crédit de l’entreprise

![Correction d’un problème](../assets/fix.svg) <!--- MC-41551--> Les administrateurs disposant de comptes restreints qui ne comportent que des privilèges au niveau du site web peuvent désormais créer une société qui utilise une devise différente de celle du site web.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce envoie désormais les courriers électroniques de la société à partir du bon `from` adresse électronique et portée. Auparavant, Adobe Commerce ne prenait pas en compte la portée du site web lors de l’envoi de courriers électroniques d’attribution de crédit ou de mise à jour de société.

### Ordre rapide

![Correction d’un problème](../assets/fix.svg) <!--- MC-42104--> La création d’une commande à l’aide d’un ordre rapide à partir d’un fichier CSV fonctionne désormais comme prévu avec des SKU inexistants.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40268--> L’utilisation de l’ordre rapide pour effectuer des recherches sur plusieurs SKU fonctionne désormais comme prévu. Auparavant, les résultats comprenaient des entrées en double.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40261--> L’affichage Liste de produits ajoutée traite désormais les SKU saisis en minuscules et en majuscules de la même manière que lorsque vous utilisez des SKU pour sélectionner plusieurs produits lors de la commande rapide.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40225--> L’utilisation de la commande rapide ajoute désormais les produits dans la quantité spécifiée par l’acheteur. Auparavant, Adobe Commerce n’ajoutait un produit que lorsque les quantités spécifiées par l’acheteur dépassent un produit.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41283--> La fonction de saisie automatique de commande rapide fonctionne désormais avec des SKU partiels.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce affiche désormais les produits configurés en tant que **Non visible individuellement** sur la liste de suggestions automatiques de la page Commande rapide et les résultats de recherche.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42402--> Les acheteurs peuvent désormais utiliser le formulaire Commande rapide pour ajouter plusieurs produits par SKU contenant des caractères en majuscules. Auparavant, seul le premier produit était ajouté.

### Citation négociable

![Correction d’un problème](../assets/fix.svg) <!--- MC-41232--> Les acheteurs sont désormais redirigés vers la page de guillemet négociable après avoir collé le lien vers un guillemet négociable dans le champ URL et se être connectés. Auparavant, les acheteurs étaient redirigés vers la page Mon compte .

![Correction d’un problème](../assets/fix.svg) <!--- MC-39317--> La réorganisation fonctionne désormais comme prévu pour les commandes qui contiennent un produit avec une option personnalisable par date pour un compte client créé lors du passage en caisse. Auparavant, Adobe Commerce ne traitait pas la réorganisation et affichait cette erreur : `The product has required options. Enter the options and try again`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39063--> L’adresse de livraison d’un devis négociable n’est plus modifiable lors du passage en caisse lorsque le module Bon de commande est désactivé. Ce comportement résultait d’un correctif précédent dans lequel `isQuoteAddressLocked` a été supprimé du rendu de passage en caisse négociable.

![Correction d’un problème](../assets/fix.svg) <!--- MC-38967--> Les marchands peuvent désormais ajouter des produits à un devis négociable de l&#39;administrateur.

### Commandes

![Correction d’un problème](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce affiche désormais un message d’erreur informatif comme prévu lorsque vous passez une commande à l’aide du paiement express PayPal lorsque la variable **[!UICONTROL Name Prefix]** est défini sur `required`. Auparavant, Adobe Commerce ne placait pas la commande ou n’affichait pas de message d’erreur.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39620--> Le composant d’interface utilisateur de l’adresse de facturation du module Bon de commande utilise désormais correctement l’adresse de devis lorsque le Gestionnaire de balises de Google est activé. Auparavant, une erreur JavaScript se produisait sur la page de paiement.

### Listes de demandes

![Correction d’un problème](../assets/fix.svg) <!--- MC-40426--> Les vendeurs peuvent désormais utiliser le POST `rest/all/V1/requisition_lists` point de terminaison pour créer une liste de demandes d’achat pour un client. Auparavant, Adobe Commerce générait cette erreur 400 lorsque vous tentiez de créer une liste de demandes : `Could not save Requisition List`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41123--> La variable **[!UICONTROL Add to Requisition List]** s’affiche maintenant pour les produits en stock d’un panier lorsque ce dernier contient également des produits en rupture de stock. Auparavant, si un panier contenait deux produits, dont l’un était en rupture de stock, la variable _[!UICONTROL Add to Requisition List]_n’apparaissait pour aucun des produits.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40877--> Vous pouvez désormais utiliser l’API REST pour ajouter un produit à une liste de demandes d’acquisition.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40155--> Liste des demandes **[!UICONTROL Latest Activity Date]** respectent désormais le format des paramètres régionaux.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce ne renvoie plus d’erreur fatale lorsque vous modifiez un produit en bundle à partir d’une liste de demandes d’acquisition.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce affiche désormais le prix correct du produit lorsque vous ajoutez un produit avec une option personnalisable. `(File)` à une liste de souhaits d’une liste de demandes d’acquisition. Le lien vers le fichier téléchargé est également visible comme prévu. Auparavant, Adobe Commerce affichait des prix de produit incorrects et n’affichait pas le lien vers le fichier.

![Correction d’un problème](../assets/fix.svg) <!--- MC-36383--> Produits avec une option personnalisable `(File)` peut maintenant être ajouté à un panier à partir d’une liste de demandes d’achat.

### Catalogue partagé

![Correction d’un problème](../assets/fix.svg) <!--- MC-40497--> Un administrateur dont le rôle est limité à un site web spécifique peut désormais créer, afficher et modifier un catalogue partagé. Auparavant, Adobe Commerce générait une erreur fatale lorsqu’un administrateur avec un rôle limité tentait de créer un catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41337--> Les résultats de navigation par couches incluent désormais un nombre précis de produits avec des attributs filtrés, et les acheteurs peuvent désormais appliquer plusieurs filtres. Auparavant, un seul filtre pouvait être appliqué et Adobe Commerce affichait un nombre de produits inexact dans la navigation par couches.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce affiche désormais correctement le nombre de produits dans les filtres de navigation superposés dans les résultats de recherche. Auparavant, un module externe de la page Résultats de la recherche n’utilisait pas Elasticsearch, mais envoyait une nouvelle requête à la base de données.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce ne supprime plus les prix de niveau lorsqu’un commerçant supprime tous les produits d’un catalogue partagé par défaut.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39802--> Les filtres sont désormais filtrés par catégorie actuelle et affichés correctement sur toutes les pages lorsque les catalogues partagés sont activés. Auparavant, les filtres étaient mal calculés uniquement pour la page active et n’étaient pas filtrés par la catégorie actuelle.

![Correction d’un problème](../assets/fix.svg) <!--- MC-39522--> GraphQL `products` La requête ne renvoie plus la plage de prix et la catégorie d’un produit pour les produits qui ne sont pas affectés à un catalogue partagé lorsque le catalogue partagé est activé. Auparavant, la requête renvoyait les agrégations du produit, même si le produit lui-même n’était pas renvoyé dans la variable `items` tableau.

## B2B v1.3.1

*9 février 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.2.

![Nouveau](../assets/new.svg) Les modes de paiement en ligne sont désormais pris en charge pour les commandes d’achat.

![Correction d’un problème](../assets/fix.svg) L’ajout d’un produit configurable au panier directement à partir d’une liste de commandes lorsque ce produit a été utilisé dans une commande antérieure ne renvoie plus d’erreur système.

![Correction d’un problème](../assets/fix.svg) Adobe Commerce affiche désormais correctement l’onglet Demande mon approbation pour les commandes d’achat lorsqu’une configuration de base de données partagée est déployée.

![Correction d’un problème](../assets/fix.svg) Adobe Commerce affiche désormais des détails sur les produits en bundle et la carte-cadeau lorsque vous affichez les commandes.

![Correction d’un problème](../assets/fix.svg) Les acheteurs sont désormais redirigés comme prévu après s’être connectés à leur compte lors de leur navigation dans un magasin où **[!UICONTROL Website Restriction]** est activé et **[!UICONTROL Restriction Mode]** est défini sur `Private Sales: Login Only`. Auparavant, les clients étaient redirigés vers la page d’accueil du magasin. <!--- MC-38934-->

![Correction d’un problème](../assets/fix.svg) L’historique des commandes se charge désormais comme prévu dans la page de tableau de bord du compte d’un administrateur de l’entreprise dans les déploiements avec une hiérarchie d’entreprises B2B qui contient de nombreux clients (supérieurs à 13 000). Auparavant, l’historique des commandes était chargé lentement ou pas du tout, et Adobe Commerce affichait une erreur 503. <!--- MC-38830-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce n’affiche plus plusieurs messages d’avertissement identiques lorsque vous ajoutez un produit non configuré avec des options personnalisables à une liste de demandes d’approvisionnement à partir d’une page Catégorie. <!--- MC-38342-->

![Correction d’un problème](../assets/fix.svg) Les nouveaux produits et les produits dupliqués sont désormais visibles comme prévu sur la page de catégorie lorsque les catalogues partagés B2B sont activés. <!--- MC-38307-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce conserve désormais la `store_id` qui est associé à un administrateur de société lorsque le groupe de clients d’une société est mis à jour. Auparavant, la variable `store_id` remplacée par le magasin par défaut lors de la mise à jour du groupe. <!--- MC-38196-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce enregistre désormais un produit groupé dans une liste de commandes sous la forme d’une liste de produits simples, de la même manière qu’il ajoute un produit groupé à un panier. Auparavant, en raison de la manière dont Adobe Commerce enregistrait les produits groupés, le lien d’un produit groupé depuis la liste des demandes d’achat était toujours redirigé vers des produits simples et non vers le produit groupé. <!--- MC-38049-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais filtrer les commandes selon la variable **[!UICONTROL Company Name]** lors de l’exportation des informations de commande au format CSV. Auparavant, Adobe Commerce consignait une erreur dans `var/export/{file-id}`. <!--- MC-37785-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce affiche désormais la fenêtre contextuelle Créer une liste de demandes d’acquisition comme prévu lorsque vous sélectionnez l’onglet Créer une liste de demandes d’acquisition sur le storefront. <!--- MC-37915-->

![Correction d’un problème](../assets/fix.svg) Les listes de demandes d’approvisionnement incluent désormais tous les produits et quantités groupés qui ont été ajoutés à la liste. Auparavant, lorsqu’un commerçant accédait à une liste de demandes d’achat après y avoir ajouté des produits à partir d’une page des détails du produit, Adobe Commerce affichait cette erreur : `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Correction d’un problème](../assets/fix.svg) La vue de magasin correcte est désormais associée au site web approprié lorsque vous créez une entreprise dans un déploiement multisite. Auparavant, vous ne pouviez pas créer d’entreprise et Adobe Commerce affichait cette erreur : `The store view is not in the associated website`. <!--- MC-37488-->

![Correction d’un problème](../assets/fix.svg) La commande de produits par SKU à l’aide de l’option Commande rapide n’entraîne plus la duplication de quantités de produits dans le fichier CSV. <!--- MC-37427-->

![Correction d’un problème](../assets/fix.svg) La variable **[!UICONTROL Add to Cart]** n’est plus bloqué lorsque la fonction _[!UICONTROL Enter Multiple SKUs]_de la page Ordre rapide contient une valeur vide. Adobe Commerce affiche désormais un message vous invitant à saisir des SKU valides. <!--- MC-37387-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce affiche maintenant ce message sur la page de produits lorsque vous soumettez une révision de produit à partir d’une liste de demandes d’achat : `You submitted your review for moderation`. La révision s’affiche également sur la page des révisions en attente (administrateur). **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Auparavant, bien qu’Adobe Commerce ait ajouté la révision à la liste des révisions en attente, une erreur 404 s’affichait sur la page du produit. <!--- MC-37119-->

![Correction d’un problème](../assets/fix.svg) Les performances de la variable `sharedCatalogUpdateCategoryPermissions` Le consommateur a été amélioré. Après la création d’un catalogue partagé, l’indexeur d’autorisations du catalogue utilise désormais uniquement l’ID de groupe de clients du catalogue partagé, et non tous les groupes de clients. <!--- MC-36770-->

![Correction d’un problème](../assets/fix.svg) Les champs d’attribut d’adresse client personnalisés associés à l’adresse par défaut d’un acheteur sont désormais enregistrés comme prévu dans le workflow de passage en caisse du storefront. <!--- MC-36630-->

![Correction d’un problème](../assets/fix.svg) Les commandes de produits appartenant au catalogue partagé par défaut d’un magasin peuvent désormais être passées pour les acheteurs via l’ API REST d’administration (`rest/V1/carts/{<CART_ID>/items`) comme prévu. Adobe Commerce vérifie désormais si le produit a été affecté à un catalogue public avant la validation des autorisations de catalogue partagées dans `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Auparavant, Adobe Commerce n’ajoutait pas le produit au panier de l’acheteur et envoyait cette erreur : `No such shared catalog entity`. <!--- MC-36535-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce envoie désormais des courriers électroniques d’enregistrement des utilisateurs de la société à partir de l’adresse de la boutique Adobe Commerce. Auparavant, cet email était envoyé à partir de l’adresse de l’administrateur de l’entreprise. <!--- MC-36480-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce vérifie désormais les attributs personnalisés pour la duplication des noms d’attributs de société réservés avant d’autoriser un commerçant à enregistrer un nouvel attribut. <!--- MC-36282-->

![Correction d’un problème](../assets/fix.svg) La variable `credit_history` la requête renvoie désormais l’historique de crédit de la société spécifiée pour le montant initialement alloué et le montant acheté. Auparavant, cette requête renvoyait une erreur.

![Correction d’un problème](../assets/fix.svg) La variable **[!UICONTROL Company]** et  **[!UICONTROL Job Title]** Les champs de la page Modifier les informations du compte ne sont plus modifiables.

### Problèmes connus

- Les acheteurs B2B peuvent utiliser des méthodes de paiement en ligne pour contourner le flux de commande habituel. Ce scénario peut se produire si l’acheteur peut réduire le total de son passage en caisse à 0 (par exemple, par un code promotionnel ou une carte-cadeau), puis supprimer le code ou la carte-cadeau. Même dans ces conditions, Adobe Commerce continue de passer la commande pour le bon montant en fonction des prix des articles dans leur catalogue assigné. **_Solution_**: désactivez les cartes-cadeaux et les codes de bon lorsque les méthodes de paiement en ligne sont activées pour la validation de la commande. <!--- B2B-1603-->

- Les acheteurs sont redirigés vers le panier lorsqu’ils tentent de passer une commande à partir d’une commande à l’aide de PayPal Express Checkout lorsque **[!UICONTROL In-Context Mode]** est désactivée. <!--- B2B-1604-->

- Adobe Commerce affiche parfois une erreur 404 lorsqu’un acheteur crée une commande, puis accède à la page de passage en caisse. Cette erreur se produit lorsqu’un acheteur a précédemment créé une commande différente avec un mode de paiement en ligne avant d’accéder à la page de passage en caisse sans avoir effectué l’achat précédent. L&#39;acheteur peut toujours passer la commande. **_Solution_**: aucune. <!--- B2B-1605-->

- Les remises pour un mode de paiement spécifique persistent pendant le passage en caisse pour une commande, même lorsque l’acheteur modifie son mode de paiement lors du passage en caisse final. Par conséquent, les clients peuvent recevoir une remise à laquelle ils n’ont pas droit. Ce problème se produit car une règle de panier pour le mode de paiement d’origine est toujours appliquée malgré le changement du mode de paiement. **_Solution_**: aucune. Voir [Problème connu d’Adobe Commerce 2.4.2 B2B : la remise reste pour les commandes en ligne après modification du mode de paiement](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Base de connaissances_ article. <!-- B2B-1012 -->

- La variable `deleteRequisitionListOutput` la requête renvoie des détails sur la liste des demandes supprimées au lieu des listes de demandes restantes. <!--- MC-39894-->

## B2B v1.3.0

*15 octobre 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

Cette version comprend des améliorations concernant les approbations de commandes, les méthodes d’expédition, le panier et la journalisation des actions d’administration.

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.1.

![Nouveau](../assets/new.svg) Les validations de commandes B2B ont été améliorées afin d’améliorer la convivialité et de permettre des actions en bloc sur les commandes.

![Nouveau](../assets/new.svg) Les marchands B2B peuvent désormais contrôler les méthodes d’expédition proposées à chaque entreprise.<!--- BUNDLE-160 161 162 -->

![Nouveau](../assets/new.svg) Les vendeurs peuvent désormais permettre aux utilisateurs d’effacer le contenu de leur panier en une seule action et configurer cette fonctionnalité indépendamment sur chaque site web. <!--- BUNDLE-108 -->

![Nouveau](../assets/new.svg) Les acheteurs B2B peuvent désormais ajouter des éléments individuels ou tout le contenu de leur panier directement à une liste de demandes. <!--- BUNDLE-145 144-->

![Nouveau](../assets/new.svg) Les commerçants B2B peuvent créer des commandes de l’administrateur pour le compte des clients en utilisant le mode de paiement Paiement sur compte . <!--- BUNDLE-166 178-->

![Nouveau](../assets/new.svg) Les vendeurs peuvent désormais afficher directement tous les guillemets associés à un utilisateur à partir de la page des détails du client. <!--- BUNDLE-139 -->

![Nouveau](../assets/new.svg) Les vendeurs peuvent désormais filtrer la grille Clients maintenant en ligne par société. <!--- BUNDLE-137 -->

![Nouveau](../assets/new.svg) Les administrateurs peuvent désormais filtrer les clients dans l’administrateur par représentant commercial. <!--- BUNDLE-110 -->

![Nouveau](../assets/new.svg) Pour réduire la création de comptes frauduleux ou indésirables, les marchands peuvent désormais activer Google reCAPTCHA sur le formulaire de demande de nouvelle entreprise sur le storefront. <!--- BUNDLE-154 -->

![Nouveau](../assets/new.svg) Les actions d’administration effectuées dans les modules d’entreprise sont désormais consignées dans le journal des actions d’administration. Les actions sont consignées à partir de tous les modules d’entreprise pertinents : `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce n’affiche plus le **[!UICONTROL Delete customer]** sur le bouton **Clients** lorsque l’administrateur connecté n’a pas les droits de supprimer des clients dans les déploiements où B2B est installé. <!--- MC-35655-->

![Correction d’un problème](../assets/fix.svg) Le groupe de clients n’est plus automatiquement modifié pour un client affecté à une entreprise lorsque vous modifiez le client sur la grille de clients. <!--- MC-35254-->

![Correction d’un problème](../assets/fix.svg) Lorsqu’un commerçant crée un catalogue partagé, les autorisations sont désormais automatiquement définies sur `Allow` pour le **[!UICONTROL Display Product Prices]** et **[!UICONTROL Add to Cart]** fonctionnalités des catégories lorsque cet accès est attribué au groupe de clients dans les paramètres d’autorisation du catalogue. Auparavant, ces paramètres étaient automatiquement définis sur `Deny` même lorsque les autorisations de catalogue étaient définies sur `Allow`.<!--- MC-34792-->

![Correction d’un problème](../assets/fix.svg) Les autorisations de catégorie de catalogue partagé ne sont plus remplacées lorsqu’un produit est modifié à partir de la page de modification du produit.<!--- MC-34777-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce envoie désormais une notification par e-mail confirmant qu’un client est autorisé à dépasser la limite de crédit désignée lorsqu’un commerçant active la variable **[!UICONTROL Allow To Exceed Credit Limit]** . Auparavant, l’e-mail de notification envoyé par Adobe Commerce indiquait que le client n’était pas autorisé à dépasser la limite. <!--- MC-34584-->

![Correction d’un problème](../assets/fix.svg) Le conteneur de HTMLS qui entoure le prix du produit sur les listes de demande est désormais rendu correctement pour les enfants de produits regroupés. <!--- MC-36331-->

![Correction d’un problème](../assets/fix.svg) Les commerçants peuvent désormais désigner la langue dans laquelle le courrier électronique des utilisateurs de l’entreprise est envoyé lors de la création d’une entreprise dans des déploiements multilingues. Auparavant, le menu déroulant du permet aux marchands de sélectionner la vue de magasin appropriée et la langue ne s’affichait pas.  <!--- MC-35777-->

![Correction d’un problème](../assets/fix.svg) Les champs d’attributs d’adresse client personnalisés s’affichent désormais comme prévu dans le workflow de passage en caisse du storefront. <!--- MC-35607-->

![Correction d’un problème](../assets/fix.svg) L’onglet Configuration des fonctionnalités B2B s’ouvre désormais correctement. <!--- MC-35458-->Les invités peuvent désormais utiliser QuickOrder pour ajouter des produits à leur panier, puis supprimer des articles avec succès. Auparavant, lorsqu’un acheteur utilisait QuickOrder pour ajouter plusieurs produits à son panier, puis supprimait un produit, celui-ci n’était pas supprimé. <!--- MC-35327-->

![Correction d’un problème](../assets/fix.svg) Une société peut désormais être mise à jour à l’aide du PUT API REST. `/V1/company/:companyId` sans spécifier la variable `region_id` lorsque l’état est configuré comme **non requis**. Auparavant, même si `region_id` n’était pas obligatoire, Adobe Commerce envoyait une erreur si elle n’était pas spécifiée. <!--- MC-35304-->

![Correction d’un problème](../assets/fix.svg) Lorsque vous créez ou mettez à jour une entreprise B2B à l’aide de l’API REST (`http://magento.local/rest/V1/company/2`, où `2` représente l’ID d’entreprise), la réponse inclut désormais les paramètres pour `applicable_payment_method` ou `available_payment_methods` comme prévu. <!--- MC-35248-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce n’affiche plus de page 404 lorsqu’un commerçant utilise la variable **Entrée** au lieu de cliquer sur le bouton **[!UICONTROL Save]** lors de la création d’une liste de demandes d’acquisition sur le storefront.<!--- MC-35094-->

![Correction d’un problème](../assets/fix.svg) Les autorisations de catégorie ne changent plus lorsqu’un nouveau produit est affecté à un catalogue partagé public. Auparavant, les autorisations de catégorie étaient dupliquées. <!--- MC-34386-->

![Correction d’un problème](../assets/fix.svg) PUT de point d’entrée de l’API REST `rest/default/V1/company/{id}`, qui est utilisé pour mettre à jour le courrier électronique de la société, n’est plus sensible à la casse. <!--- MC-34308-->

![Correction d’un problème](../assets/fix.svg) La désactivation des modules de récompense n’affecte plus les fonctionnalités B2B des comptes clients. Auparavant, lorsque les modules de récompense étaient désactivés, les onglets suivants liés au B2B ne s’affichaient pas : Profil de la société, Utilisateurs de la société, Rôles et autorisations.<!--- MC-34191-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce utilise désormais le nom d’expéditeur correct dans les notifications par e-mail lorsque des modifications sont apportées aux comptes de l’entreprise. Auparavant, Adobe Commerce utilisait le nom général de l&#39;expéditeur du contact défini dans la portée par défaut pour tous les emails. <!--- MC-33917-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais implémenter avec succès le multishipping pour les commandes qui contiennent des produits physiques et virtuels. <!--- MC-33818-->

![Correction d’un problème](../assets/fix.svg) Les vendeurs peuvent désormais créer des utilisateurs de l’entreprise à partir de _[!UICONTROL Company Users]_dans les pages Mon compte et Structure d’entreprise lorsque **[!UICONTROL Access Restriction]**est activé et **[!UICONTROL Restriction Mode]**est défini sur `Sales: Login Only`. Auparavant, Adobe Commerce renvoyait cette erreur lorsqu’un commerçant tentait de créer un utilisateur : `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce ne réinitialise plus le groupe de clients d’un client à la valeur par défaut lorsqu’un client enregistre ses informations de compte. <!--- MC-33554-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce ne génère plus d’erreur fatale lorsqu’un administrateur affecte un client disposant d’un panier actif à un groupe de clients. <!--- MC-33313-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce fournit désormais une `addToCart` L’événement DataLayer pour les pages de commande rapide et de demande d’acquisition.  <!--- MC-33295-->

![Correction d’un problème](../assets/fix.svg) Les e-mails de notification envoyés aux représentants commerciaux affectés à une entreprise incluent désormais le logo d’entreprise affecté. Auparavant, l’e-mail de notification incluait le logo LUMA par défaut, et non le logo d’entreprise chargé. <!--- MC-33232-->

![Correction d’un problème](../assets/fix.svg) Une liste de demandes d’approvisionnement inclut désormais tous les produits et quantités groupés qui ont été ajoutés à la liste. Auparavant, lorsqu’un commerçant accédait à une liste de demandes d’achat après y avoir ajouté des produits à partir d’une page des détails du produit, Adobe Commerce affichait cette erreur : `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Correction d’un problème](../assets/fix.svg) La variable `products` la requête renvoie désormais une valeur exacte. `total_count` lorsque le catalogue partagé est activé. <!--- MC-42268-->

![Correction d’un problème](../assets/fix.svg) Les pages Configuration de l’entreprise et Créer une entreprise fonctionnent désormais comme prévu une fois que vous avez désactivé un mode de livraison en ligne. Une vérification a été ajoutée pour empêcher le traitement des modules d’expédition désactivés. Auparavant, Adobe Commerce affichait cette erreur : `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Correction d’un problème](../assets/fix.svg) La consommation de mémoire de test d’intégration a été réduite, ce qui améliore les performances du test et réduit le temps nécessaire à la fin du test. <!--- AC-266-->

## B2B v1.2.0

*28 juillet 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.0.

![Nouveau](../assets/new.svg) Storefront Order Search, avec ajout des remerciements de Marek Mularczyk pour sa contribution [Divante](https://www.divante.com/) et les membres de la communauté.

![Nouveau](../assets/new.svg) Les commandes d’achat sont améliorées et réécrites. Ils sont désormais inclus par défaut dans Adobe Commerce.

![Nouveau](../assets/new.svg) Des règles d’approbation de bon de commande ont été mises en oeuvre. Ces règles permettent aux utilisateurs de contrôler le workflow Bon de commande en créant des règles d’achat pour les commandes.

![Nouveau](../assets/new.svg) Connexion en tant que client est désormais inclus par défaut dans Adobe Commerce. Cette fonctionnalité permet aux employés du site d’aider les clients en se connectant en tant que client pour voir ce qu’ils voient.

![Correction d’un problème](../assets/fix.svg) Les agrégations d’attributs fonctionnent désormais correctement pour la navigation par couches avec Elasticsearch

![Correction d’un problème](../assets/fix.svg) La recherche de commandes par caractères spéciaux fonctionne désormais correctement.

![Correction d’un problème](../assets/fix.svg) Cliquez sur le bouton **[!UICONTROL Clear All]** Le bouton permet désormais d’étendre tous les filtres, plutôt que de les réduire.

![Correction d’un problème](../assets/fix.svg) Le SKU/nom du produit est désormais inclus dans le résumé du filtre de recherche Historique des commandes .

![Correction d’un problème](../assets/fix.svg) L’indicateur de tri s’affiche désormais correctement dans la grille Mes commandes .

![Correction d’un problème](../assets/fix.svg) Désormais, vous ne pouvez cliquer qu’une seule fois sur les boutons Approuver, Annuler, Rejeter et Bon de commande. Auparavant, vous pouviez cliquer plusieurs fois sur le bouton.

![Correction d’un problème](../assets/fix.svg) Les boutons Approuver, Rejeter, Annuler et Valider du bon de commande s’affichent désormais correctement sur les périphériques mobiles.

![Correction d’un problème](../assets/fix.svg) Auparavant, l’approbation d’un bon de commande avec une remise expirée plaçait la commande au montant complet et ne mettait pas à jour le total du bon de commande. Maintenant, le total du bon de commande est mis à jour afin d’afficher le bon total.

![Correction d’un problème](../assets/fix.svg) Un problème a été introduit dans la version 2.3.4, en raison duquel les attributs d’extension personnalisés ne seraient pas copiés de l’adresse du client vers l’adresse citée. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Une fois B2B installé, une erreur SQL s’affichait lors de l’affectation de catégories à des catalogues partagés. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) En raison d’une valeur de type de variable incorrecte, les administrateurs n’ont pas pu ajouter de produits configurables à une commande. Les listes déroulantes d’options ne sont pas renseignées. Cette fonctionnalité fonctionne désormais correctement.

![Correction d’un problème](../assets/fix.svg) Auparavant, lors de la modification des autorisations de catégorie pour le groupe Non connecté , une erreur se produisait lors de l’enregistrement des modifications. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Un correctif est ajouté pour permettre aux administrateurs de magasin d’ajouter des produits à une commande qui ne se trouve pas dans le catalogue partagé. Auparavant, un message d’erreur s’affichait lors de l’ajout d’un élément qui ne se trouvait pas dans le catalogue.

![Correction d’un problème](../assets/fix.svg) Auparavant, après avoir exécuté la commande `php bin/magento indexer:set-dimensions-mode catalog_product_price website` puis en essayant de créer un catalogue partagé, une erreur se produisait. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Lors de l’ajout d’une société et de l’affectation de l’administrateur de la société à un site web autre qu’un site web par défaut, un identifiant de site incorrect était envoyé, ce qui provoquait une erreur. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Auparavant, une fois qu’un client avait été déplacé vers un autre groupe de clients, l’ajout d’un produit à une commande à l’aide de _Ordre rapide_ échoue avec une erreur. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Auparavant, lorsque vous tentiez d’extraire à l’aide de WebAPI avec un guillemet B2B, une valeur incorrecte était envoyée à l’API, ce qui provoquait une erreur. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Auparavant, une erreur se produisait lors de la définition d’une société sur &quot;Actif&quot; via l’API. Ce problème a maintenant été corrigé.

![Correction d’un problème](../assets/fix.svg) En raison d’un paramètre non nécessaire `form` , la page de commande est automatiquement actualisée lorsque vous appuyez sur Entrée après avoir modifié une facture de livraison proposée. Ce problème a été corrigé.

![Correction d’un problème](../assets/fix.svg) Auparavant, une erreur se produisait lors de la définition d’une limite d’affichage de produit sur une page de catalogue, qui était inférieure au nombre total de produits. Cette fonctionnalité fonctionne désormais comme prévu.

![Correction d’un problème](../assets/fix.svg) Auparavant, lors du changement d’administrateur d’une société, l’adresse d’administrateur d’origine était copiée vers le nouvel administrateur, lui donnant deux adresses. Désormais, seule l’adresse correcte est ajoutée.

![Correction d’un problème](../assets/fix.svg) Auparavant, l’utilisation de l’API pour enregistrer un élément de guillemet lorsque git est défini sur &quot;Autorisé et avertir le client&quot; échouait. Cet appel API fonctionne désormais comme prévu.

![Correction d’un problème](../assets/fix.svg) La taxe sur les produits fixes s’affiche désormais sur la page de détails Guillemets.

![Correction d’un problème](../assets/fix.svg) Auparavant, le fait de cliquer sur une pièce jointe dans l’onglet Commentaires de la page Mes guillemets ne pouvait pas télécharger le fichier. Ce comportement fonctionne désormais comme prévu.

### Problèmes connus

- Adobe Commerce renvoie une exception lors de la mise à niveau vers B2B 1.2.0 dans un déploiement multisite. When `setup:upgrade` s’exécute, cette erreur se produit sur la variable `PurchaseOrder` module : `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Solution**: installez le `B2B-716 Add NonTransactionableInterface` de l’interface `InitPurchaseOrderSalesSequence` le correctif de correctif de données, désormais disponible à partir de la **Mon compte** > **Téléchargements** section de `magento.com`.
- Si un code de remise expire avant qu’un bon de commande (bon de commande) ne soit approuvé, le bon de commande continue à afficher le montant de remise, mais une fois le bon de commande approuvé, la commande est placée au total sans remise. **Solution**: installez le `B2B-709 Purchase Order Discount patch` Correctif pour ce problème, qui est désormais disponible dans le **Mon compte** > **Téléchargements** section de `magento.com`.
- Si des articles d’une commande sont en rupture de stock ou d’une quantité insuffisante lorsque la commande est convertie en commande réelle, une erreur se produit. Si les commandes en arrière-plan sont activées, la commande est traitée normalement.
