---
title: Expédition au tarif du tableau
description: Découvrez comment configurer une option d’expédition au tarif fixe pour votre boutique.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# Expédition au tarif du tableau

Le _tableau des tarifs_ méthode d&#39;expédition fait référence à un tableau de données permettant de calculer les tarifs d&#39;expédition en fonction d&#39;une combinaison de conditions, notamment :

- Poids v. Destination
- Prix v. Destination
- Nombre d’éléments par rapport à la destination

Par exemple, si votre entrepôt est à Los Angeles, il coûte moins cher d&#39;expédier à San Diego qu&#39;au Vermont. Vous pouvez utiliser la livraison à tarif fixe pour transmettre les économies à vos clients.

Les données utilisées pour calculer les taux des tables sont préparées dans une feuille de calcul et importées dans votre magasin. Lorsque le client demande un devis, les résultats apparaissent dans la section devis d’expédition du panier.

>[!NOTE]
>
>Un seul ensemble de données de taux de table peut être actif à la fois.

![Tableau option d’expédition des taux dans la synthèse des commandes de panier](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Étape 1 : définition des paramètres par défaut

La première étape consiste à définir les paramètres par défaut des taux du tableau. Vous pouvez effectuer cette étape sans modifier la portée de la configuration.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans la section _[!UICONTROL Sales]_du panneau de gauche, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Table Rates]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants comme décrit.

   ![Taux du tableau](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Saisissez la **[!UICONTROL Title]** que vous souhaitez afficher pour la section de taux de table lors du passage en caisse.

   Le titre par défaut est `Best Way`.

1. Saisissez le **[!UICONTROL Method Name]** que vous souhaitez afficher en tant qu’étiquette en regard du taux calculé dans le panier.

1. Définissez **[!UICONTROL Condition]** l’une des méthodes de calcul suivantes :

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Pour les commandes qui incluent des produits virtuels, définissez **[!UICONTROL Include Virtual Products in Price Calculation]** sur `Yes` si vous souhaitez pouvoir inclure les produits virtuels dans le calcul.

   >[!NOTE]
   >
   >Étant donné que les produits virtuels, tels que les services, n’ont pas de poids, ils ne peuvent pas modifier le résultat d’un calcul basé sur la condition Poids par rapport à Destination . Cependant, les produits virtuels peuvent modifier le résultat d’un calcul basé sur la condition Prix par rapport à Destination ou Nombre d’articles par rapport à Destination .

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de manutention sont facultatifs et apparaissent comme des frais supplémentaires qui s&#39;ajoutent aux frais d&#39;expédition. Si vous souhaitez inclure des frais de manutention, procédez comme suit :

   - Définir **[!UICONTROL Calculate Handling Fee]** :

      - `Fixed`
      - `Percent`

   - Entrez le taux de **[!UICONTROL Handling Fee]** en fonction de la méthode utilisée pour calculer les frais.

     Par exemple, si les frais sont basés sur des frais fixes, saisissez le montant sous la forme d’une décimale, comme `4.90`. Toutefois, si les frais de gestion sont basés sur un pourcentage de la commande, saisissez le montant sous forme de pourcentage. Par exemple, si vous facturez six pour cent de la commande, saisissez la valeur `.06`.

1. Si nécessaire, modifiez la **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un message différent que vous souhaitez faire apparaître si cette méthode de diffusion n’est plus disponible.

1. Définir **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste des _[!UICONTROL Ship to Specific Countries]_s’affiche. Sélectionnez dans la liste chaque pays où ce mode de diffusion peut être utilisé.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** sur `Yes` si vous souhaitez afficher les taux de la table en permanence

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l&#39;ordre dans lequel l&#39;expédition à taux fixe apparaît lorsqu&#39;elle est répertoriée avec d&#39;autres modes de livraison lors du passage en caisse.

   `0` = premier, `1` = deuxième, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 2 : Préparer les données de taux du tableau

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur `Main Website` ou sur tout autre site web auquel s’applique la configuration.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants comme décrit.

1. Modifiez le **[!UICONTROL Condition]** selon vos besoins.

1. Cliquez sur **[!UICONTROL Export CSV]**.

   ![Exporter CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Enregistrez le fichier `tablerates.csv` sur votre système.

1. Ouvrez le fichier dans une application de feuille de calcul.

1. Complétez le tableau avec les valeurs appropriées pour la condition de calcul d&#39;expédition.

   - Utilisez un astérisque (*) comme caractère générique représentant toutes les valeurs possibles dans n’importe quelle catégorie.
   - La colonne _[!UICONTROL Country]_doit contenir un [code à trois caractères valide](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) pour chaque ligne.
   - Triez les données par _[!UICONTROL Region/State]_afin que les emplacements spécifiques se trouvent en haut de la liste et les emplacements de caractères génériques en bas. L’utilisation de cette méthode traite d’abord les règles avec les valeurs absolues, puis les valeurs génériques plus tard.
   - Les plages de codes postaux ne sont pas prises en charge. Utilisez un astérisque (*) pour autoriser tous les codes de la région ou de l’État, ou spécifiez un seul code pour un emplacement spécifique dans la colonne _[!UICONTROL Zip/Postal Code]_.
   - Les valeurs de la colonne _[!UICONTROL Weight (and above)]_peuvent contenir au maximum quatre décimales (par exemple, `2.5075`). L’utilisation de décimales supplémentaires dans les données entraîne l’échec de l’importation.

   ![Poids par rapport à la destination (Australie)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Enregistrez le fichier `tablerates.csv`.

## Étape 3 : Importer les données de taux de la table

1. Revenez à la section **[!UICONTROL Table Rates]** de la configuration de votre boutique.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur le site web où cette méthode est utilisée.

1. Par **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre fichier `tablerates.csv` terminé pour importer les taux.

   ![Importer les taux des tables](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 4 : vérifier les taux

Pour vous assurer que les données du taux de la table sont correctes, passez par le processus de paiement avec plusieurs adresses différentes pour vous assurer que les taux d&#39;expédition et de manutention sont calculés correctement.

### Exemple 1 : prix et destination

Cet exemple utilise la condition Prix / Destination pour créer un ensemble de trois tarifs d&#39;expédition différents en fonction du montant du sous-total de la commande pour les États-Unis continentaux, l&#39;Alaska et Hawaï. L’astérisque (*) est un caractère générique qui représente toutes les valeurs.

| PAYS | RÉGION/ÉTAT | CODE POSTAL | SOUS-TOTAL COMMANDE (et plus) | PRIX D&#39;EXPÉDITION |
|--- |--- |--- |--- |--- |
| USA | BONJOUR | * | 100 | 10 |
| USA | BONJOUR | * | 50 | 15 |
| USA | BONJOUR | * | 0 | 20 |
| USA | AK | * | 100 | 10 |
| USA | AK | * | 50 | 15 |
| USA | AK | * | 0 | 20 |
| USA | * | * | 100 | 5 |
| USA | * | * | 50 | 10 |
| USA | * | * | 0 | 15 |

{style="table-layout:auto"}

### Exemple 2 : poids et destination

Cet exemple utilise la condition Poids par rapport à Destination pour créer des frais d&#39;expédition différents en fonction du poids de la commande.

| PAYS | RÉGION/ÉTAT | CODE POSTAL | POIDS (et plus) | PRIX D&#39;EXPÉDITION |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39,95 |
| AUS | NT | * | 0 | 19,95 |
| AUS | CIV | * | 9 | 19,95 |
| AUS | CIV | * | 0 | 5,95 |
| AUS | WA | * | 9 | 39,95 |
| AUS | WA | * | 0 | 19,95 |
| AUS | * | * | 9 | 29,95 |
| AUS | * | * | 0 | 9,95 |

{style="table-layout:auto"}

### Exemple 3 : limitation de la livraison gratuite vers le continent américain

1. Créez un fichier `tablerates.csv` qui inclut toutes les destinations d’état vers lesquelles vous êtes prêt à fournir une livraison gratuite.

1. Effectuez la configuration du taux de table avec les paramètres suivants :

   | Paramètre | Valeur |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur `Main Website` ou sur tout autre site web auquel s’applique la configuration.

1. Par **[!UICONTROL Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez votre fichier `tablerates.csv` terminé pour importer les taux.
