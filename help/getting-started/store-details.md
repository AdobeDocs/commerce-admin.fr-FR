---
title: Détails de la boutique
description: Découvrez comment mettre à jour les informations de base de votre boutique.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1780'
ht-degree: 0%

---

# Détails de la boutique

Les informations de base de votre boutique incluent le nom et l’adresse du magasin, le numéro de téléphone et l’adresse électronique qui apparaissent dans les emails, les factures et autres communications envoyés à vos clients.

![Configuration générale - détails du magasin](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

La section _[!UICONTROL Store Information]_&#x200B;fournit les informations de base qui apparaissent sur les documents de vente et dans d’autres communications.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous **[!UICONTROL General]** dans le panneau de navigation de gauche, sélectionnez **[!UICONTROL General]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Store Information]** .

   ![Configuration générale - informations de magasin](./assets/general-store-information.png){width="700"}

1. Définissez les options en fonction des détails de votre boutique :

   - Saisissez le **[!UICONTROL Store Name]** que vous souhaitez utiliser dans toutes les communications.

   - Saisissez le **[!UICONTROL Store Phone Number]**, formaté tel que vous souhaitez le voir apparaître.

   - Pour **[!UICONTROL Store Hours of Operation]**, saisissez les heures d’ouverture de votre boutique. Par exemple : `Mon - Fri, 9-5, Sat 9-noon PST`.

   - Sélectionnez l’ **[!UICONTROL Country]** où se trouve votre entreprise.

   - Sélectionnez le **[!UICONTROL Region/State]** avec le pays.

   - Saisissez le **[!UICONTROL Store Address]**. Si l’adresse est longue, continuez l’adresse sur la **ligne d’adresse du magasin 2**.

   - Le cas échéant, saisissez le **[!UICONTROL VAT Number]** de votre boutique.

     Pour vérifier le nombre, cliquez sur le bouton **[!UICONTROL Validate VAT Number]** . Pour en savoir plus, voir [Validation de l’ID de TVA](../stores-purchase/vat.md#vat-id-validation).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration des informations de magasin, consultez le [_Guide de référence de configuration_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

Le paramètre régional détermine la plupart des paramètres utilisés dans l’ensemble du magasin. En voici quelques-uns :

- Langue
- Pays
- Taux d&#39;imposition
- Devise
- Prix
- Format des nombres

Le paramètre régional détermine le fuseau horaire et la langue utilisés pour chaque magasin et identifie les jours de la semaine de travail dans la zone.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL General]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Locale Options]** .

   ![Configuration générale - Options des paramètres régionaux](./assets/general-locale-options.png){width="700"}

1. Sélectionnez votre **[!UICONTROL Timezone]** dans la liste.

1. Définissez **[!UICONTROL Locale]** sur la langue du magasin.

1. Définissez **[!UICONTROL Weight Unit]** sur l’unité de mesure généralement utilisée pour les envois à partir de vos paramètres régionaux.

1. Définissez **[!UICONTROL First Day of the Week]** sur le jour considéré comme le premier jour de la semaine dans votre zone.

1. Dans la liste **[!UICONTROL Weekend Days]**, sélectionnez les jours qui tombent un week-end dans votre zone.

   Pour sélectionner plusieurs jours, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration des paramètres régionaux, consultez le [Guide de référence de configuration](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

Dans de nombreux pays, l’État, la province ou la région est une partie obligatoire d’une adresse postale. Ces informations sont utilisées pour les informations d’expédition et de facturation, pour le calcul des taux d’imposition, etc. Pour les pays où l’état n’est pas obligatoire, le champ peut être entièrement omis de l’adresse ou inclus comme champ facultatif.

Comme les formats d’adresse standard varient d’un pays à l’autre, vous pouvez également modifier le modèle utilisé pour formater l’adresse pour les factures, les bordereaux d’emballage et les libellés de livraison.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous **[!UICONTROL General]** dans le panneau de navigation de gauche, sélectionnez **[!UICONTROL General]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL State Options]** .

   ![Configuration générale - options d’état](./assets/general-state-options.png){width="700"}

1. Utilisez la liste **[!UICONTROL State is required for]** pour sélectionner chaque pays où Région/État est une entrée obligatoire.

