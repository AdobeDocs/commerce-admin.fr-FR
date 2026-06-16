---
title: Détection des fonctionnalités du navigateur
description: Découvrez comment configurer la détection des fonctionnalités du navigateur et afficher un avis si les paramètres du navigateur du client doivent être modifiés.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# Détection des fonctionnalités du navigateur

Comme la plupart des sites web et des applications sur Internet, Adobe Commerce et Magento Open Source exigent que le navigateur du visiteur autorise les cookies et JavaScript pour des opérations complètes. Cependant, il arrive parfois que le navigateur d’un utilisateur soit défini sur le paramètre de confidentialité le plus élevé qui empêche les cookies et JavaScript. Votre boutique peut être configurée pour tester les fonctionnalités du navigateur de chaque visiteur et afficher un avis si les paramètres doivent être modifiés.

- Si les paramètres de confidentialité du navigateur interdisent les cookies, vous pouvez configurer le système pour les rediriger automatiquement vers la page [Activer les cookies](../content-design/pages.md#enable-cookies), qui explique comment définir les paramètres recommandés avec la plupart des navigateurs.
- Si les paramètres de confidentialité du navigateur interdisent JavaScript, vous pouvez configurer le système pour afficher le message suivant au-dessus de l’en-tête de chaque page.

Pour obtenir des informations techniques, reportez-vous à la section [Navigateurs pris en charge](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=fr#supported-browsers) du _Guide d’installation_.

## Configuration de la détection des fonctionnalités du navigateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Browser Capabilities Detection]** et procédez comme suit :

   - Pour afficher des instructions expliquant comment configurer le navigateur afin d’autoriser les cookies, définissez **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** sur `Yes`.

   - Pour afficher une bannière au-dessus de l’en-tête lorsque JavaScript est désactivé dans le navigateur de l’utilisateur, définissez **[!UICONTROL Show Notice if JavaScript is Disabled]** sur `Yes`.

   - Pour afficher une bannière au-dessus de l’en-tête lorsque le stockage local est désactivé dans le navigateur de l’utilisateur, définissez **[!UICONTROL Show Notice if Local Storage is Disabled]** sur `Yes`.

   ![Configuration générale - Détection des fonctionnalités d’un navigateur web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
