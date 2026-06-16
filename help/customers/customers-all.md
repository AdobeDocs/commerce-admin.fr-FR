---
title: Liste des clients
description: La grille Clients répertorie tous les clients qui se sont inscrits à un compte dans votre boutique ou qui ont été ajoutés par l’administrateur.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
TQID: https://experienceleague.adobe.com/h3KHVcnOa1LqrynEuml6XgDB5-t5fJJa0yhgRF7RATE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 589
ht-degree: 0%

---

# Liste des clients

Dans Admin, la grille de [!UICONTROL Customers] répertorie tous les clients qui se sont inscrits à un compte dans votre boutique ou qui ont été ajoutés par l’administrateur. Utilisez les [contrôles de grille](../getting-started/admin-grid-controls.md) standard pour filtrer la liste et ajuster la disposition des colonnes. Pour en savoir plus, voir [Gestion des comptes clients](../customers/manage-account.md).

![Liste des clients](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Mettre à jour les informations sur le client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez l’enregistrement du client et cliquez sur [!UICONTROL **Modifier**] dans la colonne _[!UICONTROL Action]_.

1. Dans le panneau de gauche, sélectionnez les informations à modifier et apportez les modifications nécessaires.

   >[!NOTE]
   >
   >Pour en savoir plus, voir [Mettre à jour les comptes clients](../customers/update-account.md).

1. Cliquez ensuite sur **[!UICONTROL Save Customer]**.

## Contrôles Workspace

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Crée un compte client. |
| **[!UICONTROL Search]** | Lance une recherche de clients en fonction des filtres actuels. |
| **[!UICONTROL Filters]** | Définit un ensemble de paramètres de recherche utilisés pour filtrer les enregistrements qui apparaissent dans la [grille](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Détermine la colonne [mise en page](../getting-started/admin-grid-controls.md) par défaut de la grille. |
| **[!UICONTROL Columns]** | Détermine la sélection des [colonnes](../getting-started/admin-grid-controls.md) et leurs comptes dans la grille. La disposition des colonnes peut être modifiée et enregistrée en tant que _vue_. Par défaut, seules certaines des colonnes sont incluses dans la grille. |
| **[!UICONTROL Export]** | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |

{style="table-layout:auto"}

## Colonnes

| Colonne | Description |
| --- | --- |
| **[!UICONTROL Select]** | Gère les sélections de cases à cocher pour les enregistrements de client pour l’application d’une action. Vous pouvez également utiliser la commande de sélection de l’en-tête de colonne pour tout sélectionner/désélectionner. |
| **[!UICONTROL ID]** | Identifiant numérique unique attribué lors de la création du compte client. |
| **[!UICONTROL Name]** | Prénom et nom du client. |
| **[!UICONTROL Email]** | Adresse e-mail du client. |
| **[!UICONTROL Group]** | Groupe de clients auquel le client est affecté. |
| **[!UICONTROL Phone]** | Numéro de téléphone du client. |
| **[!UICONTROL ZIP]** | Code postal du client. |
| **[!UICONTROL Country]** | Pays dans lequel le client est situé. |
| **[!UICONTROL State/Province]** | État ou province où se trouve le client. |
| **[!UICONTROL Customer Since]** | Date et heure de création du compte client. |
| **[!UICONTROL Web Site]** | Site web dans la hiérarchie du magasin auquel le compte client est associé. |
| **[!UICONTROL Confirmed Email]** | Indique si un e-mail de confirmation est requis. |
| **[!UICONTROL Account Created In]** | Indique la vue du magasin à partir de laquelle le compte client a été créé. |
| **[!UICONTROL Date of Birth]** | Date de naissance du client. <br><br>**_Important:_** Conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, soyez conscient de tous les risques juridiques et de sécurité potentiels associés au stockage de la date de naissance complète du client (mois, jour, année) avec d&#39;autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clientes et clients et d’utiliser l’année de naissance du client comme alternative. |
| **[!UICONTROL Tax / VAT Number]** | Le cas échéant, le numéro de taxe ou [taxe sur la valeur ajoutée](../stores-purchase/vat.md) attribué au client. <br/><br/>Ce champ est différent du numéro de TVA. |
| **[!UICONTROL Gender]** | Sexe du client. |
| **[!UICONTROL Action]** | Modifier - Ouvre le compte d’entreprise en mode d’édition. |

{style="table-layout:auto"}

### Colonnes supplémentaires

Ces colonnes sont disponibles en modifiant la [disposition des colonnes](../getting-started/admin-grid-controls.md) de la grille.

| Colonne | Description |
| --- | --- |
| **[!UICONTROL Company]** | Nom de la société du client. |
| **[!UICONTROL Street Address]** | Adresse postale du client. |
| **[!UICONTROL City]** | Ville où se trouve le client. |
| **[!UICONTROL Fax]** | Numéro de fax du client, le cas échéant. |
| **[!UICONTROL Billing Firstname]** | Prénom dans l’adresse de facturation du client. |
| **[!UICONTROL Billing Lastname]** | Nom dans l’adresse de facturation du client. |
| **[!UICONTROL Billing Address]** | Adresse à laquelle les informations de facturation doivent être envoyées. |
| **[!UICONTROL Shipping Address]** | Adresse à laquelle les commandes doivent être expédiées. |
| **[!UICONTROL VAT Number]** | Numéro de TVA associé à l&#39;adresse du client. Pour les [biens numériques](../stores-purchase/taxes.md) vendus dans l’UE, la TVA est basée sur l’adresse de facturation du client. <br/><br/>Ce champ n&#39;est pas identique au numéro de taxe/TVA. |
| **[!UICONTROL Account Lock]** | Indique le statut du compte. Par mesure de sécurité, les comptes clients peuvent être [verrouillés](../customers/password-options.md) après un trop grand nombre de tentatives de connexion. Valeurs : `Locked` / `Unlocked` |

{style="table-layout:auto"}
