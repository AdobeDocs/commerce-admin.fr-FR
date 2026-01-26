---
title: Créer des étiquettes et des colis d'expédition
description: Découvrez comment conditionner des articles dans une commande et créer des étiquettes d’expédition.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Créer des étiquettes d&#39;expédition

Pour créer des étiquettes d&#39;expédition, vous devez d&#39;abord configurer votre compte de transporteur pour prendre en charge les étiquettes. Suivez ensuite les invites pour saisir une description du package et de son contenu.

Une fois que vous avez configuré les informations sur l’étiquette d’expédition et envoyé une commande, Commerce se connecte au système du transporteur, envoie une commande et reçoit une étiquette d’expédition et un numéro de suivi. Si une étiquette d&#39;expédition pour cette expédition existe dans le système, elle est remplacée par une nouvelle. Toutefois, les numéros de suivi existants ne sont pas remplacés. Tout nouveau numéro de suivi est ajouté au numéro existant.

## Étape 1 : Contactez votre transporteur

Avant de commencer, assurez-vous que vos comptes d&#39;expédition sont configurés pour traiter les étiquettes. Certains transporteurs peuvent facturer des frais supplémentaires pour ajouter des étiquettes d&#39;expédition à votre compte.

Contactez chaque transporteur que vous utilisez pour activer les étiquettes d&#39;expédition pour votre magasin.

Suivez les instructions fournies par chaque transporteur pour ajouter la prise en charge des étiquettes d’expédition à votre compte.

- **FedEx** - Contactez [FedEx Web Integration Services](https://www.fedex.com/en-us/api/get-support.html) pour en savoir plus sur les exigences en matière d&#39;impression d&#39;étiquettes pour votre compte.
- **USPS** - Reportez-vous au [Portail d&#39;API des outils Web](https://www.usps.com/business/web-tools-apis/#ssc) sous Centre de support des expéditeurs pour savoir comment configurer vos informations d&#39;identification d&#39;impression d&#39;étiquettes.
- **UPS**- Contactez [UPS](https://www.ups.com/us/en/support/contact-us.page) pour confirmer que votre compte prend en charge les étiquettes d&#39;expédition. Pour générer des étiquettes d&#39;expédition, vous devez utiliser l&#39;option XML UPS.
- **DHL** - Contactez [DHL eCommerce Solutions](https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html) pour en savoir plus sur les conditions d’impression des étiquettes pour votre compte.

## Étape 2 : mettre à jour la configuration pour chaque opérateur

1. Assurez-vous que les [Informations de la boutique](../getting-started/store-details.md#store-information) sont complètes.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Origin]** et configurez le **[!UICONTROL Shipping Origin Address]**.

1. Suivez les instructions ci-dessous pour chaque compte d’opérateur activé pour l’impression des étiquettes.

### Configuration de l&#39;onduleur

United Parcel Service expédie des colis au Canada et à l&#39;étranger. Toutefois, les étiquettes d&#39;expédition ne peuvent être générées que pour les expéditions provenant des États-Unis.

1. Dans la section _[!UICONTROL Sales]_du panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL UPS]** .

1. Vérifiez que votre onduleur **[!UICONTROL Shipper Number]** est correct.

   Votre numéro d&#39;expéditeur s&#39;affiche uniquement lorsque [!DNL United Parcel Service XML] est activé.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration USPS

Le [!DNL United States Postal Service] est expédié tant au Canada qu&#39;à l&#39;étranger.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. En poursuivant dans la configuration **[!UICONTROL Delivery Methods]**, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL USPS]** .

1. Sélectionnez **[!UICONTROL USPS Type]** comme `USPS Rest APIs` ou `USPS Web Tools API`.

1. Vérifiez que la **[!UICONTROL Secure Gateway URL]** est correcte.

1. Entrez le **[!UICONTROL Password]** qui vous a été fourni par USPS.

1. Vérifiez que la configuration suivante est terminée en fonction de l’**[!UICONTROL USPS Type]** sélectionnée :

   Si vous utilisez l&#39;API des outils Web USPS :
   - Identifiant De L&#39;Utilisateur
   - Mot de passe

   Si vous utilisez les API REST USPS :
   - Clé du client
   - Secret du client
   - Options de tarification
   - Type de compte
   - Numéro de compte
   - ID d’enregistrement du client (CRID)
   - Identifiant de l’expéditeur (MID)
   - MID du manifeste
   - AES/ITN

1. Définissez **[!UICONTROL Size]** sur `Large` et saisissez des valeurs pour les dimensions suivantes :

   - Longueur
   - Largeur
   - Hauteur
   - Naissance

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration de FedEx

FedEx expédie ses produits au pays et à l&#39;étranger. Les magasins situés en dehors des États-Unis peuvent créer des étiquettes FedEx pour les expéditions internationales uniquement.

1. En poursuivant dans la configuration **[!UICONTROL Delivery Methods]**, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL FedEx]** .

1. Vérifiez que les informations d’identification FedEx suivantes sont correctes :

   - Numéro du compteur
   - Clé
   - Mot de passe

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration DHL

DHL fournit des services de transport maritime international.

1. En poursuivant dans la configuration **[!UICONTROL Delivery Methods]**, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL DHL]** .

1. Vérifiez que la **[!UICONTROL Gateway URL]** est correcte.

1. Vérifiez que les informations d’identification suivantes sont complètes :

   - ID d’accès
   - Mot de passe
   - Numéro de compte

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 3 : Créer des étiquettes d&#39;expédition

### Méthode 1 : créer une étiquette pour une nouvelle expédition

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez la commande dans la grille et ouvrez l’enregistrement.

   Le statut de la commande doit être `Pending` ou `Processing`.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Ship]**.

