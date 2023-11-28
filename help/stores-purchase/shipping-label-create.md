---
title: Création de libellés et de packages d’expédition
description: Découvrez comment regrouper des articles dans une commande et créer des libellés d’expédition.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# Création de libellés d’expédition

Pour créer des étiquettes d’expédition, vous devez d’abord configurer votre compte d’opérateur d’expédition afin de prendre en charge les étiquettes. Suivez ensuite les invites pour saisir une description du package et de son contenu.

Une fois que vous avez configuré les informations sur les étiquettes d’expédition et envoyé une commande, Commerce se connecte au système des opérateurs d’expédition, envoie une commande et reçoit une étiquette d’expédition et un numéro de suivi. Si un libellé d’expédition pour cette cargaison existe dans le système, il est remplacé par un nouveau libellé. Toutefois, les numéros de suivi existants ne sont pas remplacés. Tout nouveau numéro de suivi est ajouté à celui existant.

## Étape 1 : contactez vos opérateurs de transport

Avant de commencer, assurez-vous que vos comptes d’expédition sont configurés pour traiter les libellés. Certains opérateurs peuvent facturer des frais supplémentaires pour ajouter des libellés d’expédition à votre compte.

Contactez chaque opérateur que vous utilisez pour activer les libellés d’expédition pour votre boutique.

Suivez les instructions fournies par chaque opérateur pour ajouter la prise en charge des libellés d’expédition à votre compte.

- **FedEx** - Contact [Services d’intégration Web FedEx][1] pour en savoir plus sur les exigences d’impression d’étiquettes pour votre compte.
- **USPS** - Voir la section [Portail API des outils Web][4] sous le centre d’assistance aux expéditeurs pour savoir comment configurer vos informations d’identification d’impression d’étiquettes.
- **UPS**- Contact [UPS][2] pour confirmer que votre compte prend en charge les libellés d’expédition. Pour générer des libellés d’expédition, vous devez utiliser l’option UPS XML .
- **DHL** - Contact [Solutions de commerce électronique DHL][3] pour en savoir plus sur les exigences d’impression d’étiquettes pour votre compte.

## Etape 2 : mettre à jour la configuration pour chaque opérateur

1. Assurez-vous que la variable [Informations sur le magasin](../getting-started/store-details.md#store-information) est terminée.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Origin]** et configurez les **[!UICONTROL Shipping Origin Address]**.

1. Suivez les instructions ci-dessous pour chaque compte d’opérateur activé pour l’impression de libellés.

### Configuration UPS

United Parcel Service est expédié tant au pays qu&#39;à l&#39;étranger. Cependant, les étiquettes d’expédition ne peuvent être générées que pour les envois provenant des États-Unis.

1. Dans le _[!UICONTROL Sales]_dans le panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL UPS]** .

1. Vérifiez que votre onduleur **[!UICONTROL Shipper Number]** est correcte.

   Votre numéro d’expéditeur s’affiche uniquement lorsque [!DNL United Parcel Service XML] est activée.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration USPS

La variable [!DNL United States Postal Service] des navires tant à l&#39;intérieur qu&#39;à l&#39;étranger.

1. Dans la section **[!UICONTROL Delivery Methods]** configuration, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL USPS]** .

1. Vérifiez que la variable **[!UICONTROL Secure Gateway URL]** est correcte.

1. Saisissez le **[!UICONTROL Password]** fourni par USPS.

1. Définir **[!UICONTROL Size]** to `Large` et saisissez les valeurs des dimensions suivantes :

   - Longueur
   - Largeur
   - Hauteur
   - Fille

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration de FedEx

FedEx embarque sur le plan intérieur et international. Les magasins situés en dehors des États-Unis peuvent créer des étiquettes FedEx pour les envois internationaux uniquement.

{{beta2-updates}}

1. Dans la section **[!UICONTROL Delivery Methods]** configuration, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL FedEx]** .

1. Vérifiez que les informations d’identification FedEx suivantes sont correctes :

   - Nombre de mètres
   - Clé
   - Mot de passe

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration DHL

DHL fournit des services de transport international.

1. Dans la section **[!UICONTROL Delivery Methods]** configuration, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL DHL]** .

