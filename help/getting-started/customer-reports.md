---
title: Rapports sur les clients
description: Les rapports sur les clients disponibles dans Adobe Commerce et Magento Open Source fournissent des informations sur l’activité des clients au cours d’une période ou d’une période spécifiée.
exl-id: 7bee414b-b605-4aed-9749-78bb8056a6a4
feature: Customers, Reporting
source-git-commit: a530d74f8d073f834f310826562407b8f949f17b
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 1%

---

# Rapports sur les clients

Les rapports sur les clients fournissent des informations sur l’activité des clients au cours d’une période ou d’une période spécifiée.

## [!UICONTROL Order Total Report]

La variable [!UICONTROL Order Total Report] affiche les commandes client pour un intervalle de temps ou une période spécifié. Le rapport inclut le nombre de commandes par client, le montant moyen de la commande et le montant total.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Order Total]**.

![Rapport Total de la commande](./assets/customers-order-total.png){width="600"}

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL From / To] | Utilisé pour définir une recherche pour les commandes en fonction des dates de début et de fin. |
| [!UICONTROL Show By] | Définit la granularité du fractionnement de l’enregistrement de commande. Options : `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | Met à jour la grille avec les filtres spécifiés. |
| [!UICONTROL Export] | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |
| [!UICONTROL Scope] | Utilisé pour définir le site ou le magasin pour lequel le rapport est généré. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | l’intervalle total de l’ordre, par `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | Nom du client qui a passé les commandes. |
| [!UICONTROL Orders] | Nombre de commandes pour l’intervalle spécifié. |
| [!UICONTROL Average] | Montant moyen de la commande. Ce montant est toujours calculé pour les prix des produits. **taxe à l&#39;exclusion** même si les prix des produits catalogues, le sous-total des commandes et le total des commandes comprennent la taxe. Par conséquent, le montant indiqué dans le rapport est différent du montant indiqué dans les détails de la commande lorsque les totaux de la commande comprennent la taxe. |
| [!UICONTROL Total] | Somme de toutes les commandes de la période. Ce montant est toujours calculé pour les prix des produits. **taxe à l&#39;exclusion** même si les prix des produits catalogues, le sous-total des commandes et le total des commandes comprennent la taxe. Par conséquent, le total affiché dans le rapport est différent du montant affiché dans les détails de la commande lorsque les totaux de la commande comprennent la taxe. |

{style="table-layout:auto"}

## [!UICONTROL Order Count Report]

La variable [!UICONTROL Order Count Report] indique le nombre de commandes par client pour un intervalle de temps ou une période spécifié. Le rapport inclut le nombre de commandes par client, le montant moyen de la commande et le montant total.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Order Count]**.

![Rapport Nombre de commandes](./assets/customer-order-count.png){width="600"}

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL From / To] | Utilisé pour définir une recherche pour les commandes en fonction des dates de début et de fin. |
| [!UICONTROL Show By] | Définit la granularité du fractionnement de l’enregistrement de commande. Options : `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | Met à jour la grille avec les filtres spécifiés. |
| [!UICONTROL Export] | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |
| [!UICONTROL Scope] | Utilisé pour définir le site ou le magasin pour lequel le rapport est généré. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | l’intervalle de comptage de l’ordre, par `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | Le client qui a passé la commande. |
| [!UICONTROL Orders] | Nombre de commandes pour l’intervalle spécifié. |
| [!UICONTROL Average] | Montant moyen de la commande. Ce montant est toujours calculé pour les prix des produits. **taxe à l&#39;exclusion** même si les prix des produits catalogues, le sous-total des commandes et le total des commandes comprennent la taxe. Par conséquent, le montant indiqué dans le rapport est différent du montant indiqué dans les détails de la commande lorsque les totaux de la commande comprennent la taxe. |
| [!UICONTROL Total] | Somme de toutes les commandes de la période. Ce montant est toujours calculé pour les prix des produits. **taxe à l&#39;exclusion** même si les prix des produits catalogues, le sous-total des commandes et le total des commandes comprennent la taxe. Par conséquent, le total affiché dans le rapport est différent du montant affiché dans les détails de la commande lorsque les totaux de la commande incluent des balises. |

