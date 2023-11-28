---
title: Exporter des données
description: Découvrez les filtres et attributs d’exportation des données et comment exporter des données à partir de votre magasin.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Exporter des données

La meilleure façon de se familiariser avec la structure de votre base de données consiste à exporter les données et à les ouvrir dans une feuille de calcul. Une fois que vous vous êtes familiarisé avec le processus, vous pouvez l’utiliser comme un moyen efficace de gérer de grandes quantités d’informations.

Les caractères spéciaux, tels que le signe égal, les symboles supérieur et inférieur à, les guillemets simples et doubles, la barre oblique inverse, la barre verticale et l’esperluette, peuvent entraîner des problèmes lors du transfert des données. Pour s’assurer que ces caractères spéciaux sont correctement interprétés, ils peuvent être marqués comme _séquence d’échappement_. Par exemple, si les données incluent une chaîne de texte telle que `code="str"`, `code="str2"`, le fait d’encadrer le texte entre guillemets doubles garantit que les guillemets doubles originaux sont compris comme faisant partie des données : `"code="str""`. Lorsque le système rencontre un jeu de guillemets doubles, il comprend que l’ensemble externe de guillemets doubles renferme les données réelles.

L’exportation des données est une opération asynchrone qui s’exécute en arrière-plan afin que vous puissiez continuer à travailler dans l’administrateur sans attendre la fin de l’opération. Le système affiche un message lorsque la tâche est terminée.

## Critères d’exportation

Les filtres d’exportation sont utilisés pour spécifier les données que vous souhaitez inclure dans le fichier d’exportation, en fonction de la valeur d’attribut. En outre, vous pouvez spécifier les données d’attribut que vous souhaitez inclure ou exclure de l’exportation.

![Critères d’exportation des données](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Exporter les filtres

Vous pouvez utiliser des filtres pour déterminer les SKU qui sont inclus dans le fichier d’exportation. Par exemple, si vous saisissez une valeur dans le filtre Pays de fabrication , le fichier CSV exporté inclut uniquement les produits fabriqués dans ce pays.

Le type de filtre correspond au type de données. Pour les champs de date, vous pouvez choisir la date dans le calendrier. ![Icône Calendrier](../assets/icon-calendar.png). Voir [Types d’entrée d’attribut](../catalog/attributes-input-types.md) pour plus d’informations.

Le format de la date est déterminé par la variable [locale](../getting-started/store-details.md#locale-options).

Pour inclure uniquement les enregistrements avec une valeur spécifique, telle qu’un SKU, saisissez la valeur dans le champ Filtre . Certains champs tels que Prix, Poids et Définir le produit comme nouveau comportent une plage de valeurs de/à.

### Exclure des attributs

La case à cocher de la première colonne permet d’exclure des attributs du fichier d’exportation. Si un attribut est exclu, la colonne associée dans les données d’exportation est incluse, mais vide.

| Exclure | Filtrer | Résultat |
|--- |--- |--- |
| ![Case à cocher Effacée](../assets/checkbox-clear.png) | Non | Le fichier exporté contient chaque attribut pour tous les enregistrements existants. |
| ![Case à cocher Effacée](../assets/checkbox-clear.png) | Oui | Le fichier d&#39;export contient chaque attribut avec uniquement les enregistrements autorisés par le filtre. |
| ![Case à cocher sélectionnée](../assets/checkbox-selected.png) | Non | Le fichier d’exportation n’inclut pas la colonne de l’attribut exclu, mais comprend tous les enregistrements existants. |
| ![Case à cocher sélectionnée](../assets/checkbox-selected.png) | Oui | Le fichier d&#39;export n&#39;inclut pas la colonne de l&#39;attribut exclu et contient uniquement les enregistrements autorisés par le filtre. |

{style="table-layout:auto"}

## Exporter des données

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Dans le _Paramètres d’exportation_ , définissez **[!UICONTROL Entity Type]** à l’une des options suivantes :

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Paramètres d’exportation des données](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Acceptation de la valeur par défaut **[!UICONTROL Export File Format]** de fichier CSV.

1. Si vous souhaitez placer des caractères spéciaux dans les données sous la forme d’une _séquence d’échappement_, sélectionnez la variable **[!UICONTROL Fields Enclosure]** .

1. Si nécessaire, modifiez l’affichage des attributs d’entité.

   Par défaut, la section Attributs d’entité répertorie tous les attributs disponibles dans l’ordre alphabétique. Vous pouvez utiliser la variable [contrôles de liste](../getting-started/admin-grid-controls.md) pour rechercher des attributs spécifiques et trier la liste. Les contrôles Rechercher et Réinitialiser le filtre contrôlent l’affichage de la liste, mais n’ont aucun effet sur la sélection des attributs à inclure dans le fichier d’exportation.

   ![Attributs d’entité filtrés pour l’exportation de données](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Pour filtrer les données exportées en fonction de la valeur d’attribut, procédez comme suit :

   - Pour n’exporter que les enregistrements avec des valeurs d’attribut spécifiques, saisissez la valeur requise dans la variable **[!UICONTROL Filter]** colonne . L’exemple suivant exporte uniquement un SKU spécifique.

   - Pour omettre un attribut de l’exportation, sélectionnez la variable **[!UICONTROL Exclude]** au début de la ligne. Par exemple, pour n’exporter que le `sku` et `image` , cochez la case de chaque autre attribut. La colonne apparaît dans le fichier d&#39;export, mais sans aucune valeur.

1. Faites défiler la page vers le bas et cliquez sur **[!UICONTROL Continue]** dans le coin inférieur droit de la page.

   Une fois la tâche terminée, le fichier est traité via une file d’attente de messages (assurez-vous que votre tâche cron est en cours d’exécution). Le fichier exporté est enregistré dans la variable `var/export/ folder`. Pour plus d’informations sur la file d’attente des messages, voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_.

   Vous pouvez enregistrer ou ouvrir le fichier CSV exporté sous forme de feuille de calcul, puis modifier les données et le réimporter dans votre magasin.

   >[!NOTE]
   >
   >Par défaut, tous les fichiers exportés se trouvent dans la variable `<Magento-root-directory>/var/export` dossier. Si le module de stockage à distance est activé, tous les fichiers exportés se trouvent dans la variable `<remote-storage-root-directory>/import_export/export` dossier.

## Ressources de dépannage

Pour obtenir de l’aide sur la résolution des problèmes d’exportation des données, reportez-vous aux articles suivants de la base de connaissances de l’assistance clientèle de Commerce :

- [Le fichier .csv des produits exportés n’apparaît pas](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [Le fichier d’exportation de produit ne s’affiche pas dans Admin](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [Problème lors de l’exportation de commandes au format CSV](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
