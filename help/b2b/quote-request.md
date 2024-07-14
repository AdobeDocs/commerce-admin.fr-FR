---
title: Demande de devis
description: Découvrez comment les clients associés à un compte d’entreprise peuvent envoyer une demande de devis.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Demande de devis

Si les devis sont activés dans la [configuration des fonctionnalités de vente](configure-quotes.md), un acheteur autorisé d’une société peut lancer le processus de négociation des prix en demandant un devis dans son panier. Si un acheteur n&#39;est pas prêt à soumettre un devis à négociation, il peut le conserver en tant que brouillon.

>[!NOTE]
>
>Une demande de devis ne peut pas inclure de codes de réduction ou de cartes-cadeaux.

## Expérience de demande de devis client

1. Le client se connecte à son compte utilisateur en tant qu’acheteur avec l’ [autorisation](account-company-roles-permissions.md) pour demander un devis.

1. Ajoute les produits à inclure dans le guillemet au panier.

   >[!TIP]
   > 
   >Les clients peuvent ajouter plus rapidement une liste de SKU de produit au panier à l’aide de [Quick Order](quick-order.md).

1. Sélectionne **[!UICONTROL Request a Quote]**.

   ![Demande d’un devis dans le panier](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Dans la zone **[!UICONTROL Add your comment]**, le client saisit une brève note pour décrire la requête.

1. Entrez un **[!UICONTROL Quote Name]**.

   ![Saisie des commentaires de guillemet et nom](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Si nécessaire, joint un document ou une image de support au guillemet :

   - Sélectionne **[!UICONTROL Attach file]**.
   - Choisit le fichier à partir de son système.

   Par défaut, un [fichier joint](configure-quotes.md) peut atteindre 2 Mo, dans n’importe quel format de fichier suivant : DOC, DOCX, XLS, XLSX, PDF, TXT, JPG ou JPEG, PNG.

1. Crée et traite le guillemet :

   - Envoie le guillemet au vendeur en sélectionnant **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0-beta fonctionnalité]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme Beta"}**[!UICONTROL Save as Draft]**.

     Si l’acheteur enregistre le guillemet en tant que brouillon, le guillemet est disponible dans l’état [!UICONTROL My Quotes] dans `Draft`. Les versions préliminaires ne sont pas visibles par le vendeur tant que l’acheteur ne les a pas envoyées pour révision.
