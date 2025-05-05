---
title: Importation de produits téléchargeables
description: Examinez un exemple d’importation de données de produit pour un produit téléchargeable.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Importation de produits téléchargeables

Le flux d&#39;importation des produits téléchargeables est le même que pour [Bundle Products](data-transfer-bundle-products.md) ou [Configurable Products](data-transfer-configurable-products.md). La différence est qu’un produit téléchargeable contient [des liens téléchargeables](../catalog/product-create-downloadable.md) et des [exemples téléchargeables](../catalog/product-create-downloadable.md) avec ses images.

Le répertoire racine par défaut pour les exemples et liens téléchargeables est `<Magento-root-folder>/pub/media/import`. Si le module de stockage distant est activé, le répertoire racine par défaut pour les exemples et liens téléchargeables est le répertoire `<remote-storage-root-folder>/media/import`.

Le fichier CSV contient des colonnes distinctes pour `downloadable_links` et `downloadable_samples`.

- **Images de lien téléchargeables** — Dans l’exemple suivant, les images de lien téléchargeables (`red.jpg` et `black.jpg`) se trouvent dans le dossier `<Magento-root-folder>/pub/media/import/test`. Si le stockage à distance est activé, ces images se trouvent dans le dossier `<remote-storage-root-folder>/media/import/test`.

  ![Exemple de données - produit téléchargeable avec liens téléchargeables](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Exemple d’image téléchargeable** — Dans l’exemple suivant, l’exemple d’image téléchargeable (`white.jpg`) se trouve dans le dossier `<Magento-root-folder>/pub/media/import/test`. Si le stockage à distance est activé, cette image se trouve dans le dossier `<remote-storage-root-folder>/media/import/test`.

  ![Exemple de données - produit téléchargeable avec exemples téléchargeables](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Pour plus d’informations sur l’activation et la gestion du module de stockage distant, voir [Configuration du stockage distant](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=fr) dans le _Guide de configuration_.
