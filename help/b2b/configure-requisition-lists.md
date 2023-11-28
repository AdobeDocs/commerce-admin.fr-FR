---
title: Configuration du nombre maximal de demandes
description: Découvrez la configuration de la liste des demandes d’approvisionnement, qui contrôle le nombre maximal pouvant être conservé pour chaque compte client.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Configuration du nombre maximal de demandes

Lorsque la fonction de liste de commandes est activée, les clients peuvent créer plusieurs listes d’articles fréquemment achetés et les utiliser pour leur emplacement de commande. Il est disponible pour les utilisateurs connectés et les invités. Vous pouvez activer les listes de demandes lorsque vous [configuration des fonctionnalités B2B](enable-basic-features.md).

Un client peut avoir plusieurs listes qui se concentrent sur des produits provenant de différents fournisseurs, acheteurs, équipes, campagnes ou tout autre élément qui rationalise les workflows communs. [Fonctionnalité Liste de demandes](requisition-lists.md) est similaire aux listes de souhaits, avec les différences suivantes :

- Une liste de demandes d’achat n’est pas effacée après l’envoi d’articles au panier. Il peut être utilisé plusieurs fois.
- L’interface utilisateur des listes de demandes d’approvisionnement utilise une vue compacte pour afficher de nombreux éléments.

Par défaut, les clients peuvent conserver jusqu’à 999 listes de demandes pour leur compte. Vous pouvez toutefois modifier la configuration et indiquer un nombre inférieur pour réduire la charge sur votre boutique.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Requisition Lists]**.

   ![Listes de demandes - paramètre général](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Number of Requisition Lists]**, saisissez le nombre maximal de listes de demandes d’approvisionnement pouvant être conservées pour chaque compte client.

   Le nombre minimum est `2`, et la valeur maximale est `999`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
