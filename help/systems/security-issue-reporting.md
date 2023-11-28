---
title: Rapports sur les problèmes de sécurité
description: Découvrez comment configurer les coordonnées et les liens liés à la sécurité qui peuvent être utilisés par les chercheurs en sécurité pour signaler les problèmes de sécurité sur votre site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Rapports sur les problèmes de sécurité

La variable `security.txt` contient les coordonnées et les liens liés à la sécurité que les chercheurs en sécurité peuvent utiliser pour signaler les problèmes de sécurité liés à votre site. Si vos informations de sécurité changent au fil du temps, assurez-vous que les informations de la variable `security.txt` est à jour.

**_Pour configurer security.txt :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL Security]_, cliquez sur **[!UICONTROL Security.txt]**.

1. Dans le _[!UICONTROL General]_, définissez **[!UICONTROL Enable]**to `Yes`.

   ![Configuration générale de la sécurité](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Contact Information]_, saisissez ce qui suit :

   - Adresse électronique et numéro de téléphone de la personne qui gère les problèmes de sécurité pour votre boutique.

   - L’URL de la variable **[!UICONTROL Contact Page]**. Cette page peut être une liste des contacts de sécurité du magasin ou votre _Nous contacter_ page.

   ![Configuration des informations de contact](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Other Information]_, saisissez ce qui suit :

   - L&#39;URL de votre public **[!UICONTROL Encryption]** clé. Par exemple: `https://example.com/pgp-key.txt`

   - L’URL d’une **[!UICONTROL Acknowledgments]** où les chercheurs en sécurité sont reconnus pour leurs efforts au nom de votre boutique.

   - Votre **[!UICONTROL Preferred Languages]** pour les communications liées à la sécurité. Saisissez les deux caractères standard [code de langue](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) pour chaque langue prise en charge, séparés par une virgule. Par exemple, pour indiquer l’anglais, l’espagnol et le français, saisissez `en, es, fr`. Toutes les langues spécifiées ont la même priorité, quel que soit leur ordre d’apparition.

   - L’URL d’une **[!UICONTROL Hiring]** qui répertorie les opportunités d’emploi liées à la sécurité dans votre boutique.

   - URL de votre sécurité **[!UICONTROL Policy]** page.

   - L’URL d’un fichier numérique **[!UICONTROL Signature]** qui est enregistré sur votre serveur. Par exemple: `https://mystore.com/.well-known/security.txt.sig`

   La signature numérique doit être configurée à partir de l’interface de ligne de commande (CLI) du serveur. Pour en savoir plus, voir [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) sur GitHub.

   ![Autres informations](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
