---
title: Configuration de la conception
description: La configuration de conception facilite la modification des règles et des paramètres de configuration liés à la conception en affichant les paramètres sur une seule page.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Configuration de la conception

La configuration Conception facilite la modification des règles et des paramètres de configuration liés à la conception en affichant les paramètres sur une seule page.

![Page de configuration de conception](./assets/configuration.png){width="700" zoomable="yes"}

## Modification de la configuration de conception

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin que vous souhaitez configurer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

   La page affiche les paramètres de conception actuels de la vue de magasin.

1. Pour modifier le thème par défaut, définissez **[!UICONTROL Applied Theme]** sur le thème que vous souhaitez appliquer à la vue.

   Si aucun thème n’est spécifié, le thème par défaut du système est utilisé. Certaines extensions tierces modifient le thème par défaut du système.

1. Si le thème doit être utilisé uniquement pour un appareil spécifique, définissez **[!UICONTROL User Agent Rules]**.

   ![Règles User-Agent](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Pour chaque type d’appareil sur lequel vous souhaitez spécifier un thème :

   - Cliquez sur **[!UICONTROL Add New User Agent Rule]**.

   - Pour **[!UICONTROL Search String]**, saisissez l’identifiant du navigateur pour l’appareil spécifique.

     Une chaîne de recherche peut être soit une expression normale, soit une expression régulière compatible avec Perl (PCRE) (voir [User Agent](https://en.wikipedia.org/wiki/User_agent) pour plus d’informations). La chaîne de recherche suivante identifie Firefox :

         /^mozilla/i
     
   - Pour **[!UICONTROL Theme Name]**, choisissez le thème à utiliser pour l’appareil spécifié.

   >[!NOTE]
   >
   >Vous pouvez ajouter autant de règles que vous le souhaitez pour les appareils que vous souhaitez désigner. Les chaînes de recherche correspondent dans l’ordre dans lequel elles sont entrées.

1. Sous _[!UICONTROL Other Settings]_, développez chaque section et suivez les instructions des rubriques liées pour modifier les paramètres si nécessaire.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Autres paramètres pour affecter la conception](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Configuration]**.
