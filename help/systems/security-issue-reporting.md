---
title: Rapports sur les problèmes de sécurité
description: Découvrez comment configurer les coordonnées et les liens liés à la sécurité qui peuvent être utilisés par les chercheurs en sécurité pour signaler les problèmes de sécurité sur votre site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Rapports sur les problèmes de sécurité

Le fichier `security.txt` contient des informations de contact et des liens liés à la sécurité qui peuvent être utilisés par les chercheurs en sécurité pour signaler les problèmes de sécurité liés à votre site. Si vos informations de sécurité changent au fil du temps, vérifiez que les informations du fichier `security.txt` sont à jour.

**_Pour configurer security.txt:_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL Security]_, cliquez sur **[!UICONTROL Security.txt]**.

1. Dans la section _[!UICONTROL General]_, définissez **[!UICONTROL Enable]**&#x200B;sur `Yes`.

   ![Configuration générale de la sécurité](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Contact Information]_, saisissez ce qui suit :

   - Adresse électronique et numéro de téléphone de la personne qui gère les problèmes de sécurité pour votre boutique.

   - L’URL de **[!UICONTROL Contact Page]** de votre boutique. Cette page peut être une liste de contacts de sécurité du magasin ou votre page _Nous contacter_.

   ![Configuration des coordonnées](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Other Information]_, saisissez ce qui suit :

   - URL de votre clé publique **[!UICONTROL Encryption]**. Par exemple : `https://example.com/pgp-key.txt`

   - URL d’une page **[!UICONTROL Acknowledgments]** où les chercheurs en sécurité sont reconnus pour leurs efforts pour le compte de votre boutique.

   - Votre **[!UICONTROL Preferred Languages]** pour les communications liées à la sécurité. Saisissez le [code de langue](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard à deux caractères pour chaque langue prise en charge, séparé par une virgule. Par exemple, pour indiquer l’anglais, l’espagnol et le français, saisissez `en, es, fr`. Toutes les langues spécifiées ont la même priorité, quel que soit leur ordre d’apparition.

   - URL d’une page **[!UICONTROL Hiring]** qui répertorie les opportunités d’emploi liées à la sécurité dans votre magasin.

   - URL de la page de sécurité **[!UICONTROL Policy]**.

   - URL d’un fichier numérique **[!UICONTROL Signature]** enregistré sur votre serveur. Par exemple : `https://mystore.com/.well-known/security.txt.sig`

   La signature numérique doit être configurée à partir de l’interface de ligne de commande (CLI) du serveur. Pour en savoir plus, voir [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) sur GitHub.

   ![Autres informations](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
