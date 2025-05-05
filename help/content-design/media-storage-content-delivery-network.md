---
title: Utiliser un réseau de diffusion de contenu
description: Découvrez comment utiliser un réseau de diffusion de contenu (CDN) pour stocker des fichiers multimédias.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Utiliser un réseau de diffusion de contenu

Un réseau de diffusion de contenu (CDN) peut être utilisé pour stocker des fichiers multimédias. Adobe Commerce sur l’infrastructure cloud inclut le réseau de diffusion de contenu Fastly (voir [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html?lang=fr) dans le _Guide de l’infrastructure Commerce sur le cloud_). Une instance Commerce installée _sur site_ n’inclut pas d’intégration à un réseau de diffusion de contenu spécifique. Vous pouvez utiliser le réseau de diffusion de contenu de votre choix.

Après avoir configuré le réseau de diffusion de contenu, vous devez effectuer la configuration à partir de l’administrateur. Les modifications peuvent être apportées au niveau global ou au niveau du site web. Lorsqu’un réseau de diffusion de contenu est utilisé pour le stockage des médias, tous les chemins d’accès aux médias sur les pages de magasin Commerce sont modifiés en chemins d’accès au réseau de diffusion de contenu spécifiés dans la configuration.

## Workflow CDN

1. **Le navigateur demande le média** : une page du magasin s’ouvre dans le navigateur du client, et le navigateur demande le média spécifié dans l’HTML.
1. **Demande envoyée au CDN ; images trouvées et diffusées** - La demande est envoyée en premier au CDN. Si le réseau de diffusion de contenu contient des images en stockage, il diffuse les fichiers multimédias vers le navigateur du client.
1. **Média introuvable, demande envoyée à [!DNL Commerce] serveur web** - Si le réseau de diffusion de contenu ne contient pas les fichiers multimédias, la demande est envoyée au serveur web [!DNL Commerce]. Si les fichiers multimédias se trouvent dans le système de fichiers, le serveur web les envoie au navigateur du client.

>[!IMPORTANT]
>
>Pour des raisons de sécurité, lorsqu’un CDN est utilisé comme stockage multimédia, JavaScript peut ne pas fonctionner correctement si le CDN se trouve en dehors de votre sous-domaine.

## Configurer un réseau de diffusion de contenu

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** selon les besoins.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Base URLs]** et procédez comme suit :

   ![Configuration générale - URL de base web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Mettez à jour **[!UICONTROL Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où sont stockés les fichiers d’affichage statique.

   - Mettez à jour **[!UICONTROL Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le CDN.

     Ces deux champs peuvent rester vides ou commencer avec l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Base URLs (Secure)]** et procédez comme suit :

   ![Configuration générale - URL de base web (sécurisé)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Mettez à jour **[!UICONTROL Secure Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où sont stockés les fichiers d’affichage statique.

   - Mettez à jour **[!UICONTROL Secure Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le CDN.

     Ces deux champs peuvent rester vides ou commencer avec l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
