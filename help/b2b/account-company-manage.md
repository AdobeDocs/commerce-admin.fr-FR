---
title: Gestion des comptes d’entreprise
description: Découvrez comment gérer les comptes d’entreprise de votre boutique Adobe Commerce à l’aide de la page Entreprises et des outils disponibles dans la grille.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 0%

---

# Gestion des comptes d’entreprise

La page _[!UICONTROL Companies]_&#x200B;répertorie tous les comptes d’entreprise en cours, quel que soit leur état. Toutes les demandes en attente d’approbation apparaissent en haut de la liste.

![Grille d’entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Utilisez le contrôle *[!UICONTROL Columns]* pour personnaliser les colonnes affichées dans la grille. Personnalisez les entreprises affichées dans la vue à l’aide des fonctionnalités de recherche et de filtrage.

- Recherchez des entreprises dans la grille **Entreprises** à l’aide de _[!UICONTROL Search]_. La recherche indexe les colonnes **Nom de la société**&#x200B;et **Parent**.

- Personnalisez la vue pour inclure les enregistrements qui répondent à des critères spécifiques à l’aide de [!UICONTROL Filter]. Par exemple, si le site B2B est configuré pour gérer les comptes d’entreprise uniques et les [hiérarchies d’entreprise](manage-companies.md), vous pouvez filtrer par `[!UICONTROL Company Type - Company]` pour n’afficher que les sociétés uniques, ou par `[!UICONTROL Company Type - Parent]` pour n’afficher que la société mère pour chaque hiérarchie.

Appliquez une action à plusieurs enregistrements d’entreprise à l’aide du contrôle _[!UICONTROL Actions]_&#x200B;situé au-dessus de la grille. Par exemple, plutôt que d’approuver chaque demande d’entreprise, vous pouvez sélectionner plusieurs demandes pour activer les comptes en une seule action. Les actions disponibles dépendent des [autorisations](../systems/permissions.md) pour le rôle attribué à votre compte utilisateur d’administrateur.

## Ressources relatives aux rôles de l’entreprise

Les paramètres [Role Resources](../systems/permissions-user-roles.md#role-resources) déterminent la capacité à :

- Ajout d’une société
- Suppression d’une société
- Appliquer le remboursement du solde
- Affichage des entreprises

Ces ressources de rôle doivent être définies pour le [rôle d’utilisateur](../systems/permissions-user-roles.md) attribué au compte d’utilisateur administrateur.

## Gestion des comptes d’entreprise à partir de la grille Entreprises

Affichez et gérez les comptes utilisateur des entreprises dans le menu Admin en sélectionnant **[!UICONTROL Customers]** > **[!UICONTROL Companies]** pour ouvrir la page *[!UICONTROL Companies]*.

Vous pouvez gérer les comptes individuellement ou en groupes.

- Pour afficher ou modifier les paramètres de configuration d’un compte d’entreprise individuel, sélectionnez **[!UICONTROL Edit]** dans la colonne **[!UICONTROL Action]** pour l’enregistrement du compte d’entreprise.

  ![Sélectionner l’action à appliquer aux entreprises sélectionnées](assets/companies-change-settings-edit-selection.png){width="675" zoomable="yes"}

- Affichez ou modifiez un groupe de comptes d’entreprise sélectionnés à l’aide des options disponibles dans le contrôle [!UICONTROL Actions]** au-dessus de la grille.

  ![Sélectionner l’action à appliquer aux entreprises sélectionnées](assets/companies-change-settings-mass-action-selection.png){width="675" zoomable="yes"}

Consultez les sections suivantes pour obtenir des instructions sur l’application de chaque action.

### Activation des comptes d’entreprise

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Set Active]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

### Définir actif/inactif

Les clients disposant de comptes inactifs ne peuvent pas se connecter ou effectuer des achats sur leur compte. Il existe deux méthodes pour définir un compte client comme actif ou inactif :

Méthode 1 : **à partir de la grille Clients**

1. Sur la barre latérale _Admin_, accédez à [!UICONTROL **Customers**] > [!UICONTROL **Tous les clients**].

1. Dans le menu **[!UICONTROL Actions]**, sélectionnez l’une des options suivantes :

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Lorsque vous y êtes invité, sélectionnez **[!UICONTROL OK]** pour appliquer la modification.

Méthode 2 : **à partir de la page de modification du compte**

1. Sur la barre latérale _Admin_, accédez à [!UICONTROL **Customers**] > [!UICONTROL **Tous les clients**].

1. Dans la grille, recherchez l’enregistrement du client à modifier.

1. Dans la colonne _Actions_ à l’extrême droite, sélectionnez [!UICONTROL **Modifier**].

1. Sélectionnez l’onglet [!UICONTROL **Informations sur le compte**].

1. Définissez [!UICONTROL **Customer Active**] sur `Yes` ou `No`.

1. Cliquez sur [!UICONTROL **Enregistrer le client**].

### Bloquer les comptes d’entreprise

Les utilisateurs associés à un compte de société bloqué peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. Une société dont le compte n’est pas en règle peut être temporairement bloquée jusqu’à ce que l’affaire soit résolue.

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Block]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

