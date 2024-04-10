---
title: Importer des données
description: Découvrez les instructions relatives à l’importation des données et comment utiliser les opérations d’importation de données.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 1c1327dbda76283ae28f761d1e523e049e0e492f
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%

---

# Importer des données

Les données de tous les types de produits peuvent être importées dans le magasin. En outre, vous pouvez importer des produits, des données de tarification avancées, des données client, des données d’adresse client et des images de produits. L’importation prend en charge les opérations suivantes :

- Ajouter/Mettre à jour
- Replace
- Supprimer

## Instructions d’importation

### Nouvelles entités

- Les entités sont ajoutées avec les valeurs d’attribut spécifiées dans le fichier CSV.
- Pour un attribut obligatoire sans valeur par défaut définie, l&#39;entité (la ou les lignes correspondantes) ne peut pas être importée s&#39;il n&#39;existe aucune valeur ou si une valeur n&#39;est pas valide.
- Pour un attribut obligatoire dont la valeur par défaut est définie, l’entité (la ou les lignes correspondantes) est importée et la valeur par défaut est définie pour l’attribut s’il n’existe aucune valeur ou une valeur non valide.
- Si les données complexes ne sont pas valides, l&#39;entité (la ou les lignes correspondantes) ne peut pas être importée.

### Entités existantes

- Pour les attributs qui ne sont pas des données complexes, les valeurs du fichier d’importation, y compris les valeurs vides pour les attributs non obligatoires, remplacent les valeurs existantes.
- S’il n’existe aucune valeur, ou s’il existe une valeur non valide, pour un attribut obligatoire, la valeur existante n’est pas remplacée.
- Si les données complexes de l’entité ne sont pas valides, l’entité (la ou les lignes correspondantes) ne peut pas être importée, sauf dans le cas où Supprimer les entités a été sélectionné dans le menu déroulant Comportement d’importation .

### Données complexes

Si un attribut spécifié dans le fichier d’importation existe et que sa valeur est dérivée d’un ensemble défini de valeurs, les conditions suivantes s’appliquent :

- Si la valeur n’est pas déjà incluse dans l’ensemble de valeurs défini, la ligne peut être importée et une valeur par défaut, si elle est définie, est définie pour l’attribut .
- Si la valeur est déjà incluse dans le jeu défini, la ligne correspondante ne peut pas être importée.
- Si le fichier d’importation spécifie un nom d’attribut qui n’est pas encore défini dans le système, il n’est pas créé et ses valeurs ne sont pas importées.

### Fichiers non valides

- Un fichier ne peut pas être importé si toutes les lignes ne sont pas valides.
- Une donnée de service non existante ou un nom de données complexe est spécifié dans le fichier d’importation, par exemple une colonne avec un `_<non-existing name>` titre.

Le processus d’importation d’Adobe Commerce peut ne pas reconnaître correctement les fichiers codés en UTF-8 qui utilisent une marque d’ordre d’octet (BOM). Les fichiers contenant une nomenclature peuvent entraîner des problèmes ou des échecs au cours du processus d&#39;importation.

## Opérations d’import

| Opération | Description |
| --------- | ----------- |
| Ajouter/Mettre à jour | Les nouvelles données de produit sont ajoutées aux données de produit existantes pour les entrées existantes dans la base de données. Tous les champs sauf `sku` peuvent être mises à jour.<br><br>Les nouvelles classes de taxe spécifiées dans les données d&#39;importation sont créées automatiquement.<br><br>Les nouvelles catégories de produits spécifiées dans le fichier d’importation sont créées automatiquement.<br><br>Les nouveaux SKU spécifiés dans le fichier d’importation sont créés automatiquement <br><br>**_Remarque :_**Pour les produits , vous pouvez mettre à jour tous les champs sauf le SKU grâce à l’importation.<br><br>**_Important :_** Plusieurs valeurs de champ, telles que des sites web ou des catégories, ne peuvent pas être supprimées à l’aide du _Ajouter/Mettre à jour_ Comportement d’importation. Ces champs restent dans la base de données après l’importation s’ils ne sont pas répertoriés dans le fichier CSV. |
| Replace | Les données de produit existantes sont remplacées par de nouvelles données.<br><br>**_Important :_**Faites preuve de prudence lorsque vous remplacez des données, car les données de produit existantes sont effacées et toutes les références du système sont perdues.<br><br>Si un SKU dans les données d’importation correspond au SKU d’une entité existante, tous les champs, y compris le SKU, sont supprimés et un nouvel enregistrement est créé à l’aide des données CSV. Une erreur se produit si le fichier CSV fait référence à un SKU qui n’existe pas dans la base de données. Vous pouvez Vérifier les données pour afficher l’erreur. |
| Supprimer | Toutes les entités présentes dans la base de données d&#39;importation sont supprimées de la base de données.<br><br>La suppression ignore toutes les colonnes des données d’importation, à l’exception de la SKU. Vous pouvez ignorer tous les autres attributs dans les données.<br><br>Une erreur se produit si le fichier CSV fait référence à un SKU qui n’existe pas dans la base de données. Vous pouvez Vérifier les données pour afficher l’erreur. |

