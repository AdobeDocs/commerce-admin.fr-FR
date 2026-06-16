---
title: Configurer le maximum de la liste des demandes d'approvisionnement
description: Découvrez la configuration de la liste de demandes d'approvisionnement, qui contrôle le nombre maximal pouvant être géré pour chaque compte client.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# Configurer le maximum de la liste des demandes d&#39;approvisionnement

Lorsque la fonction de liste de demandes d&#39;approvisionnement est activée, les clients peuvent créer plusieurs listes d&#39;articles fréquemment achetés et utiliser ces listes pour passer des commandes. Il est disponible pour les utilisateurs connectés et les invités. Vous pouvez activer les listes de demandes d&#39;approvisionnement lorsque vous [configurez les fonctions B2B](enable-basic-features.md).

Un client peut avoir plusieurs listes qui se concentrent sur les produits de différents fournisseurs, acheteurs, équipes, campagnes ou toute autre chose qui simplifie les workflows courants. La [fonctionnalité de liste de demandes](requisition-lists.md) est similaire aux listes de souhaits, avec les différences suivantes :

- Une liste de demandes d&#39;approvisionnement n&#39;est pas effacée après l&#39;envoi d&#39;articles au panier. Il peut être utilisé plusieurs fois.
- L&#39;interface utilisateur des listes de demandes d&#39;approvisionnement utilise une vue compacte pour afficher de nombreux articles.

Par défaut, les clients peuvent gérer jusqu&#39;à 999 listes de demandes d&#39;approvisionnement pour leur compte. Cependant, vous pouvez modifier la configuration et spécifier un nombre inférieur pour réduire la charge sur votre magasin.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Requisition Lists]**.

   ![Listes de demandes d&#39;approvisionnement - paramètre général](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Number of Requisition Lists]**, entrez le nombre maximal de listes de demandes d&#39;approvisionnement qui peuvent être gérées pour chaque compte client.

   Le nombre minimum est `2` et le maximum est `999`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
