---
title: Définir la priorité des sources d’inventaire pour un stock
description: Découvrez comment classer les sources par ordre de priorité, qui est utilisé pour déterminer les déductions d’expédition et d’inventaire.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Définir la priorité des sources pour un stock

Après avoir ajouté [sources](sources-manage.md) au [stock](stocks-manage.md), organisez ces sources de haut en bas en priorité pour exécuter les commandes. L’algorithme de sélection Source (SSA) fournit une priorité d’algorithme en utilisant cet ordre pour déterminer les déductions d’expédition et d’inventaire.

La priorité de la source sur les stocks n’a aucune incidence sur les sources attribuées lors de la modification des stocks de produits.

Dans cet exemple, UK Stock a attribué des sources hors-service pour un magasin et deux entrepôts à Londres et un entrepôt à Berlin.

![Commande Source avant priorisation](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Le marchand préfère que les envois soient classés par priorité dans l&#39;entrepôt plus vaste de Berlin, puis dans l&#39;entrepôt de Londres, dans l&#39;emplacement de débordement de Londres, et enfin dans l&#39;entrepôt de Londres. Pour modifier l’ordre, les entrées sont glissées-déposées dans l’ordre souhaité.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Ouvrez le stock en mode _Modifier_ .

1. Développez l’onglet _[!UICONTROL Sources]_, si nécessaire.

1. Utilisez ![Icône Tri](assets/icon-sort.png) pour faire glisser les sources dans une priorité allant du haut (premier) au bas (dernier).

   Cette commande est importante lors des commandes d’expédition. L&#39;ASL recommande les envois selon l&#39;ordre des sources

1. Cliquez sur **[!UICONTROL Save & Continue]** pour enregistrer les modifications.

![Commande Source après priorisation](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
