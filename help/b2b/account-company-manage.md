---
title: Gestion des comptes d’entreprise
description: Découvrez la page Entreprises et les outils disponibles dans la grille qui vous aident à gérer les comptes d’entreprise pour votre boutique Adobe Commerce.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: 1123cf4b257a83a61914c378104c43e952512e7d
workflow-type: tm+mt
source-wordcount: '2500'
ht-degree: 0%

---

# Gestion des comptes d’entreprise

La variable _[!UICONTROL Companies]_répertorie tous les comptes d’entreprise en cours, quel que soit leur état. Toutes les demandes en attente d’approbation apparaissent en haut de la liste. Le standard [contrôles sur le lieu de travail](../getting-started/admin-workspace.md) peut être utilisé pour filtrer la liste, modifier la variable [mise en page des colonnes](../getting-started/admin-grid-controls.md), enregistrez les vues ou exportez des données.

La variable _[!UICONTROL Actions]_Le contrôle au-dessus de la grille peut être utilisé pour appliquer une action à plusieurs enregistrements d’entreprise. Par exemple, plutôt que d’approuver chaque demande d’entreprise, vous pouvez sélectionner plusieurs demandes et activer les comptes en une seule action. Les actions disponibles dépendent de la variable [permissions](../systems/permissions.md) pour le rôle affecté à votre compte utilisateur d’administrateur.

Utilisez la variable _[!UICONTROL Search]_pour rechercher des sociétés dans la variable **Entreprises**grille par mot-clé. Elle trouvera l’entreprise en recherchant le mot-clé spécifié dans la variable **Nom de la société**et **Parent**colonnes. Vous pouvez filtrer par **Type d’entreprise**afficher les sociétés mères et leurs sociétés associées, ou uniquement les entreprises filles.