1. Définissez **[!UICONTROL Allow to Choose State if it is Optional for Country]** sur l’une des options suivantes :

   `Yes` - Dans les pays où le champ d’état n’est pas obligatoire, inclut le champ État en tant qu’entrée facultative.

   `No` - Dans les pays où le champ d’état n’est pas obligatoire, omet le champ Etat .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration de l’état, consultez le [Guide de référence de configuration](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

Les options de pays identifient le pays dans lequel votre entreprise se trouve et les pays d’où vous acceptez le paiement.

### Définition des options de pays pour votre magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL General]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Country Options]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour chaque paramètre que vous souhaitez modifier.

   ![Configuration générale - paramètres du pays](./assets/general-country-options.png){width="700"}

1. Sélectionnez l’ **[!UICONTROL Default Country]** où se trouve votre entreprise.

1. Dans la liste **[!UICONTROL Allow Countries]**, sélectionnez chaque pays à partir duquel vous acceptez des commandes.

   Par défaut, tous les pays de la liste sont sélectionnés. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

1. Utilisez la liste **[!UICONTROL Zip/Postal Code is Optional for]** pour sélectionner chaque pays dans lequel vous dirigez une entreprise qui ne nécessite pas l&#39;inclusion d&#39;un code postal dans l&#39;adresse postale.

1. Dans la liste **[!UICONTROL European Union Countries]**, sélectionnez chaque pays de l’UE dans lequel vous dirigez des activités.

   Par défaut, tous les pays de l’UE sont sélectionnés. Pour sélectionner les pays dont vous avez besoin, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée et cliquez sur chaque élément.

1. Dans la liste **[!UICONTROL Top Destinations]**, sélectionnez les pays principaux que vous ciblez pour les ventes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Définition des options de pays pour un mode de remise spécifique

Vous pouvez également configurer la livraison vers des pays spécifiques pour chaque [méthode de livraison](../stores-purchase/delivery.md) disponible (UPS, FedEx, etc.).

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Sélectionnez le transporteur auquel vous souhaitez appliquer des pays spécifiques.

1. Pour **[!UICONTROL Ship to Applicable Countries]**, désélectionnez la case **[!UICONTROL Use system value]** et sélectionnez l’option **[!UICONTROL Specific Countries]**.

1. Dans la liste **[!UICONTROL Top Destinations]**, sélectionnez les pays principaux que vous ciblez pour la livraison.

   ![Exemple de définition des options de pays pour la méthode de remise DHL](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Ressources de dépannage

Pour obtenir de l’aide sur la résolution des problèmes de configuration des pays, reportez-vous aux [!DNL Commerce] articles suivants de la base de connaissances d’assistance :

- [Comment ajouter un pays](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html?lang=fr)

## [!UICONTROL Merchant Location]

Le paramètre Merchant Location est utilisé pour configurer les [méthodes de paiement](../stores-purchase/payments.md). S’il n’existe aucune valeur pour ce paramètre, le paramètre [Default Country](#uicontrol-country-options) est utilisé.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de la **Emplacement du magasin** et choisissez votre **[!UICONTROL Merchant Country]**.

   ![ Paramètre de position du site marchand ](./assets/payment-methods-merchant-location.png){width="600"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration des méthodes de paiement, consultez le [Guide de référence de configuration](../configuration-reference/sales/payment-methods.md).

## Devise

Configuration de devise : définit la [devise](../stores-purchase/currency-configuration.md) de base et toute autre devise acceptée comme paiement. Établit également la connexion et le planning d&#39;import utilisés pour mettre à jour automatiquement les taux de change.

Symboles de devise : définit les [symboles de devise](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) qui apparaissent dans les prix des produits et les documents de vente tels que les commandes et les factures. [!DNL Commerce] prend en charge les devises de plus de 200 pays dans le monde.

Mise à jour des taux de devise : les taux de devise peuvent être [mis à jour](../stores-purchase/currency-update.md) manuellement ou importés dans votre magasin selon les besoins, ou selon un calendrier prédéfini.

Sélecteur de devise : si plusieurs devises sont disponibles, le [programme de sélection de devise](../stores-purchase/currency.md) est disponible dans l’en-tête du magasin.

## [!UICONTROL Store Email Addresses]

Vous pouvez avoir jusqu’à cinq adresses électroniques différentes pour représenter des fonctions ou des services distincts pour chaque magasin ou affichage. Outre les identités d’email prédéfinies suivantes, vous pouvez configurer quelques identités personnalisées en fonction de vos besoins.

- Contact général
- représentant commercial
- Assistance clientèle

Chaque identité et son adresse électronique associée peuvent être associées à des messages électroniques automatisés spécifiques et apparaître comme l’expéditeur des messages électroniques envoyés depuis votre boutique.

### Étape 1 : configuration des adresses électroniques de votre domaine

Avant de pouvoir configurer des adresses électroniques pour le magasin, chacune d’elles doit être configurée en tant qu’adresse électronique valide pour votre domaine. Pour créer chaque adresse électronique nécessaire, suivez les instructions de votre administrateur de serveur ou de votre fournisseur d’hébergement de messagerie.

### Étape 2 : configurer les adresses électroniques de votre magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous **[!UICONTROL General]** dans le panneau de navigation de gauche, sélectionnez **[!UICONTROL Store Email Addresses]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL General Contact]** et procédez comme suit :

   ![Configuration générale - stocker les adresses électroniques](./assets/store-email-addresses-general-contact.png){width="600"}

   - Pour **[!UICONTROL Sender Name]**, saisissez le nom de la personne associée à l’identité de contact général qui apparaîtra comme expéditeur de tout message électronique.

   - Pour **[!UICONTROL Sender Email]**, saisissez l’adresse électronique associée.

1. Répétez cette procédure pour chaque adresse électronique de magasin que vous prévoyez d’utiliser.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Etape 3 : mise à jour de la configuration de l&#39;email de vente

Si vous utilisez des adresses électroniques personnalisées, veillez à mettre à jour la configuration de tout message électronique associé afin que l’identité correcte apparaisse comme expéditeur.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales Emails]**.

   La page comporte une section distincte pour chacun des éléments suivants :

   - Commande et commentaires des commandes
   - Commentaires sur les factures et les factures
   - Commentaires sur l’envoi et l’envoi
   - Note de crédit et commentaires de note de crédit
   - RMA, RMA Authorization, RMA Admin Comments et RMA Customer Comments ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

1. À partir de **[!UICONTROL Order]**, développez la section pour chaque message et assurez-vous que l’expéditeur correct est sélectionné.

   ![Configuration des ventes - emails de vente](./assets/sales-emails-order.png){width="600"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration des emails de vente, consultez le [_Guide de référence de configuration_](../configuration-reference/sales/sales-emails.md).

## Formulaire de contact

Le lien _Nous contacter_ dans le pied de page de la boutique est un moyen facile pour les clients de rester en contact avec vous. Les clients peuvent remplir le formulaire pour envoyer un message à votre boutique. Une installation [!DNL Commerce] standard affiche le formulaire par défaut _Nous contacter_. Après l’envoi du formulaire, un message de remerciement s’affiche.

Il est important de comprendre que le formulaire de contact par défaut est généré directement à partir du code plutôt qu’à partir d’une page CMS.

![Page de contact par défaut](./assets/page-contact-us-default.png){width="700"}

Le pied de page du magasin comprend un lien vers la page Nous contacter , disponible dans tout le magasin.

![Lien de contact dans le pied de page](./assets/storefront-footer-contact-us.png){width="700"}

Les exemples de données Luma incluent des informations supplémentaires sur la page Nous contacter , qui montrent comment personnaliser la page pour votre magasin.

![Page de contact](./assets/storefront-contact-us.png){width="700"}

### Configurer le formulaire de contact

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL Contacts]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Contact Us]** et définissez **[!UICONTROL Enable Contact Us]** sur `Yes`.

   ![Configuration générale - contactez-nous](./assets/contacts-contact-us.png){width="600"}

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options de contact de courrier électronique :**[!UICONTROL Email Options]**

   ![Configuration générale - options d’email](./assets/contacts-email-options.png){width="600"}

   - Pour **[!UICONTROL Send Emails to]**, saisissez l’adresse électronique à laquelle les messages du formulaire de contact sont envoyés.

   - Définissez **[!UICONTROL Email Sender]** sur l’identité du magasin qui apparaît comme expéditeur du message à partir du formulaire de contact. Par exemple : courrier électronique personnalisé 2.

   - Définissez **[!UICONTROL Email Template]** sur le modèle utilisé pour les messages envoyés à partir du formulaire de contact.

1. Lors de la mise en concurrence, cliquez sur **[!UICONTROL Save Config]**.

### Personnalisation du contenu

Vous pouvez personnaliser le contenu du formulaire _Nous contacter_ pour répondre aux besoins de votre boutique et de vos stratégies de service client.

### Méthode 1 : utilisation d’exemples de données

Les exemples de données Luma incluent un bloc _Nous contacter infos_ qui peut être personnalisé pour votre boutique. Le `contact-us-info` [block](../content-design/blocks.md) peut être facilement modifié pour ajouter votre propre contenu à la page de contact.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Recherchez le bloc **[!UICONTROL Contact Us Info]** dans la liste et ouvrez-le en mode **[!UICONTROL Edit]**.

   ![Bloc d’informations de contact](./assets/content-block-contact-us-info.png){width="700"}

1. Au bas de la page bloquée, cliquez sur **[!UICONTROL Edit with Page Builder]**.

   ![Bloc de contenu - contactez-nous exemple](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >Si vous avez [[!DNL Page Builder] désactivé](../page-builder/setup.md#disable-dnl-page-builder), vous pouvez utiliser l’éditeur [toolbar](../content-design/editor.md) pour formater le texte, et ajouter [images](../content-design/editor-insert-image.md) et [links](../content-design/editor-insert-link.md).

1. Pointez sur le conteneur d’HTML pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](../page-builder/assets/pb-icon-settings.png) ).

1. Modifiez le code de l&#39;HTML en fonction des coordonnées de votre boutique et cliquez sur **[!UICONTROL Save]**.

   ![Bloc de contenu - modifier le code d’HTML](./assets/content-block-contact-us-html.png){width="700"}

1. Quittez l’étape [!DNL Page Builder] et cliquez sur **[!UICONTROL Save Block]**.

### Méthode 2 : sans exemple de données

>[!IMPORTANT]
>
>À compter de la version 2.4.0, le formulaire de contact ne peut plus appeler dans un bloc CMS ou une page CMS. Toutes les personnalisations du formulaire de contact doivent être effectuées à l’aide du fichier xml de mise en page ou de modèles de thème personnalisés.

Par défaut, les acheteurs accèdent au formulaire de contact à l’aide du _lien de contact_ dans le pied de page des pages de storefront. Pour plus d&#39;informations sur la personnalisation de la page de contact, consultez le [Guide du développeur Frontend][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