1. Vérifiez que la variable **[!UICONTROL Gateway URL]** est correcte.

1. Vérifiez que les informations d’identification suivantes sont terminées :

   - Identifiant d’accès
   - Mot de passe
   - Numéro de compte

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 3 : création de libellés d’expédition

### Méthode 1 : créer un libellé pour la nouvelle livraison

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre dans la grille et ouvrez l’enregistrement.

   L’état de la commande doit être : `Pending` ou `Processing`.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Ship]**.

1. Confirmez les informations d’expédition en fonction des exigences de l’opérateur.

1. Dans le coin inférieur droit, sélectionnez la variable **[!UICONTROL Create Shipping Label]** .

1. Cliquez sur **[!UICONTROL Submit Shipment]**.

1. Ajouter ou mettre à jour des produits dans un package :

   - Pour ajouter des produits de la commande au module, cliquez sur **[!UICONTROL Add Products]**. La variable _[!UICONTROL Quantity]_indique le nombre maximal de produits disponibles pour le module.

   - Cochez la case de chaque produit à ajouter au package, puis saisissez le **[!UICONTROL Quantity]** de chacun. Cliquez ensuite sur **[!UICONTROL Add Selected Product(s) to Package]**.

   - Pour ajouter un package, cliquez sur **[!UICONTROL Add Package]**.

   - Pour supprimer un module, cliquez sur **[!UICONTROL Delete Package]**.

   - Pour annuler une commande, cliquez sur **[!UICONTROL Cancel]**. Une étiquette d’expédition n’est pas créée, et la variable _[!UICONTROL Create Shipping Label]_est désactivée.

   >[!NOTE]
   >
   >Si vous utilisez un type de package autre que le type par défaut ou que vous exigez une signature, le coût de livraison peut différer de celui que vous avez facturé au client. Toute différence de coût d’expédition n’est pas prise en compte dans votre boutique.

1. Cliquez sur **[!UICONTROL OK]**.

   Commerce se connecte au système de l’opérateur de transport, envoie la commande et reçoit un libellé d’expédition et un numéro de suivi pour chaque package.

### Méthode 2 : créer un libellé pour une expédition existante

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Recherchez la commande dans la grille et ouvrez le formulaire de livraison.

1. Dans le _[!UICONTROL Shipping and Tracking Information]_, cliquez sur **[!UICONTROL Create Shipping Label]**.

1. Distribuez les produits commandés dans les packages appropriés et cliquez sur **[!UICONTROL OK]**.

1. Pour consulter les informations du module, cliquez sur **[!UICONTROL Show Packages]**.

## Étape 4 : Imprimer les libellés

Les libellés d’expédition sont générés au format PDF et peuvent être imprimés à partir de l’administrateur. Chaque libellé comprend le numéro de commande et le numéro du package.

>[!NOTE]
>
>Comme une commande d’expédition individuelle pour chaque package est créée, plusieurs étiquettes d’expédition peuvent être reçues pour une seule livraison.

### Méthode 1 : imprimer le libellé du formulaire d’expédition

1. Sur le _Barre latérale d’administration_, accédez à l’une des pages suivantes, puis localisez l’enregistrement d’expédition :

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Recherchez l’ordre dans la grille et ouvrez l’enregistrement. Dans le panneau de gauche, choisissez **[!UICONTROL Shipments]**. Ouvrez ensuite l’enregistrement de l’expédition.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Recherchez l&#39;envoi dans la grille et ouvrez l&#39;enregistrement.

1. Pour télécharger le fichier du PDF, accédez au _[!UICONTROL Shipping and Tracking]_du formulaire, puis cliquez sur **[!UICONTROL Print Shipping Label]**.

   Selon les paramètres de votre navigateur, les libellés d’expédition peuvent être affichés et imprimés directement à partir du fichier du PDF.

   La variable _[!UICONTROL Print Shipping Label]_n’apparaît qu’une fois que le fournisseur a généré les étiquettes pour l’envoi. Si le bouton est manquant, cliquez sur **[!UICONTROL Create Shipping Label]**. Le bouton s’affiche une fois que Commerce a reçu le libellé de l’opérateur.

### Méthode 2 : impression des libellés pour plusieurs commandes

