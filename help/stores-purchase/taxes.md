---
title: Taxes
description: Découvrez comment paramétrer votre boutique pour calculer les taxes en fonction des paramètres régionaux.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Taxes

Configurez votre boutique pour calculer les taxes en fonction des paramètres régionaux. Vous pouvez configurer [classes d&#39;impôts](tax-class.md) pour les produits et les groupes de clients, et créez [règles fiscales](tax-rules.md) qui combinent les classes de produits et de clients, les zones fiscales et les taux. Commerce fournit également des paramètres de configuration pour les taxes sur les produits fixes, les taxes composites et l’affichage des prix au-delà des frontières internationales. Si vous devez collecter une [taxe sur la valeur ajoutée](vat.md), vous pouvez configurer votre boutique pour calculer automatiquement le montant approprié avec validation.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source comprenaient l’extension développée par le fournisseur Vertex, utilisée pour l’intégration à Vertex Cloud afin de fournir la gestion fiscale et la normalisation des adresses. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version principale et doit être installée et mise à jour à partir du Commerce Marketplace ou directement à partir du fournisseur. [Contact Vertex](https://marketplace.magento.com/partner/vertex_inc) pour plus d’informations sur l’extension et la documentation.<br><br>
>
>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier compositeur.json dans le cadre du processus de mise à niveau 2.4.4 et gérer les mises à jour de l’extension. Voir [Mettre à niveau les modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_.

## Référence rapide

Certains paramètres de taxe offrent le choix d’options qui déterminent la manière dont la taxe est calculée et présentée au client. Pour plus d’informations, voir [Directives fiscales internationales](international-tax-guidelines.md).

Utilisez les tableaux suivants à titre de référence lors de la configuration des paramètres de calcul des taxes :

### Méthodes de calcul des taxes

Les options de méthode de calcul des taxes incluent : [!UICONTROL Unit Price], [!UICONTROL Row Total], et [!UICONTROL Total]. Le tableau suivant explique comment l’arrondi (à deux chiffres) est géré pour différents paramètres.

| Paramètre | Calcul et affichage |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce calcule la taxe pour chaque élément et affiche les prix inclusifs. Pour calculer le total de la taxe, la taxe est arrondie à chaque article, puis additionnée. |
| [!UICONTROL Row Total] | Commerce calcule la taxe pour chaque ligne. Pour calculer le total de la taxe, la taxe est arrondie à chaque ligne, puis additionnée. |
| [!UICONTROL Total] | Commerce calcule la taxe de chaque article et ajoute ces valeurs afin de calculer le montant total de la taxe non arrondie pour la commande. Il applique ensuite le mode arrondi spécifié à la taxe totale afin de déterminer la taxe totale pour la commande. |

{style="table-layout:auto"}

### Prix du catalogue avec ou sans taxe

Les champs d&#39;affichage possibles varient selon la méthode de calcul et selon que les prix du catalogue incluent ou excluent des taxes. Les champs d’affichage ont une précision de deux décimales dans les calculs normaux. Certaines combinaisons de paramètres de prix affichent des prix qui incluent et excluent des taxes. Lorsque les deux éléments apparaissent sur la même ligne, cela peut dérouter les clients et déclencher une [warning](taxes.md#warning-messages).

| Paramètre | Calcul et affichage |
|--- |--- |
| [!UICONTROL Excluding Tax] | Grâce à ce paramètre, le prix de base de l&#39;article est utilisé tel qu&#39;il est entré et les méthodes de calcul de la taxe sont appliquées. |
| [!UICONTROL IncludingTax] | En utilisant ce paramètre, le prix de base de l’article qui exclut la taxe est calculé en premier. Cette valeur sert de prix de base et les méthodes de calcul de la taxe sont appliquées. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Il existe des modifications par rapport aux versions antérieures pour les marchands de l’UE ou d’autres marchands de TVA qui affichent des prix incluant les taxes et opèrent dans plusieurs pays avec plusieurs vues de magasins. Si vous chargez les prix avec plus de deux chiffres de précision, Commerce arrondit automatiquement tous les prix à deux chiffres afin de garantir qu’un prix cohérent est présenté aux acheteurs.

### Prix de livraison avec ou sans taxes

| Paramètre | Affichage | Calcul |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Apparaît sans impôt. | Calcul normal. Les frais d’expédition sont ajoutés au total du panier, généralement affichés sous la forme d’un article distinct. |
| [!UICONTROL Including Tax] | Peuvent être taxes incluses, ou les taxes peuvent être affichées séparément. | L’expédition est traitée comme un autre article du panier, avec taxes, selon les mêmes calculs. |

{style="table-layout:auto"}

### Montant des taxes sous forme d’éléments de ligne

Pour afficher deux montants de taxe différents comme éléments de ligne distincts, comme la TPS et la TSP pour les magasins canadiens, vous devez définir des priorités différentes pour les règles fiscales connexes. Toutefois, dans les calculs fiscaux précédents, les impôts avec des priorités différentes seraient automatiquement alourdis. Pour afficher correctement les différents montants d’impôts sans une composition incorrecte des montants d’impôts, vous pouvez définir différentes priorités et également sélectionner la variable _Calcul du sous-total uniquement_ . Ce paramètre génère des montants de taxe correctement calculés qui apparaissent sous la forme d’éléments de ligne distincts.

## Messages d’avertissement

Certaines combinaisons d’options liées à la taxe peuvent dérouter les clients et déclencher un avertissement. Ces conditions peuvent se produire lorsque la méthode de calcul de la taxe est définie sur `Row` ou `Total`, et le client reçoit des prix qui excluent et incluent des taxes. Cela peut également se produire lorsqu’il y a une taxe par article dans le panier. Étant donné que le calcul de la taxe est arrondi, le montant qui apparaît dans le panier peut différer du montant qu’un client prévoit de payer.

Si votre calcul de la taxe est basé sur une configuration problématique, les avertissements suivants s&#39;affichent :

![Point d’exclamation](../assets/icon-warning.png) **Avertissement**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Point d’exclamation](../assets/icon-warning.png) **Avertissement**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Lieu de livraison des biens numériques (UE)

Les marchands de l&#39;Union Européenne (UE) doivent déclarer leurs produits numériques vendus par trimestre à chaque pays membre. Les biens numériques sont taxés en fonction de l&#39;adresse de livraison du client. La loi exige que les marchands produisent un rapport d&#39;impôt et identifient les montants de taxe pertinents pour les biens numériques, par opposition aux biens physiques.

Les commerçants doivent déclarer tous les produits numériques vendus par les pays membres de l&#39;UE sur une base trimestrielle à une administration centrale des impôts, ainsi que le paiement des taxes perçues sur cette période.

Les commerçants qui n&#39;ont pas encore atteint le seuil (50 000 euros par an) doivent continuer à signaler les marchandises physiques vendues aux Etats de l&#39;UE où ils ont enregistré des numéros de TVA.

Les commerçants contrôlés pour les taxes payées pour les produits numériques doivent fournir deux pièces d&#39;information justificatives pour établir le lieu de résidence du client.

- L’adresse de livraison du client et un enregistrement d’une transaction de paiement réussie peuvent être utilisés pour établir le lieu de résidence du client. (Le paiement n’est accepté que si l’adresse de livraison correspond aux informations du fournisseur de paiement.)
- Les informations peuvent également être capturées directement à partir de l’entrepôt de données dans les tables de base de données Commerce.

_**Pour recueillir des renseignements sur la taxe sur les produits numériques :**_

1. Charger les taux d&#39;imposition pour tous les pays membres de l&#39;UE.

1. Créez une classe de taxe sur les produits numériques.

1. Attribuez toutes vos marchandises numériques à la classe de taxe des produits numériques.

1. Créer [règles fiscales](tax-rules.md) pour vos biens physiques, en utilisant des classes de taxe sur les produits physiques et en les associant aux taux d’imposition appropriés.

1. Créez des règles fiscales pour vos produits numériques, en utilisant la classe de taxe sur les produits pour les produits numériques, et associez-les aux taux d’imposition appropriés pour les pays membres de l’UE.

1. Exécutez le rapport sur les taxes pour la période appropriée et collectez les renseignements requis sur les marchandises numériques.

1. Exportez les montants de taxe qui sont liés aux taux de taxe pour la classe de taxe sur les produits numériques.

Ressources supplémentaires :

- [Taxation et union douanière de la Commission européenne][1]
- [Changements de lieu de livraison UE 1015][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
