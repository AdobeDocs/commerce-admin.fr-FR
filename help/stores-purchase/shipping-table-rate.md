---
title: Expédition du taux de change
description: Découvrez comment configurer une option d’expédition à taux variable pour votre magasin.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 0f368e87275a85e3801e6770b8985184e2071384
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# Expédition du taux de change

La méthode d’expédition _table rate_ fait référence à un tableau de données pour calculer les taux d’expédition en fonction d’une combinaison de conditions, notamment :

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

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans la section _[!UICONTROL Sales]_&#x200B;du panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Table Rates]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

   ![Taux de table](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Saisissez le **[!UICONTROL Title]** que vous souhaitez afficher pour la section des taux de table lors du passage en caisse.

   Le titre par défaut est `Best Way`.

1. Saisissez le **[!UICONTROL Method Name]** que vous souhaitez afficher en tant que libellé en regard du taux calculé dans le panier.

1. Définissez **[!UICONTROL Condition]** sur l’une des méthodes de calcul suivantes :

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Pour les commandes qui incluent des produits virtuels, définissez **[!UICONTROL Include Virtual Products in Price Calculation]** sur `Yes` si vous souhaitez pouvoir inclure les produits virtuels dans le calcul.

   >[!NOTE]
   >
   >Les produits virtuels (tels que les services) n’ayant aucun poids, ils ne peuvent pas modifier le résultat d’un calcul basé sur la condition Poids contre Destination . Cependant, les produits virtuels peuvent modifier le résultat d’un calcul basé sur la condition Prix v. Destination ou Nombre d’éléments par rapport à la condition Destination .

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Définissez **[!UICONTROL Calculate Handling Fee]** :

      - `Fixed`
      - `Percent`

   - Saisissez le taux **[!UICONTROL Handling Fee]** en fonction de la méthode de calcul de la taxe.

     Par exemple, si le coût est basé sur des frais fixes, saisissez le montant sous forme de décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous chargez six pour cent de la commande, saisissez la valeur `.06`.

1. Si nécessaire, modifiez le **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si ce mode de diffusion devient indisponible.

1. Définissez **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous choisissez cette option, la liste _[!UICONTROL Ship to Specific Countries]_&#x200B;s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** sur `Yes` si vous souhaitez afficher les taux de tableau tout le temps.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’expédition du taux de table apparaît lorsqu’elle est répertoriée avec d’autres méthodes de remise lors du passage en caisse.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Etape 2 : Préparation des données de taux du tableau

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur `Main Website` ou sur tout autre site web sur lequel s’applique la configuration.

   >[!NOTE]
   >
   >Si nécessaire, désélectionnez tout d’abord la case à cocher **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Modifiez le **[!UICONTROL Condition]** selon vos besoins.

1. Cliquez sur **[!UICONTROL Export CSV]**.

   ![Exporter CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Enregistrez le fichier `tablerates.csv` sur votre système.

1. Ouvrez le fichier dans une application de feuille de calcul.

1. Complétez le tableau avec les valeurs appropriées pour la condition de calcul de l’expédition.

   - Utilisez un astérisque (*) comme caractère générique qui représente toutes les valeurs possibles dans n’importe quelle catégorie.
   - La colonne _[!UICONTROL Country]_&#x200B;doit contenir un [code à trois caractères valide][1] pour chaque ligne.
   - Triez les données par _[!UICONTROL Region/State]_&#x200B;afin que les emplacements spécifiques soient en haut de la liste et les emplacements de caractères génériques en bas de la liste. L’utilisation de cette méthode traite d’abord les règles avec les valeurs absolues et ensuite les valeurs du caractère générique.
   - Les plages de codes postaux ne sont pas prises en charge. Utilisez un astérisque (*) pour autoriser tous les codes dans la région/l’état ou spécifiez un seul code pour un emplacement spécifique dans la colonne _[!UICONTROL Zip/Postal Code]_.
   - Les valeurs de la colonne _[!UICONTROL Weight (and above)]_&#x200B;peuvent avoir un maximum de quatre décimales (telles que `2.5075`). L’utilisation de davantage de décimales dans les données entraîne l’échec de l’importation.

   ![&#x200B; Poids/Destination (Australie)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Enregistrez le fichier `tablerates.csv`.

## Etape 3 : Importer les données du taux du tableau

1. Revenez à la section **[!UICONTROL Table Rates]** de votre configuration de magasin.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur le site web sur lequel cette méthode est utilisée.

1. Pour **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre fichier `tablerates.csv` terminé pour importer les taux.

   ![Importer des taux de tableau](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

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
| AUS | NT | * | 9 | 39,95 |
| AUS | NT | * | 0 | 19,95 |
| AUS | VIC | * | 9 | 19,95 |
| AUS | VIC | * | 0 | 5,95 |
| AUS | WA | * | 9 | 39,95 |
| AUS | WA | * | 0 | 19,95 |
| AUS | * | * | 9 | 29,95 |
| AUS | * | * | 0 | 9,95 |

{style="table-layout:auto"}

### Exemple 3 : limitation de la livraison gratuite vers les États-Unis continentaux

1. Créez un fichier `tablerates.csv` qui comprend toutes les destinations d’état auxquelles vous êtes prêt à fournir la livraison gratuite.

1. Renseignez la configuration du taux du tableau avec les paramètres suivants :

   | Paramètre | Valeur |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur `Main Website` ou sur tout autre site web sur lequel s’applique la configuration.

1. Pour **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre fichier `tablerates.csv` terminé pour importer les taux.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