1. Confirmez les informations d’expédition conformément aux exigences du transporteur.

1. Dans le coin inférieur droit, cochez la case **[!UICONTROL Create Shipping Label]** .

1. Cliquez sur **[!UICONTROL Submit Shipment]**.

1. Ajouter ou mettre à jour des produits dans le package :

   - Pour ajouter des produits de la commande au package, cliquez sur **[!UICONTROL Add Products]**. La colonne _[!UICONTROL Quantity]_indique le nombre maximal de produits disponibles pour le package.

   - Cochez la case de chaque produit à ajouter au package et saisissez le **[!UICONTROL Quantity]** de chacun. Cliquez ensuite sur **[!UICONTROL Add Selected Product(s) to Package]**.

   - Pour ajouter un package, cliquez sur **[!UICONTROL Add Package]**.

   - Pour supprimer un package, cliquez sur **[!UICONTROL Delete Package]**.

   - Pour annuler une commande, cliquez sur **[!UICONTROL Cancel]**. Aucune étiquette d&#39;expédition n&#39;est créée et la case à cocher _[!UICONTROL Create Shipping Label]_est désactivée.

   >[!NOTE]
   >
   >Si vous utilisez un type de package autre que le type par défaut ou que vous avez besoin d&#39;une signature, les frais d&#39;expédition peuvent être différents de ceux que vous avez facturés au client. Toute différence de coût d&#39;expédition n&#39;est pas reflétée dans votre magasin.

1. Cliquez sur **[!UICONTROL OK]**.

   Commerce se connecte au système du transporteur, soumet la commande et reçoit une étiquette d’expédition et un numéro de suivi pour chaque colis.

### Méthode 2 : créer une étiquette pour l&#39;expédition existante

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Recherchez la commande dans la grille et ouvrez le formulaire d’expédition.

1. Dans la section _[!UICONTROL Shipping and Tracking Information]_, cliquez sur **[!UICONTROL Create Shipping Label]**.

1. Distribuez les produits commandés aux packages appropriés et cliquez sur **[!UICONTROL OK]**.

1. Pour consulter les informations sur le package, cliquez sur **[!UICONTROL Show Packages]**.

## Étape 4 : Imprimer les étiquettes

Les étiquettes d&#39;expédition sont générées au format PDF et peuvent être imprimées à partir de l&#39;administrateur. Chaque étiquette comprend le numéro de commande et le numéro de colis.

>[!NOTE]
>
>Comme une commande d&#39;expédition individuelle pour chaque colis est créée, plusieurs étiquettes d&#39;expédition peuvent être reçues pour une seule expédition.

### Méthode 1 : imprimer l&#39;étiquette à partir du formulaire d&#39;expédition

1. Dans la barre latérale _Admin_, accédez à l’une des pages suivantes, puis recherchez l’enregistrement de l’expédition :

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Recherchez la commande dans la grille et ouvrez l’enregistrement. Dans le panneau de gauche, choisissez **[!UICONTROL Shipments]**. Ouvrez ensuite l’enregistrement de l’expédition.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Recherchez l&#39;expédition dans la grille et ouvrez l&#39;enregistrement.

1. Pour télécharger le fichier PDF, accédez à la section _[!UICONTROL Shipping and Tracking]_du formulaire et cliquez sur **[!UICONTROL Print Shipping Label]**.

   Selon les paramètres de votre navigateur, les étiquettes d’expédition peuvent être affichées et imprimées directement à partir du fichier PDF.

   Le bouton _[!UICONTROL Print Shipping Label]_n&#39;apparaît qu&#39;une fois que le transporteur a généré les étiquettes pour l&#39;expédition. Si le bouton n’apparaît pas, cliquez sur **[!UICONTROL Create Shipping Label]**. Le bouton apparaît une fois que Commerce a reçu le libellé de l’opérateur.

