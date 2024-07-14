---
title: Détection des fonctionnalités du navigateur
description: Découvrez comment configurer la détection des fonctionnalités du navigateur et afficher un avis si les paramètres du navigateur du client doivent être modifiés.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Détection des fonctionnalités du navigateur

Comme la plupart des sites web et des applications sur Internet, Adobe Commerce et Magento Open Source exigent que le navigateur du visiteur autorise les cookies et JavaScript pour des opérations complètes. Cependant, il arrive que le navigateur d’un utilisateur soit défini sur le paramètre de confidentialité le plus élevé qui empêche les cookies et JavaScript. Votre magasin peut être configuré pour tester les fonctionnalités du navigateur de chaque visiteur et afficher un avis si les paramètres doivent être modifiés.

- Si les paramètres de confidentialité du navigateur n’autorisent pas les cookies, vous pouvez configurer le système pour les rediriger automatiquement vers la page [Activer les cookies](../content-design/pages.md#enable-cookies), ce qui explique comment définir les paramètres recommandés avec la plupart des navigateurs.
- Si les paramètres de confidentialité du navigateur n’autorisent pas JavaScript, vous pouvez configurer le système pour qu’il affiche le message suivant au-dessus de l’en-tête de chaque page.

Pour plus d&#39;informations techniques, reportez-vous à la section [Navigateurs pris en charge](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) du _Guide d&#39;installation_.

## Configuration de la détection des fonctionnalités du navigateur

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Browser Capabilities Detection]** et procédez comme suit :

   - Pour afficher des instructions expliquant comment configurer le navigateur pour autoriser les cookies, définissez **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** sur `Yes`.

   - Pour afficher une bannière au-dessus de l’en-tête lorsque JavaScript est désactivé dans le navigateur de l’utilisateur, définissez **[!UICONTROL Show Notice if JavaScript is Disabled]** sur `Yes`.

   - Pour afficher une bannière au-dessus de l’en-tête lorsque l’espace de stockage local est désactivé dans le navigateur de l’utilisateur, définissez **[!UICONTROL Show Notice if Local Storage is Disabled]** sur `Yes`.

   ![Configuration générale - détection des fonctionnalités du navigateur web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
