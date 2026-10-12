---
title: Importer des produits téléchargeables
description: Consultez un exemple d’importation de données de produit pour un produit téléchargeable.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: 'https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%
---
# Importer des produits téléchargeables

Le flux d’importation des produits téléchargeables est le même que pour les [Produits groupés](data-transfer-bundle-products.md) ou [Produits configurables](data-transfer-configurable-products.md). La différence est qu’un produit téléchargeable comporte des [liens téléchargeables](../catalog/product-create-downloadable.md) et des [exemples téléchargeables](../catalog/product-create-downloadable.md) avec ses images.

Le répertoire racine par défaut pour les liens et exemples téléchargeables est `<Magento-root-folder>/pub/media/import`. Si le module de stockage distant est activé, le répertoire racine par défaut pour les liens téléchargeables et les exemples est le répertoire `<remote-storage-root-folder>/media/import`.

Le fichier CSV comporte des colonnes distinctes pour `downloadable_links` et `downloadable_samples`.

- **Images de lien téléchargeables** — Dans l&#39;exemple suivant, les images de lien téléchargeables (`red.jpg` et `black.jpg`) se trouvent dans le dossier `<Magento-root-folder>/pub/media/import/test`. Si le stockage distant est activé, ces images se trouvent dans le dossier `<remote-storage-root-folder>/media/import/test` .

  ![Exemple de données - produit téléchargeable avec liens téléchargeables](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Exemples d’images téléchargeables** — Dans l’exemple suivant, l’exemple d’image téléchargeable (`white.jpg`) se trouve dans le dossier `<Magento-root-folder>/pub/media/import/test`. Si le stockage distant est activé, cette image se trouve dans le dossier `<remote-storage-root-folder>/media/import/test`.

  ![Exemple de données - produit téléchargeable avec des exemples téléchargeables](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Pour plus d’informations sur l’activation et la gestion du module de stockage distant, voir [Configurer le stockage distant](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage) dans le _Guide de configuration_.
