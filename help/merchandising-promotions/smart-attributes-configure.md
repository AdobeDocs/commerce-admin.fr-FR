---
title: Configuration des attributs intelligents pour Visual Merchandiser
description: Découvrez comment configurer les attributs intelligents utilisés par le marchandiseur visuel.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: 'https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 76cfaac4-e563-56dd-8938-708bf8b84956
    internal-label: Attributes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%
---
# Configuration des attributs intelligents pour Visual Merchandiser

{{ee-feature}}

La configuration du marchandiseur visuel détermine les attributs qui peuvent être utilisés dans la fenêtre de marchandisage et le seuil de stock minimal. La configuration identifie également l’attribut utilisé pour la couleur et l’ordre des valeurs de couleur.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Visual Merchandiser]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General Options]** .

   ![Configuration du catalogue - Marchandiseur visuel](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. Dans la liste **[!UICONTROL Attributes for Category Rules]**, sélectionnez chaque attribut que vous souhaitez rendre disponible pour le marchandisage visuel.

   Pour sélectionner plusieurs attributs, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque élément.

1. Saisissez le **[!UICONTROL Minimum Stock Threshold]** d’affichage d’un produit dans la fenêtre Visual Merchandiser .

1. Saisissez le **[!UICONTROL Color Attribute Code]**.

   La valeur par défaut est `color`. Si votre catalogue utilise un attribut différent, saisissez le nom de l’attribut en minuscules.

1. Par **[!UICONTROL Color Order]**, saisissez chaque valeur de couleur sur une ligne distincte et dans l’ordre pour déterminer la priorité de chaque couleur.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
