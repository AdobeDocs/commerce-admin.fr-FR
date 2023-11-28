---
title: Utilisation d’une base de données multimédia
description: Découvrez comment utiliser une base de données multimédia pour stocker votre [!DNL Commerce] fichiers multimédias.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Utilisation d’une base de données multimédia

>[!IMPORTANT]
>
>La méthode de stockage des médias dans la base de données est obsolète depuis Adobe Commerce et Magento Open Source 2.4.3.

Par défaut, toutes les images, les fichiers CSS compilés et les fichiers JavaScript compilés du [!DNL Commerce] sont stockées dans le système de fichiers sur le serveur web. Vous pouvez choisir de stocker ces fichiers dans une base de données sur un serveur de base de données. L’un des avantages de cette approche est la possibilité d’une synchronisation automatique et d’une synchronisation inverse entre le système de fichiers du serveur web et la base de données. Vous pouvez utiliser la base de données par défaut pour stocker ou créer un média. Pour pouvoir utiliser une nouvelle base de données comme stockage multimédia, vous devez ajouter des informations la concernant et ses informations d’identification d’accès au `env.php` fichier .

## Workflow de base de données

1. **Média de demandes de navigateur** - Une page du magasin s’ouvre dans le navigateur du client et le navigateur demande le média spécifié dans le HTML.

1. **Le système recherche le média dans le système de fichiers** - Le système recherche le média dans le système de fichiers et, s’il le trouve, le transmet au navigateur.

1. **Le système localise le média dans la base de données** - Si le média est introuvable dans le système de fichiers, une demande de média est envoyée à la base de données spécifiée dans la configuration.

1. **Le système localise le média dans la base de données** - Un script PHP transfère les fichiers de la base de données vers le système de fichiers et les envoie au navigateur du client. La demande de navigateur pour le média déclenche l’exécution du script comme suit :

   - Si le serveur web [rewrites](../merchandising-promotions/url-rewrite.md) sont activés pour [!DNL Commerce] et pris en charge par le serveur, le script PHP s’exécute uniquement lorsque le média demandé est introuvable dans le système de fichiers.
   - Si les réécritures du serveur web sont désactivées pour [!DNL Commerce], ou non pris en charge par le serveur, le script PHP s’exécute de toute façon, même si le support requis est disponible dans le système de fichiers.

## Utiliser une base de données pour le stockage des médias

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** to `Default Config` pour appliquer la configuration au niveau global.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Storage Configuration for Media]** et procédez comme suit :

   ![Configuration avancée - Configuration du stockage pour les médias](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Media Storage]** to `Database`.

   - Définir **[!UICONTROL Select Media Database]** dans la base de données que vous souhaitez utiliser.

   - Pour transférer le média existant vers la base de données nouvellement sélectionnée, cliquez sur **[!UICONTROL Synchronize]**.

   - Saisissez le **[!UICONTROL Environment Update Time]** en secondes.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
