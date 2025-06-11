---
title: Utiliser une base de données des médias
description: Découvrez comment utiliser une base de données multimédia pour stocker vos fichiers  [!DNL Commerce] .
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Utiliser une base de données des médias

>[!IMPORTANT]
>
>La méthode de stockage des médias de base de données est obsolète à partir d’Adobe Commerce et de Magento Open Source 2.4.3.

Par défaut, toutes les images, les fichiers CSS compilés et les fichiers JavaScript compilés de l’instance [!DNL Commerce] sont stockés dans le système de fichiers sur le serveur web. Vous pouvez choisir de stocker ces fichiers dans une base de données sur un serveur de base de données. Un avantage de cette approche est l’option de synchronisation automatique et de synchronisation inverse entre le système de fichiers du serveur web et la base de données. Vous pouvez utiliser la base de données par défaut pour stocker des médias ou en créer un. Pour pouvoir utiliser une base de données nouvellement créée comme espace de stockage multimédia, vous devez ajouter des informations la concernant et ses informations d’identification d’accès au fichier `env.php`.

## Workflow de base de données

1. **Le navigateur demande le média** - Une page du magasin s’ouvre dans le navigateur du client et le navigateur demande le média spécifié dans l’HTML.

1. **Le système recherche les médias dans le système de fichiers** - Le système recherche les médias dans le système de fichiers et, s’il les trouve, les transmet au navigateur.

1. **Le système localise le média dans la base de données** - Si le média est introuvable dans le système de fichiers, une demande de média est envoyée à la base de données spécifiée dans la configuration.

1. **Le système localise les médias dans la base de données** - Un script PHP transfère les fichiers de la base de données vers le système de fichiers, et envoie au navigateur du client. La requête de navigateur pour le média déclenche l’exécution du script comme suit :

   - Si les [réécritures](../merchandising-promotions/url-rewrite.md) du serveur web sont activées pour la [!DNL Commerce] et prises en charge par le serveur, le script PHP s&#39;exécute uniquement lorsque le média demandé est introuvable dans le système de fichiers.
   - Si les réécritures du serveur web sont désactivées pour [!DNL Commerce], ou ne sont pas prises en charge par le serveur, le script PHP s&#39;exécute quand même, même si le média requis est disponible dans le système de fichiers.

## Utiliser une base de données pour le stockage de médias

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur `Default Config` pour appliquer la configuration au niveau global.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Storage Configuration for Media]** et procédez comme suit :

   ![Configuration avancée - Configuration du stockage pour les médias](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Media Storage]** sur `Database`.

   - Définissez **[!UICONTROL Select Media Database]** sur la base de données à utiliser.

   - Pour transférer le média existant vers la base de données nouvellement sélectionnée, cliquez sur **[!UICONTROL Synchronize]**.

   - Saisissez le **[!UICONTROL Environment Update Time]** en secondes.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
