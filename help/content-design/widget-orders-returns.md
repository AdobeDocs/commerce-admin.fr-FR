---
title: Widget Commandes et retours
description: Découvrez comment utiliser le widget Commandes et retours pour permettre aux clients de vérifier l’état de leurs commandes, d’imprimer des factures et de suivre les envois.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Widget Commandes et retours

Le widget _Commandes et retours_ permet aux invités de vérifier l’état de leurs commandes, d’imprimer des factures et de suivre les envois. Lorsque le widget est ajouté au storefront, il est visible uniquement pour les invités et les clients qui ne sont pas connectés à leurs comptes. Les clients peuvent trouver les commandes en indiquant l’identifiant de commande, le nom de la facturation et l’adresse électronique ou le code postal.

![Widget Commandes et retours dans la barre latérale sur le storefront](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Widget commandes et retours sur le storefront

1. Le client peut utiliser l’option **[!UICONTROL Find Order By]** pour choisir l’un des paramètres suivants à utiliser pour trouver la commande :

   - Adresse électronique
   - Code postal

1. Le client entre les **[!UICONTROL Order ID]** et **[!UICONTROL Billing Last Name]**.

1. Entrez la facturation **[!UICONTROL Email Address]** ou **[!UICONTROL ZIP Code]** associée à la commande.

1. Cliquez sur **[!UICONTROL Search]** pour récupérer la commande.

   ![Informations de commande affichées dans le storefront](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configuration du widget Commandes et retours

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_, procédez comme suit :

   - Définissez **[!UICONTROL Type]** sur `Orders and Returns`.

   - Sélectionnez le **[!UICONTROL Design Theme]** utilisé par le magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement à partir de l’administrateur.

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget est visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**&#x200B;et procédez comme suit :

   - Définissez **[!UICONTROL Display On]** sur le type de page sur lequel vous souhaitez que le widget s’affiche.

   - Pour déterminer l’emplacement d’affichage du widget sur la page, renseignez les autres informations de mise à jour de la mise en page.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le lien contenu dans le message situé en haut de la page et suivez les instructions.