### Méthode 2 : Imprimer des étiquettes pour plusieurs commandes

1. Dans la barre latérale _Admin_, accédez à l’une des pages suivantes, puis sélectionnez les commandes ou les expéditions à imprimer :

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Dans la grille, cochez la case de chaque commande dont les étiquettes de livraison doivent être imprimées.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Dans la grille, cochez la case de chaque expédition dont les étiquettes doivent être imprimées.

1. Définissez la commande **[!UICONTROL Actions]** sur `Print Shipping Labels`.

1. Cliquez sur **[!UICONTROL Submit]**.

Un jeu complet d&#39;étiquettes d&#39;expédition est imprimé pour chaque expédition associée aux commandes sélectionnées.

## Paramètres d’opérateur requis

| Champ | Description |
|--- |--- |
| [!UICONTROL Type] | Les types de colis diffèrent selon le transporteur et la méthode. Le type de package par défaut de chaque opérateur est initialement sélectionné. USPS n&#39;exige pas le type de colis pour les expéditions nationales. |
| [!UICONTROL Customs Value] | (Expéditions internationales uniquement) Valeur déclarée ou prix de vente du contenu d&#39;une expédition internationale. |
| [!UICONTROL Total Weight] | Le poids total de tous les produits ajoutés au package est calculé automatiquement. La valeur peut également être modifiée manuellement et saisie en livres ou en kilogrammes. |
| [!UICONTROL Length, Width, Height] | (Facultatif) Les dimensions de package sont utilisées uniquement pour les packages personnalisés. Vous pouvez indiquer les unités de mesure en pouces ou en centimètres.<br/><br/>**[!UICONTROL Not Required]**: Aucune confirmation de livraison n&#39;est envoyée au magasin par le transporteur.<br/><br/>**[!UICONTROL No Signature]** : Une confirmation de livraison sans la signature du destinataire est envoyée au magasin par le transporteur.<br/><br/>**[!UICONTROL Signature Required]**: Le transporteur obtient la signature du destinataire et fournit au magasin une copie imprimée.<br/><br/>**[!UICONTROL Direct]** : (FedEx uniquement) FedEx obtient une signature de quelqu’un à l’adresse de livraison. Si personne n&#39;est disponible pour signer le colis, le transporteur essaie de livrer le colis à un autre moment.<br/><br/>**[!UICONTROL Indirect]**: (Livraisons à domicile FedEx uniquement) FedEx obtient la signature d&#39;une personne (éventuellement un voisin ou un chef d&#39;immeuble) à l&#39;adresse de livraison. Le destinataire peut laisser une étiquette de porte FedEx signée pour autoriser le colis à être laissé sans que personne ne soit présent pour la signer.<br/><br/>**[!UICONTROL Contents]** : (USPS uniquement) Sélectionnez l’une des descriptions suivantes du colis :<br/>- Cadeau<br/>- Documents<br/>- Échantillon commercial<br/>- Marchandises retournées<br/>- Marchandises<br/>- Autre <br/><br/>**[!UICONTROL Explanation]**: (USPS uniquement) Une description détaillée du contenu du colis.<br/><br/>**[!UICONTROL Adult Required]** : Le transporteur obtient la signature d&#39;un destinataire adulte et fournit au magasin une copie imprimée. |

{style="table-layout:auto"}

## Créer des packages

La fenêtre _[!UICONTROL Create Packages]_s&#39;affiche lorsque vous choisissez de créer une étiquette d&#39;expédition. Vous pouvez commencer à configurer le premier package immédiatement.

### Configuration d’un package

>[!NOTE]
>
>Si vous sélectionnez une valeur autre que la valeur par défaut pour le [!UICONTROL Type] ou si vous choisissez d&#39;exiger une confirmation de signature, le prix d&#39;une expédition peut différer de celui que vous avez facturé au client.

1. Pour afficher la liste des produits expédiés et les ajouter au package, cliquez sur **[!UICONTROL Add Products]**.

   - Spécifiez les produits et les quantités.

     La colonne _[!UICONTROL Qty]_indique la quantité maximale pouvant être ajoutée. Pour le premier colis, le numéro correspond à la quantité totale du produit à expédier.

   - Pour ajouter les produits au package, cliquez sur **[!UICONTROL Add Selected Product(s) to Package]**.

1. Pour ajouter un package, cliquez sur **[!UICONTROL Add Package]**.

   Vous pouvez ajouter plusieurs packages et les modifier en même temps.

