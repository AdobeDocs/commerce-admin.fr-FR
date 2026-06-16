---
title: Expédier une commande
description: Découvrez comment compléter les informations d’expédition d’une commande de traitement et afficher les informations d’expédition et de suivi.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 0%

---

# Expédier une commande

Une commande qui a été payée mais qui est en attente d&#39;expédition a le statut `Processing`. L’enregistrement d’expédition contient un historique détaillé du processus d’exécution associé à la commande. Des envois partiels peuvent être effectués jusqu&#39;à ce que la commande soit honorée.

1. Dans la barre latérale _Admin_, sélectionnez **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Dans la liste _[!UICONTROL Orders]_, recherchez la commande à expédier et cliquez pour l&#39;ouvrir.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Ship]** .

1. Si vous souhaitez mettre à jour l’adresse de facturation ou d’expédition, cliquez sur le lien **[!UICONTROL Edit]** dans le coin supérieur droit de la section.

   Effectuez les modifications nécessaires, puis cliquez sur **[!UICONTROL Save Order Address]**.

1. Pour que le transporteur génère une étiquette d&#39;expédition, cochez la case **[!UICONTROL Create Shipping Label]** et définissez les options suivantes :

   - Pour ajouter un numéro de suivi, faites défiler l’écran jusqu’à la section _[!UICONTROL Shipping Information]_, puis cliquez sur **[!UICONTROL Add Tracking Number]**.

   - Effectuez l’une des opérations suivantes :

      - Sélectionnez le **[!UICONTROL Carrier]** et renseignez le **[!UICONTROL Number]** de tracking.

      - Définissez **[!UICONTROL Carrier]** sur `Custom Value`, saisissez un **[!UICONTROL Title]** pour l’opérateur personnalisé, puis saisissez le **[!UICONTROL Number]** de suivi.

      - [Afficher les informations de suivi](#track-the-shipment).

1. Pour effectuer une expédition partielle, faites défiler l&#39;écran jusqu&#39;à la section Articles à expédier, puis saisissez le **[!UICONTROL Qty to Ship]** de chaque article.

1. Pour informer les clients par e-mail de l’expédition, procédez comme suit :

   - Saisissez les commentaires que vous souhaitez inclure dans la zone de **[!UICONTROL Shipment Comments]**.

   - Pour inclure les commentaires dans l’e-mail de notification envoyé au client ou à la cliente, cochez la case **[!UICONTROL Append Comments]** .

   - Pour vous envoyer une copie de l’e-mail d’expédition, cochez la case **[!UICONTROL Email Copy of Shipment]** .

     Le statut d’un e-mail de facture s’affiche en regard du numéro de facture de la facture terminée, qu’elle ait été envoyée ou non.

1. Cliquez ensuite sur **[!UICONTROL Submit Shipment]**.

   Le statut de la commande passe de `Processing` à `Complete`.

>[!NOTE]
>
>Si une commande est passée en tant que « livraison en magasin », les options d’expédition ne sont pas disponibles. Cliquez sur **[!UICONTROL Notify Order is Ready for Pickup]** pour déclencher un e-mail au client. Le statut de la commande est alors modifié en `Complete`.

## Afficher les détails de l&#39;expédition

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Recherchez l&#39;expédition dans la liste, puis cliquez pour ouvrir l&#39;enregistrement.

1. Si vous souhaitez ajouter un commentaire à l’ordre, faites défiler l’écran jusqu’à la section _[!UICONTROL Comments History]_, puis saisissez le commentaire dans la zone.

   - Pour envoyer le commentaire au client ou à la cliente par e-mail, cochez la case **[!UICONTROL Notify Customer by Email]** .

   - Pour publier le commentaire dans le compte du client, cochez la case **[!UICONTROL Visible on Frontend]**.

1. Cliquez sur **[!UICONTROL Update]**.

## Suivre l’expédition

**Méthode 1 :** à partir de l’onglet Informations de commande

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l&#39;ordre d&#39;expédition dans la grille, puis cliquez sur **[!UICONTROL View]**.

1. Faites défiler jusqu’à la section _[!UICONTROL Shipping & Handling Information]_&#x200B;et cliquez sur **[!UICONTROL Track Order]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, cliquez sur **[!UICONTROL Close Window]**.

**Méthode 2:** à partir de l&#39;onglet Expédition de la commande

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Recherchez l&#39;expédition dans la liste, puis cliquez pour ouvrir l&#39;enregistrement.

1. Cliquez sur **[!UICONTROL Track this Shipment]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, cliquez sur **[!UICONTROL Close Window]**.