### Suppression de comptes d’entreprise

Les comptes d’entreprise supprimés ne peuvent pas être restaurés. L’état des comptes d’utilisateurs associés à l’entreprise est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système.

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Delete]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

### Modification des paramètres de l’entreprise

Mettez à jour la configuration [Paramètres avancés](account-company-create.md#advanced-settings) pour appliquer les mêmes paramètres à plusieurs entreprises sélectionnées sur la *grille Entreprises*.

>[!NOTE]
>
>Gérez la configuration des paramètres avancés d’une entreprise avec un parent et des entreprises enfants associées à partir de la [vue Hiérarchie de l’entreprise](manage-company-hierarchy.md#change-company-settings).

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Change company settings]**.

   Sur le formulaire *[!UICONTROL Change company settings]*, les paramètres de configuration initiaux sont définis sur les valeurs par défaut.

1. Pour chaque paramètre de configuration à modifier, cochez la case **[!UICONTROL Change]** pour activer le paramètre. Mettez ensuite le paramètre à jour selon vos besoins.

   ![Modification des paramètres de la société pour plusieurs entreprises](assets/companies-change-advanced-settings-action.png){width="675" zoomable="yes"}

1. Après la mise à jour des paramètres de configuration, sélectionnez **[!UICONTROL Apply Changes]**.

1. Lorsque vous y êtes invité, sélectionnez **[!UICONTROL Change settings]** pour mettre à jour la configuration des entreprises sélectionnées.

>[!TIP]
>
>Vous pouvez modifier la configuration avancée des paramètres d’une seule entreprise en sélectionnant **[!UICONTROL Edit]** dans la colonne **[!UICONTROL Action]** pour l’enregistrement du compte de l’entreprise.

### Convertir la devise de crédit

Le crédit figurant dans les comptes des sociétés sélectionnées est converti au taux actuel de la devise sélectionnée.

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Convert Currency]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

1. Sélectionnez le **[!UICONTROL Credit Currency]** à utiliser pour les comptes d’entreprise sélectionnés.

   Les montants sont recalculés en fonction des taux de conversion actuels, le cas échéant. Si elle n’est pas disponible, vous pouvez saisir manuellement des taux de conversion personnalisés. Le système affiche autant de calculs de conversion que nécessaire pour la devise de crédit utilisée par les sociétés sélectionnées.

1. Cliquez sur **[!UICONTROL Proceed]** pour terminer la conversion.

## Modification d’un compte d’entreprise

Méthode 1 : **Modification rapide**

1. Dans la première colonne, cochez la case du compte de la société à éditer.