1. Pour supprimer un package, cliquez sur **[!UICONTROL Delete Package]**.

Une fois les produits ajoutés au package, la quantité ne peut pas être modifiée directement.

### Augmenter la quantité

1. Cliquez sur **[!UICONTROL Add Selection]**.

1. Saisissez la quantité supplémentaire.

   Le numéro est ajouté à la quantité précédente du produit dans l&#39;emballage.

### Diminuer la quantité

1. Supprimez le produit du package.

1. Cliquez sur **[!UICONTROL Add Selection]**.

1. Saisissez la nouvelle valeur, plus petite.

### Générer les étiquettes d&#39;expédition

Après avoir distribué tous les produits, le nombre total de packages que vous allez utiliser est égal au numéro du dernier package de la liste. Le bouton _OK_ est désactivé jusqu&#39;à ce que tous les articles expédiés soient distribués aux packages et que toutes les informations nécessaires soient terminées.

Pour générer les libellés, cliquez sur **[!UICONTROL OK]**.

Vous pouvez cliquer sur **[!UICONTROL Cancel]** pour arrêter le processus, si nécessaire. Les colis ne sont pas enregistrés et le traitement de l&#39;étiquette d&#39;expédition est annulé.

### Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Type] | Spécifie le type d&#39;un package. Sélectionnez l’une des valeurs prédéfinies. Les types de colis disponibles sont différents pour chaque transporteur. Lorsque la fenêtre pop-up Créer des packages s’ouvre, le package par défaut du transporteur apparaît dans le champ Type. Si vous sélectionnez un colis qui n&#39;est pas conçu par un transporteur, vous devez entrer les dimensions du colis. Pour les étiquettes d&#39;expédition créées pour les expéditions DHL, FedEx et UPS, le champ Type de marchandises est défini sur `Merchandise`. Pour USPS, le champ reflète la valeur du champ _Contenu_ dans la fenêtre de _[!UICONTROL Create Packages]_. |
| [!UICONTROL Total Weight] | Poids total d’un package. Le champ est prérenseigné avec le poids total des produits dans un package. L&#39;unité de mesure peut être définie sur des livres ou des kilogrammes. |
| [!UICONTROL Length] | Longueur d’un package, entier et nombres à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. L’unité de mesure peut être définie sur pouces ou centimètres. |
| [!UICONTROL Width] | Largeur d’un package, entier et nombres à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. Les unités de mesure peuvent être spécifiées à l&#39;aide du menu déroulant en regard du champ Hauteur ; choisissez entre pouces et centimètres. |
| [!UICONTROL Height] | Hauteur d’un package, d’un entier et de nombres à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. Les unités de mesure peuvent être spécifiées à l&#39;aide du menu déroulant en regard du champ Hauteur ; choisissez entre pouces et centimètres. |
| [!UICONTROL Signature] | Définit la confirmation de diffusion. Options : <br/><br/>**[!UICONTROL Not Required]**: aucune lettre de confirmation de livraison ne vous est envoyée.<br/><br/>**[!UICONTROL No Signature]** : une lettre de confirmation de diffusion sans signature du destinataire vous est envoyée.<br/><br/>**[!UICONTROL Signature Required]**: Le transporteur obtient la signature du destinataire et vous fournit sa copie imprimée.<br/><br/>**[!UICONTROL Adult Required]** : Le transporteur obtient la signature du destinataire adulte et vous fournit sa copie imprimée.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx obtient la signature d&#39;une personne à l&#39;adresse de livraison et tente à nouveau la livraison si personne n&#39;est disponible pour signer le paquet.<br/><br/>**[!UICONTROL Indirect (FedEx only)]** : FedEx obtient une signature de l&#39;une des trois façons suivantes : <br/>(1) d&#39;une personne à l&#39;adresse de livraison ; <br/>(2) d&#39;un voisin, d&#39;un directeur d&#39;immeuble ou d&#39;une autre personne à l&#39;adresse ; ou <br/>(3) le destinataire peut laisser une étiquette de porte FedEx signée autorisant la sortie du colis sans la présence de personne. Disponible uniquement pour les diffusions résidentielles. Les options peuvent varier légèrement selon les modes d&#39;expédition. Pour obtenir les informations les plus récentes, consultez les ressources du transporteur. |
| [!UICONTROL Contents] | (Disponible uniquement pour les expéditions USPS) Description du contenu du colis. Options : `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Expéditions USPS uniquement) Description détaillée du contenu du colis. |

{style="table-layout:auto"}


<!-- Last updated from includes: 2025-11-26 10:55:00 -->
