---
title: Expédition du taux de change
description: Découvrez comment configurer une option d’expédition à taux variable pour votre magasin.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# Expédition du taux de change

La variable _taux de la table_ le mode d’expédition référence un tableau de données pour calculer les taux d’expédition en fonction d’une combinaison de conditions, notamment :

- Poids v. destination
- Prix v. Destination
- Nombre d’éléments v. Destination

Par exemple, si votre entrepôt se trouve à Los Angeles, il coûte moins cher de s&#39;adresser à San Diego qu&#39;au Vermont. Vous pouvez utiliser l’expédition à taux variable pour transmettre les économies à vos clients.

Les données utilisées pour calculer les taux des tableaux sont préparées dans une feuille de calcul et importées dans votre magasin. Lorsque le client demande un devis, les résultats apparaissent dans la section Estimation de la livraison du panier.

>[!NOTE]
>
>Un seul ensemble de données de taux de tableau peut être actif à la fois.

![Option d’expédition Taux de tableau dans le résumé de la commande du panier](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Étape 1 : définition des paramètres par défaut

La première étape consiste à renseigner les paramètres par défaut pour les taux de tableau. Vous pouvez effectuer cette étape sans modifier la portée de la configuration.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le _[!UICONTROL Sales]_dans le panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Table Rates]** .

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

   ![Taux sur les tableaux](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enabled]** to `Yes`.

1. Saisissez le **[!UICONTROL Title]** que vous souhaitez afficher pour la section taux de tableau lors du passage en caisse.

   Le titre par défaut est : `Best Way`.

1. Saisissez le **[!UICONTROL Method Name]** que vous souhaitez afficher sous forme de libellé en regard du taux calculé dans le panier.

1. Définir **[!UICONTROL Condition]** à l’une des méthodes de calcul suivantes :

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Pour les commandes qui incluent des produits virtuels, définissez **[!UICONTROL Include Virtual Products in Price Calculation]** to `Yes` si vous souhaitez pouvoir inclure les produits virtuels dans le calcul.

   >[!NOTE]
   >
   >Les produits virtuels (tels que les services) n’ayant aucun poids, ils ne peuvent pas modifier le résultat d’un calcul basé sur la condition Poids contre Destination . Cependant, les produits virtuels peuvent modifier le résultat d’un calcul basé sur la condition Prix v. Destination ou Nombre d’éléments par rapport à la condition Destination .

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Définir **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - Saisissez le **[!UICONTROL Handling Fee]** taux en fonction de la méthode de calcul de la taxe.

     Si, par exemple, les frais sont calculés à partir d’une somme fixe, saisissez la valeur décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur `.06`.

1. Si nécessaire, modifiez la variable **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si ce mode de diffusion devient indisponible.

1. Définir **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la variable _[!UICONTROL Ship to Specific Countries]_s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définir **[!UICONTROL Show Method if Not Applicable]** to `Yes` Si vous souhaitez afficher les taux de tableau en permanence

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’expédition du taux de tableau s’affiche lorsqu’elle est répertoriée avec d’autres méthodes de livraison lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Etape 2 : Préparation des données de taux du tableau

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** to `Main Website`, ou à tout autre site web sur lequel la configuration s’applique.

   >[!NOTE]
   >
   >Si nécessaire, désélectionnez tout d’abord l’option **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Modifiez la variable **[!UICONTROL Condition]** selon les besoins.

1. Cliquez sur **[!UICONTROL Export CSV]**.

   ![Exportation CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Enregistrez le `tablerates.csv` sur votre système.

1. Ouvrez le fichier dans une application de feuille de calcul.

1. Complétez le tableau avec les valeurs appropriées pour la condition de calcul de l’expédition.

   - Utilisez un astérisque (*) comme caractère générique qui représente toutes les valeurs possibles dans n’importe quelle catégorie.
   - La variable _[!UICONTROL Country]_doit contenir une colonne [code à trois caractères valide][1] pour chaque ligne.
   - Trier les données par _[!UICONTROL Region/State]_ainsi, les emplacements spécifiques se trouvent en haut de la liste et les emplacements avec caractères génériques en bas de la liste. L’utilisation de cette méthode traite d’abord les règles avec les valeurs absolues et ensuite les valeurs du caractère générique.
   - Les valeurs de la variable _[!UICONTROL Weight (and above)]_peut contenir, au maximum, quatre décimales (telles que `2.5075`). L’utilisation de davantage de décimales dans les données entraîne l’échec de l’importation.

   ![Poids par rapport à la destination (Australie)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Enregistrez le `tablerates.csv` fichier .

## Etape 3 : Importer les données du taux du tableau

1. Revenez au **[!UICONTROL Table Rates]** de votre configuration de magasin.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur le site web sur lequel cette méthode est utilisée.

1. Pour **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre `tablerates.csv` pour importer les taux.

   ![Taux d’importation du tableau](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Etape 4 : Vérifier les taux

Pour vérifier que les données du taux du tableau sont correctes, passez en revue le processus de paiement avec plusieurs adresses différentes pour vous assurer que les taux d&#39;expédition et de traitement sont correctement calculés.

### Exemple 1 : prix et destination

Cet exemple utilise la condition Price v. Destination pour créer un ensemble de trois taux d’expédition différents en fonction du montant du sous-total de la commande pour le continent américain, l’Alaska et Hawaï. L’astérisque (*) est un caractère générique qui représente toutes les valeurs.

| PAYS | RÉGION/ETAT | CODE POSTAL/ZIP | SOUS-TOTAL DE LA COMMANDE (et supérieur) | PRIX D&#39;EXPÉDITION |
|--- |--- |--- |--- |--- |
| USA | HI | * | 100 | 10 |
| USA | HI | * | 50 | 15 |
| USA | HI | * | 0 | 20 |
| USA | AK | * | 100 | 10 |
| USA | AK | * | 50 | 15 |
| USA | AK | * | 0 | 20 |
| USA | * | * | 100 | 5 |
| USA | * | * | 50 | 10 |
| USA | * | * | 0 | 15 |

{style="table-layout:auto"}

### Exemple 2 : poids et destination

Cet exemple utilise la condition Poids v. Destination pour créer différents taux d’expédition en fonction du poids de la commande.

| PAYS | RÉGION/ETAT | CODE POSTAL/ZIP | POIDS (et supérieur) | PRIX D&#39;EXPÉDITION |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### Exemple 3 : limitation de la livraison gratuite vers les États-Unis continentaux

1. Créez un `tablerates.csv` fichier contenant toutes les destinations d’état auxquelles vous êtes prêt à fournir la livraison gratuite.

1. Renseignez la configuration du taux du tableau avec les paramètres suivants :

   | Paramètre | Valeur |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** to `Main Website`, ou à tout autre site web sur lequel la configuration s’applique.

1. Pour **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre `tablerates.csv` pour importer les taux.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
