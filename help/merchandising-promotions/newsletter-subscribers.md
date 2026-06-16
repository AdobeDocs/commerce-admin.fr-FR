---
title: Gérer les abonnés à la newsletter
description: Découvrez comment gérer vos abonnés à la newsletter à l’aide d’une simple liste d’abonnements actifs.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
TQID: https://experienceleague.adobe.com/l4Kmwm62UeLYZva-SCsVHPmf4IbKQhgoyN9N7zo4O0g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 509
ht-degree: 0%

---

# Gérer les abonnés à la newsletter

En règle générale, il est recommandé de gérer régulièrement votre liste d’abonnements et de veiller à traiter toutes les demandes de désabonnement. Dans certaines juridictions, la loi exige que les demandes de désabonnement soient traitées dans un délai spécifique.

Vous pouvez facilement gérer vos abonnés à l&#39;aide d&#39;une simple liste d&#39;abonnements actifs. Lorsqu’un client envoie une demande de désabonnement, vous pouvez simplement appliquer une action _Désabonnement_ à un ou plusieurs abonnements sélectionnés.

Dans les configurations à site unique avec plusieurs vues de magasin, un abonnement à un compte client peut être associé à une vue de magasin spécifique.

Dans les configurations multi-magasin et multi-site avec une étendue de compte client globale [customer account scope](../customers/customer-account-scope.md), un compte client peut être abonné à des newsletters pour plusieurs sites/magasins. Dans ce cas, vous pouvez modifier le compte client pour gérer un groupe d’abonnements ou annuler un abonnement pour un site/magasin spécifique afin de répondre à une demande.

Si vous souhaitez utiliser un service tiers pour envoyer des newsletters, vous pouvez exporter votre liste d’abonnements sous la forme d’un fichier CSV ou XML.

## Gérer les abonnements pour un client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Cliquez sur **[!UICONTROL Newsletter]** dans le panneau de gauche.

1. Modifiez les abonnements pour le client en fonction de la configuration de votre site ou de votre boutique.

   Pour une configuration de site/magasin unique, vous pouvez simplement cocher ou décocher la case **[!UICONTROL Subscribed to Newsletter]**.

   ![Case à cocher d’abonnement à la newsletter du client d’une boutique unique](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Pour une configuration unique de site/multi-magasin, vous pouvez cocher ou décocher la case **[!UICONTROL Subscribed to Newsletter]** et **[!UICONTROL Subscribed on Store View]** à la vue de magasin appropriée pour l’abonnement.

   ![Case à cocher d’abonnement à la newsletter client multi-magasin et sélecteur d’affichage de magasin](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Pour une configuration multi-site/multi-magasin avec une portée de compte client globale, la page affiche le statut d’abonnement pour tous les sites. Vous pouvez cocher ou décocher la case **[!UICONTROL Subscribed]** et/ou modifier la **[!UICONTROL Store View]** de l’abonnement.

   ![Cases à cocher d’abonnement à la newsletter client multi-site et sélecteurs d’affichage de magasin](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Customer]**.

## Annuler un abonnement depuis la liste des abonnés

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Dans le cas d’une configuration multisite où certains clients disposent d’abonnements pour plusieurs sites, chaque abonnement s’affiche sous la forme d’un élément de ligne dans la grille.

1. Recherchez l&#39;abonné dans la grille et cochez la case dans la première colonne.

   >[!NOTE]
   >
   >Pour un désabonnement en bloc, cochez la case de chaque abonné que vous souhaitez annuler.

1. Définissez la commande _[!UICONTROL Action]_sur **[!UICONTROL Unsubscribe]**, puis cliquez sur **[!UICONTROL Submit]**.

   ![Désabonnement de la newsletter](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Le statut de l’enregistrement passe à `Unsubscribed`.

## Export de la liste des abonnés

1. Dans la liste _[!UICONTROL Newsletter Subscribers]_, utilisez les contrôles de filtre pour inclure uniquement les enregistrements avec un_ Statut _de `Subscribed` et pour la vue de site web, de magasin ou de magasin appropriée.

1. Définissez le contrôle **[!UICONTROL Export to]** sur l’une des options suivantes :

   - `CSV`
   - `XML`

1. Cliquez sur **[!UICONTROL Export]** et recherchez l’invite en bas de l’écran, puis enregistrez le fichier.

   ![Exporter les abonnés à la newsletter](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Supprimer un abonné de la liste des abonnés

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Recherchez l&#39;abonné dans la grille et cochez la case dans la première colonne.

1. Définissez la commande _[!UICONTROL Action]_sur **[!UICONTROL Delete]**, puis cliquez sur **[!UICONTROL Submit]**.

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.
