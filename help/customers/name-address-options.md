---
title: Options de nom et d’adresse du client
description: Les options de nom et d’adresse du client déterminent les champs inclus dans les formulaires de nom et d’adresse.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/qMXVcVWZJCrCNywOJF3psuO5vLWkNt9LoNtgFfFBzT8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 809
ht-degree: 0%

---

# Options de nom et d’adresse du client

Les _Options de nom et d’adresse_ déterminent quels champs sont inclus dans les formulaires de nom et d’adresse lorsque les clients créent un [compte](../customers/account-create.md) avec votre magasin.

![Formulaire d’inscription au compte client](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

Les étapes de configuration des options nom et adresse sont différentes pour Adobe Commerce et Magento Open Source.

## Configurer les options de nom et d’adresse pour Adobe Commerce

Vous pouvez configurer les options de nom et d’adresse qui sont présentées aux clients sur le storefront lorsqu’ils créent leur compte.

### Étape 1 : définir la portée de la configuration

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Name and Address Options]** .

   >[!INFO]
   >
   >Notez que la portée des options de nom et d’adresse s’applique au niveau du `website`.

1. Faites défiler la page jusqu’en haut et définissez la portée de la configuration sur l’une des options suivantes :

   - `Default Config`
   - `Main Website` (ou site spécifique pour les installations multi-sites)

   >[!INFO]
   >
   >La section _[!UICONTROL Name and Address Options]_&#x200B;n’apparaît pas lorsque l’étendue est définie sur `Default Store View`.

   ![Portée de la configuration](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### Étape 2 : configurer les options de nom et d’adresse

1. Revenez à la section [!UICONTROL _Options de nom et d’adresse_] de la page Configuration du client.

   >[!INFO]
   >
   > Si vous n’utilisez pas le paramètre d’étendue `Default config`, vous devez décocher la case `Use Default` pour chaque champ avant de modifier la valeur.

   ![Options de nom et d’adresse](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Prefix Dropdown Options]**, saisissez chaque préfixe qui doit apparaître dans la liste en les séparant par des points-virgules.

   >[!IMPORTANT]
   >
   >Placez un point-virgule avant la première valeur pour afficher une valeur vide en haut de la liste.

1. Par **[!UICONTROL Suffix Dropdown Options]**, saisissez chaque suffixe que vous souhaitez voir apparaître dans la liste, séparé par un point-virgule.

1. Pour inclure les champs suivants dans les formulaires client, définissez la valeur de chaque sur `Optional` ou `Required`, selon les besoins.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Étape 3 : Enregistrer et actualiser

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Dans le message en haut de la page, cliquez sur **[!UICONTROL Cache Management]** et [actualiser](../systems/cache-management.md) chaque cache non valide.

## Configurer les options de nom et d’adresse pour Magento Open Source

Configurez les options de nom et d’adresse qui sont présentées aux clients sur le storefront lorsqu’ils créent leur compte.

![Formulaire d’inscription au compte client](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### Étape 1 : définir la portée de la configuration

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Name and Address Options]** .

   >[!IMPORTANT]
   >
   > Notez que la portée des options de nom et d’adresse s’applique au niveau du `website`.

   ![Options de nom et d’adresse](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. Faites défiler jusqu’en haut de la page et définissez la portée de la configuration sur l’une des options suivantes :

   - `Default Config`
   - `Main Website` (ou site spécifique pour les installations multi-sites)

   >[!NOTE]
   >
   >La section _Options de nom et d’adresse_ n’apparaît pas lorsque l’étendue est définie sur `Default Store View`.

   ![Portée de la configuration](assets/configuration-scope.png){width="600" zoomable="yes"}

### Étape 2 : configurer les options de nom et d’adresse

1. Revenez à la section [!UICONTROL _Options de nom et d’adresse_] de la page Configuration du client.

   >[!INFO]
   >
   >Si vous n’utilisez pas le paramètre d’étendue `Default config`, vous devez décocher la case `Use Default` pour chaque champ avant de modifier la valeur.

1. Pour **Nombre de lignes dans une adresse postale**, saisissez un nombre compris entre 1 et 4.

   >[!WARNING]
   >
   >Par défaut, l’adresse postale est de trois lignes.

1. Pour inclure un préfixe (tel que M. ou Mme) dans le cadre du nom, définissez **Afficher le préfixe** sur `Yes`.

   ![Préfixe dans le formulaire d’inscription du client](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Pour **Options de liste déroulante de préfixe**, saisissez chaque préfixe qui doit apparaître dans la liste, en les séparant par des points-virgules. Vous pouvez placer un point-virgule avant la première valeur pour afficher une valeur vide en haut de la liste.

1. Pour inclure un champ facultatif pour le deuxième prénom ou l’initial du client, définissez **[!UICONTROL Show Middle Name (initial)]** sur `Yes`.

1. Pour inclure un suffixe (comme Jr. ou père) après le nom du client, définissez **[!UICONTROL Show Suffix]** sur l’une des valeurs suivantes :

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Pour **Options de liste déroulante des suffixes**, saisissez chaque suffixe qui doit apparaître dans la liste, en les séparant par des points-virgules. Vous pouvez placer un point-virgule avant la première valeur pour afficher une valeur vide en haut de la liste.

1. Pour inclure la date de naissance, définissez **[!UICONTROL Show Date of Birth]** sur l’une des valeurs suivantes :

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, soyez conscient de tous les risques juridiques et de sécurité potentiels associés au stockage de la date de naissance complète du client (mois, jour, année) avec d&#39;autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clientes et clients et de suggérer d’utiliser leur année de naissance comme alternative.

   Les clients peuvent utiliser l’icône Calendrier après le champ pour choisir la date de naissance dans un calendrier pop-up.

   ![Date de naissance dans le formulaire d’inscription du client](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. Pour permettre aux clients de saisir leur numéro de taxe ou de [TVA](../stores-purchase/vat.md), définissez l&#39;**[!UICONTROL Show Tax/VAT Number]** sur l&#39;une des valeurs suivantes :

   - `Optional`
   - `Required`

1. Pour inclure un champ pour le genre dans le formulaire client, définissez **[!UICONTROL Show Gender]** sur l’une des valeurs suivantes :

   - `Optional`
   - `Required`

   ![Options de genre dans le formulaire d’inscription du client](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. Pour inclure les champs suivants dans les formulaires client, définissez la valeur de chaque sur `Optional` ou `Required`, selon les besoins.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Étape 3 : Enregistrer et actualiser

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Dans le message en haut de la page, cliquez sur **[!UICONTROL Cache Management]** et [actualiser](../systems/cache-management.md) chaque cache non valide.