1. Dans la commande **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Edit]**.

   Chaque valeur pouvant être mise à jour apparaît dans une zone de texte.

   ![Modification rapide pour un compte d’entreprise](./assets/companies-grid-quick-edit.png){width="675" zoomable="yes"}

1. Mettez à jour l’une des valeurs suivantes si nécessaire :

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Cliquez sur **[!UICONTROL Save]**.

Méthode 2 : **Modification complète**

1. Dans la grille, recherchez l’enregistrement de la société à éditer.

1. Sélectionnez **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Apportez les modifications nécessaires aux informations de l’entreprise.

   Pour consulter la description des champs, voir [Création d’un compte d’entreprise](account-company-create.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Attribution d’un représentant commercial

Le représentant commercial est un [utilisateur administrateur](../systems/permissions.md) qui se voit attribuer le rôle de point de contact d’un compte de société et qui reçoit tous les [ messages électroniques](../b2b/enable-basic-features.md#configure-company-email-options) automatisés liés à la société. Un seul représentant commercial peut être affecté par compte de société, mais un seul représentant commercial peut gérer plusieurs comptes de société. Le compte d’utilisateur administrateur par défaut est attribué en tant que représentant commercial, sauf si un autre utilisateur administrateur est affecté.

Le nom et l’adresse électronique du représentant commercial affecté sont visibles par les membres de la société à partir de la page du compte et des devis de la société.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille et ouvrez-la en mode d’édition.

1. Définissez **[!UICONTROL Sales Representative]** sur l’utilisateur administrateur que vous souhaitez affecter comme point de contact de la société.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   Le représentant commercial affecté reçoit une notification par courrier électronique de l’affectation.

## Mise à jour d’un profil d’entreprise

Le profil de l’entreprise peut être conservé à partir du storefront par l’administrateur de l’entreprise, ainsi que depuis l’administrateur par un administrateur de magasin.

![Profil de la société](./assets/company-update.png){width="700" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Mettez à jour les valeurs de champ dans chaque section selon les besoins à l’aide des descriptions de champ à titre de référence.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Démonstration du compte de la société

Pour en savoir plus sur la gestion des comptes d’entreprise, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3410771?quality=12&learn=on&captions=fre_fr)

## Gestion des entreprises

Une fois une société créée, les utilisateurs administrateurs disposant des autorisations appropriées peuvent utiliser la section [!UICONTROL Company Hierarchy] pour créer une organisation de société mère en modifiant la société mère désignée et en affectant les sociétés associées.

Si une société a été ajoutée à une hiérarchie, la grille [!UICONTROL Company Hierarchy] affiche la société mère et toutes les sociétés affectées dans la grille.

Voir [Gérer la hiérarchie de l’entreprise](manage-company-hierarchy.md) pour plus d’informations.

## Options et colonnes de l’entreprise

Les sections suivantes contiennent une référence pour les actions, options et informations affichées disponibles pour la gestion des comptes d’entreprise.

### Options de contrôle des actions

| Option | Description |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Définit l’état de tous les enregistrements d’entreprise sélectionnés sur `Active`. Les administrateurs d’entreprise reçoivent des instructions pour définir leurs mots de passe afin qu’ils puissent accéder à leurs comptes et gérer leurs entreprises à partir du storefront. |
| [!UICONTROL Block] | Limite les comptes d’entreprise qui ne sont pas en règle, tout en préservant le compte. Les membres de la société peuvent se connecter et accéder au catalogue, mais ils ne peuvent pas passer de commandes pour le compte de la société. |
| [!UICONTROL Delete] | Supprime les comptes d’entreprise sélectionnés. L’état des comptes d’utilisateurs associés à une société supprimée est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système. |
| [!UICONTROL Edit] | Permet de modifier certaines valeurs de l’enregistrement d’entreprise sélectionné à partir de la grille. Par défaut, les valeurs Nom de la société, Adresse électronique de la société et Numéro de téléphone sont disponibles pour modification rapide. |
| [!UICONTROL Change company settings] | Ouvre le formulaire *Modifier les paramètres de la société* pour mettre à jour la configuration [Paramètres avancés](account-company-create.md#advanced-settings) et appliquer les modifications aux entreprises sélectionnées. |
| [!UICONTROL Convert Credit] | Convertit le crédit sur compte des sociétés sélectionnées en fonction des taux de la monnaie spécifiée. |

{style="table-layout:auto"}

### Descriptions des colonnes


#### Disposition des colonnes par défaut

| Colonne | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Les cases à cocher utilisées pour sélectionner les enregistrements d’entreprise qui doivent faire l’objet d’une action ou utiliser le contrôle de sélection dans l’en-tête de colonne pour sélectionner/désélectionner tout. |
| [!UICONTROL ID] | Identifiant numérique unique attribué lors de l’envoi de la demande de création d’une société. |
| [!UICONTROL Company Name] | Le nom de la société est saisi lors de la création du compte de la société et peut être une version abrégée du nom légal complet. |
| [!UICONTROL Company Type] | Type de [company](manage-companies.md). Options : <br/>**[!UICONTROL Company]**- Par défaut, de nouvelles entreprises sont créées en tant que sociétés uniques.<br/>**[!UICONTROL Parent]** - La société est une société mère d’autres sociétés. <br/>**[!UICONTROL Child]**- Cette société est liée à une société mère. |
| [!UICONTROL Parent] | Affiche la société mère pour cette ligne de société spécifique. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |
| [!UICONTROL Country] | Le pays dans lequel la société est enregistrée pour mener une activité commerciale. |
| [!UICONTROL State Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Group/Shared Catalog] | Le nom de la colonne varie selon que le catalogue partagé est activé ou non dans la configuration. Options : <br/>**[!UICONTROL Customer Group]**- Si le catalogue partagé n’est pas activé dans la configuration, indique le nom du [groupe de clients](../customers/customer-groups.md) auquel appartient l’entreprise.<br/>**[!UICONTROL Shared Catalog]** - Si le catalogue partagé est activé dans la configuration, indique le nom du catalogue partagé attribué au client. |
| [!UICONTROL Outstanding Balance] | Le solde impayé sur le compte de la société. la colonne est vide si la société n’a pas d’historique de crédit et que sa limite de crédit est zéro. |
| [!UICONTROL Company Admin] | Prénom et nom de l’administrateur de la société. |
| [!UICONTROL Job Title] | Fonction de l’administrateur de l’entreprise. |
| [!UICONTROL Work Phone Number] | Numéro de téléphone de travail de l’administrateur de la société. |
| [!UICONTROL Email] | Adresse électronique de l’administrateur de la société. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Ouvre le compte de la société en mode d’édition. |

{style="table-layout:auto"}

#### Colonnes supplémentaires

Les colonnes suivantes sont disponibles en modifiant la [mise en page des colonnes](../getting-started/admin-grid-controls.md) de la grille.

| Colonne | Description |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Nom légal complet de la société. |
| [!UICONTROL Street Address] | Adresse de la rue où l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL ZIP] | Code postal où l’entreprise est enregistrée pour exercer ses activités. |
| [!UICONTROL Reseller ID] | Numéro de revente attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL VAT/TAX ID] | Numéro de la [taxe sur la valeur ajoutée](../stores-purchase/vat.md) qui est attribué à la société par certaines juridictions à des fins de déclaration fiscale. Pour configurer l’ID de TVA/TAX du client pour qu’il s’affiche dans le storefront, voir [Créer des options de compte](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | Limite de crédit étendue au compte de la société. |
| [!UICONTROL Credit Currency] | Devise acceptée par le magasin pour les achats à crédit de la société. |
| [!UICONTROL Status] | Indique le [statut](account-company-approve.md) du compte de la société. Options : <br/>**[!UICONTROL Active]**- Le compte de la société est approuvé par l’administrateur du magasin. L’administrateur de la société et les membres associés peuvent se connecter au compte à partir du storefront et effectuer des achats.<br/>**[!UICONTROL Pending Approval]** - Une demande d’ouverture d’un compte de société a été envoyée, mais n’est pas encore approuvée par l’administrateur du magasin. <br/>**[!UICONTROL Rejected]**- Une demande d’ouverture d’un compte de société a été envoyée, mais n’a pas été approuvée par l’administrateur du magasin. Les informations de connexion initiales utilisées pour envoyer la demande sont bloquées.<br/>**[!UICONTROL Blocked]** - Les membres de la société peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. L’administrateur du magasin peut bloquer un compte d’entreprise qui n’est pas en règle. Le bloc du compte peut être supprimé à tout moment par l’administrateur du magasin. |
| [!UICONTROL Gender] | Genre de l’administrateur de l’entreprise. Options : homme/femme/non spécifié |
| [!UICONTROL Comment] | Remarques sur le compte de l’entreprise à titre de référence et visibles uniquement par l’administrateur. |

{style="table-layout:auto"}

### Barre de boutons

| Bouton | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Renvoie à la page Entreprises sans enregistrer les modifications. |
| [!DNL Delete Company] | Supprime le compte de la société. L’état des comptes d’utilisateurs associés à l’entreprise est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système. |
| [!DNL Reset] | Restaure les valeurs d’origine dans tous les champs avec des modifications non enregistrées. |
| [!DNL Reimburse Balance] | Permet à l&#39;administrateur de rembourser le solde du crédit de magasin, référencé par le numéro du bon de commande. |
| [!DNL Save] | Enregistre les modifications apportées à l’entreprise et conserve le profil ouvert. |
| [!UICONTROL Save & Close] | Enregistre les modifications apportées à l’entreprise et ferme le profil. |

{style="table-layout:auto"}

### Descriptions des champs

| Champ | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Le nom de la société est saisi lors de la création du compte de la société et peut être une version abrégée du nom légal complet. |
| [!UICONTROL Status] | Indique le [statut](account-company-approve.md) du compte de la société. Options : <br/>**[!UICONTROL Active]**- Le compte de la société est approuvé par l’administrateur du magasin. L’administrateur de la société et les membres associés peuvent se connecter au compte à partir du storefront et effectuer des achats.<br/>**[!UICONTROL Pending Approval]** - Une demande d’ouverture d’un compte de société a été envoyée, mais n’est pas encore approuvée par l’administrateur du magasin. <br/>**[!UICONTROL Rejected]**- Une demande d’ouverture d’un compte de société a été envoyée, mais n’a pas été approuvée par l’administrateur du magasin. Les informations de connexion initiales utilisées pour envoyer la demande sont bloquées.<br/>**[!UICONTROL Blocked]** - Les membres de la société peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. L’administrateur du magasin peut bloquer un compte d’entreprise qui n’est pas en règle. Le bloc du compte peut être supprimé à tout moment par l’administrateur du magasin. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Sales Representative] | Utilisateur administrateur qui est le contact principal pour le compte de la société. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Champ | Description |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Nom légal complet de la société. |
| [!UICONTROL VAT / TAX ID] | Numéro de taxe ou de [taxe sur la valeur ajoutée](../stores-purchase/vat.md) attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL Reseller ID] | Numéro de revente attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL Comment] | Ces notes sur le compte de la société sont à titre de référence et ne sont visibles que par l’administrateur. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Colonnes | Description |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Numéro d’ID de la société. |
| [!UICONTROL Company Name] | Nom complet de la société. <br/>Un `current company indicator` apparaît dans la ligne de l’entreprise en cours de modification. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |
| [!UICONTROL State/Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Customer Group] | (Admin uniquement) Indique le [groupe de clients](../customers/customer-groups.md) ou le [catalogue partagé](catalog-shared.md) affecté à la société. |
| [!UICONTROL Company Admin] | Nom complet de l’administrateur de la société. |
| [!UICONTROL Action] | Liste des actions possibles pour cette ligne d’entreprise. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Colonnes | Description |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Adresse de la rue où l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Country] | Le pays dans lequel la société est enregistrée pour mener une activité commerciale. |
| [!UICONTROL State/Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL ZIP/Postal Code] | Code postal où l’entreprise est enregistrée pour exercer ses activités. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Champ | Description |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Définissez la [portée du site web](../getting-started/websites-stores-views.md) pour le compte de la société. La valeur par défaut est *[!UICONTROL Main Website]*. |
| [!UICONTROL Job Title] | Titre de l’administrateur de la société qui gère le compte de la société. |
| [!UICONTROL Work Phone Number] | Numéro de téléphone de l’administrateur de l’entreprise qui gère le compte de l’entreprise. |
| [!UICONTROL Email] | L’adresse électronique de l’administrateur de l’entreprise peut être identique à celle de l’entreprise. Si une autre adresse électronique est saisie, un compte individuel distinct est créé pour l’administrateur de la société en plus du compte de la société. |
| [!UICONTROL Prefix] | Le cas échéant, le préfixe associé au nom de l’administrateur de l’entreprise (par exemple `Mr.`, `Ms.`, `Mrs.` ou `Dr.`). Selon le paramétrage, le champ de saisie peut être un champ de texte ou une liste. |
| [!UICONTROL First Name] | Prénom de l’administrateur de la société. |
| [!UICONTROL Middle Name/Initial] | Nom intermédiaire ou initial de l’administrateur de la société. |
| [!UICONTROL Last Name] | Nom de l’administrateur de la société. |
| [!UICONTROL Suffix] | Le cas échéant, le suffixe associé au nom de l’administrateur de l’entreprise (par exemple `Jr.`, `Sr.` ou `III`). Selon le paramétrage, le champ de saisie peut être un champ de texte ou une liste. |
| [!UICONTROL Gender] | Genre de l’administrateur de l’entreprise. Options : `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Définissez la vue d’ensemble à utiliser lors de l’envoi de l’e-mail de bienvenue au nouvel administrateur de la société si vous ne souhaitez pas utiliser le *[!UICONTROL Default Store View]*. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Champ | Description |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | Devise acceptée par le magasin pour les achats à crédit de la société. |
| [!UICONTROL Credit Limit] | Limite de crédit étendue au compte de la société. |
| [!UICONTROL Allow to Exceed Credit Limit] | Indique si l’entreprise est autorisée à dépasser la limite de crédit. Options : Oui/Non |
| [!UICONTROL Reason for Change] | Note qui explique les circonstances dans lesquelles la société peut ou ne peut pas dépasser la limite de crédit. Ce champ est actif uniquement si l’autorisation de dépasser la limite de crédit change. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Champ | Description |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Indique le [groupe de clients](../customers/customer-groups.md) ou le [catalogue partagé](catalog-shared.md) attribué à la société. |
| [!UICONTROL Allow Quotes] | Détermine si les membres de la société peuvent préparer et soumettre des citations négociables pour le compte de la société. |
| [!UICONTROL Enable Purchase Orders] | Détermine si les commandes d’achat sont autorisées pour la société. Pour que les commandes d’achat fonctionnent pour les comptes des membres de la société, l’administrateur de la société doit également activer cette fonction sur le storefront. |
| [!UICONTROL Applicable Payment Methods] | Indique les modes de paiement disponibles pour les achats de l’entreprise. Options : `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Administrateur uniquement) Devient actif si des méthodes de paiement spécifiques sont indiquées. Pour sélectionner plusieurs modes de paiement, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option. |

{style="table-layout:auto"}
