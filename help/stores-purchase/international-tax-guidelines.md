---
title: Directives fiscales par pays
description: Examinez les paramètres fiscaux recommandés en fonction du pays.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Directives fiscales par pays

## Configuration fiscale américaine

Ces paramètres recommandés peuvent être utilisés pour la plupart des configurations de taxe pour les magasins situés aux États-Unis.

| Option Taxe | Recommandation |
|--- |--- |
| Chargement des prix du catalogue | Exclure la taxe |
| FPT | Non, car FPT n&#39;est pas imposé. |
| Taxe basée sur | Origine de l’expédition |
| Calcul des taxes | Au total |
| Frais d&#39;expédition fiscale ? | Non |
| Appliquer la remise | Avant impôts |
| Commentaire | Toutes les zones fiscales ont la même priorité ; idéalement, une zone pour l’état et une ou plusieurs zones pour la recherche de code postal. |

{style="table-layout:auto"}

### Classes fiscales

| Classe fiscale | Paramètre recommandé |
|--- |--- |
| Classe fiscale pour l&#39;expédition | Aucun |

{style="table-layout:auto"}

### Paramètres de calcul

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Calcul de la destination de la taxe par défaut

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | État où se trouve l’entreprise. |
| [!UICONTROL Default Post Code] | Code postal utilisé dans vos zones fiscales. |

{style="table-layout:auto"}

### Paramètres d&#39;affichage des prix

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Paramètres d&#39;affichage du panier

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Commandes, factures, notes de crédit et paramètres d’affichage

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Taxes sur les produits fixes (FPT)

