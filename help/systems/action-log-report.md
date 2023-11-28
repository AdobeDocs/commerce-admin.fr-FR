---
title: Rapport Journaux d’actions
description: Découvrez comment afficher, filtrer et exporter le rapport Journal d’actions , qui fournit un enregistrement détaillé de toutes les actions d’administration activées dans les journaux.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Rapport Journaux d’actions

{{ee-feature}}

La variable _Journaux des actions_ affiche un enregistrement détaillé de toutes les actions d’administration activées pour la journalisation. Chaque enregistrement est horodaté et enregistre l’adresse IP et le nom de l’utilisateur. Le détail du journal comprend les données utilisateur de l’administrateur et les modifications associées qui ont été apportées pendant l’action.

Les actions que vous souhaitez afficher dans le rapport doivent être activées dans la variable [Journalisation des actions d’administration](action-log.md) s’affiche dans les paramètres du magasin. Si le type d’action est coché (activé), ces types d’actions d’administration sont affichés dans le rapport Journaux d’actions .

Le rapport peut être filtré à l&#39;aide des options de chaque colonne. Vous pouvez définir une option de filtre unique ou des options de filtre pour plusieurs colonnes afin que le rapport répertorie les actions spécifiques. Vous pouvez également exporter des données de rapport au format CSV ou XML Excel.

Le rapport Journaux d’action comprend les informations suivantes :

- **[!UICONTROL Time]** : date et heure auxquelles l’action a eu lieu
- **[!UICONTROL Action Group]** : affiche le type d’action, correspond aux actions activées sur . _Journalisation des actions d’administration_ écran dans les paramètres de la boutique
- **[!UICONTROL Action]** - Affiche l’action enregistrée.
- **[!UICONTROL IP Address]** : affiche l’adresse IP de la machine sur laquelle l’action a été effectuée.
- **[!UICONTROL Username]** - Affiche l’ID de connexion de l’utilisateur qui a exécuté l’action.
- **[!UICONTROL Result]** - Affiche la réussite ou l’échec de l’action de l’utilisateur.
- **[!UICONTROL Full Action Name]** : affiche le nom de l’action du serveur principal.
- **[!UICONTROL Details]** - Affiche la catégorie d’actions du serveur principal.
- **[!UICONTROL Full Details]** : affiche tous les détails consignés de l’action d’administration.

## Affichage du rapport Journaux d’actions

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Logs d’action](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Pour afficher tous les détails d’une action d’administration répertoriée, cliquez sur **[!UICONTROL View]**.

   ![Détails de l’entrée du journal d’action](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtrage du rapport Journaux d’actions

Vous pouvez définir les champs des options de filtrage, puis cliquer sur **[!UICONTROL Search]** pour limiter les actions affichées.

Pour effacer les options de filtre et revenir au rapport complet, cliquez sur **[!UICONTROL Reset Filter]**.

![Filtres de rapports du journal des actions](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Champ | description |
|--- |--- |
| [!UICONTROL Time] | Dans **[!UICONTROL From]**, cliquez pour sélectionner une date dans le calendrier dynamique afin de définir la date de début du filtre. Dans **[!UICONTROL To]**, cliquez pour sélectionner une date pour définir la date de fin du filtre. |
| [!UICONTROL Action Group] | Choisissez un groupe d’actions. |
| [!UICONTROL Action] | Sélectionnez une action. |
| [!UICONTROL IP Address] | Saisissez l’adresse IP de la machine utilisée pour une action. |
| [!UICONTROL Username] | Sélectionnez un nom d’utilisateur. Par défaut : `All Users`. |
| [!UICONTROL Result] | Sélectionnez Réussite ou Échec. |
| [!UICONTROL Full Action Name] | Entrez le texte de la recherche à faire correspondre dans le champ. |
| [!UICONTROL Details] | Entrez le texte de la recherche à faire correspondre dans le champ. |

{style="table-layout:auto"}

## Exportation du rapport Journaux d’actions

1. Pour **[!UICONTROL Export to]**, choisissez un format d&#39;export :

   - `CSV` : fichier de valeurs séparées par des virgules contenant des données de texte brut
   - `Excel XML` - Un format de données de feuille de calcul XML

1. Cliquez sur **[!UICONTROL Export]**.

   Le fichier généré est automatiquement enregistré dans le dossier désigné pour les téléchargements.

   ![Exportation du rapport Journaux d’action](./assets/action-log-report-export.png){width="200"}
