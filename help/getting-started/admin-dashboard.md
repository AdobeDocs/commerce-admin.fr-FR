---
title: Tableau de bord Admin
description: Découvrez le tableau de bord Admin, qui est généralement la première page qui s’affiche lorsque vous vous connectez.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Tableau de bord Admin

Le tableau de bord est généralement la première page qui s’affiche lorsque vous vous connectez à l’ _administrateur_ et vous permet de consulter un aperçu en temps réel des ventes et de l’activité des clients. Les données du tableau de bord fournissent un instantané des ventes au cours de la durée de vie, du montant moyen des commandes, des commandes récentes et des termes de recherche. Le graphique présente les commandes et les montants terminés pour la période sélectionnée et peut être généré à partir de données dynamiques en temps réel ou de données agrégées historiques. Les onglets au bas de la page fournissent des rapports rapides sur vos produits les plus vendus, les produits les plus consultés, les nouveaux clients et les clients qui ont effectué le plus d’achats.

Si le traitement d’une quantité importante de données est nécessaire, le graphique peut être désactivé afin d’améliorer les performances. Le tableau de bord de l’exemple suivant est configuré pour utiliser les données en temps réel et affiche les commandes terminées par heure pendant les dernières 24 heures. Le graphique est mis à jour pour chaque ordre terminé.

![Tableau de bord](./assets/dashboard-full.png){zoomable="yes"}

La [création de rapports avancés](business-intelligence.md#advanced-reporting) affiche un tableau de bord personnalisé basé sur les données de votre produit, de votre commande et de votre client.

![Création de rapports avancés](./assets/dashboard-advanced-reporting.png){zoomable="yes"}

## Configuration du tableau de bord

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**et renseignez l’un des paramètres suivants.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Après avoir enregistré les modifications, cliquez sur **[!UICONTROL Cache Management]** et actualisez chaque cache non valide.

### Activer les graphiques

Si vous avez une grande quantité de données à traiter, vous pouvez désactiver l’affichage du graphique pour améliorer les performances. Lorsqu’elle n’est pas activée, le message &quot;Aucune donnée trouvée&quot; apparaît à la place du graphique, bien que les totaux de résumé ci-dessous soient toujours générés.

1. Dans le panneau de navigation de gauche sous **[!UICONTROL Advanced]**, choisissez **[!UICONTROL Admin]**.

1. Si nécessaire, développez la section **[!UICONTROL Dashboard]** .

   ![Configuration avancée - Activer les graphiques](./assets/admin-dashboard-config.png){width="600"}

1. Pour modifier la valeur par défaut, décochez la case **[!UICONTROL Use system value]** .

1. Définissez **Activer les graphiques** sur `Yes`.

Pour plus d’informations sur les options de configuration de l’administrateur, consultez le [Guide de référence de configuration](../configuration-reference/advanced/admin.md).

### Modifier la page de démarrage

Le tableau de bord est la [page de démarrage](../configuration-reference/advanced/admin.md) par défaut pour l’administrateur, bien que vous puissiez configurer une autre page de démarrage.

1. Si les options de configuration de l’administrateur ne sont pas encore ouvertes, choisissez **[!UICONTROL Admin]** sous _[!UICONTROL Advanced]_dans le panneau de navigation de gauche.

1. Cliquez pour développer la section **Startup Page**.

   ![ Tableau de bord d’administration - paramètre de page de démarrage ](./assets/admin-startup-page.png){width="600"}

1. Décochez la case **[!UICONTROL Use system value]** et sélectionnez la **page de démarrage** que vous souhaitez afficher lorsque vous vous connectez à l’administrateur.

### Choisir les dates de début

1. Dans le panneau de navigation de gauche sous **[!UICONTROL General]**, sélectionnez **Rapports**.

1. Sur la page, développez la section **[!UICONTROL Dashboard]** .

1. Décochez les cases **[!UICONTROL Use system value]** pour les paramètres de date et procédez comme suit :

   - Définissez **Year-To-Date Starts** sur **Month** et **Day**.

   - Définissez **Début du mois en cours** sur le **Jour**.

   ![Tableau de bord Admin - paramètres de date](./assets/reports-dashboard.png){width="600"}

Pour plus d’informations sur les options de configuration [!UICONTROL Reports], consultez le [_Guide de référence de configuration_](../configuration-reference/general/reports.md).

### Configuration de la source de données

Le tableau de bord peut être généré en temps réel ou à l’aide de données historiques agrégées. Si les performances posent problème, vous pouvez accélérer les choses en utilisant des données agrégées.

1. Dans le panneau de navigation de gauche, cliquez pour développer **Sales** et sélectionnez **Sales** en dessous.

1. Sur la page, développez la section **[!UICONTROL Dashboard]** .

   ![Tableau de bord d’administration - paramètre de source de données](./assets/config-sales-dashboard.png){width="600"}

1. Décochez la case **[!UICONTROL Use system value]** et définissez **[!UICONTROL Use Aggregated Data]** sur l’une des options suivantes :

   - Pour les données historiques et agrégées, choisissez `Yes`.
   - Pour les données en temps réel, choisissez `No`.

## Sections du graphique

| Section | Description |
|--- |--- |
| [!UICONTROL Orders] | Cet onglet affiche un graphique en temps réel de toutes les commandes terminées pour la vue actuelle du magasin et la période spécifiée. |
| [!UICONTROL Amounts] | Cet onglet affiche un graphique en temps réel de tous les montants de commande effectués pour la vue de magasin actuelle et la période spécifiée. |
| [!UICONTROL Time Range] | Détermine les données représentées dans le graphique et les totaux de synthèse ci-dessous. Options : `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | Les totaux des recettes, des taxes, de l’expédition et de la quantité sous le graphique sont basés sur les données du graphique et le paramètre de période en cours. |

{style="table-layout:auto"}

## Données instantanées

| Section | Description |
|--- |--- |
| [!UICONTROL Lifetime Sales] | Total agrégé des ventes au cours de la durée de vie du magasin. |
| [!UICONTROL Average Order] | Montant moyen de la commande pendant la durée de vie du magasin. |
| [!UICONTROL Last Orders] | Résumé des cinq dernières commandes passées. |
| [!UICONTROL Last Search Terms] | Les cinq derniers termes de recherche. |
| [!UICONTROL Top Search Terms] | Les cinq termes de recherche les plus utilisés. |

{style="table-layout:auto"}

## Onglets Rapport

| Section | Description |
|--- |--- |
| [!UICONTROL Bestsellers] | Les cinq produits les plus vendus au cours d’une période donnée. |
| [!UICONTROL Most Viewed Products] | Les cinq produits les plus consultés au cours d’une période donnée. |
| [!UICONTROL New Customers] | Les cinq derniers clients qui se sont inscrits à un compte au cours d’une période donnée. |
| [!UICONTROL Customers] | Les cinq derniers clients ayant passé une commande et qui ont terminé le traitement au cours d’une période spécifiée. |

{style="table-layout:auto"}

## Boutons du tableau de bord

| Bouton | Description |
|--- |--- |
| [!UICONTROL Reload Data] | Actualise les données du tableau de bord. |
| [!UICONTROL Go to Advanced Reporting] | Affiche un tableau de bord personnalisé de graphiques et de rapports dynamiques en fonction des données de votre produit, de votre commande et de vos clients. Pour une analyse plus approfondie, voir [Création de rapports avancés](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