| Option | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`, sauf en Californie. |

{style="table-layout:auto"}

## Configuration fiscale britannique

Ces paramètres recommandés peuvent être utilisés pour la plupart des configurations de taxe pour les magasins situés au Royaume-Uni.

### Configuration fiscale B2C britannique

| Option Taxe | Recommandation |
|--- |--- |
| Chargement des prix du catalogue | Exclure la taxe |
| FPT | Oui, y compris FPT et description |
| Taxe basée sur | [!UICONTROL Shipping Address] |
| Calcul des taxes | Au total |
| Frais d&#39;expédition fiscale ? | Oui |
| Appliquer la remise | Avant taxe, remise sur les prix, y compris la taxe. |
| Commentaire | Pour les commerçants qui marquent les factures des fournisseurs (TVA comprise). |

{style="table-layout:auto"}

### Configuration fiscale B2B au Royaume-Uni

| Option Taxe | Recommandation |
|--- |--- |
| Chargement des prix du catalogue | Exclure la taxe |
| FPT | Oui, y compris FPT et description |
| Taxe basée sur | [!UICONTROL Shipping Address] |
| Calcul des taxes | Sur l’élément |
| Frais d&#39;expédition fiscale ? | Oui |
| Appliquer la remise | Avant taxe, remise sur les prix, y compris la taxe. |
| Commentaire | Pour les commerçants B2B afin de fournir des considérations plus simples sur la chaîne d&#39;approvisionnement en TVA. Le calcul des impôts sur la ligne est également valide ; toutefois, vérifiez auprès de votre juridiction fiscale. Le programme d&#39;installation suppose qu&#39;un commerçant fait partie de la chaîne d&#39;approvisionnement et que les marchandises vendues sont utilisées par d&#39;autres vendeurs pour les rabais sur la TVA, etc. Cette définition permet de discerner facilement la taxe par article pour générer plus rapidement des remises. <br/><br/>**_Remarque :_**&#x200B;Certaines juridictions exigent des stratégies d’arrondi différentes qui ne sont actuellement pas prises en charge par Commerce et que toutes les juridictions n’autorisent pas la taxe au niveau des articles ou des lignes. |

{style="table-layout:auto"}

## Configuration fiscale canadienne

>[!IMPORTANT]
>
>Les commerçants qui se trouvent dans une province de la TPS/TSP (Montréal) devraient créer une règle fiscale et afficher un montant d&#39;impôt combiné. Assurez-vous de consulter une autorité fiscale qualifiée si vous avez des questions.

| Option Taxe | Recommandation |
|--- |--- |
| Chargement des prix du catalogue | Exclure la taxe |
| FPT | Oui, y compris FPT, description et application de la taxe à FPT. |
| Taxe basée sur | Origine de l’expédition |
| Calcul des taxes | Au total |
| Frais d&#39;expédition fiscale ? | Oui |
| Appliquer la remise | Avant impôts |

{style="table-layout:auto"}

L’exemple suivant montre comment configurer les taux de taxe sur la TVA pour le Canada et les taux de taxe sur les revenus de la consommation (TSP) pour la Saskatchewan, avec des règles fiscales qui calculent et affichent les deux taux. Ces informations présentent un exemple de configuration. Veillez à vérifier les taux et les règles d’imposition corrects pour vos juridictions fiscales. Lors de la configuration des taxes, définissez la portée du magasin pour appliquer la configuration à tous les magasins et sites web applicables.

- La taxe sur les produits fixes est incluse comme attribut de produit pour les produits pertinents.
- Au Québec, la TSP est appelée TVB. Si vous souhaitez configurer un taux pour le Québec, veillez à utiliser TVQ comme identifiant.

### Etape 1 : paramétrage du calcul des taxes

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour une configuration multisite, définissez **[!UICONTROL Store View]** sur le site web et le magasin qui est la cible de la configuration.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Cliquez sur pour développer chaque section de la page et renseignez les paramètres suivants :

#### Paramètres de calcul des taxes

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (si disponible) |

{style="table-layout:auto"}

#### Classes d’impôts

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (les frais d’expédition sont taxés) |

{style="table-layout:auto"}

#### Calcul de la destination de la taxe par défaut

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (selon le cas) |
| [!UICONTROL Default Postal Code] | `*` (astérisque) |

{style="table-layout:auto"}

#### Paramètres d’affichage du panier

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Taxes sur les produits fixes

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Paramètres d’affichage FPT | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Étape 2 : instauration de la taxe canadienne sur les produits et services (TPS)

Pour imprimer le numéro de la taxe sur les factures et autres documents de vente, indiquez-le au nom des taux de taxe applicables. La taxe apparaît dans le cadre du montant de la taxe sur les produits et services figurant dans le résumé de la commande.

#### Gestion des zones et des taux de taxe

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (astérisque) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (astérisque) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Étape 3 : configuration de la taxe de vente provinciale canadienne (TSP)

Définissez un autre taux d’imposition pour la province concernée.

#### Informations sur le taux d’imposition

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (astérisque) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Étape 4 : création d’une règle de taxe sur la taxe

Pour éviter d’additionner la taxe et d’afficher correctement la taxe calculée comme des éléments de ligne distincts pour la TVA et la TSP, définissez des priorités différentes pour chaque règle et cochez la case **Calcul du sous-total uniquement** . Chaque taxe apparaît sur une ligne distincte, mais les montants de taxe ne sont pas composés.

#### Informations sur les règles fiscales

| Champ | Paramètre recommandé |
|--- |--- |
| Nom | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Cochez cette case. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Étape 5 : création d’une règle fiscale PST pour la Saskatchewan

Pour cette règle de taxe, veillez à définir la priorité sur 0 et cochez la case **Calcul du sous-total uniquement** . Chaque taxe apparaît sur une ligne distincte, mais les montants de taxe ne sont pas composés.

#### Informations sur les règles fiscales

| Champ | Paramètre recommandé |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Cochez cette case. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Étape 6 : enregistrer et tester les résultats

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Revenez à votre vitrine et créez un exemple d’ordre pour tester les résultats.

## Configuration fiscale de l&#39;UE

L’exemple suivant illustre un magasin basé en France qui vend plus de 100 000 euros en France et plus de 100 000 euros en Allemagne.

- Les calculs fiscaux sont gérés au niveau du site web.
- Les options de conversion de devise et d’affichage des taxes sont contrôlées individuellement au niveau de la vue du magasin (cochez la case Utiliser le site web pour remplacer la valeur par défaut).
- En définissant le pays de taxe par défaut, vous pouvez afficher dynamiquement la taxe correcte pour la juridiction.
- La taxe sur les produits fixes est incluse comme attribut de produit pour les produits pertinents.
- Il peut être nécessaire de modifier le catalogue pour s’assurer qu’il s’affiche dans la vue catégorie/site web/magasin correcte.

### Étape 1 : créer trois classes de taxe sur les produits

Dans cet exemple, on suppose que plusieurs classes de taxe sur les produits allégées en TVA ne sont pas nécessaires.

1. Créez une classe de taxe sur les produits standard de la TVA.

1. Créez une classe de taxe sur les produits réduite de la TVA.

1. Créez une classe de taxe sur les produits sans TVA.

### Etape 2 : créer des taux d&#39;imposition pour la France et l&#39;Allemagne

Créez les taux de taxe suivants :

| Taux d&#39;imposition | Paramètres |
|--- |--- |
| France-StandardTVA | Pays : France <br/>État/Région : * <br/>Code postal : * <br/>Taux : 20 % |
| TVA réduite en France | Pays : France <br/>État/Région : * <br/>Code postal : * <br/>Taux : 5 % |
| Allemagne-StandardTVA | Pays : Allemagne <br/>État/Région : * <br/>Code postal : * Taux : 19 % |
| Allemagne-TVA réduite | Pays : Allemagne <br/>État/Région : * <br/>Code postal : * <br/>Taux : 7 % |

{style="table-layout:auto"}

### Etape 3 : Configurer les règles fiscales

Créez les règles fiscales suivantes :

| Règles fiscales | Paramètres |
|--- |--- |
| Retail-France-StandardTVA | Classe client : client au détail <br/>Classe fiscale : TVA-standard <br/>Taux de taxe : France-StandardTVA <br/>Priorité : 0 <br/>Ordre de tri : 0 |
| Retail-France-ReducingTVA | Classe client : client au détail <br/>Classe fiscale : TVA réduite <br/>Taux d’imposition : France-Réduction de la TVA <br/>Priorité : 0 <br/>Ordre de tri : 0 |
| Vente au détail-Allemagne-TVA standard | Classe client : client au détail <br/>Classe fiscale : TVA-standard <br/>Taux d’imposition : Allemagne-StandardTVA <br/>Priorité : 0 <br/>Ordre de tri : 0 |
| Vente au détail-Allemagne-TVA réduite | Classe client : client au détail <br/>Classe fiscale : taux d’imposition réduit de la TVA <br/>Taux d’imposition : Allemagne-Réduction de la TVA <br/>Priorité : 0 <br/>Ordre de tri : 0 |

{style="table-layout:auto"}

### Étape 4 : configuration d’une vue de magasin pour l’Allemagne

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Sous le site web par défaut, créez une vue de magasin pour **[!UICONTROL Germany]**.

1. Ensuite, procédez comme suit :

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Dans le coin supérieur gauche, définissez **[!UICONTROL Default Config]** sur le magasin français.

   - Sur la page Général, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Countries Options]** et définissez le pays par défaut sur `France`.

   - Renseignez les options des paramètres régionaux si nécessaire.

1. Dans le coin supérieur gauche, sélectionnez l’allemand **[!UICONTROL Store View]**.

1. Sur la page _Général_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** et définissez le pays par défaut sur `Germany`.

1. Renseignez les options des paramètres régionaux si nécessaire.

### Etape 5 : paramétrage des taxes pour la France

Définissez les paramètres de taxe généraux suivants :

| Champ | Paramètre recommandé |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (les frais d’expédition sont taxés) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (astérisque) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Étape 6 : Configuration des paramètres fiscaux pour l’Allemagne

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur la vue du magasin allemand et cliquez sur **[!UICONTROL OK]** pour confirmer.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Dans la section **[!UICONTROL Default Tax Destination Calculation]** , procédez comme suit :

   - Décochez la case **[!UICONTROL Use Website]** après chaque champ,

   - Pour correspondre aux [points d’origine](shipping-settings.md#point-of-origin) des paramètres d’expédition de votre site, mettez à jour les valeurs suivantes :

      - Pays par défaut
      - État par défaut
      - Code de publication par défaut

     Ce paramètre garantit que la taxe est calculée correctement lorsque les prix des produits incluent la taxe.

     ![Calcul de destination de taxe par défaut](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
