---
title: Envoyer une commande
description: Découvrez comment renseigner les informations d’expédition pour une commande de traitement et afficher les informations d’expédition et de suivi.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Envoyer une commande

Une commande qui a été payée, mais qui est en attente d’expédition a le statut `Processing`. L’enregistrement de l’expédition contient un historique détaillé du processus d’exécution associé à la commande. Des envois partiels peuvent être effectués jusqu’à ce que la commande soit passée.

1. Dans la barre latérale _Admin_, sélectionnez **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Dans la liste _[!UICONTROL Orders]_, recherchez la commande à expédier et cliquez pour l’ouvrir.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Ship]** .

1. Si vous souhaitez mettre à jour l’adresse de facturation ou de livraison, cliquez sur le lien **[!UICONTROL Edit]** dans le coin supérieur droit de la section .

   Effectuez les modifications nécessaires, puis cliquez sur **[!UICONTROL Save Order Address]**.

1. Pour que l’opérateur génère un libellé d’expédition, cochez la case **[!UICONTROL Create Shipping Label]** et définissez les options :

   - Pour ajouter un numéro de suivi, faites défiler l’écran jusqu’à la section _[!UICONTROL Shipping Information]_, puis cliquez sur **[!UICONTROL Add Tracking Number]**.

   - Effectuez l’une des opérations suivantes :

      - Sélectionnez le **[!UICONTROL Carrier]** et saisissez le suivi **[!UICONTROL Number]**.

      - Définissez **[!UICONTROL Carrier]** sur `Custom Value`, saisissez un **[!UICONTROL Title]** pour l’opérateur personnalisé, puis saisissez le suivi **[!UICONTROL Number]**.

      - [Afficher les informations de suivi](#track-the-shipment).

1. Pour effectuer une livraison partielle, faites défiler l’écran jusqu’à la section Éléments à expédier , puis saisissez le **[!UICONTROL Qty to Ship]** de chaque élément.

1. Pour notifier les clients par email de l&#39;envoi, procédez comme suit :

   - Saisissez les commentaires que vous souhaitez inclure dans la zone **[!UICONTROL Shipment Comments]**.

   - Pour inclure les commentaires dans l&#39;email de notification envoyé au client, cochez la case **[!UICONTROL Append Comments]** .

   - Pour vous envoyer une copie de l&#39;email d&#39;expédition, cochez la case **[!UICONTROL Email Copy of Shipment]** .

     L’état de l’email d’une facture est indiqué en regard du numéro de facture de la facture complétée, tel qu’elle est envoyée ou non.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Submit Shipment]**.

   L’état de la commande passe de `Processing` à `Complete`.

>[!NOTE]
>
>Si une commande est placée en tant que &quot;diffusion en magasin&quot;, les options d’expédition ne sont pas disponibles. Cliquez sur **[!UICONTROL Notify Order is Ready for Pickup]** pour déclencher un courrier électronique à l’intention du client. L’état de la commande est alors modifié en `Complete`.

## Afficher les détails de la livraison

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Recherchez l’envoi dans la liste, puis cliquez pour ouvrir l’enregistrement.

1. Si vous souhaitez ajouter un commentaire à la commande, faites défiler l’écran jusqu’à la section _[!UICONTROL Comments History]_, puis saisissez le commentaire dans la zone.

   - Pour envoyer le commentaire au client par courrier électronique, cochez la case **[!UICONTROL Notify Customer by Email]** .

   - Pour publier le commentaire dans le compte du client, cochez la case **[!UICONTROL Visible on Frontend]** .

1. Cliquez sur **[!UICONTROL Submit Comment]**.

## Suivi de l’envoi

**Méthode 1 :** à partir de l’onglet Informations sur la commande

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez la commande d&#39;expédition dans la grille, puis cliquez sur **[!UICONTROL View]**.

1. Faites défiler l’écran jusqu’à la section _[!UICONTROL Shipping & Handling Information]_et cliquez sur **[!UICONTROL Track Order]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, cliquez sur **[!UICONTROL Close Window]**.

**Méthode 2 :** à partir de l’onglet Envoi de commande

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Recherchez l’envoi dans la liste, puis cliquez pour ouvrir l’enregistrement.

1. Cliquez sur **[!UICONTROL Track this Shipment]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, cliquez sur **[!UICONTROL Close Window]**.
