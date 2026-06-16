---
title: Demande de devis
description: Découvrez comment les clients associés à un compte d’entreprise peuvent soumettre une demande de devis.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
TQID: https://experienceleague.adobe.com/lRPDBgKHCTklbiZ1QWsvXD--n86T-IySJDu9nv-umsU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Demande de devis

Si les devis sont activés dans la configuration [Fonctionnalités de vente](configure-quotes.md), un acheteur autorisé d&#39;une société peut lancer le processus de négociation des prix en demandant un devis dans son panier. Si un acheteur n&#39;est pas prêt à soumettre un devis pour négociation, il peut l&#39;enregistrer en tant que brouillon.

>[!NOTE]
>
>Une demande de devis ne peut pas inclure de codes réduction ou de cartes-cadeaux.

## Expérience de demande de devis client

1. Le client se connecte à son compte utilisateur en tant qu’acheteur avec l’autorisation [autorisation](account-company-roles-permissions.md) pour demander un devis.

1. Ajoute au panier les produits à inclure dans le devis.

   >[!TIP]
   > 
   >Les clients peuvent ajouter plus rapidement une liste de SKU de produit au panier à l’aide de [Commande rapide](quick-order.md).

1. Sélectionne des **[!UICONTROL Request a Quote]**.

   ![Demande de devis à partir du panier](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Dans la zone de **[!UICONTROL Add your comment]**, le client saisit une brève note pour décrire la demande.

1. Saisit un **[!UICONTROL Quote Name]**.

   ![Saisie des commentaires et du nom du devis](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Si nécessaire, joint un document ou une image à la citation :

   - Sélectionne des **[!UICONTROL Attach file]**.
   - Choisit le fichier à partir de son système.

   Par défaut, un [fichier joint](configure-quotes.md) peut atteindre 2 Mo, dans l’un des formats de fichiers suivants : DOC, DOCX, XLS, XLSX, PDF, TXT, JPG ou JPEG, PNG.

1. Crée et traite le devis :

   - Envoie le devis au vendeur en sélectionnant **[!UICONTROL Request a Quote]**.
   - Enregistre le devis en tant que brouillon en sélectionnant **[!UICONTROL Save as Draft]**.

     Si l&#39;acheteur enregistre le devis en tant que brouillon, le devis est disponible en [!UICONTROL My Quotes] à l&#39;état `Draft`. Le vendeur n&#39;a pas accès aux devis provisoires tant que l&#39;acheteur ne les a pas envoyés pour révision.
