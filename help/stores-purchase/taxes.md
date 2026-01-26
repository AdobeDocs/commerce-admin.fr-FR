---
title: Taxes
description: Découvrez comment configurer votre boutique pour calculer les taxes en fonction des exigences de vos paramètres régionaux.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Taxes

Configurez votre boutique pour calculer les taxes en fonction des exigences de vos paramètres régionaux. Vous pouvez configurer des [classes de taxe](tax-class.md) pour des produits et des groupes de clients, et créer des [règles de taxe](tax-rules.md) qui combinent des classes de produit et de client, des zones de taxe et des taux. Commerce fournit également des paramètres de configuration pour les taxes sur les produits fixes, les taxes composites et l’affichage des prix au-delà des frontières internationales. Si vous devez collecter une [taxe sur la valeur ajoutée](vat.md), vous pouvez configurer votre boutique pour calculer automatiquement le montant approprié avec validation.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source incluaient l’extension développée par le fournisseur Vertex utilisée pour s’intégrer à Vertex Cloud afin de fournir une gestion fiscale et de résoudre les problèmes de cleansing. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version de base et doit être installée et mise à jour à partir du Commerce Marketplace ou directement auprès du fournisseur. [Contactez Vertex](https://marketplace.magento.com/partner/vertex_inc) pour plus d’informations sur l’extension et la documentation.<br><br>
>
>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier composer.json dans le cadre du processus de mise à niveau vers la version 2.4.4 et pour gérer les mises à jour d’extension à l’avenir. Voir [Mise à niveau des modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_.

## Référence rapide

Certains paramètres de taxe offrent plusieurs options qui déterminent la façon dont la taxe est calculée et présentée au client. Pour plus d&#39;informations, voir [International Tax Guidelines](international-tax-guidelines.md).

Utilisez les tableaux suivants à titre de référence lors de la configuration des paramètres de calcul des taxes :

### Méthodes de calcul des taxes

Les options de méthode de calcul de la taxe incluent [!UICONTROL Unit Price], [!UICONTROL Row Total] et [!UICONTROL Total]. Le tableau suivant explique comment l’arrondi (à deux chiffres) est géré pour différents paramètres.

| Paramètre | Calcul et affichage |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce calcule la taxe pour chaque article et affiche les prix TTC. Pour calculer le total de taxe, il arrondit la taxe de chaque élément, puis les additionne. |
| [!UICONTROL Row Total] | Commerce calcule la taxe pour chaque ligne. Pour calculer le total de la taxe, il arrondit la taxe pour chaque élément de ligne, puis les additionne. |
| [!UICONTROL Total] | Commerce calcule la taxe pour chaque article et ajoute ces valeurs de taxe pour calculer le montant total de taxe non arrondi pour la commande. Il applique ensuite le mode d&#39;arrondi spécifié à la taxe totale pour déterminer la taxe totale de la commande. |

{style="table-layout:auto"}

### Prix catalogue avec ou sans taxe

Les champs d’affichage possibles varient selon la méthode de calcul et selon que les prix du catalogue incluent ou excluent les taxes. Les champs d’affichage ont une précision à deux décimales dans les calculs normaux. Certaines combinaisons de paramètres de prix affichent des prix qui incluent et excluent la taxe. Lorsque les deux apparaissent sur le même élément de ligne, cela peut prêter à confusion pour les clients et déclenche un [avertissement](taxes.md#warning-messages).

| Paramètre | Calcul et affichage |
|--- |--- |
| [!UICONTROL Excluding Tax] | Ce paramètre permet d&#39;utiliser le prix article de base tel qu&#39;il est saisi et d&#39;appliquer les méthodes de calcul de la taxe. |
| [!UICONTROL IncludingTax] | Ce paramètre permet de calculer en premier le prix article de base qui exclut la taxe. Cette valeur est utilisée comme prix de base et les méthodes de calcul de la taxe sont appliquées. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Les versions antérieures ont été modifiées pour les commerçants de l&#39;UE ou d&#39;autres commerçants de la TVA qui affichent les prix, y compris la taxe, et opèrent dans plusieurs pays avec plusieurs vues de magasin. Si vous chargez les prix avec plus de deux chiffres de précision, Commerce arrondit automatiquement tous les prix à deux chiffres pour s&#39;assurer qu&#39;un prix cohérent est présenté aux acheteurs.

### Prix d&#39;expédition avec ou sans taxe

| Paramètre | Affichage | Calcul |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Apparaît sans taxe. | Calcul normal. L’expédition est ajoutée au total du panier, généralement sous la forme d’un article distinct. |
| [!UICONTROL Including Tax] | Peut inclure la taxe ou la taxe peut être affichée séparément. | L&#39;expédition est traitée comme un autre article dans le panier avec des taxes, en utilisant les mêmes calculs. |

{style="table-layout:auto"}

### Montants de taxe en tant qu&#39;éléments de ligne

Pour afficher deux montants de taxe différents en tant qu&#39;éléments de ligne distincts, tels que la TPS et la TVP pour les magasins canadiens, vous devez définir des priorités différentes pour les règles de taxe associées. Cependant, dans les calculs fiscaux précédents, les impôts ayant des priorités différentes seraient automatiquement composés. Pour afficher correctement des montants de taxe distincts sans une composition incorrecte des montants de taxe, vous pouvez définir différentes priorités et également cocher la case _Calculer uniquement le sous-total_. Ce paramètre génère des montants de taxe correctement calculés qui apparaissent sous la forme d&#39;éléments de ligne distincts.

## Messages d’avertissement

Certaines combinaisons d&#39;options liées à la fiscalité peuvent être déroutantes pour les clients et déclencher un avertissement. Ces conditions peuvent se produire lorsque la méthode de calcul de la taxe est définie sur `Row` ou `Total` et que le client se voit présenter des prix qui excluent et incluent la taxe. Cela peut également se produire lorsqu’il y a une taxe par article dans le panier. Comme le calcul de la taxe est arrondi, le montant qui apparaît dans le panier peut différer du montant qu’un client s’attend à payer.

Si votre calcul de taxe repose sur une configuration problématique, les avertissements suivants s&#39;affichent :

![Point d&#39;exclamation](../assets/icon-warning.png) **Avertissement**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Point d&#39;exclamation](../assets/icon-warning.png) **Avertissement**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Lieu de livraison des biens numériques (UE)

Les commerçants de l&#39;Union européenne (UE) doivent déclarer leurs produits numériques vendus par trimestre à chaque pays membre. Les biens numériques sont taxés en fonction de l’adresse de livraison du client. La loi exige que les commerçants produisent une déclaration de taxe et identifient les montants de taxe pertinents pour les biens numériques, par opposition aux biens physiques.

Les commerçants doivent déclarer tous les biens numériques vendus par les pays membres de l&#39;UE sur une base trimestrielle à une administration fiscale centrale, ainsi que le paiement dû pour la taxe collectée au cours de la période.

Les commerçants qui n&#39;ont pas encore atteint le seuil (50 000/100 000 d&#39;euros d&#39;affaires annuelles) doivent continuer à déclarer les biens physiques vendus aux États membres de l&#39;UE où ils ont enregistré des numéros de TVA.

Les commerçants qui font l&#39;objet d&#39;une vérification pour les taxes payées sur les biens numériques doivent fournir deux pièces justificatives pour établir le lieu de résidence du client.

- L&#39;adresse de livraison du client et un enregistrement de transaction de paiement réussie peuvent être utilisés pour établir le lieu de résidence du client. (Le paiement n&#39;est accepté que si l&#39;adresse de livraison correspond aux informations du fournisseur de paiement.)
- Les informations peuvent également être capturées directement à partir du magasin de données dans les tables de la base de données Commerce.

_&#x200B;**Pour collecter des informations relatives à la taxe sur les produits numériques, procédez comme suit**&#x200B;_

1. Chargez les taux d&#39;imposition pour tous les pays membres de l&#39;UE.

1. Créez une classe de taxe sur les produits numériques.

1. Affectez tous vos biens numériques à la classe de taxe sur les produits numériques.

1. Créez des [règles fiscales](tax-rules.md) pour vos biens physiques, en utilisant des classes de taxe sur les produits physiques, et associez-les aux taux de taxe appropriés.

1. Créez des règles fiscales pour vos biens numériques, en utilisant la classe de taxe de produit pour les biens numériques, et associez-les aux taux de taxe appropriés pour les pays membres de l&#39;UE.

1. Exécutez la déclaration de taxe pour la période appropriée et collectez les informations requises sur les biens numériques.

1. Exportez les montants de taxe liés aux taux de taxe pour la classe de taxe sur les produits numériques.

Ressources supplémentaires :

- [Commission européenne Fiscalité et union douanière](https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm)
- [EU 1015 Changement de lieu d&#39;approvisionnement](https://www2.deloitte.com/global/en/services/tax.html)
