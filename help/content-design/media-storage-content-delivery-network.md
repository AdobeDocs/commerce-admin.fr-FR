---
title: Utiliser un réseau de diffusion de contenu
description: Découvrez comment utiliser un réseau de diffusion de contenu (CDN) pour stocker des fichiers multimédias.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Utiliser un réseau de diffusion de contenu

Un réseau de diffusion de contenu (CDN) peut être utilisé pour stocker des fichiers multimédias. Adobe Commerce sur l’infrastructure cloud comprend le réseau de diffusion de contenu Fastly (voir [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) dans le _Guide d’infrastructure de Commerce on Cloud_). Une instance Commerce installée _on premise_ n’inclut pas d’intégration à un réseau de diffusion de contenu spécifique, vous pouvez utiliser le réseau de diffusion de contenu de votre choix.

Après avoir configuré le réseau de diffusion de contenu, vous devez effectuer la configuration à partir de l’administrateur. Les modifications peuvent être apportées au niveau global ou au niveau du site web. Lorsqu’un réseau de diffusion de contenu est utilisé pour le stockage des médias, tous les chemins d’accès aux médias sur les pages de magasin Commerce sont modifiés en chemins d’accès au réseau de diffusion de contenu spécifiés dans la configuration.

## Workflow CDN

1. **Média de demandes de navigateur** - Une page du magasin s’ouvre dans le navigateur du client et le navigateur demande le média spécifié dans le HTML.
1. **Demande envoyée au réseau de diffusion de contenu ; images trouvées et diffusées** - La requête est envoyée en premier au réseau de diffusion de contenu. Si le réseau de diffusion de contenu contient des images en stockage, il diffuse les fichiers multimédias vers le navigateur du client.
1. **Média introuvable, requête envoyée à [!DNL Commerce] serveur web** - Si le réseau de diffusion de contenu ne contient pas les fichiers multimédias, la demande est envoyée à la variable [!DNL Commerce] serveur web. Si les fichiers multimédias se trouvent dans le système de fichiers, le serveur web les envoie au navigateur du client.

>[!IMPORTANT]
>
>Pour des raisons de sécurité, lorsqu’un CDN est utilisé comme stockage multimédia, il se peut que JavaScript ne fonctionne pas correctement si le CDN se trouve en dehors de votre sous-domaine.

## Configurer un réseau de diffusion de contenu

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** selon les besoins.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Base URLs]** et procédez comme suit :

   ![Configuration générale - URL de base web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Mettez à jour le **[!UICONTROL Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où sont stockés les fichiers d’affichage statique.

   - Mettez à jour le **[!UICONTROL Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le CDN.

     Ces deux champs peuvent être laissés vides ou commencer par l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Base URLs (Secure)]** et procédez comme suit :

   ![Configuration générale - URL de base web (sécurisées)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Mettez à jour le **[!UICONTROL Secure Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où sont stockés les fichiers d’affichage statique.

   - Mettez à jour le **[!UICONTROL Secure Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le CDN.

     Ces deux champs peuvent être laissés vides ou commencer par l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