{style="table-layout:auto"}

## [!UICONTROL New Accounts Report]

La variable [!UICONTROL New Accounts Report] indique le nombre de nouveaux comptes clients ouverts au cours d’un intervalle de temps ou d’une période spécifié.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL New]**.

![Nouveau rapport Comptes](./assets/customers-new-accounts.png){width="600"}

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL From / To] | Utilisé pour définir une recherche pour les nouveaux comptes en fonction des dates de début et de fin. |
| [!UICONTROL Show By] | Définit la granularité du fractionnement de l’enregistrement de commande. Options : mois/jour/année |
| [!UICONTROL Refresh] | Met à jour la grille avec les filtres spécifiés. |
| [!UICONTROL Export] | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |
| [!UICONTROL Scope] | Utilisé pour définir le site ou le magasin pour lequel le rapport est généré. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Interval] | Nouvel intervalle de création de compte, par mois/jour/année. |
| [!UICONTROL New Accounts] | Nombre de nouveaux comptes créés dans un certain intervalle. |

{style="table-layout:auto"}

## [!UICONTROL Customer Wish List Report]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

La variable [!UICONTROL Customer Wish List Report] fournit des informations sur les listes de souhaits des clients.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Wish Lists]**.

![Rapport Liste de souhaits](./assets/customer-wish-list.png){width="600"}

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Scope] | Utilisé pour définir le site ou le magasin pour lequel le rapport est généré. |
| [!UICONTROL Search] | Lance une recherche selon les paramètres spécifiés. |
| [!UICONTROL Reset Filter] | Lance une réinitialisation de tous les paramètres de recherche. |
| [!UICONTROL Per Page] | Définit le nombre d&#39;enregistrements affichés sur une seule page. |
| [!UICONTROL Export] | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |
| [!UICONTROL From / To] | Utilisé pour définir une recherche pour les listes de souhaits en fonction des dates de début et de fin. |
| [!UICONTROL Wishlist] | Lance une recherche de liste de souhaits par nom. |
| [!UICONTROL Status] | État de la liste de souhaits. Options : `Private` / `Public` |
| [!UICONTROL Comment] | Lance une recherche par texte dans les commentaires de la liste de souhaits. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Added] | Date de création de la liste de souhaits. |
| [!UICONTROL Customer] | Prénom et nom du client qui a créé la liste de souhaits. |
| [!UICONTROL Wishlist] | Nom de la liste de souhaits. |
| [!UICONTROL Status] | État de la liste de souhaits. Options : `Private` / `Public` |
| [!UICONTROL Product] | Nom du produit ajouté à la liste de souhaits. |
| [!UICONTROL SKU] | SKU du produit ajouté à la liste de souhaits. |
| [!UICONTROL Comment] | Le texte du commentaire saisi lors de la création de la liste de souhaits. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segment Report]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

La variable [!UICONTROL Customer Segment Report] fournit des informations sur le nombre de clients dans chaque segment.

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Segments]**.

![Rapport Segments](./assets/customers-segments.png){width="600"}

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Search] | Lance une recherche selon les paramètres spécifiés. |
| [!UICONTROL Reset Filter] | Lance une réinitialisation de tous les paramètres de recherche. |
| [!UICONTROL Action] | Lance l’affichage des segments par paramètres. Options : `Action` / `View Combined Report` |
| [!UICONTROL Per Page] | Définit le nombre d&#39;enregistrements affichés sur une seule page. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à chaque segment. |
| [!UICONTROL Segment] | Nom du segment. |
| [!UICONTROL Status] | État du segment. Options : `Active` / `Inactive` |
| [!UICONTROL Website] | Site web auquel le segment est affecté. |
| [!UICONTROL Customers] | Nombre de clients affectés au segment. |

{style="table-layout:auto"}