![Grille des entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Ressources relatives aux rôles de l’entreprise

La variable [Ressources de rôle](../systems/permissions-user-roles.md#role-resources) les paramètres déterminent la possibilité de :

- Ajout d’une société
- Suppression d’une société
- Appliquer le remboursement du solde
- Affichage des entreprises

Ces ressources de rôle doivent être définies pour la variable [Rôle d’utilisateur](../systems/permissions-user-roles.md) affecté au compte utilisateur Admin.

## Application d’une action

Les actions suivantes peuvent être appliquées à un ou plusieurs enregistrements.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Dans la première colonne de la grille, cochez la case de chaque enregistrement que vous souhaitez mettre à jour et suivez les instructions de l&#39;action que vous souhaitez appliquer :

### Activation des comptes d’entreprise

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Set Active`.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

### Définir actif/inactif

Les clients disposant de comptes inactifs ne peuvent pas se connecter ou effectuer des achats sur leur compte. Il existe deux méthodes pour définir un compte client comme actif ou inactif :

Méthode 1 : **Depuis la grille des clients**

1. Sur le _Administration_ barre latérale, accédez à [!UICONTROL **Clients**] > [!UICONTROL **Tous les clients**].

1. Définissez la variable [!UICONTROL **Actions**] à l’une des options suivantes :

   - `Active`
   - `Inactive`

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

Méthode 2 : **Dans la page de modification du compte**

1. Sur le _Administration_ barre latérale, accédez à [!UICONTROL **Clients**] > [!UICONTROL **Tous les clients**].

1. Dans la grille, recherchez l’enregistrement du client à modifier.

1. Dans le _Actions_ à l’extrême droite, cliquez sur [!UICONTROL **Modifier**].

1. Sélectionnez la variable [!UICONTROL **Informations du compte**] .

1. Définir [!UICONTROL **Client actif**] to `Yes` ou `No`.

1. Cliquez sur [!UICONTROL **Enregistrer le client**].

### Bloquer les comptes d’entreprise

Les utilisateurs associés à un compte de société bloqué peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. Une société dont le compte n’est pas en règle peut être temporairement bloquée jusqu’à ce que l’affaire soit résolue.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Block`.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

### Suppression de comptes d’entreprise

Les comptes d’entreprise supprimés ne peuvent pas être restaurés. L’état des comptes d’utilisateurs associés à la société est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Delete`.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

### Convertir la devise de crédit

Le crédit figurant dans les comptes des sociétés sélectionnées est converti au taux actuel de la devise sélectionnée.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Convert Currency`.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

1. Choisissez la **[!UICONTROL Credit Currency]** à utiliser pour les comptes d’entreprise sélectionnés.

   Les montants sont recalculés en fonction des taux de conversion actuels, le cas échéant. Si elle n’est pas disponible, vous pouvez saisir manuellement des taux de conversion personnalisés. Le système affiche autant de calculs de conversion que nécessaire pour la devise de crédit utilisée par les sociétés sélectionnées.

1. Cliquez sur **[!UICONTROL Proceed]** pour terminer la conversion.

### Modification d’un compte d’entreprise

Méthode 1 : **Modification rapide**

1. Dans la première colonne, cochez la case du compte de la société à éditer.

1. Définissez la variable **[!UICONTROL Actions]** colonne à `Edit`.

   Chaque valeur pouvant être mise à jour apparaît dans une zone de texte.

   ![Modification rapide pour un compte d’entreprise](./assets/companies-grid-quick-edit.png){width="700" zoomable="yes"}

1. Mettez à jour l’une des valeurs suivantes si nécessaire :

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Cliquez sur **[!UICONTROL Save]**.

Méthode 2 : **Modification complète**

1. Dans la grille, recherchez l’enregistrement de la société à éditer.

1. Cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Apportez les modifications nécessaires aux informations de l’entreprise.

Pour consulter la description des champs, reportez-vous à la section [Création d’un compte d’entreprise](account-company-create.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Attribution d’un représentant commercial

Le représentant commercial est un [Utilisateur administrateur](../systems/permissions.md) qui est désigné comme point de contact pour un compte d’entreprise et reçoit toutes les [messages électroniques](../b2b/enable-basic-features.md#configure-company-email-options) en rapport avec la société. Un seul représentant commercial peut être affecté par compte de société, mais un seul représentant commercial peut gérer plusieurs comptes de société. Le compte d’utilisateur administrateur par défaut est attribué en tant que représentant commercial, sauf si un autre utilisateur administrateur est affecté.

Le nom et l’adresse électronique du représentant commercial affecté sont visibles par les membres de la société à partir de la page du compte et des devis de la société.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille et ouvrez-la en mode d’édition.

1. Définir **[!UICONTROL Sales Representative]** à l’utilisateur administrateur que vous souhaitez affecter en tant que point de contact de la société.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   Le représentant commercial affecté reçoit une notification par courrier électronique de l’affectation.

## Mise à jour d’un profil d’entreprise

Le profil de l’entreprise peut être conservé à partir du storefront par l’administrateur de l’entreprise, ainsi que depuis l’administrateur par un administrateur de magasin.

![Profil d’entreprise](./assets/company-update.png){width="700" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la grille, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Mettez à jour les valeurs de champ dans chaque section selon les besoins à l’aide des descriptions de champ à titre de référence.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Démonstration du compte de la société

Pour en savoir plus sur la gestion des comptes d’entreprise, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Gestion des entreprises

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"}

Une fois une société créée, les utilisateurs administrateurs disposant des autorisations appropriées peuvent utiliser la variable [!UICONTROL Company Hierarchy] pour créer une organisation de société mère en modifiant la société mère désignée et en affectant des sociétés liées.

Si une société a été ajoutée à une hiérarchie, la variable [!UICONTROL Company Hierarchy] grid affiche la société mère et toutes les entreprises affectées dans la grille.

Voir [Gérer la hiérarchie de l’entreprise](assign-companies.md) pour plus d’informations.

## Options et colonnes de l’entreprise

Les sections suivantes contiennent une référence pour les actions, options et informations affichées disponibles pour la gestion des comptes d’entreprise.

### Options de contrôle des actions

| Option | Description |
|--- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Définit l’état de tous les enregistrements d’entreprise sélectionnés sur `Active`. Les administrateurs d’entreprise reçoivent des instructions pour définir leurs mots de passe afin qu’ils puissent accéder à leurs comptes et gérer leurs entreprises à partir du storefront. |
| [!UICONTROL Block] | Limite les comptes d’entreprise qui ne sont pas en règle, tout en préservant le compte. Les membres de la société peuvent se connecter et accéder au catalogue, mais ils ne peuvent pas passer de commandes pour le compte de la société. |
| [!UICONTROL Delete] | Supprime les comptes d’entreprise sélectionnés. L’état des comptes d’utilisateurs associés à une société supprimée est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système. |
| [!UICONTROL Edit] | Permet de modifier certaines valeurs de l’enregistrement d’entreprise sélectionné à partir de la grille. Par défaut, les valeurs Nom de la société, Adresse électronique de la société et Numéro de téléphone sont disponibles pour modification rapide. |
| [!UICONTROL Convert Credit] | Convertit le crédit sur compte des sociétés sélectionnées en fonction des taux de la monnaie spécifiée. |

{style="table-layout:auto"}

### Descriptions des colonnes


#### Disposition des colonnes par défaut

| Colonne | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Les cases à cocher utilisées pour sélectionner les enregistrements d’entreprise qui doivent faire l’objet d’une action ou utiliser le contrôle de sélection dans l’en-tête de colonne pour sélectionner/désélectionner tout. |
| [!UICONTROL ID] | Identifiant numérique unique attribué lors de l’envoi de la demande de création d’une société. |
| [!UICONTROL Company Name] | Le nom de la société est saisi lors de la création du compte de la société et peut être une version abrégée du nom légal complet. |
| [!UICONTROL Company Type] | Le type de [société](manage-companies.md). Options : <br/>**[!UICONTROL Company]**- Par défaut, de nouvelles entreprises sont créées en tant que sociétés uniques.<br/>**[!UICONTROL Parent]** - La société est une société mère d’autres sociétés. <br/>**[!UICONTROL Child]**- Cette société est liée à une société mère. |
| [!UICONTROL Parent] | Affiche la société mère pour cette ligne de société spécifique. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |
| [!UICONTROL Country] | Le pays dans lequel la société est enregistrée pour mener une activité commerciale. |
| [!UICONTROL State Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Group/Shared Catalog] | Le nom de la colonne varie selon que le catalogue partagé est activé ou non dans la configuration. Options : <br/>**[!UICONTROL Customer Group]**- Si le catalogue partagé n’est pas activé dans la configuration, indique le nom de la variable [groupe de clients](../customers/customer-groups.md) à laquelle appartient la société.<br/>**[!UICONTROL Shared Catalog]** - Si le catalogue partagé est activé dans la configuration, indique le nom du catalogue partagé attribué au client. |
| [!UICONTROL Outstanding Balance] | Le solde impayé sur le compte de la société. la colonne est vide si la société n’a pas d’historique de crédit et que sa limite de crédit est zéro. |
| [!UICONTROL Company Admin] | Prénom et nom de l’administrateur de la société. |
| [!UICONTROL Job Title] | Fonction de l’administrateur de l’entreprise. |
| [!UICONTROL Email] | Adresse électronique de l’administrateur de la société. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Ouvre le compte de l’entreprise en mode d’édition. |

{style="table-layout:auto"}

#### Colonnes supplémentaires

Les colonnes suivantes sont disponibles en modifiant la variable [mise en page des colonnes](../getting-started/admin-grid-controls.md) de la grille.

| Colonne | Description |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Nom légal complet de la société. |
| [!UICONTROL Street Address] | Adresse de la rue où l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL ZIP] | Code postal où l’entreprise est enregistrée pour exercer ses activités. |
| [!UICONTROL Reseller ID] | Numéro de revente attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL VAT/TAX ID] | La variable [taxe sur la valeur ajoutée](../stores-purchase/vat.md) numéro qui est attribué à la société par certaines juridictions à des fins de déclaration fiscale. Pour configurer l’ID de TVA/TAX du client pour qu’il apparaisse dans le storefront, voir [Créer des options de compte](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | Limite de crédit étendue au compte de la société. |
| [!UICONTROL Credit Currency] | Devise acceptée par le magasin pour les achats à crédit de la société. |
| [!UICONTROL Status] | Indique que la variable [status](account-company-approve.md) du compte de la société. Options : <br/>**[!UICONTROL Active]**- Le compte de la société est approuvé par l’administrateur du magasin. L’administrateur de la société et les membres associés peuvent se connecter au compte à partir du storefront et effectuer des achats.<br/>**[!UICONTROL Pending Approval]** - Une demande d’ouverture d’un compte de société a été envoyée, mais n’est pas encore approuvée par l’administrateur du magasin. <br/>**[!UICONTROL Rejected]**- Une demande d’ouverture d’un compte de société a été envoyée, mais n’a pas été approuvée par l’administrateur du magasin. Les informations de connexion initiales utilisées pour envoyer la demande sont bloquées.<br/>**[!UICONTROL Blocked]** - Les membres de la société peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. L’administrateur du magasin peut bloquer un compte d’entreprise qui n’est pas en règle. Le bloc du compte peut être supprimé à tout moment par l’administrateur du magasin. |
| [!UICONTROL Gender] | Genre de l’administrateur de l’entreprise. Options : homme/femme/non spécifié |
| [!UICONTROL Comment] | Remarques sur le compte de l’entreprise à titre de référence et visibles uniquement par l’administrateur. |

{style="table-layout:auto"}

### Barre de boutons

| Bouton | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Renvoie à la page Entreprises sans enregistrer les modifications. |
| [!UICONTROL Login as Customer] | Permet à un utilisateur administrateur de [se connecter au storefront en tant que client](../customers/login-as-customer.md) et aide sur leurs commandes. |
| [!DNL Delete Company] | Supprime le compte de la société. L’état des comptes d’utilisateurs associés à la société est défini sur `Inactive` et l’ID de société est supprimé des profils des comptes d’utilisateurs. Les informations sur l’activité et les transactions de la société sont conservées dans le système. |
| [!DNL Reset] | Restaure les valeurs d’origine dans tous les champs avec des modifications non enregistrées. |
| [!DNL Reimburse Balance] | Permet à l&#39;administrateur de rembourser le solde du crédit de magasin, référencé par le numéro du bon de commande. |
| [!DNL Save] | Enregistre les modifications apportées à l’entreprise et conserve le profil ouvert. |
| [!UICONTROL Save & Close] | Enregistre les modifications apportées à l’entreprise et ferme le profil. |

{style="table-layout:auto"}

### Descriptions des champs

| Champ | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Le nom de la société est saisi lors de la création du compte de la société et peut être une version abrégée du nom légal complet. |
| [!UICONTROL Status] | Indique que la variable [status](account-company-approve.md) du compte de la société. Options : <br/>**[!UICONTROL Active]**- Le compte de la société est approuvé par l’administrateur du magasin. L’administrateur de la société et les membres associés peuvent se connecter au compte à partir du storefront et effectuer des achats.<br/>**[!UICONTROL Pending Approval]** - Une demande d’ouverture d’un compte de société a été envoyée, mais n’est pas encore approuvée par l’administrateur du magasin. <br/>**[!UICONTROL Rejected]**- Une demande d’ouverture d’un compte de société a été envoyée, mais n’a pas été approuvée par l’administrateur du magasin. Les informations de connexion initiales utilisées pour envoyer la demande sont bloquées.<br/>**[!UICONTROL Blocked]** - Les membres de la société peuvent se connecter et accéder au catalogue, mais ne peuvent pas effectuer d’achats. L’administrateur du magasin peut bloquer un compte d’entreprise qui n’est pas en règle. Le bloc du compte peut être supprimé à tout moment par l’administrateur du magasin. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Sales Representative] | Utilisateur administrateur qui est le contact principal pour le compte de la société. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Champ | Description |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Nom légal complet de la société. |
| [!UICONTROL VAT / TAX ID] | La taxe ou [taxe sur la valeur ajoutée](../stores-purchase/vat.md) numéro attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL Reseller ID] | Numéro de revente attribué à la société à des fins de déclaration fiscale. |
| [!UICONTROL Comment] | Ces notes sur le compte de la société sont à titre de référence et ne sont visibles que par l’administrateur. |
| **[!UICONTROL Legal Address]** |                                                                                                                            |
| [!UICONTROL Street Address] | Adresse de la rue où l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Country] | Le pays dans lequel la société est enregistrée pour mener une activité commerciale. |
| [!UICONTROL State/Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL ZIP/Postal Code] | Code postal où l’entreprise est enregistrée pour exercer ses activités. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"}

| Colonnes | Description |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Numéro d’ID de la société. |
| [!UICONTROL Company Name] | Nom complet de la société. <br/>A `current company indicator` apparaît dans la ligne de l’entreprise en cours d’édition. |
| [!UICONTROL Company Email] | Adresse électronique associée au compte de la société. |
| [!UICONTROL Phone Number] | Numéro de téléphone principal de la société. |
| [!UICONTROL State/Province] | État ou province dans lequel l’entreprise est enregistrée pour exercer une activité commerciale. |
| [!UICONTROL City] | Ville dans laquelle l’entreprise est enregistrée pour faire des affaires. |
| [!UICONTROL Customer Group] | (Administrateur uniquement) Indique la variable [groupe de clients](../customers/customer-groups.md) ou [catalogue partagé](catalog-shared.md) qui est affecté à la société. |
| [!UICONTROL Company Admin] | Nom complet de l’administrateur de la société. |
| [!UICONTROL Action] | Liste des actions possibles pour cette ligne d’entreprise. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Champ | Description |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Job Title] | Titre de l’administrateur de la société qui gère le compte de la société. |
| [!UICONTROL Email] | L’adresse électronique de l’administrateur de l’entreprise peut être identique à celle de l’entreprise. Si une autre adresse électronique est saisie, un compte individuel distinct est créé pour l’administrateur de la société en plus du compte de la société. |
| [!UICONTROL Prefix] | Le cas échéant, le préfixe associé au nom de l’administrateur de l’entreprise (tel que `Mr.`, `Ms.`, `Mrs.`, ou `Dr.`). Selon le paramétrage, le champ de saisie peut être un champ de texte ou une liste. |
| [!UICONTROL First Name] | Prénom de l’administrateur de la société. |
| [!UICONTROL Middle Name/Initial] | Nom intermédiaire ou initial de l’administrateur de la société. |
| [!UICONTROL Last Name] | Nom de l’administrateur de la société. |
| [!UICONTROL Suffix] | Le cas échéant, suffixe associé au nom de l’administrateur de l’entreprise (tel que `Jr.`, `Sr.`, ou `III`). Selon le paramétrage, le champ de saisie peut être un champ de texte ou une liste. |
| [!UICONTROL Gender] | Genre de l’administrateur de l’entreprise. Options : `Male` / `Female` / `Not Specified` |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Champ | Description |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | Devise acceptée par le magasin pour les achats à crédit de la société. |
| [!UICONTROL Credit Limit] | Limite de crédit étendue au compte de la société. |
| [!UICONTROL Allow to Exceed Credit Limit] | Indique si l’entreprise est autorisée à dépasser la limite de crédit. Options : Oui/Non |
| [!UICONTROL Reason for Change] | Note expliquant pourquoi la société est autorisée ou non à dépasser la limite de crédit. Ce champ est actif uniquement si l’autorisation de dépasser la limite de crédit change. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Champ | Description |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Indique que la variable [groupe de clients](../customers/customer-groups.md) ou [catalogue partagé](catalog-shared.md) qui est affecté à la société. |
| [!UICONTROL Allow Quotes] | Détermine si les membres de la société peuvent préparer et soumettre des citations négociables pour le compte de la société. |
| [!UICONTROL Enable Purchase Orders] | Détermine si les commandes d’achat sont autorisées pour la société. Pour que les commandes d’achat fonctionnent pour les comptes des membres de la société, l’administrateur de la société doit également activer cette fonction sur le storefront. |
| [!UICONTROL Applicable Payment Methods] | Indique les modes de paiement disponibles pour les achats de l’entreprise. Options : `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Administrateur uniquement) Devient actif si des méthodes de paiement spécifiques sont indiquées. Pour sélectionner plusieurs modes de paiement, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option. |

{style="table-layout:auto"}
