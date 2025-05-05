---
title: Configuration des devises
description: Découvrez comment définir la portée de la devise de base et comment spécifier les devises que vous acceptez et la devise que vous souhaitez utiliser pour l’affichage des prix.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Configuration des devises

Avant de configurer des taux de change individuels, vous devez d’abord définir la portée de la [devise de base](../configuration-reference/general/currency-setup.md). Elle est définie sur global par défaut, ce qui applique le paramètre de devise de base à l’ensemble de la [hiérarchie de magasin](../getting-started/websites-stores-views.md). Si vous disposez d’une installation Adobe Commerce ou Magento Open Source multi-site, vous pouvez gérer plusieurs devises de base en définissant la portée au niveau du site web.

Vous spécifiez également les devises que vous acceptez et la devise que vous souhaitez utiliser pour l’affichage des [prix](../catalog/catalog-price-scope.md) dans votre boutique. Dans le diagramme suivant, la portée de la devise de base est définie au niveau du site web, de sorte que chaque site web peut avoir une devise de base différente.

![Diagramme de portée de devise](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Etape 1 : Sélection des devises acceptées

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Scope]** sur la vue de magasin où s’applique la configuration.

1. Dans le panneau de gauche sous _Général_, choisissez **[!UICONTROL Currency Setup]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options suivantes :**[!UICONTROL Currency Options]**

   - **[!UICONTROL Base Currency]** — Défini sur la devise principale que vous utilisez pour les transactions en ligne.

   - **[!UICONTROL Default Display Currency]** — Défini sur la devise que vous utilisez pour afficher les prix dans la vue de magasin.

   - **[!UICONTROL Allowed Currencies]** — Sélectionnez toutes les devises que vous acceptez comme paiement dans la vue de magasin. Veillez également à sélectionner votre devise principale.

     Pour plusieurs devises, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   ![Configuration générale - options de devise](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Options de devise](../configuration-reference/general/currency-setup.md) dans le _Guide de référence de configuration_.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur _Fermer_ ( ![Fermer la boîte](../assets/icon-close-x.png) ) dans le coin supérieur droit du message système.

   Vous pouvez [actualiser le cache](../systems/cache-management.md) ultérieurement.

1. Définissez la portée de la devise de base :

   - Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

   - Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Price]** . (Cette section n’apparaît que si la portée est définie sur **[!UICONTROL Store View:]** _Configuration par défaut_.)

   - Définissez **[!UICONTROL Catalog Price Scope]** sur `Global` ou `Website`.

   ![ Configuration du catalogue - options de prix](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Etape 2 : paramétrer la connexion à l&#39;import

1. Faites défiler la page jusqu’en haut.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL Currency Setup]**.

1. Configurez votre connexion au service de devise :

   Il existe trois options de service : _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ et _[!UICONTROL Currency Converter API]_.

   >[!IMPORTANT]
   >
   >À compter de la version 2.4.6, le service [[!DNL Fixer.io]](https://fixer.io/) est obsolète et remplacé par le service [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Il est vivement recommandé d’utiliser un compte APILayer au lieu d’un compte [!DNL Fixer.io] obsolète.

   - _Pour vous connecter au [service fixeur.io](https://fixer.io/) :_

      - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Fixer.io]** .

      - Entrez votre fichier de fixeur.io **[!UICONTROL API key]**.

      - Pour **[!UICONTROL Connection Timeout in Seconds]**, saisissez le nombre de secondes d’inactivité à autoriser avant l’expiration de la connexion.

     ![Configuration générale - configuration de devise - options de Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Pour se connecter au [[!DNL Fixer Api (APILayer)] service](https://apilayer.com/) :_

      - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Fixer Api (APILayer)]** .

      - Saisissez votre [!DNL APILayer] **[!UICONTROL API key]**.

      - Pour **[!UICONTROL Connection Timeout in Seconds]**, saisissez le nombre de secondes d’inactivité à autoriser avant l’expiration de la connexion.

     ![ Configuration générale - Configuration de devise - Options de l’API du correcteur (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Pour se connecter au [[!DNL Currency Convertor API] service](https://free.currencyconverterapi.com/) :_

      - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Currency Convertor API]** .

      - Saisissez votre convertisseur de devises **[!UICONTROL API key]**.

      - Pour **[!UICONTROL Connection Timeout in Seconds]**, saisissez le nombre de secondes d’inactivité à autoriser avant l’expiration de la connexion.

     ![ Configuration générale - Configuration de la devise - Options de l’API du convertisseur de devise](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Étape 3 : configuration des paramètres d&#39;import planifiés

1. Continuez avec Configuration de devise, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Scheduled Import Settings]** .

   ![Configuration générale - Paramètres d’importation planifiés en devise](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Pour mettre automatiquement à jour les taux de change, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Définissez les options de mise à jour :

   - **[!UICONTROL Service]** — Défini sur le fournisseur de taux. La valeur par défaut est `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** : définissez sur l’heure, la minute et la seconde où les taux sont mis à jour selon le planning.

   - **[!UICONTROL Frequency]** — Pour déterminer la fréquence de mise à jour des taux, définissez sur l’une des options suivantes :

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Entrez l&#39;adresse email de la personne qui doit recevoir la notification par email en cas d&#39;erreur lors du processus d&#39;import.

     Pour saisir plusieurs adresses électroniques, séparez-les par une virgule.

   - **[!UICONTROL Error Email Sender]** — Défini sur le [contact de magasin](../getting-started/store-details.md#store-email-addresses) qui apparaît comme l’expéditeur de la notification d’erreur.

   - **[!UICONTROL Error Email Template]** — Défini sur le modèle de courrier électronique utilisé pour la notification d’erreur.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur le lien **[!UICONTROL Cache Management]** et actualisez le cache non valide.

   ![ Message système : actualisez le cache non valide](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Etape 4 : Mise à jour des taux de change

Les taux de change doivent être mis à jour avec les valeurs actuelles avant qu’elles ne prennent effet. [Mettez à jour les taux](currency-update.md) manuellement ou pour les importer automatiquement.

## Étape 5 : personnalisation des symboles de devise (facultatif)

La gestion des symboles de devise vous permet de personnaliser le symbole associé à chaque devise acceptée comme paiement dans votre magasin.

![Symboles de devise](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Chaque devise activée pour votre magasin apparaît dans la liste _[!UICONTROL Currency]_.

1. Modifiez les paramètres de la liste selon vos besoins :

   - Saisissez un symbole personnalisé pour chaque devise à utiliser ou cochez la case **[!UICONTROL Use Standard]** pour chaque devise.

   - Pour remplacer le symbole par défaut, décochez la case _[!UICONTROL Use Standard]_&#x200B;et saisissez le symbole à utiliser.

   >[!NOTE]
   >
   >Il n’est pas possible de modifier l’alignement du symbole monétaire de gauche à droite.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Currency Symbols]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur le lien **[!UICONTROL Cache Management]** et actualisez le cache non valide.
