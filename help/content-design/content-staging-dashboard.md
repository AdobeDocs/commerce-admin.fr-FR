---
title: Tableau de bord d’évaluation du contenu
description: Utilisez le tableau de bord d’évaluation du contenu pour accéder à un aperçu de toutes les campagnes actives et à venir.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/Hwrb3dYdJlggWN-Z-nUKxVBhsejFMZR-yWIgRzfJifQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Tableau de bord d’évaluation du contenu

{{ee-feature}}

Le tableau de bord [!UICONTROL Content Staging] fournit un aperçu de toutes les campagnes actives et à venir. Le format du tableau de bord peut être modifié d’une grille en chronologie. Vous pouvez également utiliser des filtres pour rechercher des campagnes, personnaliser la disposition des colonnes et enregistrer différentes vues de la grille. Pour plus d’informations sur les commandes de l’espace de travail, voir [Espace de travail d’administration](../getting-started/admin-workspace.md).

![Tableau de bord d’évaluation en mode Grille](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Affichage du tableau de bord d’évaluation

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Pour modifier le format du tableau de bord, définissez le contrôle **[!UICONTROL View As]** sur `list`, `Grid` ou `Timeline`.

   ![Mode Chronologie](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Lorsque la chronologie s’affiche, le curseur dans le coin inférieur droit peut être utilisé pour ajuster l’affichage d’une à quatre semaines. Chaque colonne représente un jour.

1. Si la chronologie s’affiche, faites glisser le curseur vers la position `4w` tout à droite pour afficher une période plus longue.

   ![Vue sur quatre semaines](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Pour afficher des informations générales sur la campagne, cliquez sur un élément de la page.

   - Pour ouvrir la campagne, cliquez sur **[!UICONTROL View/Edit]**.

   - Pour voir à quoi ressemble la campagne pour les clients du magasin ce jour-là, cliquez sur **[!UICONTROL Preview]**.

   ![Informations sur la campagne](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Descriptions des colonnes du tableau de bord d’évaluation

| Colonne | Description |
|--- |--- |
| [!UICONTROL Status] | Statut de la campagne. `Active` ou `Upcoming`. |
| [!UICONTROL Update Name] | Nom de la campagne. |
| [!UICONTROL Includes] | Définit le nombre d’objets inclus dans la campagne. |
| [!UICONTROL Start Time] | Date de début de la campagne. |
| [!UICONTROL End Time] | Date de fin de la campagne. |
| [!UICONTROL Description] | Description supplémentaire de chaque campagne. |
| [!UICONTROL Action] | Les actions pouvant être appliquées à un enregistrement individuel sont les suivantes : <br/>**[!UICONTROL View/Edit]**- Ouvre la campagne en mode d’édition.<br/>**[!UICONTROL Preview]** : affiche la campagne en mode Aperçu. |

{style="table-layout:auto"}

## Modification d’une campagne

Les objets de campagne existants peuvent être modifiés à partir du tableau de bord d&#39;évaluation, à l&#39;exception des campagnes de règles de prix qui n&#39;ont pas de dates de fin.

>[!NOTE]
>
>Si une campagne active est initialement créée sans date de fin, la campagne ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une campagne en double et de saisir la date de fin nécessaire.

![Détails de la campagne](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

Dans cet exemple, la campagne comprend deux catégories et trois produits individuels.

Pour modifier les objets de cette campagne, procédez comme suit.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Recherchez la campagne dans la liste ou la chronologie affichée et ouvrez-la pour accéder aux détails :

   - Pour afficher une liste, cliquez sur **[!UICONTROL Select]** puis **[!UICONTROL View/Edit]** dans la colonne _[!UICONTROL Action]_.
   - Pour un affichage chronologique, cliquez une fois pour afficher le résumé, puis cliquez sur **[!UICONTROL View/Edit]**.

1. Mettez à jour l’un des paramètres de la section _[!UICONTROL General]_selon vos besoins.

1. Développez ![sélecteur de développement](../assets/icon-display-expand.png) toute section contenant un élément à modifier.

   ![Mise à jour des produits affectés à un élément de campagne](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.
