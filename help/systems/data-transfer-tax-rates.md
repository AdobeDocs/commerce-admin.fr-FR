---
title: Mettre à jour les données de taux de taxe
description: Découvrez comment utiliser les opérations d’exportation et d’importation pour mettre à jour les taux de taxe de votre boutique.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
TQID: https://experienceleague.adobe.com/QPY-XfiA3XhBSV3eiiYtxb9K-quf5AycMcHDBUBtE0k
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 624
ht-degree: 0%

---

# Mettre à jour les données de taux de taxe

Si vous travaillez dans plusieurs États et expédiez une grande quantité de produits, la saisie manuelle des taux de taxe peut prendre beaucoup de temps. Il est plus rapide et plus efficace de télécharger les taux de taxe par code postal et de les importer dans Commerce. L&#39;exemple suivant montre comment importer un ensemble de taux d&#39;imposition spécifiques à un état téléchargé à partir d&#39;une source approuvée. Avalara fournit des [tableaux des taux d&#39;imposition](https://www.avalara.com/taxrates/en/download-tax-tables.html), que vous pouvez télécharger gratuitement, pour chaque code postal dans les États-Unis.

>[!NOTE]
>
>Si vous souhaitez automatiser vos ventes et utiliser la conformité fiscale et le reporting, vous pouvez trouver des options approuvées par Commerce sur le site [Partenaires Commerce](https://solutionpartners.adobe.com/s/directory/?solution=commerce).

## Étape 1 : Exporter les données de taux de taxe Commerce

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Cliquez sur **[!UICONTROL Export Tax Rates]**.

1. Recherchez le fichier à l’emplacement de téléchargement de votre navigateur web.

1. Enregistrez et ouvrez le fichier dans une feuille de calcul.

   Cet exemple utilise [!DNL OpenOffice Calc].

   Les données de taux de taxe Commerce exportées comprennent les colonnes suivantes :
   - Code
   - Pays
   - État
   - Code Postal
   - Taux
   - Plage De
   - Plage de fin
   - Une colonne pour chaque vue de magasin

   ![Données exportées - taux de taxe](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. Ouvrez les nouvelles données de taux de taxe dans une deuxième instance de la feuille de calcul, afin de les afficher côte à côte.

1. Dans les nouvelles données de taux de taxe, notez toutes les données de taux de taxe supplémentaires que vous devrez peut-être configurer dans votre boutique avant l’importation des données.

   Par exemple, les données sur les taux d’imposition pour la Californie incluent également :

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   Si vous devez importer des [zones et taux de taxe](../stores-purchase/tax-zones-rates.md) supplémentaires, vous devez d’abord les définir à partir de l’administrateur de votre magasin et mettre à jour les [règles de taxe](../stores-purchase/tax-rules.md) si nécessaire. Ensuite, exportez les données et ouvrez le fichier dans un éditeur de texte afin qu’il puisse être utilisé comme référence. Toutefois, pour que cet exemple reste simple, nous importons uniquement les colonnes de taux d’imposition standard.

## Etape 2 : préparation des données d&#39;import

Vous avez deux feuilles de calcul ouvertes, côte à côte. L’un contient la structure du fichier d’exportation Commerce, et l’autre contient les nouvelles données de taux de taxe que vous souhaitez importer.

1. Pour créer un emplacement de travail dans la feuille de calcul avec les nouvelles données de taux de taxe, insérez autant de colonnes vides à l’extrémité droite que nécessaire pour ajouter les données du fichier d’exportation de Commerce. Effectuez un couper-coller pour ajouter les données, puis réorganisez les colonnes afin qu’elles correspondent à l’ordre du fichier de données d’exportation Commerce.

1. Renommez les en-têtes de colonne pour qu’ils correspondent aux données d’exportation Commerce.

1. Supprimez toutes les colonnes qui ne contiennent aucune donnée.

   Dans le cas contraire, la structure du fichier d’importation doit correspondre aux données d’exportation Commerce d’origine.

1. Avant d’enregistrer le fichier, faites défiler vers le bas et assurez-vous que les colonnes Taux de taxe ne contiennent que des données numériques.

   Tout texte trouvé dans une colonne de taux de taxe empêche l’importation des données.

1. Enregistrez les données préparées au format .CSV.

   Lorsque vous y êtes invité, vérifiez qu’une virgule est utilisée comme délimiteur de champ et que le délimiteur de texte est placé entre guillemets. Cliquez ensuite sur **[!UICONTROL OK]**.

## Etape 3 : Importer les taux de taxe

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier de taux de taxe CSV que vous souhaitez importer.

1. Cliquez sur **[!UICONTROL Import Tax Rates]**.

   L’importation des données peut prendre plusieurs minutes. Une fois le processus terminé, le message `The tax rate has been imported` s’affiche. Si vous recevez un message d’erreur, corrigez le problème dans les données et réessayez.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   Les taux importés apparaissent dans la liste.

1. Utilisez les commandes de page pour afficher les nouveaux taux de taxe.

   ![Taux de taxe sur les importations de données](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. Exécutez des transactions de test dans votre magasin avec des clients ayant des codes postaux différents pour vous assurer que les nouveaux taux de taxe fonctionnent correctement.
