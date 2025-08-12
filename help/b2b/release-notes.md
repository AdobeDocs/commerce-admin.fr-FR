---
title: Notes de mise à jour de [!DNL Adobe Commerce B2B]
description: Consultez les notes de mise à jour pour plus d’informations sur les modifications apportées aux versions  [!DNL Adobe Commerce B2B] .
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 298dae1e7ff3ec2af42d70a255075877458eeb4f
workflow-type: tm+mt
source-wordcount: '9030'
ht-degree: 0%

---

# Notes de mise à jour de [!DNL Adobe Commerce B2B]

Ces notes de mise à jour pour l’extension B2B capturent les ajouts et correctifs qu’Adobe a ajoutés au cours d’un cycle de publication, notamment :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités
![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

>[!NOTE]
>
>Consultez [Disponibilité du produit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) pour plus d’informations sur les versions de l’extension Commerce B2B prises en charge pour les versions d’Adobe Commerce disponibles.

## B2B v1.5.3-alpha2

*12 août 2025*

Compatible avec Adobe Commerce version 2.4.9-alpha2

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p2

*12 août 2025*

[!BADGE Prises en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.8-p2, 2.4.7-p7 et 2.4.6-p12 du correctif de sécurité d’Adobe Commerce.
Compatible avec Adobe Commerce versions 2.4.7 à 2.4.7-p6, 2.4.6 à 2.4.6-p11.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p1

*10 juin 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.8-p1, 2.4.7-p6 et 2.4.6-p11 du correctif de sécurité d’Adobe Commerce.
Compatible avec Adobe Commerce versions 2.4.7 à 2.4.7-p5, 2.4.6 à 2.4.6-p10

![Problème résolu](../assets/fix.svg) Inclut les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html).

## B2B 1.5.2

*8 avril 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.8, 2.4.7-p5 et 2.4.6-p10 du correctif de sécurité d’Adobe Commerce.
Compatible avec Adobe Commerce versions 2.4.7 à 2.4.7-p4, 2.4.6 à 2.4.6-p9

La version B2B v1.5.2 comprend des améliorations de qualité et des correctifs de bugs.

### Gestion d&#39;entreprise

![New](../assets/new.svg)<!-- B2B-4123 -->Administrators peut désormais gérer plusieurs sociétés à partir d’un seul compte à l’aide du sélecteur de sociétés de storefront. Les principaux avantages sont les suivants :

- **Gestion simplifiée de plusieurs sociétés** : les administrateurs peuvent désormais superviser plusieurs sociétés à partir d’un seul compte utilisateur, ce qui élimine la nécessité de créer et de gérer des connexions distinctes pour chaque société.
- **Changement d’entreprise efficace** : une interface intuitive permet aux administrateurs de basculer rapidement d’une entreprise à l’autre et d’effectuer des mises à jour, améliorant ainsi la productivité lors de la gestion de plusieurs entités.
- **Rationalisation des opérations** - Les gestionnaires régionaux et les chefs d&#39;entreprise peuvent gérer toutes leurs entreprises de manière centralisée, ce qui permet une prise de décision plus rapide et des opérations commerciales plus fluides.

Cette amélioration s’appuie sur la fonctionnalité d’appartenance à plusieurs sociétés de B2B 1.5.0, qui permettait aux utilisateurs d’appartenir à plusieurs sociétés, mais ne prenait pas en charge l’accès administrateur entre les sociétés. Le sélecteur d’entreprise élimine la nécessité de comptes d’administration distincts tout en conservant des contrôles d’accès appropriés et des vues spécifiques à l’entreprise.

### Société

![Correction d’un problème](../assets/fix.svg)<!-- B2B-4480 --> Correction d’un problème en raison duquel les clients invités voyaient un message d’erreur `No such entity with cartId = ?` lors de la connexion en tant qu’utilisateur d’entreprise avec des produits dans leur panier.

### Devis négociable

![Problème résolu](../assets/fix.svg) La version 1.5.2 de B2B comprend les correctifs suivants pour les devis négociables :

- <!-- B2B-3252 -->Le champ [!UICONTROL Line Item Discount Amount] valide désormais l’entrée pour empêcher la saisie de valeurs de remise négatives.
- <!-- B2B-3224 -->Correction d’un problème d’expérience utilisateur en raison duquel les notes d’élément de ligne longues étaient tronquées et difficiles à lire pour les clients B2B.
- <!-- B2B-2865 -->Les clients B2B peuvent désormais spécifier des quantités de produits à l’aide de valeurs décimales (1,5 ou 2,75, par exemple) lors de la création de devis.

### Modèle de devis

![Nouveau](../assets/new.svg)<!-- B2B-4104 --> Nouvelle possibilité pour les acheteurs et les vendeurs B2B de joindre des liens vers des documents externes à des modèles de devis. Cette fonctionnalité permet d’établir des liens vers des documents hébergés dans des services tels que DocuSign et Adobe Sign directement à partir de guillemets, en complément de la fonctionnalité de pièce jointe existante. Les principaux avantages sont les suivants :

- Une collaboration rationalisée grâce à un accès direct aux contrats et aux accords critiques
- Transparence améliorée avec accès instantané à la documentation la plus récente
- Des négociations de devis plus rapides en éliminant la nécessité de télécharger et de télécharger des fichiers
- Gestion flexible des documents à l’aide de services d’hébergement de documents externes

## B2B 1.5.1

*1 février 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.7-p4+ et 2.4.6-p9+ des correctifs de sécurité d’Adobe Commerce.
Compatible avec les versions Adobe Commerce 2.4.8-beta1 à 2.4.8-beta2, 2.4.7 à 2.4.7-p3, 2.4.6 à 2.4.6-p8

La version B2B v1.5.1 comprend des améliorations de qualité et des correctifs de bugs.

### Société

![Correction d’un problème](../assets/fix.svg)<!-- B2B-4422 --> Si un client tente de changer de société sur la page Détails du devis, le système redirige désormais le client vers une page *Accès refusé* pour s’assurer qu’un devis créé pour une société ne peut pas être utilisé pour passer une commande avec les prix d’une autre société. Auparavant, un utilisateur pouvait créer un devis avec le prix d’une société, puis passer à une autre société pour passer une commande avec des prix différents.

### Remises ligne

![Correction du problème](../assets/fix.svg)<!-- B2B-2938 --> Amélioration de l’efficacité du système en remédiant à une dégradation des performances observée dans le scénario de recalcul du devis. Auparavant, deux nouvelles entités étaient ajoutées à chaque ligne de panier, ce qui entraînait une augmentation notable des demandes de base de données, ce qui ralentissait les performances.

### Devis négociable

![Correction d’un problème](../assets/fix.svg)<!-- B2B-3820 --> Le système conserve désormais la position des éléments de l’interface utilisateur lorsque la validation de JavaScript est appliquée aux champs de *[!UICONTROL min/max qty]* sur la page Modèle de devis du storefront de Luma. Auparavant, l’application de la validation JavaScript à ces champs entraînait le déplacement d’autres éléments de l’interface utilisateur de la page.

### Panier

![Correction d’un problème](../assets/fix.svg)<!-- B2B-4222 --> Ajout d’un nouveau système de gestion des paniers conçu pour rationaliser l’expérience d’achat des utilisateurs qui gèrent plusieurs comptes d’entreprise. Le nouveau système associe les paniers à des sociétés individuelles plutôt qu’au compte client afin de rationaliser l’expérience d’achat et d’améliorer le workflow en prenant en charge les fonctionnalités suivantes.

- **Paniers spécifiques à l’entreprise :**—Les paniers sont désormais liés à des entreprises individuelles pour prendre en charge les prix et les options de produits spécifiques à l’entreprise.
- **Commutation transparente** : les utilisateurs peuvent facilement basculer entre différents comptes d’entreprise sans affecter le contenu du panier de chaque entreprise.
- **Intégrité contextuelle** : tous les détails du panier restent dans le contexte de l’entreprise correspondante, offrant ainsi une expérience d’achat cohérente et fiable.

## B2B 1.5.0

*30 octobre 2024*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.7-p3+ et 2.4.6-p8+ des correctifs de sécurité d’Adobe Commerce.
Compatible avec les versions Adobe Commerce 2.4.8-beta1, 2.4.7 à 2.4.7-p2, 2.4.6 à 2.4.6-p7.

La version 1.5.0 d’Adobe Commerce B2B est également compatible avec PHP 8.3 et prend en charge le serveur d’applications [GraphQL](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

La version B2B v1.5.0 comprend de nouvelles fonctionnalités, des améliorations de qualité et des correctifs de bugs.

>[!NOTE]
>
> Découvrez les modifications non rétrocompatibles (BIC) introduites dans la version 1.5.0 de B2B en consultant les points forts et les informations de référence dans la rubrique [ Modifications non rétrocompatibles ](backward-incompatible-changes.md).

### Gestion d&#39;entreprise

![Nouveau](../assets/new.svg) **Gestion d’entreprise**<!--B2B-2901--> : les commerçants peuvent désormais afficher et gérer les sociétés Adobe Commerce sous la forme d’organisations hiérarchiques en attribuant des sociétés à des sociétés mères désignées. Une fois qu&#39;une société est affectée à un parent, l&#39;administrateur de la société parent peut gérer le compte de la société. Seuls les utilisateurs administrateurs autorisés peuvent ajouter et gérer des affectations d’entreprise. Pour plus d’informations, voir [Gérer la hiérarchie de l’entreprise](manage-company-hierarchy.md).

- Ajoutez et gérez les affectations d’entreprise à partir de la nouvelle section *[!UICONTROL Company Hierarchy]* de la page *[!UICONTROL Company Account]* de l’Administration.

- Triez et filtrez les sociétés selon le nouveau paramètre de *[!UICONTROL Company Type]*. Dans la grille Sociétés, la colonne *[!UICONTROL Company Type]* indique si une société est une société individuelle ou fait partie de la hiérarchie organisationnelle (parent ou enfant).

![Nouveau](../assets/new.svg) **Gérer la configuration de l’entreprise à grande échelle**<!--B2B-2849--> : modifiez rapidement les paramètres de configuration de l’entreprise pour les entreprises sélectionnées à l’aide de l’action en bloc *[!UICONTROL Change company setting]* désormais disponible lors de la gestion des entreprises à partir de la grille *[!UICONTROL Companies]* ou *[!UICONTROL Company Hierarchy]*. Par exemple, si vous créez un catalogue partagé pour un groupe d’entreprises, vous pouvez modifier la configuration du catalogue partagé en une seule action au lieu de modifier chaque entreprise individuellement.

![Nouveau](../assets/new.svg) Les développeurs d’API peuvent utiliser la nouvelle `/V1/company/{parentId}/relations` de point d’entrée de l’API REST Relations d’entreprise pour créer, afficher et supprimer des affectations d’entreprise. Voir [Gérer les objets d’entreprise](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) dans le *Guide du développeur de l’API Web*.

### Comptes d’entreprise

![Nouveau](../assets/new.svg)<!--B2B-2828--> **Affectation multisociété**—Simplifiez l&#39;accès au compte d&#39;entreprise pour les utilisateurs de l&#39;entreprise en affectant un utilisateur à plusieurs sociétés. Par exemple, si vous avez un acheteur qui commande à partir de plusieurs sites d&#39;entreprise, créez un compte unique et affectez toutes les entreprises avec lesquelles l&#39;acheteur travaille à ce compte. Ensuite, l’acheteur peut se connecter une seule fois et passer d’un compte d’entreprise à l’autre en choisissant l’entreprise sur le storefront.

>[!NOTE]
>
>Un utilisateur d’entreprise peut être affecté à plusieurs sociétés, mais il ne peut être l’administrateur d’une seule société.

![Nouveau](../assets/new.svg) <!--B2B-2747--> **Sélecteur de portée d&#39;entreprise** : permet aux utilisateurs d&#39;entreprise affectés à plusieurs entreprises de changer d&#39;entreprise sur le storefront. Lorsque l’étendue est changée, les données sont mises à jour pour afficher les informations en fonction du nouveau contexte de l’entreprise. Par exemple, si la nouvelle société utilise un catalogue partagé différent, l’utilisateur de la société voit les produits, les prix et d’autres informations en fonction du nouveau catalogue partagé. Le contenu relatif aux commandes, devis et modèles de devis est également mis à jour en fonction du contexte de la société sélectionnée.

>[!NOTE]
>Le contenu du panier reflète les articles sélectionnés par le client actuel. Si le client possède un panier actif et sélectionne une autre société, il est invité à mettre à jour le panier pour refléter l’assortiment de produits, le prix et les remises promotionnelles en fonction du nouveau contexte de la société. Les produits qui ne sont pas disponibles dans le catalogue associé à la nouvelle entreprise sont supprimés du panier. Si le produit a un prix ou une disponibilité différents, le panier est mis à jour pour refléter les données disponibles dans le contexte de la société sélectionnée.<!--B2B-4222-->

![Correction d’un problème](../assets/fix.svg)<!--ACP2E-1933--> Les administrateurs de l’entreprise peuvent désormais ajouter des utilisateurs de l’entreprise depuis le storefront. Auparavant, Commerce consignait une erreur lorsqu’un utilisateur administrateur tentait d’ajouter un nouvel utilisateur : `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Devis et modèles de devis

Les améliorations apportées aux fonctionnalités de devis aident les acheteurs et les vendeurs à gérer plus efficacement les devis et la négociation de devis.

![Nouveau](../assets/new.svg) **Modèles de devis**—<!--B2B-3367-->Les acheteurs et les vendeurs peuvent désormais rationaliser le processus de devis en créant des modèles de devis réutilisables et personnalisables. Grâce aux modèles de devis, le processus de négociation de devis peut être terminé une seule fois, et les acheteurs peuvent générer des devis liés préapprouvés pour les commandes récurrentes au lieu de passer par le processus de négociation de devis pour chaque commande. Les modèles de devis étendent la fonctionnalité de devis existante en ajoutant les fonctionnalités avancées suivantes :

- **Seuils de commande** permettent aux vendeurs de définir des engagements de commande minimum et maximum, en veillant à ce que l&#39;acheteur respecte les volumes d&#39;achat convenus.
- La **définition des quantités de commande d&#39;article minimales et maximales** permet à l&#39;acheteur d&#39;ajuster les quantités de commande sur le devis lié sans avoir besoin d&#39;un nouveau modèle ou d&#39;une négociation ultérieure.
- **Suivez le nombre de devis liés générés et de commandes exécutées avec succès** pour obtenir des informations sur l&#39;exécution des accords négociés.
- Les **devis liés** sont des devis préapprouvés que l&#39;acheteur génère à partir d&#39;un modèle de devis actif afin de soumettre des commandes récurrentes basées sur les conditions négociées dans le modèle de devis.

![Nouveau](../assets/new.svg) **Améliorations apportées aux fonctionnalités de devis existantes**

- **Mise à jour des règles de la liste de contrôle d’accès (ACL)** Commerce permettant aux responsables et aux superviseurs B2B de gérer les devis et les modèles de devis des utilisateurs subordonnés. Des règles distinctes prennent en charge la configuration granulaire pour l’accès en affichage, modification et suppression.

- **Enregistrer le devis en tant que brouillon**<!--B2B-2566--> : lors de la création d&#39;une [demande de devis](quote-request.md) à partir du panier, les acheteurs peuvent désormais enregistrer le devis en tant que brouillon afin de pouvoir le consulter et le mettre à jour avant de lancer le processus de négociation du devis avec le vendeur. Le devis provisoire n&#39;a pas de date d&#39;expiration. Les acheteurs peuvent consulter et mettre à jour les devis provisoires dans la section [!UICONTROL My Quotes] du tableau de bord de leur compte.

- **Renommer le devis**<!--B2B-2596--> : les acheteurs peuvent désormais modifier le nom d&#39;un devis à partir de la page [Détails du devis](account-dashboard-my-quotes.md#quote-actions) en sélectionnant l&#39;option **[!UICONTROL Rename]**. Cette option est disponible pour les acheteurs autorisés lorsqu&#39;ils modifient le devis. Les événements de changement de nom sont enregistrés dans le journal de l’historique des devis.

- **Dupliquer le devis**<!--B2B-2701--> : les acheteurs et les vendeurs peuvent désormais créer un devis en copiant un devis existant. Une copie est créée à partir de la vue des détails du devis en sélectionnant **[!UICONTROL Create Copy]** dans la vue [Détails du devis](quote-price-negotiation.md#button-bar) dans l&#39;Admin ou le [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Déplacer l&#39;article du devis vers la liste des demandes d&#39;approvisionnement**<!--B2B-2755--> : les acheteurs ont désormais la possibilité de supprimer des produits d&#39;un devis et de les enregistrer dans une liste de demandes d&#39;approvisionnement s&#39;ils décident de ne pas les inclure dans le processus de négociation du devis.

- **Supprimer plusieurs produits d&#39;un devis**<!--B2B-2881--> : pour les devis comportant un grand nombre de produits, les acheteurs peuvent désormais supprimer plusieurs produits du devis en les sélectionnant et en utilisant l&#39;option *[!UICONTROL Remove]* du contrôle *[!UICONTROL Actions]* de la page des détails du devis. Dans les versions précédentes, un acheteur devait supprimer les produits un par un.

- **Verrouillage de la remise sur article de ligne**<!--B2B-2597--> : pendant la négociation du devis, les vendeurs peuvent utiliser le verrouillage de la remise sur article de ligne pour plus de flexibilité lors de l&#39;application des remises pendant le processus de négociation du devis. Par exemple, un vendeur peut appliquer une remise spéciale sur une ligne à un article et verrouiller l&#39;article pour empêcher toute remise supplémentaire. Lorsqu&#39;un article est verrouillé, le prix de l&#39;article ne peut pas être mis à jour lorsqu&#39;une remise au niveau du devis est appliquée. Voir [Lancer le devis pour un acheteur](sales-rep-initiates-quote.md).

![Correction d’un problème](../assets/fix.svg) **correctifs pour les fonctionnalités de devis existantes**

- Les commerçants qui cliquent sur le bouton *[!UICONTROL Print]* dans la vue des détails du devis dans l&#39;Administration sont maintenant invités à enregistrer le devis en tant que PDF. Auparavant, les commerçants étaient redirigés vers une page qui contenait des détails sur le devis. <!--ACP2E-1984-->

- Auparavant, lors de l’envoi d’un devis client avec `0` pourcentage et une quantité variable, l’administrateur générait une exception mais enregistrait la quantité. Une fois que ce correctif est appliqué, l’exception appropriée `0 percentage` avec un message est générée. <!--ACP2E-1742-->

- Lors de la négociation du devis, un vendeur peut maintenant spécifier une remise `0%` dans le champ Remise du devis négocié et renvoyer le devis à l&#39;acheteur. Auparavant, si le vendeur saisissait une remise de 0 % et renvoyait le devis à l&#39;acheteur, l&#39;administrateur renvoyait un message d&#39;erreur `Exception occurred during quote sending`. <!--ACP2E-1742-->

- La validation ReCaptcha fonctionne désormais correctement pendant le processus de passage en caisse pour un devis B2B lorsque ReCaptcha V3 est configuré pour le passage en caisse storefront. Auparavant, la validation échouait avec un message d’erreur `recaptcha validation failed, please try again`.  <!--ACP2E-2097-->

### Commandes achat

![Problème résolu](../assets/fix.svg) <!--ACP2E-1825-->Les commandes fournisseur ne peuvent plus être passées par un utilisateur associé à la société après le blocage de celle-ci. Auparavant, un utilisateur associé à la société pouvait passer des commandes fournisseur lorsque la société était bloquée.

## B2B v1.4.2-p7

*12 août 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.7-p7+ et 2.4.6-p12+.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

{{b2b-compatibility}}

## B2B v1.4.2-p6

*10 juin 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.7-p6+ et 2.4.6-p11+.

![Problème résolu](../assets/fix.svg) Inclut les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html).

{{b2b-compatibility}}

## B2B v1.4.2-p5

*8 avril 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.7-p5+ et 2.4.6-p10+.

![Nouveau ](../assets/new.svg) compatibilité ajoutée avec les versions 2.4.7-p5+ et 2.4.6-p10+ des correctifs de sécurité d’Adobe Commerce.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

{{b2b-compatibility}}

## B2B v1.4.2-p4

*1 février 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.7-p4+ et 2.4.6-p9+ des correctifs de sécurité d’Adobe Commerce.

![Nouveau ](../assets/new.svg) compatibilité ajoutée avec les versions 2.4.7-p4+ et 2.4.6-p9+ des correctifs de sécurité d’Adobe Commerce.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 octobre 2024*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions 2.4.7-p3+ et 2.4.6-p8+ des correctifs de sécurité d’Adobe Commerce.

![Nouveau ](../assets/new.svg) compatibilité ajoutée avec les versions 2.4.7-p3+ et 2.4.6-p8+ des correctifs de sécurité d’Adobe Commerce.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.7-p2+ et 2.4.6-p7+.

![Nouveau ](../assets/new.svg) compatibilité ajoutée avec les versions 2.4.7-p2+ et 2.4.6-p7+ des correctifs de sécurité d’Adobe Commerce.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans le Bulletin de sécurité xxxx.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 août 2024*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.7-p1+ et 2.4.6-p6+.

![Nouveau ](../assets/new.svg) compatibilité ajoutée avec les versions de correctifs de sécurité Adobe Commerce 2.4.7-p1+ et 2.4.6-p6+.

{{b2b-compatibility}}

## B2B v1.4.2

*10 octobre 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce version 2.4.7 et version 2.4.6 à 2.4.6-p5.

La version B2B v1.4.2 comprend des améliorations de qualité et des correctifs de bugs.

![Problème résolu](../assets/fix.svg) <!--B2B-2897-->Si un vendeur crée un devis acheteur qui inclut un SKU de produit non disponible dans le catalogue partagé associé à la société acheteur, le système affiche le message d&#39;erreur `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Le vendeur ne peut pas enregistrer le devis tant qu&#39;il n&#39;a pas supprimé le produit qui n&#39;est pas disponible. Auparavant, le devis était enregistré avec le SKU indisponible inclus et le chargement du devis sur le storefront échouait.

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ est compatible avec PHP 8.2. Si vous mettez à niveau l’instance Commerce vers la version 2.4.7+, assurez-vous que l’instance utilise PHP version 8.2 pour maintenir la compatibilité avec la version B2B d’Adobe Commerce. En outre, B2B 1.4.2+ ne prend actuellement pas en charge le [serveur d’applications GraphQL](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 août 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible avec Adobe Commerce 2.4.7-beta1.

La version B2B v1.4.1 comprend des améliorations de qualité et des correctifs de bugs.

![Problème résolu](../assets/fix.svg) <!--ACP2E-1825-->Les commandes fournisseur ne peuvent plus être passées par un utilisateur associé à la société après le blocage de celle-ci. Auparavant, un utilisateur associé à la société pouvait passer des commandes fournisseur lorsque la société était bloquée.

![Problème résolu](../assets/fix.svg) <!--ACP2E-1943-->Le statut du produit en retard s’affiche désormais correctement sur le storefront. Auparavant, les produits disponibles pour expédition étaient incorrectement identifiés comme en retard.

![Problème résolu](../assets/fix.svg) <!--ACP2E-1862-->Si le formulaire d&#39;enregistrement de la société comporte un attribut de type de fichier client, le fichier chargé pendant le processus d&#39;enregistrement est désormais inclus dans les informations de compte de l&#39;administrateur de la société une fois la société créée. Auparavant, la pièce jointe était manquante.

![Correction d&#39;un problème](../assets/fix.svg) <!--ACP2E-1793-->Le sélecteur d&#39;échantillon d&#39;un produit configurable s&#39;affiche désormais comme prévu dans la page de configuration des éléments de la liste de demandes d&#39;approvisionnement. Auparavant, le sélecteur d&#39;échantillon s&#39;affichait sous forme de champ déroulant dans la page de configuration des éléments de la liste de demandes d&#39;approvisionnement.

![Problème résolu](../assets/fix.svg) <!--ACP2E-1968-->Lors de l’utilisation de la requête [GraphQL d’entreprise](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) pour renvoyer les détails de l’entreprise, les résultats sont désormais renvoyés sans erreur.

## B2B v1.4.0

*13 juin 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible avec Adobe Commerce 2.4.7-beta1

Cette version comprend de nouvelles fonctionnalités et améliorations pour les devis négociables B2B et plusieurs correctifs de bogues.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec Adobe Commerce 2.4.7-bêta1.

![Nouveau](../assets/new.svg) **Devis initié par le vendeur** : les vendeurs peuvent désormais initier un devis pour un acheteur directement à partir des grilles Devis et Client de l&#39;administrateur. Cette fonctionnalité simplifie le processus de devis et réduit la complexité pour les clients. Si un client n&#39;a pas lancé de commande, un vendeur peut rapidement créer un devis au nom du client et lancer le processus de négociation. Auparavant, les devis ne pouvaient être créés qu&#39;à partir du storefront par l&#39;acheteur ou par un vendeur connecté en tant que client.

![Nouveau](../assets/new.svg) **Remises et négociation d&#39;article de ligne**—<!--B2B-2440--> Dans un devis, les acheteurs et les vendeurs B2B peuvent désormais négocier au niveau de l&#39;article de ligne, en appliquant des remises et en échangeant des notes jusqu&#39;à ce qu&#39;un accord soit conclu. La création et les mises à jour de notes sont incluses dans l&#39;historique des lignes et des devis pour suivre la communication. Auparavant, les acheteurs et les vendeurs ne pouvaient échanger que des billets et appliquer des remises au niveau du devis.

![Problème résolu](../assets/fix.svg) Adobe Commerce affiche désormais les informations correctes lors du paiement lorsque l&#39;option Commandes est activée et qu&#39;un devis virtuel créé avec l&#39;option de paiement PayPal a été sélectionné. Auparavant, les totaux s’affichaient en tant que zéro dans ces conditions.

![Problème résolu ](../assets/fix.svg) les erreurs de validation <!--ACP2E-1504--> ne se produisent plus lorsque vous tentez de sauver une entreprise dont la limite de crédit dépasse 999. Auparavant, pour les limites de crédit d’entreprise supérieures à 999, Adobe commerce insérait un séparateur à virgules, ce qui provoquait une erreur de validation qui empêchait l’enregistrement des mises à jour.

![Problème résolu](../assets/fix.svg) <!--ACP2E-1474--> L&#39;adresse d&#39;expédition sélectionnée reste inchangée lorsque vous passez une commande avec un devis négociable. Auparavant, lorsque vous passiez une commande, l’adresse de livraison sélectionnée était remplacée par l’adresse de livraison par défaut.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1429--> Dans les paramètres de configuration du magasin pour les fonctionnalités B2B, le champ **[!UICONTROL Enable Shared Catalog direct products price assigning]** est désormais automatiquement désactivé. Sur le storefront, il est masqué lorsque le paramètre **[!UICONTROL Enable Company]** ou **[!UICONTROL Enable Shared Catalog]** paramètre est défini sur **[!UICONTROL No]**.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1683--> lors de la création d’un compte de société à partir du storefront, Commerce valide désormais l’adresse e-mail avant de traiter l’enregistrement de la société. Si l’adresse e-mail n’est pas valide, l’opération échoue et aucune mise à jour de compte n’est traitée. Auparavant, un compte client était créé même si la demande de création d’un compte d’entreprise échouait en raison d’une adresse e-mail non valide.

![Correction d’un problème](../assets/fix.svg) les SKU de produit <!--ACP2E-1664--> qui incluent des guillemets doubles dans le catalogue partagé et la structure de tarification ne provoquent plus d’erreurs dans l’administration.

![Correction d’un problème](../assets/fix.svg) <!--ACP2E-1498--> Mise à jour de la configuration du vernis pour l’application Commerce afin d’empêcher les utilisateurs invités de voir les données d’autres groupes de clients.

### Problème connu

Si vous installez ou mettez à niveau B2B 1.4.0 sur [Adobe Commerce version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), l’erreur suivante se produit :

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Vous pouvez résoudre ce problème en ajoutant des dépendances manuelles pour le package de sécurité B2B en ajoutant des dépendances manuelles pour le package de sécurité B2B avec une [ balise de stabilité ](https://getcomposer.org/doc/04-schema.md#package-links). Pour obtenir des instructions, consultez la [Base de connaissances Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5-p12

*12 août 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.6-p12+.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.5-p10

*8 avril 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.6-p10+.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec les versions des correctifs de sécurité Adobe Commerce 2.4.6-p10.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

## B2B v1.3.5-p9

*1 février 2025*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.6-p9+.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec les versions des correctifs de sécurité Adobe Commerce 2.4.6-p9.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

## B2B v1.3.5-p8

*8 octobre 2024*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.6-p8+.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec les versions des correctifs de sécurité Adobe Commerce 2.4.6-p8.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

## B2B v1.3.5-p7

*9 août 2024*

[!BADGE Prise en charge]{type=Informative tooltip="Pris en charge"} versions des correctifs de sécurité Adobe Commerce 2.4.6-p7+.

![Nouveau](../assets/new.svg) Ajout de la compatibilité avec les versions des correctifs de sécurité Adobe Commerce 2.4.6-p7.

## B2B v1.3.5

*14 mars 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 - 2.4.6 et versions plus récentes

Publication de la version 1.3.5-p2 de ![New](../assets/new.svg) B2B pour assurer la compatibilité avec la version 2.4.6-p2 d’Adobe Commerce.

Publication de la version 1.3.5-p1 de ![New](../assets/new.svg) B2B pour assurer la compatibilité avec la version 2.4.6-p1 d’Adobe Commerce.

>[!NOTE]
>
>Après avoir mis à niveau Commerce de la version 2.4.6 vers la [dernière version](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), veillez à effectuer la mise à jour vers la version de correctif B2B 1.3.5 prise en charge. Vous pouvez également mettre à niveau l’extension B2B de la version 1.3.5 vers la version 1.4.0 ou une version ultérieure pour obtenir les dernières fonctionnalités.

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.6.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce affiche désormais les détails corrects lors du paiement lorsque l&#39;option Commandes est activée et qu&#39;un devis virtuel créé avec l&#39;option de paiement PayPal a été sélectionné. Auparavant, les totaux s’affichaient en tant que zéro dans ces conditions.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-609--> la liste des groupes de clients pour le paramètre **Autoriser la catégorie de navigation** ne contient plus de groupes de clients associés aux catalogues partagés.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-1244--> L’attribut client Numéro de taxe/TVA fonctionne désormais comme prévu avec les comptes d’administration de la société sur les storefront et Admin. Les attributs Taxe/TVA personnalisés ne sont plus nécessaires pour créer un compte d’entreprise. Auparavant, lorsqu’un commerçant créait un compte de société avec un attribut Taxe/TVA personnalisé, Adobe Commerce générait une erreur de validation sur le storefront et l’administrateur.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1236--> La désactivation de la fonctionnalité de catalogue partagé sur une portée spécifique fonctionne désormais correctement. Auparavant, Adobe Commerce définissait une portée non valide lorsqu’un commerçant enregistrait la configuration de catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1203--> les utilisateurs administrateurs peuvent désormais enregistrer les valeurs d’attributs personnalisés du client pour les utilisateurs de l’entreprise. Auparavant, les attributs personnalisés du client pour les utilisateurs de l’entreprise ne pouvaient pas être enregistrés.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-1221--> Les problèmes de performances sont résolus avec la validation des autorisations d’entreprise fournies via GraphQL lorsque de nombreuses autorisations d’entreprise sont déjà attribuées.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce ne renvoie plus d’erreur sur la page du panier lorsque la commande rapide est utilisée pour ajouter un produit dans une quantité qui dépasse le stock disponible.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-1090--> Les performances des opérations d’autorisations d’`SELECT` société se sont améliorées.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-2456--> requêtes Catégorie renvoient désormais les prix des produits en fonction des paramètres de configuration du magasin lorsqu’aucune autorisation de catégorie n’est explicitement définie sur la catégorie faisant l’objet de la requête.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-6829--> Le bouton **[!UICONTROL Place Order]** fonctionne désormais comme prévu lors de l&#39;exécution d&#39;un achat avec une demande de devis approuvée. Les problèmes liés au module externe de `negotiableQuoteCheckoutSessionPlugin` de devis négociable ont été résolus.

## B2B v1.3.4-p14

*12 août 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.4-p13

*10 juin 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5-p12.

![Problème résolu](../assets/fix.svg) Inclut les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html).

## B2B v1.3.4-p12

*8 avril 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5-p12.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

## B2B v1.3.4-p11

*1 février 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5-p11.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

## B2B v1.3.4-p10

*9 octobre 2024*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5-p10.

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

## B2B v1.3.4

*9 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce n’envoie plus de notifications par e-mail chaque fois qu’une entreprise existante est mise à jour par un appel API. Désormais, les e-mails ne sont envoyés que lorsqu’une entreprise est créée.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce calcule désormais correctement le total général d&#39;un devis négociable lorsque le paramètre de calcul de taxe **[!UICONTROL Enable Cross Border Trade]** est activé.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-322-->Les produits configurables sont désormais déplacés à la dernière position de la liste des produits après la mise à jour du stock lorsque le paramètre **[!UICONTROL Move out of stock to the bottom]** est activé. Une nouvelle requête de base de données personnalisée est implémentée pour s’assurer que l’ordre de tri de l’index Elasticsearch respecte désormais l’ordre de tri activé par l’administrateur. Auparavant, les produits configurables et leurs produits enfants n’étaient pas déplacés en bas de la liste lorsque ce paramètre était activé.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-308-->L’e-mail de bon de commande respecte désormais le paramètre d’envoi d’e-mail de chaque site web dans un déploiement multisite. Une vérification du paramètre **[!UICONTROL Disable Email Communications]** est ajoutée à la logique personnalisée pour les files d’attente d’e-mails. Auparavant, Adobe Commerce ne respectait pas le paramètre d’envoi d’e-mail pour le site web secondaire.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-302-->Le titre du champ SKU de la page Commande rapide a été modifié pour plus de clarté.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce affiche désormais un message d’erreur plus informatif lorsqu’un acheteur saisit un SKU non valide dans le champ **Saisir le SKU ou le nom du produit**.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-1753-->Le champ **[!UICONTROL Account Created in]** d’un administrateur d’entreprise conserve désormais sa valeur telle qu’attendue après l’enregistrement de l’entreprise.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-722 -->La requête `customer` ne renvoie plus de résultats vides lorsqu&#39;elle récupère les listes de demandes d&#39;approvisionnement filtrées par `uid`.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-210 -->Ajout d’un plug-in avant l’appel `collectQuoteTotals` pour s’assurer que les crédits de magasin ne sont appliqués qu’une seule fois.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-665 -->les clients sont désormais redirigés vers la page de connexion lorsque leur compte est supprimé par un administrateur de l’administration. Auparavant, Adobe Commerce générait une erreur. Le bloc de code du plug-in (`SessionPlugin`) se trouve désormais dans le bloc `try…catch`. Auparavant, ce code n’était pas encapsulé dans le bloc générique de gestion des exceptions.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-661 --> Sur la page Commande rapide en mode mobile, si vous appuyez sur **Entrée** après avoir saisi un nom de produit ou un SKU valide, l’acheteur accède au champ suivant comme prévu.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-607 -->Le nom de la société est désormais visible comme prévu dans les sections Adresse de facturation et d’expédition du workflow de passage en caisse.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-375 -->Le crédit de la boutique est désormais indisponible lorsque le mode de paiement **[!UICONTROL Zero Subtotal Checkout]** est désactivé. Auparavant, la case à cocher Stocker le crédit n’était pas fonctionnelle lors du placement de la commande auprès de l’administrateur. L&#39;application n&#39;a pas passé la commande avec le crédit de magasin et a affiché cette erreur : `The requested Payment Method is not available`.

## B2B v1.3.3-p15

*12 août 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Problème résolu](../assets/fix.svg) Comprend les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.3-p14

*10 juin 2025*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.5-p12.

![Problème résolu](../assets/fix.svg) Inclut les correctifs de sécurité documentés dans [Bulletin de sécurité APSB25-50](https://helpx.adobe.com/security/products/magento/apsb25-50.html).

## B2B v1.3.3

*9 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.4.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41985--> Le temps nécessaire à la mise à niveau d’Adobe Commerce 2.3.x vers Adobe Commerce 2.4.x dans les déploiements avec plus de 100 000 rôles d’entreprise a été considérablement réduit.

![Problème résolu](../assets/fix.svg) <!--- MC-42153--> La demande de `V1/order/:orderId/invoice` POST prend désormais en charge la création de factures partielles lorsque le mode de paiement **[!UICONTROL Payment on Account]** est activé. Auparavant, Adobe Commerce générait cette erreur : `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problème résolu](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro fonctionne désormais comme prévu avec un devis négociable B2B lorsque le panier du client contient d&#39;autres produits. Adobe Commerce traite maintenant la commande avec succès et envoie un e-mail au client comme prévu. Auparavant, Adobe Commerce générait une erreur fatale et envoyait un e-mail de confirmation au client qui ne contenait aucune valeur.

![Problème résolu](../assets/fix.svg) <!--- MC-41819--> Pagination s’affiche désormais correctement sur la page des résultats de la recherche dans le catalogue après l’exclusion de certains produits du catalogue partagé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42886--> les attributs personnalisés du client sont désormais enregistrés comme prévu lors de la création ou de l’enregistrement d’un utilisateur d’entreprise dans Admin.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42927--> Le bouton **[!UICONTROL Submit]** du formulaire Créer une nouvelle entreprise est désormais désactivé après un clic pour empêcher plusieurs envois de formulaire. Auparavant, vous pouviez envoyer ce formulaire plusieurs fois en cliquant sur ce bouton à plusieurs reprises, ce qui générait une erreur.

![Problème résolu](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce n’affiche plus le lien de réorganisation sur le storefront lorsqu’un acheteur se connecte à un magasin pour lequel les réorganisations ont été désactivées.

![Problème résolu](../assets/fix.svg) <!--- MC-43115--> recherche rapide de commandes par SKU ne respecte plus la casse lorsque le catalogue partagé est activé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42203--> Vous pouvez désormais mettre à jour un fichier pour un attribut de client lors de la création d’une entreprise. Auparavant, lorsque vous tentiez de créer une société avec une pièce jointe de type `File`, Adobe Commerce n’effectuait pas cette création et consignait cette erreur dans le journal des exceptions : `Something went wrong while saving file`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42242--> Vous pouvez désormais créer une entreprise avec un compte client qui possède un attribut personnalisé de type (`File`) ou (`Image`). Auparavant, si le compte disposait de l’une de ces options personnalisables, le chargeur de page de modification d’entreprise ne se résolvait pas, ce qui empêchait la modification des détails de l’entreprise.

![Problème résolu](../assets/fix.svg) <!--- MC-42268--> La requête `products` renvoie désormais un champ `total_count` précis lorsque le catalogue partagé est activé.

![Correction d’un problème](../assets/fix.svg) <!--- MC-42203--> Vous pouvez désormais mettre à jour un fichier pour un attribut de client lors de la création d’une entreprise. Auparavant, lorsque vous tentiez de créer une société avec une pièce jointe de type `File`, Adobe Commerce n’effectuait pas cette création et consignait cette erreur dans le journal des exceptions : `Something went wrong while saving file`.

![Correction d’un problème](../assets/fix.svg) <!--- MC-43178--> les pages _Configuration de l’entreprise_ et _Créer une entreprise_ fonctionnent désormais comme prévu après la désactivation d’une méthode d’expédition en ligne. Une vérification a été ajoutée pour empêcher la tentative de traitement des modules d&#39;expédition désactivés. Auparavant, Adobe Commerce affichait cette erreur : `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problème résolu](../assets/fix.svg) <!--- MC-42214--> La page _Catégorie_ affiche désormais des données de produit cohérentes pendant la génération des autorisations lors de l’indexation partielle. Un nouvel indexeur partiel pour les autorisations de répertoire a été ajouté à ce processus. Auparavant, les données affichées pendant l’exécution de l’indexeur étaient incorrectes.

![Problème résolu](../assets/fix.svg) <!--- MC-42567--> La requête `categoryList` renvoie désormais le nombre correct de produits lorsque des autorisations de catalogue sont utilisées et que des produits sont affectés à un catalogue partagé.

![Problème résolu](../assets/fix.svg) <!--- MC-42528--> La requête `categoryList` respecte désormais les autorisations de catégorie et renvoie uniquement les catégories autorisées. Auparavant, elle renvoyait toutes les catégories affectées et non affectées.

![Problème résolu](../assets/fix.svg) <!--- MC-42399--> La demande de `rest/V1/company/{id}` renvoie désormais `is_purchase_order_enabled` valeurs d’attribut comme prévu.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-128--> les attributs personnalisés du client s’affichent désormais comme prévu dans l’onglet _Administrateur d’entreprise_.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-130--> le bloc Ma liste de souhaits de la page Mon compte s’affiche désormais comme prévu pour les administrateurs de l’entreprise et les utilisateurs de l’entreprise.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-133--> erreurs de commande rapide ne s’affichent plus dans le panier. Auparavant, Adobe Commerce affichait cette erreur dans le panier lorsque le SKU était introuvable dans le catalogue : `The SKU was not found in the catalog`.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-194--> les opérations d’enregistrement de catalogue partagé ont été optimisées pour s’exécuter plus rapidement. Auparavant, l’enregistrement d’un catalogue partagé avec de nombreux groupes de clients pouvait prendre plusieurs minutes.

![Problème résolu](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce supprime désormais toutes les autorisations de sous-catégorie de la table `sharedcatalog_category_permissions` lorsque la catégorie parent est supprimée. Auparavant, seules les données de la catégorie parente étaient supprimées.

## B2B v1.3.2

*29 août 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.3.

![Problème résolu](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce envoie désormais avec succès des e-mails de mise à jour sur les devis négociables expirés. Auparavant, lorsqu’un devis négociable expirait, Adobe Commerce n’envoyait pas d’e-mails de mise à jour.

![Problème résolu](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce envoie désormais avec succès des e-mails de mise à jour sur le point d’expirer et des devis négociables expirés lorsqu’un traitement de `cron` est manquant.

### Société

![Problème résolu](../assets/fix.svg) <!--- MC-41542--> le champ déroulant Pays de la page Créer un nouveau compte d’entreprise ne répertorie plus les valeurs d’option vides. Auparavant, les deux premières valeurs d’option et le code pays `AN` étaient vides.

![Problème résolu](../assets/fix.svg) <!--- MC-41260--> Cliquez sur le bouton **[!UICONTROL Return]** d’une commande créée par un utilisateur de l’entreprise pour rediriger un utilisateur administrateur vers la page Créer un retour comme prévu. Auparavant, l’administrateur était redirigé vers la page Historique des commandes.

![Correction du problème](../assets/fix.svg) [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} <!--- MC-40798--> Adobe Commerce n’échoue plus avec une erreur de mémoire insuffisante lors de l’exécution de la méthode `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` pendant l’`bin/magento setup:upgrade`. Auparavant, Adobe Commerce n’utilisait pas la taille de lot pour la collection lors de l’initialisation des autorisations, mais chargeait à la place une collection de tous les rôles de société.

![Problème résolu](../assets/fix.svg) <!--- MC-40551--> utilisateurs de la société peuvent désormais modifier et mettre à jour les valeurs d’attribut personnalisé du client. Auparavant, ces attributs ne se liaient pas correctement au formulaire de création et de modification d’utilisateur. Un utilisateur de société peut saisir différentes valeurs d’attribut, mais Adobe Commerce ne les a pas enregistrées correctement.

![Correction d’un problème](../assets/fix.svg) <!--- MC-32653--> L’arborescence de ressources pour les autorisations des rôles d’entreprise peut désormais être traduite comme prévu. Auparavant, l’arborescence des autorisations n’était pas traduite même si des fichiers de traduction valides étaient présents.

![Problème résolu](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce enregistre désormais les valeurs d’attributs du client personnalisées pour les utilisateurs B2B comme prévu. Auparavant, la création d’un compte de société contenant des attributs de client personnalisés déclenchait une erreur de modèle et Adobe Commerce ne chargeait pas correctement le formulaire. L’ajout d’un argument à la disposition des `company_create_account` a résolu ce problème.

![Problème résolu](../assets/fix.svg) <!--- MC-41721--> filtres utilisateur de l’entreprise, tels que Afficher tous les utilisateurs, Afficher les utilisateurs actifs et Afficher les utilisateurs inactifs fonctionnent désormais comme prévu. Auparavant, les actions de filtrage sur la page utilisateur de la société provoquaient une erreur JavaScript.

### Crédit d’entreprise

![Correction d’un problème](../assets/fix.svg) <!--- MC-41551--> les administrateurs et administratrices disposant de comptes restreints qui incluent uniquement des privilèges au niveau du site web peuvent désormais créer une entreprise qui utilise une devise différente de celle du site web.

![Problème résolu](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce envoie désormais des e-mails de société à partir de l’adresse e-mail et de la portée `from` correctes. Auparavant, Adobe Commerce ne prenait pas en compte la portée du site web lors de l’envoi d’e-mails d’affectation de crédit ou de mise à jour.

### Commande rapide

![Correction d’un problème](../assets/fix.svg) <!--- MC-42104--> la création d’une commande à l’aide d’une commande rapide dans un fichier CSV fonctionne désormais comme prévu avec des SKU inexistants.

![Correction d’un problème](../assets/fix.svg) <!--- MC-40268--> l’utilisation de la commande rapide pour rechercher sur plusieurs SKU fonctionne désormais comme prévu. Auparavant, les résultats incluaient des entrées en double.

![Problème résolu ](../assets/fix.svg) <!--- MC-40261--> l’affichage de la liste des produits ajoutés traite désormais de la même manière les SKU saisis en minuscules et en majuscules lorsque vous utilisez des SKU pour sélectionner plusieurs produits lors de la commande rapide.

![Problème résolu](../assets/fix.svg) <!--- MC-40225--> Utiliser la commande rapide permet désormais d’ajouter les produits dans la quantité spécifiée par l’acheteur. Auparavant, Adobe Commerce ajoutait un produit uniquement lorsque les quantités spécifiées par l’acheteur étaient supérieures à un.

![Correction d’un problème](../assets/fix.svg) <!--- MC-41283--> la fonction de saisie automatique des commandes rapides fonctionne désormais avec des SKU partiels.

![Problème résolu](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce affiche désormais les produits configurés comme **Non visibles individuellement** dans la liste de suggestions automatiques de la page Commande rapide et dans les résultats de la recherche.

![Problème résolu](../assets/fix.svg) <!--- MC-42402--> les acheteurs peuvent désormais utiliser le formulaire de commande rapide pour ajouter plusieurs produits par SKU qui incluent des caractères majuscules. Auparavant, seul le premier produit était ajouté.

### Devis négociable

![Problème résolu](../assets/fix.svg) <!--- MC-41232--> acheteurs sont maintenant redirigés vers la page de devis négociable après avoir collé le lien vers un devis négociable dans le champ URL et s’être connectés avec succès. Auparavant, les acheteurs étaient redirigés vers la page Mon compte .

![Problème résolu](../assets/fix.svg) <!--- MC-39317--> La réorganisation fonctionne désormais comme prévu pour les commandes contenant un produit avec une option personnalisable de date pour un compte client créé lors du passage en caisse. Auparavant, Adobe Commerce ne traitait pas la réorganisation et affichait cette erreur : `The product has required options. Enter the options and try again`.

![Problème résolu](../assets/fix.svg) <!--- MC-39063--> L&#39;adresse d&#39;expédition d&#39;un devis négociable n&#39;est plus modifiable lors du passage en caisse lorsque le module Bon de commande est désactivé. Ce comportement résulte d’un correctif précédent dans lequel `isQuoteAddressLocked` a été supprimé du moteur de rendu de passage en caisse de devis négociable.

![Correction d&#39;un problème](../assets/fix.svg) <!--- MC-38967--> les commerçants peuvent désormais ajouter des produits à un devis négociable de l&#39;administrateur.

### Commandes fournisseur

![Problème résolu](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce affiche désormais un message d&#39;erreur informatif comme prévu lorsque vous passez une commande à l&#39;aide de PayPal Express Checkout lorsque l&#39;attribut **[!UICONTROL Name Prefix]** est défini sur `required`. Auparavant, Adobe Commerce ne passait pas de commande et n’affichait pas de message d’erreur.

![Problème résolu](../assets/fix.svg) <!--- MC-39620--> le composant d’interface utilisateur de l’adresse de facturation dans le module Bon de commande utilise désormais correctement l’adresse du devis lorsque le Gestionnaire de balises Google est activé. Auparavant, une erreur JavaScript s’était produite sur la page de paiement.

### Listes de demandes d&#39;approvisionnement

![Correction d’un problème](../assets/fix.svg) <!--- MC-40426--> Les commerçants peuvent désormais utiliser le point d’entrée de `rest/all/V1/requisition_lists` POST pour créer une liste de demandes d’approvisionnement pour un client. Auparavant, Adobe Commerce générait cette erreur 400 lorsque vous tentiez de créer une liste de demandes d’approvisionnement : `Could not save Requisition List`.

![Problème résolu](../assets/fix.svg) <!--- MC-41123--> Le bouton **[!UICONTROL Add to Requisition List]** s’affiche désormais pour les produits en stock d’un panier lorsque le panier contient également des produits en rupture de stock. Auparavant, si un panier contenait deux produits, dont l’un était en rupture de stock, le bouton _[!UICONTROL Add to Requisition List]_ne s’affichait pour aucun d’eux.

![Correction d&#39;un problème](../assets/fix.svg) <!--- MC-40877--> Vous pouvez désormais utiliser l&#39;API REST pour ajouter un produit à une liste de demandes d&#39;approvisionnement.

![Problème résolu](../assets/fix.svg) <!--- MC-40155--> les valeurs **[!UICONTROL Latest Activity Date]** de la liste des demandes d&#39;approvisionnement sont désormais conformes au format des paramètres régionaux.

![Problème résolu](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce ne renvoie plus d’erreur irrécupérable lorsque vous modifiez un produit groupé à partir d’une liste de demandes d’approvisionnement.

![Problème résolu](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce affiche désormais le prix correct du produit lorsque vous ajoutez un produit avec une option personnalisable `(File)` à une liste de souhaits à partir d&#39;une liste de demandes d&#39;approvisionnement. Le lien vers le fichier chargé est également visible comme prévu. Auparavant, Adobe Commerce affichait des prix de produit incorrects et n’affichait pas le lien vers le fichier .

![Problème résolu](../assets/fix.svg) <!--- MC-36383--> produits dotés d&#39;une option personnalisable `(File)` peuvent désormais être ajoutés à un panier à partir d&#39;une liste de demandes d&#39;approvisionnement.

### Catalogue partagé

![Problème résolu](../assets/fix.svg) <!--- MC-40497--> Un administrateur disposant d’un rôle limité à un site web spécifique peut désormais créer, afficher et modifier un catalogue partagé. Auparavant, Adobe Commerce générait une erreur irrécupérable lorsqu’un administrateur disposant d’un rôle limité tentait de créer un catalogue partagé.

![Problème résolu](../assets/fix.svg) <!--- MC-41337--> les résultats de navigation superposée incluent désormais un nombre précis de produits avec des attributs filtrés. Les acheteurs peuvent désormais appliquer plusieurs filtres. Auparavant, un seul filtre pouvait être appliqué et Adobe Commerce affichait un nombre de produits inexact dans une navigation superposée.

![Problème résolu](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce affiche désormais correctement le nombre de produits dans les filtres de navigation superposés dans les résultats de recherche. Auparavant, un module externe pour la page Résultats de la recherche n’utilisait pas Elasticsearch, mais envoyait une nouvelle requête à la base de données.

![Problème résolu](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce ne supprime plus les prix de niveau lorsqu’un commerçant supprime tous les produits d’un catalogue partagé par défaut.

![Problème résolu](../assets/fix.svg) <!--- MC-39802--> Les filtres sont désormais filtrés par la catégorie actuelle et s’affichent correctement sur toutes les pages lorsque les catalogues partagés sont activés. Auparavant, les filtres étaient calculés par erreur pour la page active uniquement et n’étaient pas filtrés par la catégorie active.

![Problème résolu](../assets/fix.svg) <!--- MC-39522--> La requête de `products` GraphQL ne renvoie plus la plage de prix et la catégorie d’un produit pour les produits qui ne sont pas affectés à un catalogue partagé lorsque le catalogue partagé est activé. Auparavant, la requête renvoyait les agrégations du produit, même si le produit lui-même n’était pas renvoyé dans le tableau `items`.

## B2B v1.3.1

*9 février 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.2.

![Nouveau](../assets/new.svg) Les modes de paiement en ligne sont désormais pris en charge pour les commandes fournisseur.

![Problème résolu](../assets/fix.svg) L&#39;ajout d&#39;un produit configurable au panier directement à partir d&#39;une liste de demandes d&#39;approvisionnement lorsque ce produit était utilisé dans une commande précédente ne renvoie plus d&#39;erreur système.

![Problème résolu](../assets/fix.svg) Adobe Commerce affiche désormais correctement l&#39;onglet Requires My Approval pour les commandes fournisseur lorsqu&#39;une configuration de base de données partagée est déployée.

![Problème résolu](../assets/fix.svg) Adobe Commerce affiche désormais des détails sur les produits groupés et la carte cadeau lorsque vous affichez des commandes fournisseur.

![Problème corrigé](../assets/fix.svg) les acheteurs sont désormais redirigés comme prévu après s’être connectés à leur compte lors de leur navigation dans un magasin où **[!UICONTROL Website Restriction]** est activé et **[!UICONTROL Restriction Mode]** est défini sur `Private Sales: Login Only`. Auparavant, les acheteurs étaient redirigés vers la page d’accueil du magasin. <!--- MC-38934-->

![Correction d’un problème](../assets/fix.svg) L’historique des commandes se charge désormais comme prévu dans la page Tableau de bord du compte d’un administrateur d’entreprise dans les déploiements avec une hiérarchie d’entreprise B2B qui contient de nombreux clients (supérieur à 13000). Auparavant, l’historique des commandes était chargé lentement ou pas du tout et Adobe Commerce affichait une erreur 503. <!--- MC-38830-->

![Problème résolu](../assets/fix.svg) Adobe Commerce n&#39;affiche plus plusieurs messages d&#39;avertissement identiques lorsque vous ajoutez un produit non configuré avec des options personnalisables à une liste de demandes d&#39;approvisionnement à partir d&#39;une page Catégorie. <!--- MC-38342-->

![Problème résolu](../assets/fix.svg) Les nouveaux produits et les produits dupliqués sont désormais visibles comme prévu sur la page de catégorie lorsque les catalogues partagés B2B sont activés. <!--- MC-38307-->

![Problème résolu](../assets/fix.svg) Adobe Commerce conserve désormais la `store_id` correcte associée à un administrateur d’entreprise lorsque le groupe de clients d’une entreprise est mis à jour. Auparavant, le `store_id` était remplacé par le magasin par défaut lors de la mise à jour du groupe. <!--- MC-38196-->

![Problème résolu](../assets/fix.svg) Adobe Commerce enregistre désormais un produit regroupé dans une liste de demandes d&#39;approvisionnement sous la forme d&#39;une liste de produits simples, de la même manière qu&#39;il ajoute un produit regroupé à un panier. Auparavant, en raison de la manière dont Adobe Commerce avait enregistré les produits regroupés, le lien d&#39;un produit regroupé de la liste des demandes d&#39;approvisionnement était toujours redirigé vers des produits simples et non vers le produit regroupé. <!--- MC-38049-->

![Problème résolu](../assets/fix.svg) Vous pouvez désormais filtrer les commandes par le champ **[!UICONTROL Company Name]** lors de l’exportation des informations de commande au format CSV. Auparavant, Adobe Commerce consignait une erreur dans `var/export/{file-id}`. <!--- MC-37785-->

![Problème résolu](../assets/fix.svg) Adobe Commerce affiche désormais la fenêtre contextuelle Créer une liste de demandes d&#39;approvisionnement comme prévu lorsque vous sélectionnez l&#39;onglet Créer une liste de demandes d&#39;approvisionnement dans le storefront. <!--- MC-37915-->

![Problème résolu](../assets/fix.svg) Les listes de demandes d&#39;approvisionnement incluent désormais tous les produits et quantités groupés qui ont été ajoutés à la liste. Auparavant, lorsqu&#39;un commerçant accédait à une liste de demandes d&#39;approvisionnement après y avoir ajouté des produits à partir d&#39;une page de détails du produit, Adobe Commerce affichait cette erreur : `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Correction d’un problème](../assets/fix.svg) La vue correcte du magasin est désormais associée au site web approprié lorsque vous créez une entreprise dans un déploiement multisite. Auparavant, vous ne pouviez pas créer de société et Adobe Commerce affichait cette erreur : `The store view is not in the associated website`. <!--- MC-37488-->

![Problème résolu](../assets/fix.svg) La commande de produits par SKU à l’aide de la commande rapide n’entraîne plus la duplication des quantités de produits dans le fichier CSV. <!--- MC-37427-->

![Correction d’un problème](../assets/fix.svg) Le bouton **[!UICONTROL Add to Cart]** n’est plus bloqué lorsque la section _[!UICONTROL Enter Multiple SKUs]_de la page Commande rapide contient une valeur vide. À la place, Adobe Commerce affiche désormais un message vous invitant à saisir des SKU valides. <!--- MC-37387-->

![Problème résolu](../assets/fix.svg) Adobe Commerce affiche désormais ce message sur la page produit lorsque vous envoyez une révision de produit à partir d&#39;une liste de demandes d&#39;approvisionnement : `You submitted your review for moderation`. La révision s’affiche également sur la page Révisions en attente (**[!UICONTROL Marketing]** d’administration > **[!UICONTROL Pending Reviews]**). Auparavant, bien qu’Adobe Commerce ait ajouté la révision à la liste des révisions en attente, une erreur 404 était générée sur la page du produit. <!--- MC-37119-->

![Correction d’un problème](../assets/fix.svg) Les performances du consommateur `sharedCatalogUpdateCategoryPermissions` ont été améliorées. Après la création d’un catalogue partagé, l’indexeur d’autorisations de catalogue utilise désormais uniquement l’ID de groupe de clients du catalogue partagé, et pas tous les groupes de clients. <!--- MC-36770-->

![Problème résolu ](../assets/fix.svg) les champs d’attribut d’adresse de client personnalisés associés à l’adresse non par défaut d’un acheteur sont désormais enregistrés comme prévu dans le workflow de passage en caisse du storefront. <!--- MC-36630-->

![Correction d’un problème](../assets/fix.svg) Les commandes de produits appartenant au catalogue partagé par défaut d’un magasin peuvent désormais être passées pour les acheteurs par le biais de l’API Admin REST (`rest/V1/carts/{<CART_ID>/items`) comme prévu. Adobe Commerce vérifie désormais si le produit a été affecté à un catalogue public avant la validation des autorisations du catalogue partagé dans `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Auparavant, Adobe Commerce n’ajoutait pas le produit au panier de l’acheteur et générait l’erreur suivante : `No such shared catalog entity`. <!--- MC-36535-->

![Problème résolu](../assets/fix.svg) Adobe Commerce envoie désormais les nouveaux e-mails d’enregistrement des utilisateurs de l’entreprise à partir de l’adresse de la boutique Adobe Commerce. Auparavant, cet e-mail était envoyé à partir de l’adresse de l’administrateur de la société. <!--- MC-36480-->

![Problème résolu](../assets/fix.svg) Adobe Commerce recherche désormais les attributs personnalisés afin de dupliquer les noms d’attributs de société réservés avant d’autoriser un commerçant à enregistrer un nouvel attribut. <!--- MC-36282-->

![Problème résolu](../assets/fix.svg) La requête `credit_history` renvoie désormais l’historique de crédit de la société spécifiée pour le montant alloué à l’origine et le montant acheté. Auparavant, cette requête renvoyait une erreur.

![Correction d’un problème](../assets/fix.svg) Les champs **[!UICONTROL Company]** et **[!UICONTROL Job Title]** de la page Modifier les informations du compte ne sont plus modifiables.

### Problèmes connus

- Les acheteurs B2B peuvent utiliser des méthodes de paiement en ligne pour contourner le flux habituel de bon de commande. Ce scénario peut se produire si l&#39;acheteur peut réduire son total de passage en caisse à 0 (par exemple, par un code promotion ou une carte cadeau), puis supprimer le code ou la carte cadeau. Même dans ces conditions, Adobe Commerce passe toujours la commande au montant correct en fonction des prix des articles dans son catalogue attribué. **_Solution_** : Désactivez les cartes-cadeaux et les codes coupon lorsque les modes de paiement en ligne sont activés pour l’approbation du bon de commande. <!--- B2B-1603-->

- Les acheteurs sont redirigés vers le panier lorsqu&#39;ils tentent de passer une commande à partir d&#39;un bon de commande à l&#39;aide de PayPal Express Checkout lorsque **[!UICONTROL In-Context Mode]** est désactivé. <!--- B2B-1604-->

- Adobe Commerce affiche parfois une erreur 404 lorsqu’un acheteur crée une commande fournisseur, puis accède à la page de passage en caisse. Cette erreur se produit lorsqu&#39;un acheteur a précédemment créé une autre commande avec un mode de paiement en ligne avant de passer à la page de passage en caisse sans effectuer l&#39;achat précédent. L&#39;acheteur peut toujours passer la commande. **_Solution de contournement_** : aucune. <!--- B2B-1605-->

- Les remises pour un mode de paiement spécifique persistent lors de la commande fournisseur, même lorsque l&#39;acheteur modifie son mode de paiement lors de la commande finale. Par conséquent, les clients peuvent recevoir une remise à laquelle ils n’ont pas droit. Ce problème se produit, car une règle de panier pour le mode de paiement d’origine est toujours appliquée malgré le changement de mode de paiement. **_Solution de contournement_** : aucune. Consultez l’article [Adobe Commerce 2.4.2 B2B connu : la remise reste pour les commandes en ligne après le changement du mode de paiement](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Base de connaissances_. <!-- B2B-1012 -->

- La requête `deleteRequisitionListOutput` renvoie des détails sur la liste de demandes d&#39;approvisionnement supprimée au lieu des listes restantes. <!--- MC-39894-->

## B2B v1.3.0

*15 octobre 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

Cette version comprend des améliorations des approbations de commande, des méthodes d’expédition, du panier et de la journalisation des actions d’administration.

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.1.

![Nouvelle](../assets/new.svg) les approbations de commande B2B ont été améliorées afin d’améliorer la convivialité et de permettre des actions en masse sur les commandes fournisseur.

![Nouveau ](../assets/new.svg) les commerçants B2B peuvent désormais contrôler les méthodes d’expédition proposées à chaque société.<!--- BUNDLE-160 161 162 -->

![Nouveau](../assets/new.svg) Les commerçants peuvent désormais permettre aux utilisateurs de supprimer le contenu de leur panier en une seule action et peuvent configurer cette fonctionnalité indépendamment sur chaque <!--- BUNDLE-108 --> de site web

![Nouveau](../assets/new.svg) les acheteurs B2B peuvent désormais ajouter des articles individuels ou l&#39;intégralité du contenu de leur panier directement à une liste de demandes d&#39;approvisionnement. <!--- BUNDLE-145 144-->

![Nouveau](../assets/new.svg) les commerçants B2B peuvent créer des commandes auprès de l’administrateur pour le compte de clients à l’aide du paiement par compte comme mode de paiement. <!--- BUNDLE-166 178-->

![Nouveau](../assets/new.svg) Les commerçants peuvent désormais consulter directement tous les devis associés à un utilisateur à partir de la page des détails du client. <!--- BUNDLE-139 -->

![Nouveau](../assets/new.svg) Les commerçants peuvent maintenant filtrer la grille Clients maintenant en ligne par entreprise. <!--- BUNDLE-137 -->

![Nouveau](../assets/new.svg) les administrateurs peuvent désormais filtrer les clients dans le <!--- BUNDLE-110 --> Admin by Sales Rep.

![Nouveau](../assets/new.svg) Pour réduire la création de comptes frauduleux ou de pourriels, les commerçants peuvent maintenant activer Google reCAPTCHA dans le formulaire de demande de nouvelle société sur le storefront. <!--- BUNDLE-154 -->

![Nouveau](../assets/new.svg) Les actions d’administration effectuées dans les modules Société sont désormais consignées dans le journal des actions d’administration. Les actions sont consignées à partir de tous les modules d’entreprise pertinents : `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Problème résolu](../assets/fix.svg) Adobe Commerce n’affiche plus le bouton **[!UICONTROL Delete customer]** sur la page **Clients** lorsque l’administrateur connecté ne dispose pas des droits de suppression des clients dans les déploiements où B2B est installé. <!--- MC-35655-->

![Problème résolu](../assets/fix.svg) Le groupe de clients n&#39;est plus modifié automatiquement pour un client affecté à une entreprise lorsque vous modifiez le client sur la grille de clients. <!--- MC-35254-->

![Correction d’un problème](../assets/fix.svg) Lorsqu’un commerçant crée un catalogue partagé, les autorisations sont désormais automatiquement définies sur `Allow` pour les fonctionnalités de **[!UICONTROL Display Product Prices]** et de **[!UICONTROL Add to Cart]** dans les catégories lorsque le groupe de clients se voit attribuer cet accès dans les paramètres d’autorisation du catalogue. Auparavant, ces paramètres étaient automatiquement définis sur `Deny` même lorsque les autorisations de catalogue étaient définies sur `Allow`.<!--- MC-34792-->

![Problème résolu ](../assets/fix.svg) les autorisations de catégorie de catalogue partagé ne sont plus remplacées lorsqu’un produit est modifié à partir de la page de modification du produit.<!--- MC-34777-->

![Problème résolu](../assets/fix.svg) Adobe Commerce envoie désormais une notification par e-mail confirmant qu’un client est autorisé à dépasser la limite de crédit désignée lorsqu’un commerçant active le paramètre **[!UICONTROL Allow To Exceed Credit Limit]**. Auparavant, l’e-mail de notification envoyé par Adobe Commerce indiquait que le client n’était pas autorisé à dépasser la limite. <!--- MC-34584-->

![Problème résolu](../assets/fix.svg) Le conteneur HTML qui entoure le prix des produits sur les listes de demandes d&#39;approvisionnement est désormais correctement rendu pour les enfants des produits groupés. <!--- MC-36331-->

![Problème résolu](../assets/fix.svg) Les commerçants peuvent désormais désigner la langue dans laquelle l’e-mail de l’utilisateur de l’entreprise est envoyé lors de la création d’une entreprise dans des déploiements multilingues. Auparavant, le menu déroulant permettant aux commerçants de sélectionner la vue de magasin appropriée et la langue n’était pas affiché.  <!--- MC-35777-->

![Problème résolu](../assets/fix.svg) les champs d’attributs d’adresse du client personnalisés s’affichent désormais comme prévu dans le workflow de passage en caisse du storefront. <!--- MC-35607-->

![Problème résolu](../assets/fix.svg) L’onglet Configuration des fonctionnalités B2B s’ouvre désormais correctement. <!--- MC-35458-->Les clients peuvent désormais utiliser QuickOrder pour ajouter des produits à leur panier, puis supprimer des articles. Auparavant, lorsqu’un acheteur utilisait QuickOrder pour ajouter plusieurs produits à son panier, puis supprimait un produit, le produit n’était pas supprimé. <!--- MC-35327-->

![Correction d’un problème](../assets/fix.svg) Il est désormais possible de mettre à jour une société à l’aide de la requête de `/V1/company/:companyId` PUT de l’API REST sans spécifier le `region_id` lorsque l’état est configuré comme **non requis**. Auparavant, même si `region_id` n’était pas obligatoire, Adobe Commerce générait une erreur si elle n’était pas spécifiée. <!--- MC-35304-->

![Correction d’un problème](../assets/fix.svg) lorsque vous créez ou mettez à jour une société B2B à l’aide de l’API REST (`http://magento.local/rest/V1/company/2`, où `2` représente l’ID de société), la réponse inclut désormais les paramètres de `applicable_payment_method` ou de `available_payment_methods` comme prévu. <!--- MC-35248-->

![Problème résolu](../assets/fix.svg) Adobe Commerce n&#39;affiche plus de page 404 lorsqu&#39;un commerçant utilise le bouton **Entrée** au lieu de cliquer sur le bouton **[!UICONTROL Save]** lors de la création d&#39;une liste de demandes d&#39;approvisionnement sur le storefront.<!--- MC-35094-->

![Problème résolu](../assets/fix.svg) Les autorisations de catégorie ne changent plus lorsqu&#39;un nouveau produit est affecté à un catalogue public partagé. Auparavant, les autorisations de catégorie étaient dupliquées. <!--- MC-34386-->

![Correction d’un problème](../assets/fix.svg) Le `rest/default/V1/company/{id}` PUT du point d’entrée de l’API REST, qui est utilisé pour mettre à jour l’adresse e-mail de l’entreprise, n’est plus sensible à la casse. <!--- MC-34308-->

![Problème résolu ](../assets/fix.svg) la désactivation des modules de récompense n’affecte plus les fonctionnalités B2B sur les comptes clients. Auparavant, lorsque les modules de récompense étaient désactivés, les onglets liés au B2B suivants n’étaient pas affichés : Profil de l’entreprise, Utilisateurs de l’entreprise et Rôles et autorisations.<!--- MC-34191-->

![Problème résolu](../assets/fix.svg) Adobe Commerce utilise désormais le nom d’expéditeur correct sur les notifications par e-mail lorsque des modifications sont apportées aux comptes d’entreprise. Auparavant, Adobe Commerce utilisait le nom général de l’expéditeur du contact défini dans la portée par défaut pour tous les e-mails. <!--- MC-33917-->

![Problème résolu](../assets/fix.svg) Vous pouvez désormais implémenter avec succès le multishipping pour les commandes contenant des produits physiques et virtuels. <!--- MC-33818-->

![Correction d’un problème](../assets/fix.svg) les commerçants peuvent désormais créer des utilisateurs d’entreprise à partir de la section _[!UICONTROL Company Users]_des pages Mon compte et Structure de l’entreprise lorsque **[!UICONTROL Access Restriction]**est activé et **[!UICONTROL Restriction Mode]**est défini sur `Sales: Login Only`. Auparavant, Adobe Commerce générait cette erreur lorsqu’un commerçant tentait de créer un utilisateur : `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce ne réinitialise plus le groupe de clients d’un client sur la valeur par défaut lorsqu’un client enregistre ses informations de compte. <!--- MC-33554-->

![Problème résolu](../assets/fix.svg) Adobe Commerce ne renvoie plus d’erreur fatale lorsqu’un administrateur affecte un client qui a un panier actif à un groupe de clients. <!--- MC-33313-->

![Problème résolu](../assets/fix.svg) Adobe Commerce fournit désormais un événement DataLayer `addToCart` pour les pages de listes de commandes rapides et de demandes d&#39;approvisionnement.  <!--- MC-33295-->

![Problème résolu](../assets/fix.svg) Les e-mails de notification envoyés aux représentants commerciaux affectés à une entreprise incluent désormais le logo attribué à l’entreprise. Auparavant, l’e-mail de notification incluait le logo LUMA par défaut, et non le logo de l’entreprise chargé. <!--- MC-33232-->

![Problème résolu](../assets/fix.svg) Une liste de demandes d&#39;approvisionnement inclut désormais tous les produits et quantités regroupés qui ont été ajoutés à la liste. Auparavant, lorsqu&#39;un commerçant accédait à une liste de demandes d&#39;approvisionnement après y avoir ajouté des produits à partir d&#39;une page de détails du produit, Adobe Commerce affichait cette erreur : `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problème résolu](../assets/fix.svg) La requête `products` renvoie désormais un champ `total_count` précis lorsque le catalogue partagé est activé. <!--- MC-42268-->

![Correction d’un problème](../assets/fix.svg) Les pages Configuration de l’entreprise et Créer une entreprise fonctionnent désormais comme prévu après la désactivation d’une méthode d’expédition en ligne. Une vérification a été ajoutée pour empêcher la tentative de traitement des modules d&#39;expédition désactivés. Auparavant, Adobe Commerce affichait cette erreur : `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problème résolu](../assets/fix.svg) La consommation de la mémoire de test de l’intégration a été réduite, ce qui améliore les performances de test et réduit le temps nécessaire à l’achèvement du test. <!--- AC-266-->

## B2B v1.2.0

*28 juillet 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Adobe Commerce 2.4.0 et versions plus récentes

![Nouveau](../assets/new.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.0.

![Nouveau](../assets/new.svg) Recherche de commande de storefront, avec des remerciements supplémentaires pour la contribution de Marek Mularczyk de [Divante](https://www.divante.com/) et des membres de la communauté.

![Nouveau](../assets/new.svg) Les bons de commande ont été améliorés et réécrits. Ils sont désormais inclus par défaut dans Adobe Commerce.

![Nouveau](../assets/new.svg) les règles d&#39;approbation des commandes fournisseur ont été mises en œuvre. Ces règles permettent aux utilisateurs de contrôler le workflow de bon de commande en créant des règles d’achat pour les commandes.

![Nouveau](../assets/new.svg) La connexion en tant que client est désormais incluse par défaut dans Adobe Commerce. Cette fonctionnalité permet aux employés du site d’aider les clients en se connectant en tant que client pour voir ce qu’ils voient.

![Problème résolu](../assets/fix.svg) les agrégations d’attributs fonctionnent désormais correctement pour la navigation par couches avec Elasticsearch

![Problème résolu](../assets/fix.svg) La recherche de commandes par caractères spéciaux fonctionne désormais correctement.

![Problème résolu](../assets/fix.svg) Cliquer sur le bouton **[!UICONTROL Clear All]** développe désormais tous les filtres, plutôt que de les réduire.

![Problème résolu](../assets/fix.svg) le SKU/nom du produit est désormais inclus dans le résumé du filtre de recherche de l’historique des commandes.

![Problème résolu](../assets/fix.svg) l&#39;indicateur de tri s&#39;affiche désormais correctement dans la grille Mes commandes.

![Problème résolu](../assets/fix.svg) Désormais, vous ne pouvez cliquer qu&#39;une seule fois sur les boutons Approuver, Annuler, Rejeter et Bon de commande. Auparavant, vous pouviez cliquer sur le bouton plusieurs fois.

![Problème résolu](../assets/fix.svg) Les boutons Approuver, Rejeter, Annuler et Valider des bons de commande s’affichent désormais correctement sur les appareils mobiles.

![Problème résolu](../assets/fix.svg) Auparavant, l&#39;approbation d&#39;une commande fournisseur avec une remise ayant expiré plaçait la commande au montant total et ne mettait pas à jour le total de la commande fournisseur. Désormais, le total de la commande fournisseur est mis à jour pour afficher le total correct.

![Correction d’un problème](../assets/fix.svg) un problème a été introduit dans la version 2.3.4 en raison duquel les attributs d’extension personnalisés n’étaient pas copiés de l’adresse du client vers l’adresse du devis. Ce problème a été résolu.

![Correction d’un problème](../assets/fix.svg) Une fois B2B installé, une erreur SQL s’affichait lors de l’affectation de catégories à des catalogues partagés. Ce problème a été résolu.

![Problème résolu](../assets/fix.svg) En raison d’une valeur de type de variable incorrecte, les administrateurs et administratrices ne pouvaient pas ajouter de produits configurables à une commande. Les listes déroulantes d’options ne sont pas renseignées. Cette fonctionnalité fonctionne désormais correctement.

![Correction d’un problème](../assets/fix.svg) Auparavant, lors de la modification des autorisations de catégorie pour le groupe Non connecté , une erreur se produisait lors de l’enregistrement des modifications. Ce problème a été résolu.

![Correction d’un problème](../assets/fix.svg) Un correctif est ajouté pour permettre aux administrateurs de magasin d’ajouter des produits à une commande qui ne se trouvent pas dans le catalogue partagé. Auparavant, un message d’erreur s’affichait lors de l’ajout d’un élément qui ne figurait pas dans le catalogue.

![Problème résolu ](../assets/fix.svg) [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} Auparavant, après avoir exécuté la commande `php bin/magento indexer:set-dimensions-mode catalog_product_price website` et tenté de créer un catalogue partagé, une erreur se produisait. Ce problème a été résolu.

![Correction d’un problème](../assets/fix.svg) Lors de l’ajout d’une entreprise et de l’affectation de l’administrateur de l’entreprise à un site web non par défaut, le mauvais ID de site était envoyé, ce qui provoquait une erreur. Ce problème a été résolu.

![Problème résolu](../assets/fix.svg) Auparavant, après le déplacement d’un client vers un autre groupe de clients, l’ajout d’un produit à une commande à l’aide de l’option _Commande rapide_ échouait avec une erreur. Ce problème a été résolu.

![Correction d’un problème](../assets/fix.svg) Auparavant, lors d’une tentative d’extraction à l’aide de l’API Web avec un guillemet B2B, une valeur incorrecte était envoyée à l’API, ce qui provoquait une erreur. Ce problème a été résolu.

![Problème corrigé](../assets/fix.svg) Auparavant, lorsque vous définissiez une entreprise sur « Active » via l’API, une erreur se produisait. Ce problème a été résolu.

![Correction d’un problème](../assets/fix.svg) En raison d’une balise `form` inutile, la page de commande était automatiquement actualisée lorsque vous avez appuyé sur Entrée après avoir modifié les frais d’expédition proposés. Ce problème a été résolu.

![Problème résolu](../assets/fix.svg) Auparavant, lorsque vous définissiez une limite d’affichage de produit sur une page de catalogue et que cette limite était inférieure au nombre total de produits, une erreur se produisait. Cette fonctionnalité fonctionne désormais comme prévu.

![Correction d’un problème](../assets/fix.svg) Auparavant, lors du changement d’administrateur d’une société, l’adresse d’administrateur d’origine était copiée sur le nouvel administrateur, lui donnant deux adresses. Désormais, seule l’adresse correcte est ajoutée.

![Problème résolu](../assets/fix.svg) Auparavant, l’utilisation de l’API pour enregistrer un élément de devis lorsque Git est défini sur « Autorisé et informer le client » échouait. Cet appel API fonctionne désormais comme prévu.

![Problème résolu](../assets/fix.svg) La taxe fixe sur les produits s&#39;affiche désormais sur la page des détails des devis.

![Problème résolu](../assets/fix.svg) Auparavant, cliquer sur une pièce jointe dans l’onglet Commentaires de la page Mes devis ne téléchargeait pas le fichier. Ce comportement fonctionne désormais comme prévu.

### Problèmes connus

- Adobe Commerce renvoie une exception lors de la mise à niveau vers B2B 1.2.0 dans un déploiement multisite. Lors de `setup:upgrade`’exécution, cette erreur se produit sur le module `PurchaseOrder` : `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Solution** : installez l’interface `B2B-716 Add NonTransactionableInterface` au correctif logiciel du correctif de données `InitPurchaseOrderSalesSequence`, désormais disponible à partir de la section **Mon compte** > **Téléchargements** de `magento.com`.
- Si un code escompte expire avant l&#39;approbation d&#39;une commande, la commande continue d&#39;afficher le montant escompté, mais une fois la commande approuvée, elle est placée au total non escompté. **Solution** : installez le correctif `B2B-709 Purchase Order Discount patch` pour ce problème, qui est désormais disponible à partir de la section **Mon compte** > **Téléchargements** de `magento.com`.
- Si des articles d&#39;une commande fournisseur sont en rupture de stock ou en quantité insuffisante lors de la conversion de la commande fournisseur en commande réelle, une erreur se produit. Si les reliquats sont activés, la commande est traitée normalement.
