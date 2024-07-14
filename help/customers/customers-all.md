---
title: Liste des clients
description: La grille Clients répertorie tous les clients qui se sont inscrits pour un compte auprès de votre boutique ou qui ont été ajoutés par l’administrateur.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Liste des clients

Dans l’Admin, la grille [!UICONTROL Customers] répertorie tous les clients qui se sont inscrits pour un compte auprès de votre boutique ou qui ont été ajoutés par l’administrateur. Utilisez les [contrôles de grille](../getting-started/admin-grid-controls.md) standard pour filtrer la liste et ajuster la disposition des colonnes. Pour en savoir plus, voir [Gestion des comptes clients](../customers/manage-account.md).

![Liste des clients](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Mise à jour des informations sur les clients

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez l’enregistrement du client et cliquez sur [!UICONTROL **Modifier**] dans la colonne _[!UICONTROL Action]_.

1. Dans le panneau de gauche, sélectionnez les informations à modifier et apportez les modifications nécessaires.

   >[!NOTE]
   >
   >Pour en savoir plus, voir [Mise à jour des comptes clients](../customers/update-account.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Customer]**.

## Contrôles Workspace

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Crée un compte client. |
| **[!UICONTROL Search]** | Lance une recherche de clients en fonction des filtres actuels. |
| **[!UICONTROL Filters]** | Définit un ensemble de paramètres de recherche utilisés pour filtrer les enregistrements qui apparaissent dans la [grille](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Détermine la colonne par défaut [layout](../getting-started/admin-grid-controls.md) de la grille. |
| **[!UICONTROL Columns]** | Détermine la sélection de [colonnes](../getting-started/admin-grid-controls.md) et de leurs comptes dans la grille. La mise en page des colonnes peut être modifiée et enregistrée en tant que _vue_. Par défaut, seules certaines colonnes sont incluses dans la grille. |
| **[!UICONTROL Export]** | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |

{style="table-layout:auto"}

## Colonnes

| Colonne | Description |
| --- | --- |
| **[!UICONTROL Select]** | Gère les sélections de cases à cocher pour les enregistrements de client lors de l’application d’une action. Vous pouvez également utiliser le contrôle de sélection dans l’en-tête de colonne pour tout sélectionner/tout désélectionner. |
| **[!UICONTROL ID]** | Identifiant numérique unique attribué lors de la création du compte client. |
| **[!UICONTROL Name]** | Prénom et nom du client. |
| **[!UICONTROL Email]** | Adresse électronique du client. |
| **[!UICONTROL Group]** | Groupe de clients auquel le client est affecté. |
| **[!UICONTROL Phone]** | Numéro de téléphone du client. |
| **[!UICONTROL ZIP]** | Code postal du client. |
| **[!UICONTROL Country]** | Pays où se trouve le client. |
| **[!UICONTROL State/Province]** | État ou province où se trouve le client. |
| **[!UICONTROL Customer Since]** | Date et heure de création du compte client. |
| **[!UICONTROL Web Site]** | Site web dans la hiérarchie de magasins à laquelle le compte client est associé. |
| **[!UICONTROL Confirmed Email]** | Indique si un email de confirmation est requis. |
| **[!UICONTROL Account Created In]** | Indique la vue de magasin à partir de laquelle le compte client a été créé. |
| **[!UICONTROL Date of Birth]** | La date de naissance du client. <br><br>**_Important :_**Conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, gardez à l’esprit tous les risques potentiels liés à la sécurité et au stockage de la date de naissance complète des clients (mois, jour, année) avec d’autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clients et de suggérer d’utiliser l’année de naissance du client comme alternative. |
| **[!UICONTROL Tax / VAT Number]** | Le cas échéant, le numéro de taxe ou le numéro de [taxe sur la valeur ajoutée](../stores-purchase/vat.md) attribué au client. <br/><br/>Ce champ n’est pas le même que le numéro de TVA. |
| **[!UICONTROL Gender]** | Genre du client. |
| **[!UICONTROL Action]** | Modifier : ouvre le compte de l’entreprise en mode d’édition. |

{style="table-layout:auto"}

### Colonnes supplémentaires

Ces colonnes sont disponibles en modifiant la [mise en page des colonnes](../getting-started/admin-grid-controls.md) de la grille.

| Colonne | Description |
| --- | --- |
| **[!UICONTROL Company]** | Nom de la société du client. |
| **[!UICONTROL Street Address]** | Adresse postale du client. |
| **[!UICONTROL City]** | Ville où se trouve le client. |
| **[!UICONTROL Fax]** | Le numéro de fax du client, le cas échéant. |
| **[!UICONTROL Billing Firstname]** | Prénom dans l’adresse de facturation du client. |
| **[!UICONTROL Billing Lastname]** | Nom dans l’adresse de facturation du client. |
| **[!UICONTROL Billing Address]** | Adresse à laquelle les informations de facturation doivent être envoyées. |
| **[!UICONTROL Shipping Address]** | Adresse à laquelle les commandes doivent être expédiées. |
| **[!UICONTROL VAT Number]** | Numéro de taxe sur la valeur ajoutée associé à l’adresse du client. Pour les [biens numériques](../stores-purchase/taxes.md) vendus dans l’UE, la TVA est basée sur l’adresse de facturation du client. <br/><br/>Ce champ n’est pas le même que le champ Numéro de taxe/TVA. |
| **[!UICONTROL Account Lock]** | Indique le statut du compte. Par mesure de sécurité, les comptes clients peuvent être [verrouillés](../customers/password-options.md) après trop de tentatives de connexion. Valeurs : `Locked` / `Unlocked` |

{style="table-layout:auto"}
