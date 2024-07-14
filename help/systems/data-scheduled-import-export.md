---
title: Import et export planifiés
description: Découvrez comment gérer les opérations d’import et d’export de données planifiées.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2378'
ht-degree: 0%

---

# Import et export planifiés

{{ee-feature}}

Les imports et exports planifiés peuvent être exécutés sur une base quotidienne, hebdomadaire ou mensuelle. Les fichiers à importer ou exporter peuvent résider sur des serveurs Adobe Commerce locaux ou sur des serveurs FTP distants. L’importation/exportation planifiée est implémentée par défaut et ne nécessite pas de configuration supplémentaire. Tous les imports et exports planifiés sont gérés par le planificateur de tâches Cron.

## Accès à l’importation/exportation planifiée

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![Importation/exportation de données planifiées](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Pour créer une tâche d’importation ou d’exportation planifiée, cliquez sur le bouton approprié et suivez les instructions correspondant au type de tâche planifiée.

   - [Ajout d’une exportation planifiée](#schedule-an-export)
   - [Ajout d’une importation planifiée](#schedule-an-import)

1. Lorsque l’enregistrement est enregistré, la tâche s’affiche dans la grille _[!UICONTROL Scheduled Import/Export]_.

   >[!NOTE]
   >
   >Lorsque vous créez ou mettez à jour une importation/exportation planifiée, la configuration du système change. Après l’enregistrement, veillez à respecter l’avis d’invalidation du cache qui s’affiche en haut de la page Admin et à vider le cache afin d’appliquer la planification nouvelle ou mise à jour.

1. Après chaque tâche planifiée, une copie du fichier est placée dans le répertoire `var/log/import_export` sur le serveur local Adobe Commerce.

   Les détails de chaque opération ne sont pas écrits dans le journal. Si une erreur se produit, une notification est envoyée de la tâche d’importation/exportation ayant échoué, avec une description de l’erreur.

## Planification d’une importation

Pour le format de fichier d’importation disponible et les types d’entités d’importation, le processus d’importation planifié est similaire au processus d’importation manuelle :

- Le fichier d’importation doit être au format .CSV
- Vous pouvez importer des données sur les produits et les clients.

L’avantage de l’import planifié est que vous pouvez importer automatiquement un fichier de données plusieurs fois après avoir spécifié les paramètres d’import et planifier une seule fois.

Les détails de chaque opération d’importation ne sont pas écrits dans un journal, mais en cas d’échec, vous recevez un e-mail _Import Failed_ avec une description de l’erreur. Le résultat de la dernière tâche d’importation planifiée s’affiche dans la colonne Dernier résultat de la page Importation/Exportation planifiée .

Après chaque opération d’importation, une copie du fichier d’importation est placée dans le répertoire `var/log/import_export` sur le serveur sur lequel Adobe Commerce ou Magento Open Source est déployé. L&#39;horodatage, le marqueur de l&#39;entité importée (produits ou clients) et le type d&#39;opération (dans ce cas, import) sont ajoutés au nom du fichier d&#39;import.

Après chaque tâche d’importation planifiée, une opération de réindexation est effectuée automatiquement. En amont, les modifications apportées aux descriptions et aux autres informations textuelles sont répercutées une fois les données mises à jour récupérées dans la base de données, et les modifications apportées aux prix ne sont répercutées qu’après l’opération de réindexation.

### Etape 1 : paramétrage de l&#39;import

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Scheduled Import]**.

1. Définissez les options de planification et d’importation :

   - **[!UICONTROL Name]** — Saisissez un nom pour l’importation planifiée.

   - **[!UICONTROL Description]** — Entrez une brève description qui explique l’objectif de l’importation et son utilisation.

   - **[!UICONTROL Entity Type]** — Définissez sur l’une des options suivantes :

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** — Définissez sur l’une des options suivantes :

      - `Add/Update Complex Data` — Ajoute ou met à jour de nouvelles données complexes aux données complexes existantes pour les entrées existantes dans la base de données. Il s’agit de la valeur par défaut.
      - `Replace` — Écrit sur le complexe existant pour les entités existantes dans la base de données.
      - `Delete Entities` — Supprime les entrées existantes dans la base de données.
      - `Custom Action` - Personnalise les entités existantes dans la base de données.

     >[!NOTE]
     >
     >Pour les types d’entités _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_et_[!UICONTROL Stock Sources]_, ces comportements d’importation s’affichent : `Add/Update`, `Replace` et `Delete`. Pour les types d&#39;entités _Customer Finances_, _Customers Main File_ et _Customers and Addresses_, ces comportements d&#39;importation s&#39;affichent : `Add/Update Complex Data`, `Delete Entities` et `Custom Action`.

   - **[!UICONTROL Start Time]** — Défini sur l’heure, la minute et la seconde auxquelles l’importation est planifiée pour commencer.

   - **[!UICONTROL Frequency]** — Défini sur l’une des valeurs suivantes : `Daily`, `Weekly` ou `Monthly`

   - **[!UICONTROL On Error]** - Défini sur l’une des valeurs suivantes : `Stop Import` ou `Continue Processing`

   - **[!UICONTROL Status]** — Pour activer l’importation planifiée, définissez sur `Enabled`.

   - **[!UICONTROL Field Separator]** — Entrez le caractère utilisé pour séparer les champs dans le fichier d’importation. Le caractère par défaut est une virgule.

   - **[!UICONTROL Multiple Value Separator]** — Entrez le caractère utilisé pour séparer plusieurs valeurs dans un champ.

   ![Importation de données - paramètres d’importation planifiés](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Etape 2 : renseigner les informations sur le fichier d&#39;import

1. Définissez **[!UICONTROL Server Type]** sur l’une des options suivantes :

   - `Local Server` - Importe les données du même serveur que celui sur lequel Adobe Commerce est installé.
   - `Remote FTP` - Importe les données d’un serveur distant.

   ![Importation de données - informations de fichier d’importation planifié](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Lorsque le module de stockage distant est activé, `Local Server` passe automatiquement à `Remote Storage`.

1. Saisissez le **[!UICONTROL File Directory]** d’où provient le fichier d’importation.

   - `Local Server` - Entrez un chemin relatif dans l’installation de Commerce. Par exemple, `var/import`. Si le module de stockage à distance est configuré, utilisez `import_export/import`.
   - `Remote FTP server` - Entrez l’URL complète et le chemin d’accès au dossier d’importation sur le serveur distant.

1. Saisissez le **[!UICONTROL File Name]** à importer.

1. Pour **[!UICONTROL Images File Directory]**, saisissez le chemin d’accès au répertoire dans lequel les images de produit sont stockées.

   Sur un serveur local, saisissez un chemin relatif tel que : `var/import`. Sur un stockage distant, saisissez un chemin relatif tel que : `import_export/import` ou `import_export/import/some/dir`.

### Etape 3 : configurer l&#39;import des emails en échec

![ Import de données - échec de l’importation des emails échoués](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Failed Email Receiver]** sur le contact du magasin qui doit recevoir la notification si une erreur se produit pendant l’importation.

1. Définissez **[!UICONTROL Failed Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur de la notification.

1. Définissez **[!UICONTROL Failed Email Template]** sur le modèle utilisé pour la notification.

1. Pour **[!UICONTROL Send Failed Email Copy To]**, saisissez l’adresse électronique de toute personne devant recevoir une copie de la notification.

   Séparez plusieurs adresses électroniques par une virgule.

1. Définissez **[!UICONTROL Failed Email Copy Method]** sur l’une des options suivantes :

   - `Bcc` - Envoie une copie de courtoisie aveugle de la notification d’importation ayant échoué. Le nom et l’adresse du destinataire sont inclus dans la distribution de l’email d’origine, mais sont masqués de la vue.
   - `Separate Email` - Envoie une copie de la notification d’importation ayant échoué sous la forme d’un email distinct.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   La nouvelle tâche d’importation planifiée est ajoutée à la liste sur la page _[!UICONTROL Scheduled Import/Export]_. À partir de cette page, il peut être exécuté immédiatement pour le test et modifié. Le fichier d&#39;import est validé avant l&#39;exécution de chaque traitement d&#39;import.

>[!NOTE]
>
>Lorsque vous créez ou mettez à jour une importation/exportation planifiée, la configuration du système change. Après l’enregistrement, veillez à respecter l’avis d’invalidation du cache qui s’affiche en haut de la page Admin et à vider le cache afin d’appliquer la planification nouvelle ou mise à jour.

### Descriptions des champs

#### [!UICONTROL Import Settings]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Name] | Nom de l’importation. Permet de le distinguer si de nombreux imports planifiés différents sont créés. |
| [!UICONTROL Description] | (Facultatif) Vous pouvez saisir une description. |
| [!UICONTROL Entity Type] | Définit les données à importer. |
| [!UICONTROL Import Behavior] | Définit comment les données complexes sont traitées si les entités importées existent dans la base de données. Les données complexes relatives aux produits comprennent les catégories, les sites web, les options personnalisées, les prix de niveau, les produits associés, les ventes incitatives, les ventes croisées et les données sur les produits associés. Les données complexes pour les clients incluent les adresses. Options :<br>**[!UICONTROL Add/Update Complex Data]**- Les nouvelles données complexes sont ajoutées ou mises à jour aux données complexes existantes pour les entrées existantes dans la base de données. Il s’agit de la valeur par défaut.<br>**[!UICONTROL Add/Update]** - De nouvelles données sont ajoutées aux entrées existantes dans la base de données. Tous les champs, à l’exception de `sku`, peuvent être mis à jour pour les produits. Toutes les valeurs de champs multiples qui ne sont pas répertoriées dans le fichier CSV, telles que les catégories ou les sites web, restent dans la base de données après l’importation.<br>**[!UICONTROL Replace]**- Les données complexes existantes pour les entités existantes sont remplacées.<br>**[!UICONTROL Delete Entities]** - Si des entités importées existent dans la base de données, elles sont supprimées de la base de données.<br>**[!UICONTROL Custom Action]**- Les entités complexes existantes sont personnalisées pendant le processus d’importation. |
| [!UICONTROL Start Time] | Définissez l’heure de début, les minutes et les secondes de l’importation. |
| [!UICONTROL Frequency] | Définissez la fréquence d’exécution de l’importation. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Définissez le comportement du système au cas où des erreurs seraient détectées lors de la validation du fichier. Options : <br>**Arrêter l’importation** — Le fichier n’est pas importé si des erreurs sont détectées lors de la validation. Il s’agit de la valeur par défaut.<br>**Continuer le traitement** - Si des erreurs sont détectées lors de la validation, mais que l’importation est possible, le fichier est importé. |
| [!UICONTROL Status] | L’importation est activée par défaut. Vous pouvez le suspendre en définissant l’état sur `Disabled`. |
| [!UICONTROL Field Separator] | Détermine le caractère utilisé pour séparer les champs. Valeur par défaut : `,` (virgule) |
| [!UICONTROL Multiple Value Separator] | Détermine le caractère utilisé pour séparer plusieurs valeurs dans un champ. Valeur par défaut : `,` (virgule) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Vous pouvez importer depuis un fichier sur le même serveur que celui sur lequel Commerce est déployé (sélectionnez `Local Server`) ou depuis le serveur FTP distant (sélectionnez `Remote FTP`). Si vous sélectionnez _[!UICONTROL Remote FTP]_, des options supplémentaires pour les informations d’identification et les paramètres de transfert de fichiers s’affichent. Si le module de stockage distant est activé, le type `Local Server` est automatiquement activé sur `Remote Storage`. |
| [!UICONTROL File Directory] | Spécifiez le répertoire dans lequel se trouve le fichier d’importation. Si Server Type est défini sur _[!UICONTROL Local Server]_, spécifiez le chemin d’accès relatif au répertoire d’installation de Commerce. Par exemple : `var/import` ou `import_export/import` pour le stockage à distance. |
| [!UICONTROL File Name] | Indiquez le nom du fichier d&#39;importation. |
| [!UICONTROL Images File Directory] | Entrez le chemin d’accès au répertoire dans lequel les images de produit sont stockées. Pour un serveur local, saisissez un chemin relatif. Par exemple : `var/import` ou `import_export/import` pour le stockage à distance. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Indiquez l’adresse électronique à laquelle une notification électronique (message électronique d’importation en échec) est envoyée en cas d’échec de l’importation. |
| [!UICONTROL Failed Email Sender] | Indiquez l’adresse électronique utilisée comme expéditeur de l’e-mail d’importation qui a échoué. |
| [!UICONTROL Failed Email Template] | Sélectionnez un modèle pour le courrier électronique importé en échec. Par défaut, seule l’option Échec de l’importation (modèle par défaut à partir des paramètres régionaux) est disponible. Les modèles personnalisés peuvent être créés sous _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | Adresse électronique à laquelle une copie du courrier électronique d’importation a échoué est envoyée. |
| [!UICONTROL Send Failed Email Copy Method] | Sélectionnez la méthode d&#39;envoi de copie pour l&#39;email importé en échec. |

{style="table-layout:auto"}

## Planification d’une exportation

L’exportation planifiée est similaire à une [exportation](data-export.md) manuelle dans le format de fichier d’exportation disponible et les types d’entités qui peuvent être exportés :

- Vous pouvez effectuer une exportation au format CSV.
- Vous pouvez exporter des données sur les produits et les clients

L’avantage de l’utilisation de l’option Exportation planifiée est que vous pouvez exporter les données plusieurs fois automatiquement, après avoir spécifié les paramètres d’exportation, et ne planifier qu’une seule fois.

Les détails de chaque exportation ne sont pas écrits dans un journal, mais en cas d’échec, vous recevez un email Export Failed (Échec de l’exportation), qui contient la description de l’erreur. Le résultat de la dernière tâche d’exportation apparaît dans la colonne Dernier résultat de la page Importation/Exportation planifiée .

Après chaque exportation, le fichier d’exportation est placé à l’emplacement défini par l’utilisateur et une copie dans le répertoire `var/log/import_export` sur le serveur sur lequel Adobe Commerce ou Magento Open Source est déployé. L’horodatage et le marqueur de l’entité exportée (produits ou clients) et le type d’opération (dans ce cas, export) sont ajoutés au nom du fichier d’export.

### Étape 1 : Définition des paramètres d’exportation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Scheduled Export]** et procédez comme suit :

   - Saisissez un **[!UICONTROL Name]** pour l’exportation planifiée.

   - Saisissez un résumé **[!UICONTROL Description]** expliquant l’objectif de l’exportation et la manière dont elle doit être utilisée.

   - Définissez **[!UICONTROL Entity Type]** sur l’une des options suivantes :

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     La section _[!UICONTROL Entity Attributes]_au bas de la page est mise à jour pour prendre en compte le type d’entité sélectionné.

   - Définissez **[!UICONTROL Start Time]** sur l’heure, la minute et la seconde auxquelles l’exportation est planifiée pour commencer.

   - Définissez **[!UICONTROL Frequency]** sur l’une des options suivantes :

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Pour activer l’exportation planifiée, définissez **[!UICONTROL Status]** sur `Enabled`.

1. Acceptez `CSV` comme valeur par défaut **[!UICONTROL File Format]**.

   ![Paramètres d’exportation planifiés](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Etape 2 : renseigner les informations sur le fichier d&#39;export

1. Définissez **[!UICONTROL Server Type]** sur l’une des options suivantes :

   - `Local Server` - Pour enregistrer le fichier d’exportation sur le même serveur que celui sur lequel Commerce est installé.
   - `Remote FTP` — Pour enregistrer le fichier d’exportation sur un serveur distant.

   ![Informations sur les fichiers d’exportation planifiés](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Lorsque le module de stockage distant est activé, le `Local Server` passe automatiquement à `Remote Storage`.

1. Pour **[!UICONTROL File Directory]**, saisissez le répertoire dans lequel le fichier d&#39;export doit être enregistré comme suit :

   - Pour **[!UICONTROL Local Server]**, saisissez un chemin relatif dans l’installation de Commerce, par exemple `var/export`. Si le module de stockage distant est configuré, utilisez `import_export/export`.
   - Pour **[!UICONTROL Remote FTP server]**, saisissez l’URL complète et le chemin d’accès au dossier cible sur le serveur de destination.

1. Si le serveur _[!UICONTROL Remote FTP]_est sélectionné, saisissez les informations de connexion au serveur et sélectionnez des paramètres supplémentaires :

   - Pour **[!UICONTROL FTP Host[:Port]]**, saisissez l’adresse d’hôte FTP distante.
   - Pour **[!UICONTROL User Name]**, saisissez le nom d’utilisateur utilisé pour accéder au serveur distant.
   - Pour **[!UICONTROL Password]**, saisissez le mot de passe du compte de nom d’utilisateur fourni.
   - Pour **[!UICONTROL File Mode]**, choisissez `Binary` ou `ASCII`.
   - Pour **[!UICONTROL Passive Mode]**, choisissez `No` ou `Yes`.

### Etape 3 : configuration des emails d&#39;échec d&#39;export

1. Définissez **[!UICONTROL Failed Email Receiver]** sur le contact du magasin qui doit recevoir la notification si une erreur se produit pendant l’exportation.

1. Définissez **[!UICONTROL Failed Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur de la notification.

1. Définissez **[!UICONTROL Failed Email Template]** sur le modèle utilisé pour la notification.

1. Pour **[!UICONTROL Send Failed Email Copy To]**, saisissez l’adresse électronique de toute personne devant recevoir une copie de la notification.

   Pour plusieurs adresses électroniques, séparez-les par une virgule.

1. Définissez **[!UICONTROL Failed Email Copy Method]** sur l’une des options suivantes :

   - `Bcc` - Envoie une copie de courtoisie pour aveugles. Le nom et l’adresse du destinataire sont inclus dans la distribution d’email d’origine, mais sont masqués.
   - `Separate Email` — Envoie la copie en tant qu’email distinct.

### Étape 4 : Sélection des attributs d’entité

1. Dans la section _[!UICONTROL Entity Attributes]_, sélectionnez les attributs que vous souhaitez inclure dans les données d&#39;exportation.

   - Pour filtrer les données d’exportation par valeur d’attributs, saisissez la valeur d’attribut dans la colonne _[!UICONTROL Filter]_.
   - Pour exclure des produits ou des clients avec certaines valeurs d’attribut, saisissez les valeurs des attributs que vous souhaitez exclure, puis cochez la case dans la colonne Ignorer.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   La nouvelle tâche d’exportation planifiée est ajoutée à la liste sur la page _[!UICONTROL Scheduled Import/Export]_. À partir de cette page, il peut être exécuté immédiatement, testé et modifié.

>[!NOTE]
>
>Lorsque vous créez ou mettez à jour une importation/exportation planifiée, la configuration du système change. Après l’enregistrement, veillez à respecter l’avis d’invalidation du cache qui s’affiche en haut de la page Admin et à vider le cache afin d’appliquer la planification nouvelle ou mise à jour.

### Descriptions des champs

#### [!UICONTROL Export Settings]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Name] | Nom de l’exportation. Permet de le distinguer si de nombreuses exportations planifiées différentes sont créées. |
| [!UICONTROL Description] | (Facultatif) Description de l’exportation planifiée. |
| [!UICONTROL Entity Type] | Identifie les données à exporter. Une fois la sélection effectuée, les attributs d’entité apparaissent ci-dessous. Options : `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | Définissez l’heure de début, les minutes et les secondes de l’exportation. |
| [!UICONTROL Frequency] | Définissez la fréquence d’exécution de la tâche d’exportation. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | Une nouvelle exportation planifiée est activée par défaut. Vous pouvez la suspendre en définissant État sur Désactivé. Options : `Enabled` / `Disabled` |
| [!UICONTROL File Format] | Sélectionnez le format du fichier d&#39;export. Actuellement, seule l’option `.CSV` est disponible. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Détermine l’emplacement du fichier d’exportation. Options : <br>**Serveur local** — Place le fichier d’exportation sur le même serveur que celui sur lequel Commerce est déployé. Si le module de stockage à distance est activé, `Local Server` est remplacé par `Remote Storage`.<br>**FTP distant** : place le fichier d’exportation sur un serveur distant. Des options supplémentaires pour les informations d’identification et les paramètres de transfert de fichiers s’affichent. |
| [!UICONTROL File Directory] | Indiquez le répertoire dans lequel se trouve le fichier d’exportation. Si _[!UICONTROL Server Type]_est défini sur `Local Server`, indiquez le chemin d’accès relatif au chemin d’installation de Commerce. Par exemple, `var/export` ou `import_export/export` pour le stockage à distance. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Champ | Description |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Indiquez l’adresse électronique à laquelle une notification électronique (adresse électronique en échec de l’exportation) est envoyée en cas d’échec de l’exportation. |
| [!UICONTROL Failed Email Sender] | Indiquez l’adresse électronique utilisée comme expéditeur de courrier électronique en échec de l’exportation. |
| [!UICONTROL Failed Email Template] | Sélectionnez un modèle pour l’email d’exportation en échec. Par défaut, seule l’option `Export Failed (Default Template from Locale)` est disponible. |
| [!UICONTROL Send Failed Email Copy To] | Adresse électronique à laquelle une copie de l’adresse électronique d’exportation en échec est envoyée. |
| [!UICONTROL Send Failed Email Copy Method] | Indiquez la méthode d’envoi de copie pour le courrier électronique dont l’exportation a échoué. |

{style="table-layout:auto"}