{style="table-layout:auto"}

## Processus d’import

La taille du fichier d’importation est déterminée par les paramètres dans le `php.ini` fichier sur le serveur. Message système sur le _Importer_ indique la limite de taille actuelle. La taille par défaut est de 2 Mo.

Les caractères spéciaux (tels que le signe égal, les symboles supérieur et inférieur à, les guillemets simples et doubles, la barre oblique inverse, la barre verticale et les esperluettes) peuvent entraîner des problèmes lors du transfert de données. Pour vous assurer que ces caractères spéciaux sont correctement interprétés, ils peuvent être marqués comme _séquence d&#39;échappement_. Par exemple, si les données incluent une chaîne de texte telle que : `code="str"`, `code="str2"`, le fait de placer le texte entre guillemets doubles garantit que les guillemets doubles d’origine sont compris comme faisant partie des données. Lorsque le système rencontre un double ensemble de guillemets doubles, il comprend que l&#39;ensemble externe de guillemets doubles entoure les données réelles.

Lors de l’importation de données de produit, les nouvelles données de produit sont ajoutées aux entrées de données de produit existantes dans la base de données. Tous les champs, à l’exception du SKU, peuvent être mis à jour par le biais de l’importation. Toutes les données de produit existantes sont remplacées par les nouvelles données importées. Faites preuve de prudence lorsque vous remplacez des données. Toutes les données de produit existantes sont effacées et toutes les références du système sont perdues.

![Import de données](./assets/import-options.png){width="600" zoomable="yes"}

### Étape 1 : préparation des données

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _Importer paramètres_, set **[!UICONTROL Entity Type]** à l’un des éléments suivants :

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Clic **[!UICONTROL Download Sample File]**.

