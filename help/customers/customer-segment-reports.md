---
title: Rapport Segment de client
description: Le rapport Segment de client fournit des informations sur le nombre de clients dans chaque segment.
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Rapport Segment de client

{{ee-feature}}

Le rapport Segment de client fournit des informations sur le nombre de clients dans chaque segment.

![Rapport Segment De Client](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| Colonne | Description |
|--- |--- |
| **[!UICONTROL Select]** | Cochez la case correspondant à chaque segment à soumettre à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | Identifiant numérique unique attribué à chaque segment. |
| **[!UICONTROL Segment]** | Nom du segment |
| **[!UICONTROL Status]** | État du segment. Options : `Active` / `Inactive` |
| **[!UICONTROL Website]** | Site web auquel le segment est affecté |
| **[!UICONTROL Customers]** | Nombre de clients affectés à un segment |

{style="table-layout:auto"}

Vous pouvez accéder à une liste de clients dans le segment et exporter les données.

![Exploration des données client](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

Pour vous assurer que vous disposez des données les plus récentes, les données du segment doivent être actualisées. Si les données de segment ne sont pas disponibles ou sont obsolètes, cliquez sur **[!UICONTROL Refresh Segment Data]** dans la barre de boutons pour les mettre à jour.

1. Pour **[!UICONTROL Export to]**, choisissez un format d’exportation :

   * CSV : fichier de valeurs séparées par des virgules contenant des données de texte brut.
   * Excel XML : format de données de feuille de calcul XML.

1. Cliquez sur **[!UICONTROL Export]**.

   | Colonne | Description |
   |--- |--- |
   | **[!UICONTROL ID]** | Identifiant numérique unique attribué à chaque utilisateur |
   | **[!UICONTROL Name]** | Nom du client |
   | **[!UICONTROL Email]** | Adresse électronique d’un client enregistré |
   | **[!UICONTROL Group]** | Groupe de clients auquel le client est affecté |
   | **[!UICONTROL Phone]** | Numéro de téléphone du client |
   | **[!UICONTROL ZIP]** | Code postal où se trouve le client |
   | **[!UICONTROL Country]** | Pays où se trouve le client |
   | **[!UICONTROL State/Province]** | État ou province où se trouve le client |
   | **[!UICONTROL Customer Since]** | Date et heure de création du compte client |

   {style="table-layout:auto"}

1. Le fichier généré est automatiquement enregistré sur votre ordinateur local.
