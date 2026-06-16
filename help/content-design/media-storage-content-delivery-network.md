---
title: Utiliser un réseau de diffusion de contenu
description: Découvrez comment utiliser un réseau de diffusion de contenu (CDN) pour stocker des fichiers multimédias.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/c-Aw3S5unZlMdDG1k080D4CIMcILglNa4ymZxPt6HBk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# Utiliser un réseau de diffusion de contenu

Un réseau de diffusion de contenu (CDN) peut être utilisé pour stocker des fichiers multimédias. Adobe Commerce sur l’infrastructure cloud inclut le réseau CDN Fastly (voir [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html?lang=fr) dans le _Guide de Commerce sur l’infrastructure cloud_). Une instance Commerce installée _on-premise_ n’inclut pas d’intégration à un réseau CDN spécifique. Vous pouvez utiliser le réseau CDN de votre choix.

Après avoir configuré le réseau CDN, vous devez effectuer la configuration à partir de l’administration. Les modifications peuvent être apportées au niveau global ou au niveau du site web. Lorsqu’un réseau CDN est utilisé pour le stockage de médias, tous les chemins d’accès aux médias sur les pages de magasin Commerce sont modifiés en chemins d’accès CDN spécifiés dans la configuration.

## Workflow CDN

1. **Le navigateur demande le média** - Une page du magasin s’ouvre dans le navigateur du client et le navigateur demande le média spécifié dans l’HTML.
1. **Requête envoyée au réseau CDN ; images trouvées et diffusées** - La requête est d’abord envoyée au réseau CDN. Si le réseau de diffusion de contenu stocke les images, il diffuse les fichiers multimédias au navigateur du client.
1. **Média introuvable, requête envoyée à [!DNL Commerce] serveur web** - Si le réseau CDN ne dispose pas des fichiers médias, la requête est envoyée au serveur web [!DNL Commerce]. Si les fichiers multimédias se trouvent dans le système de fichiers, le serveur web les envoie au navigateur du client.

>[!IMPORTANT]
>
>Pour des raisons de sécurité, lorsqu’un réseau CDN est utilisé comme stockage multimédia, JavaScript peut ne pas fonctionner correctement si le réseau CDN est situé en dehors de votre sous-domaine.

## Configuration d’un réseau de diffusion de contenu

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** selon vos besoins.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Base URLs]** et procédez comme suit :

   ![Configuration générale - URL de base web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Mettez à jour le **[!UICONTROL Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où les fichiers d’affichage statiques sont stockés.

   - Mettez à jour le **[!UICONTROL Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le réseau CDN.

     Ces deux champs peuvent être laissés vides ou commencer par l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Base URLs (Secure)]** et procédez comme suit :

   ![Configuration générale - URL de base web (sécurisée)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Mettez à jour le **[!UICONTROL Secure Base URL for Static View Files]** avec l’URL de l’emplacement sur le réseau de diffusion de contenu où les fichiers d’affichage statiques sont stockés.

   - Mettez à jour le **[!UICONTROL Secure Base URL for User Media Files]** avec l’URL des fichiers JavaScript sur le réseau CDN.

     Ces deux champs peuvent être laissés vides ou commencer par l’espace réservé : `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