1. Localisez le fichier d’exportation à l’emplacement de téléchargement de votre navigateur web et ouvrez le fichier.

   L’exemple de fichier comprend des en-têtes de colonne avec des données d’espace réservé pour les types de produits.

   ![Importer un fichier d’exemple de données](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Examinez la structure du fichier d’exemple et utilisez-le pour préparer votre fichier d’importation CSV en vous assurant que les en-têtes des colonnes sont correctement orthographiés.

1. Vérifiez que la taille du fichier d’importation ne dépasse pas la limite affichée dans le message.

   ![Notification de la taille de l&#39;import de données](./assets/data-import-size-notification.png){width="600"}

1. Si les données d’importation comprennent des chemins d’accès aux images du produit, assurez-vous que les fichiers image ont été chargés à l’emplacement approprié.

   L’emplacement par défaut sur le serveur Commerce est le suivant : `pub/media/import`.

   Si les images résident sur un serveur externe, vérifiez que vous disposez de l’URL complète du répertoire contenant les images.

### Etape 2 : choix du comportement de l&#39;import

![Comportement d’importation des données](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Import Behavior]** à l’un des éléments suivants :

   - `Add/Update` (Pour les produits, vous pouvez mettre à jour tous les champs à l’exception du SKU via l’importation.)
   - `Replace`
   - `Delete`

1. Pour déterminer ce qui se produit lorsqu’une erreur se produit lors de l’importation de données, choisissez l’une des options suivantes :

   - `Stop on Error`
   - `Skip error entries`

1. Pour **[!UICONTROL Allowed Errors Count]**, saisissez le nombre d’erreurs pouvant se produire avant l’annulation de l’importation.

   La valeur par défaut est 10.

1. Accepter la valeur par défaut d’une virgule (`,`) pour **[!UICONTROL Field separator]**.

1. Accepter la valeur par défaut d’une virgule (`,`) pour **[!UICONTROL Multiple value separator]**.

   Dans un fichier CSV, une virgule est le séparateur par défaut. Pour utiliser un autre caractère, assurez-vous que les données du fichier CSV correspondent au caractère spécifié.

1. Accepter la valeur par défaut `_EMPTY_VALUE_` pour **[!UICONTROL Empty attribute value constant]**.

1. Si vous souhaitez entourer des caractères spéciaux pouvant se trouver dans les données sous la forme d’un _séquence d&#39;échappement_, sélectionnez le **[!UICONTROL Fields Enclosure]** case à cocher.

### Étape 3 : identifier le fichier d&#39;import

![Fichier d’import de données](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Choose File]** pour sélectionner le fichier à importer.

1. Recherchez le fichier CSV que vous êtes prêt à importer et cliquez **[!UICONTROL Open]**.

1. Pour **[!UICONTROL Images File Directory]**, saisissez le chemin d’accès relatif à l’emplacement sur le serveur de Commerce où sont stockées les images chargées.

   Par exemple : `product_images`.

   >[!NOTE]
   >
   >Prise en main d’Adobe Commerce et de Magento Open Source `2.3.2` version, chemin spécifié dans _[!UICONTROL Images File Directory]_concatène pour l’importation dans le répertoire de base des images : `<Magento-root-folder>/var/import/images`. Par exemple, placez le `product_images` fichiers dans le `<Magento-root-directory>/var/import/images/product_images` dossier. Le répertoire de base des images d&#39;import peut être configuré dans le `\Magento\ImportExport\etc\config.xml` fichier . Si le module de stockage distant est activé, importez les fichiers dans le `<remote-storage-root-directory>/var/import/images/product_images` dossier.

   Pour en savoir plus sur l’importation d’images de produit, voir [Importer des images de produit](data-import-product-images.md).

### Étape 4 : vérifier les données d’importation

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Check Data]**.

1. Patientez quelques instants le temps que le processus de validation se termine.

   Si les données d&#39;import sont valides, le message suivant apparaît :

   ![Message de succès - Le fichier est valide](./assets/data-import-validation-message.png){width="600"}

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

   Sinon, corrigez chaque problème avec les données répertoriées dans le message et réessayez d’importer le fichier.

1. Le processus d’importation se poursuit jusqu’à la fin des données, sauf si une erreur se produit.

   Si un message d’erreur s’affiche dans les résultats de la validation, corrigez le problème dans les données et importez à nouveau le fichier.

   ![Message d’erreur - La clé URL existe déjà](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Un message s’affiche une fois l’importation terminée.

## Historique des imports

Commerce conserve un enregistrement des données importées dans votre magasin, notamment la date et l’heure de début, l’utilisateur, l’heure d’exécution et un lien vers le fichier importé. Le _Heure d’exécution_ correspond à la durée du processus d’importation.

**_Pour afficher l’historique des imports :_**

Le _Admin_ barre latérale, accéder à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Historique des imports de données](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Par défaut, les fichiers d’historique d’importation se trouvent dans `<Magento-root-directory>/var/import_history` dossier. Si le module de stockage distant est activé, les fichiers d’historique d’importation se trouvent dans le `<remote-storage-root-directory>/import_export/import_history` dossier.

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Numéro interne utilisé pour désigner un transfert. |
| [!UICONTROL Start Date & Time] | Date et heure spécifiques auxquelles le transfert a eu lieu. |
| [!UICONTROL User] | Client qui a effectué le transfert. |
| [!UICONTROL Imported file] | Lien de téléchargement du fichier importé. |
| [!UICONTROL Error file] | Fichier d’erreur correspondant. |
| [!UICONTROL Execution Time] | Intervalle de temps du processus d’importation. |
| [!UICONTROL Summary] | Nombre d’éléments créés, mis à jour et supprimés, ou message d’erreur. |

{style="table-layout:auto"}

Pour télécharger le _Importé/Erreur_ fichier, cliquez sur **[!UICONTROL Download]**.