1. Sur le _Barre latérale d’administration_, accédez à l’une des pages suivantes, puis sélectionnez les commandes ou les envois à imprimer :

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Dans la grille, cochez la case de chaque commande avec les libellés d’expédition à imprimer.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Dans la grille, cochez la case de chaque envoi avec les libellés à imprimer.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Print Shipping Labels`.

1. Cliquez sur **[!UICONTROL Submit]**.

Un ensemble complet de libellés d’expédition est imprimé pour chaque envoi associé aux commandes sélectionnées.

## Paramètres de l’opérateur requis

| Champ | Description |
|--- |--- |
| [!UICONTROL Type] | Les types de packages diffèrent selon l’opérateur et la méthode. Le type de package par défaut pour chaque opérateur est initialement sélectionné. USPS ne nécessite pas le type de package pour les envois intérieurs. |
| [!UICONTROL Customs Value] | (Transferts internationaux uniquement) Valeur déclarée ou prix de vente du contenu d’une cargaison internationale. |
| [!UICONTROL Total Weight] | Le poids total de tous les produits ajoutés au kit est calculé automatiquement. La valeur peut également être modifiée manuellement et saisie en kilos ou en kilos. |
| [!UICONTROL Length, Width, Height] | (Facultatif) Les dimensions du module sont utilisées uniquement pour les modules personnalisés. Vous pouvez spécifier les unités de mesure en pouces ou en centimètres.<br/><br/>**[!UICONTROL Not Required]**: aucune confirmation de livraison n&#39;est envoyée au magasin par le transporteur.<br/><br/>**[!UICONTROL No Signature]**: une confirmation de diffusion sans signature du destinataire est envoyée au magasin par le transporteur.<br/><br/>**[!UICONTROL Signature Required]**: le transporteur obtient la signature du destinataire et fournit au magasin une copie imprimée.<br/><br/>**[!UICONTROL Direct]**: (FedEx uniquement) FedEx obtient une signature d’une personne à l’adresse de livraison. Si personne n’est disponible pour signer le package, l’opérateur tente de le livrer à un autre moment.<br/><br/>**[!UICONTROL Indirect]**: (Diffusions résidentielles FedEx uniquement) FedEx obtient la signature d’une personne (éventuellement un voisin ou un responsable de construction) à l’adresse de diffusion. Le destinataire peut laisser une balise de porte FedEx signée pour autoriser le paquet à laisser sans que personne ne soit présent pour le signer.<br/><br/>**[!UICONTROL Contents]**: (USPS uniquement) sélectionnez l’une des descriptions suivantes du package :<br/>- Cadeau<br/>- Documents<br/>- Exemple commercial<br/>- Biens retournés<br/>- Marchandisage<br/>- Autre <br/><br/>**[!UICONTROL Explanation]**: (USPS uniquement) description détaillée du contenu du package.<br/><br/>**[!UICONTROL Adult Required]**: le transporteur obtient la signature d&#39;un destinataire adulte et fournit au magasin une copie imprimée. |

{style="table-layout:auto"}

## Création de packages

La variable _[!UICONTROL Create Packages]_s’affiche lorsque vous choisissez de créer un libellé d’expédition. Vous pouvez commencer à configurer le premier module immédiatement.

### Configuration d’un module

>[!NOTE]
>
>Si vous sélectionnez la valeur autre que la valeur par défaut pour la variable [!UICONTROL Type] ou choisissez d&#39;exiger une confirmation de signature, le prix d&#39;une cargaison peut différer de celui que vous avez facturé au client.

1. Pour afficher une liste des produits expédiés et les ajouter au module, cliquez sur **[!UICONTROL Add Products]**.

   - Indiquez les produits et les quantités.

     La variable _[!UICONTROL Qty]_indique la quantité maximale pouvant être ajoutée. Pour le premier package, le nombre correspond à la quantité totale du produit à expédier.

   - Pour ajouter les produits au package, cliquez sur **[!UICONTROL Add Selected Product(s) to Package]**.

1. Pour ajouter un package, cliquez sur **[!UICONTROL Add Package]**.

   Vous pouvez ajouter plusieurs packages et les modifier simultanément.

1. Pour supprimer un module, cliquez sur **[!UICONTROL Delete Package]**.

Une fois les produits ajoutés au package, la quantité ne peut pas être modifiée directement.

### Augmenter la quantité

1. Cliquez sur **[!UICONTROL Add Selection]**.

1. Saisissez la quantité supplémentaire.

   Le nombre est ajouté à la quantité précédente du produit dans le package.

### Réduire la quantité

1. Supprimez le produit du package.

1. Cliquez sur **[!UICONTROL Add Selection]**.

1. Saisissez la nouvelle valeur plus petite.

### Générer des libellés d’expédition

Une fois tous les produits distribués, le nombre total de packages que vous allez utiliser est égal au nombre du dernier package de la liste. La variable _OK_ est désactivé tant que tous les éléments envoyés ne sont pas distribués aux modules et que toutes les informations nécessaires ne sont pas complètes.

Pour générer les libellés, cliquez sur **[!UICONTROL OK]**.

Cliquez sur **[!UICONTROL Cancel]** pour arrêter le processus, si nécessaire. Les packages ne sont pas enregistrés et le traitement des libellés d’expédition est annulé.

### Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Type] | Indique le type d’un module. Sélectionnez l’une des valeurs prédéfinies. Les types de packages disponibles sont différents pour chaque opérateur de livraison. Lorsque la fenêtre contextuelle Créer des packages s’ouvre, le package par défaut de l’opérateur de livraison s’affiche dans le champ Type . Si vous sélectionnez un package qui n’est pas conçu par un opérateur de livraison, vous devez saisir les dimensions du package. Pour les libellés d’expédition créés pour les envois DHL, FedEx et UPS, le champ Type de marchandises est défini sur `Merchandise`. Pour USPS, le champ reflète la valeur de la variable _Contenu_ dans le champ _[!UICONTROL Create Packages]_fenêtre. |
| [!UICONTROL Total Weight] | Le poids total d’un kit. Le champ est prérenseigné avec le poids total des produits dans un package. L&#39;unité de mesure peut être fixée à l&#39;unité de mesure soit en kilos, soit en kilogrammes. |
| [!UICONTROL Length] | Longueur d’un package, nombre entier et nombre à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. L’unité de mesure peut être définie sur pouces ou centimètres. |
| [!UICONTROL Width] | Largeur d’un package, nombre entier et nombre à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. Les unités de mesure peuvent être spécifiées à l&#39;aide du menu déroulant situé en regard du champ Hauteur ; sélectionnez entre pouces et centimètres. |
| [!UICONTROL Height] | Hauteur d’un package, nombre entier et nombre à virgule flottante. Le champ est activé si le type de package personnalisé est utilisé. Les unités de mesure peuvent être spécifiées à l&#39;aide du menu déroulant situé en regard du champ Hauteur ; sélectionnez entre pouces et centimètres. |
| [!UICONTROL Signature] | Définit la confirmation de diffusion. Options :<br/><br/>**[!UICONTROL Not Required]**: aucune lettre de confirmation de diffusion ne vous est envoyée.<br/><br/>**[!UICONTROL No Signature]**: une lettre de confirmation de diffusion sans signature du destinataire vous est envoyée.<br/><br/>**[!UICONTROL Signature Required]**: le transporteur obtient la signature du destinataire et vous fournit sa copie imprimée.<br/><br/>**[!UICONTROL Adult Required]**: le transporteur obtient la signature du destinataire adulte et vous fournit sa copie imprimée.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx obtient la signature d’une personne à l’adresse de livraison et tente à nouveau la livraison si personne n’est disponible pour signer le kit.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx obtient une signature de l’une des trois façons suivantes :<br/>(1) d&#39;une personne à l&#39;adresse de livraison ; <br/>(2) d’un voisin, d’un directeur de construction ou d’une autre personne à l’adresse ; ou <br/>(3) le destinataire peut laisser une balise FedEx Door signée autorisant la publication du package sans que personne ne soit présent. Disponible uniquement pour les diffusions résidentielles. Les options peuvent varier légèrement en fonction des différents modes de livraison. Pour obtenir les informations les plus récentes, reportez-vous aux ressources de l’opérateur de transport. |
| [!UICONTROL Contents] | (Disponible pour les envois USPS uniquement) Description du contenu du package. Options : `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Livraisons USPS uniquement) Description détaillée du contenu du package. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
