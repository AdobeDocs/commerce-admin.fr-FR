---
title: Créer une règle de prix de panier
description: Découvrez comment créer une règle de prix de panier basée sur les attributs de panier ou de produit.
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 83f341c59ab9517a076eaaba71f4988e21abf826
workflow-type: tm+mt
source-wordcount: '3386'
ht-degree: 0%

---

# Créer une règle de prix de panier

Pour ajouter une règle, décrire les conditions et définir les actions, procédez comme suit. Renseignez également les étiquettes et testez la règle. Les conditions de règle de prix peuvent être basées sur le panier ou les [attributs de produit](../catalog/product-attributes.md) ou les [audiences Real-Time CDP](#use-real-time-cdp-audiences-to-set-a-condition), mais pas sur les [options personnalisables](../catalog/settings-advanced-custom-options.md).

## Étape 1 : Ajouter une règle

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Cliquez sur **[!UICONTROL Add New Rule]** et procédez comme suit :

   - Sous _[!UICONTROL Rule Information]_, terminez les **[!UICONTROL Rule Name]**et **[!UICONTROL Description]**.

   - Si vous ne souhaitez pas que la règle entre immédiatement en vigueur, définissez **[!UICONTROL Active]** sur `No`.

   ![Règle de prix du panier - Informations sur la règle](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. Pour établir la [portée](../getting-started/websites-stores-views.md#scope-settings) de la règle, procédez comme suit :

   - Sélectionnez l’ **[!UICONTROL Websites]** où la promotion doit être disponible.

   - Sélectionnez le **[!UICONTROL Customer Groups]** auquel s’applique la promotion.

     Si vous souhaitez que la promotion ne soit disponible que pour les clients enregistrés, **_ne pas_** sélectionnez l’option `NOT LOGGED IN` .

1. Définissez la règle à appliquer avec ou sans [coupon](price-rules-cart-coupon.md) comme suit :

   - Pour appliquer la règle de panier sans utiliser de code de bon, définissez **[!UICONTROL Coupon]** sur `No Coupon` et passez à l’étape 5.

   - Pour associer un coupon à une règle de prix, définissez **[!UICONTROL Coupon]** sur `Specific Coupon` et procédez comme suit :

      - Entrez un texte libre **[!UICONTROL Coupon Code]** que le client doit saisir pour recevoir la remise.

      - Pour définir une limite sur le nombre de fois où le coupon peut être utilisé, renseignez les options suivantes :

     | Option | Description |
     |------|-----------|
     | `Uses per Coupon` | Détermine le nombre de fois où le code de coupon peut être utilisé. Si aucune limite n’est définie, laissez le champ vide. |
     | `Uses per Customer` | Détermine le nombre de fois où la règle de prix du panier peut être utilisée par le même client enregistré qui appartient à l’un des groupes de clients sélectionnés. Le paramètre ne s’applique pas aux clients qui font des achats invités appartenant au groupe DE clients NON CONNECTÉS , ni aux clients qui font des achats sans se connecter à leurs comptes. Si aucune limite n’est définie, laissez le champ vide. |

     {style="table-layout:auto"}

     Pour en savoir plus, voir [Codes de bon](price-rules-cart-coupon.md).

     ![Règle de prix du panier - Paramètres des coupons](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Utilisez le _calendrier_ (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la plage de dates **[!UICONTROL From]** et **[!UICONTROL To]** pour la promotion.

1. Saisissez un nombre pour définir la **[!UICONTROL Priority]** de cette règle de prix par rapport aux Paramètres d’action des autres règles de prix actives en même temps.

   >[!NOTE]
   >
   >Le paramètre _[!UICONTROL Priority]_est important lorsque deux règles de panier ou codes de bon sont valides pour le même produit en même temps. La règle avec le paramètre [!UICONTROL Priority] le plus élevé contrôlant l’action du panier.  Les priorités du plus haut au plus bas sont `0,1,2,3...`. Voir_ Ignorer les règles de prix suivantes _à l’étape_[ Définir les actions ](#step-3-define-the-actions)_.

   >[!NOTE]
   >
   >Les règles de prix du panier ayant la même priorité ne génèrent pas de remise combinée. Chaque règle (coupon) est appliquée séparément aux produits correspondants, un par un, selon l&#39;identifiant de règle de prix du panier dans la base de données. Pour contrôler l’ordre d’application des remises, Adobe recommande de définir une priorité différente pour chaque règle de prix du panier ajoutée.

1. Pour appliquer la règle aux [flux RSS](social-rss.md#rss-feeds) publiés, définissez **Flux RSS public** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Une fois la règle enregistrée, le nom de la règle de prix du panier apparaît en haut de la page.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Une fois la règle enregistrée, le nom de la règle de prix du panier et la zone [Modifications planifiées](price-rule-cart-scheduled-changes.md) s’affichent en haut de la page.

     ![Règle de prix du panier - modifications planifiées](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## Etape 2 : décrire les conditions

Au cours de cette étape, les conditions doivent être remplies pour qu’une commande soit admissible pour la promotion. La règle est appliquée chaque fois que l’ensemble de conditions est satisfait.

Si vous utilisez des audiences de Real-Time CDP, passez à [cette section](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>La règle de prix du panier est appliquée à **_chaque_** produit dans le panier chaque fois que l’ensemble des conditions de l’onglet _[!UICONTROL Conditions]_est satisfait. Ajoutez des conditions dans l’onglet_[!UICONTROL Actions]_ pour limiter le nombre de produits affectés par la règle de prix du panier.

>[!NOTE]
>
>Si au moins un attribut de produit conditionnel a une valeur vide, la règle de prix du panier n’est pas appliquée au produit.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Conditions]**.

   ![Règle de prix du panier - conditions](./assets/conditions.png){width="600" zoomable="yes"}

   La première condition s’affiche par défaut et indique :

   `If **ALL** of these conditions are **TRUE**:`

   L’instruction comporte deux liens en gras sur lesquels vous pouvez cliquer pour afficher la sélection des options de cette partie de l’instruction. Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Effectuez l’une des opérations suivantes :

   - Cliquez sur **[!UICONTROL ALL]** et sélectionnez `ALL` ou `ANY`.
   - Cliquez sur **[!UICONTROL TRUE]** et sélectionnez `TRUE` ou `FALSE`.
   - Ne modifiez pas la condition pour appliquer la règle à tous les produits.

1. Cliquez sur _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) au début de la ligne suivante et sélectionnez une option pour la condition, telle que l’attribut du panier, la sous-sélection de produit ou la combinaison.

   Pour cet exemple, remplissez la partie suivante de la condition comme suit :

   - Lorsque vous y êtes invité, choisissez `Products Subselection`.**[!UICONTROL Choose the condition to add]**

     ![Condition de règle de prix du panier - sous-sélection de produits](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - Dans l’instruction de condition, cliquez sur **[!UICONTROL total quantity]** et sélectionnez `total quantity` ou `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] est un total de ligne. Par conséquent, les taxes ne sont pas incluses dans `total amount` pour la condition de règle de prix du panier [!UICONTROL Products Subselection]. Utilisez la condition [!UICONTROL Subtotal (Incl. Tax)] pour inclure des taxes.

   - Dans l’instruction de condition, cliquez sur **[!UICONTROL is]** et sélectionnez `greater than`.

1. Lorsque la partie suivante de la condition s’affiche, cliquez sur les éléments de l’instruction afin que vous puissiez voir où se trouve chaque lien avec des valeurs de variable.

1. Cliquez sur le lien &quot;plus&quot; (...) et saisissez `100`.

   Pour cette condition, la quantité totale du panier doit être de `101` ou supérieure.

   ![ Condition de règle de prix du panier - valeur de quantité totale ](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. Cliquez sur **Ajouter** (![Ajouter une icône](../assets/icon-add-green-circle.png)) au début de la ligne suivante, puis ajoutez une condition basée sur **Catégorie**.

   ![ Condition de règle de prix du panier - catégorie d’attributs de produit](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. Dans la partie suivante de la condition, cliquez sur le lien _more_ (**...**) pour afficher le champ de saisie, puis ouvrez le _sélecteur_ (![icône Liste](../assets/icon-list-chooser.png)) pour afficher l’arborescence des catégories.

1. Cochez la case de la catégorie que vous souhaitez utiliser comme condition pour la règle de prix et cliquez sur l’icône ![Ajouter une icône](../assets/icon-checkmark-green-circle.png) pour accepter les sélections de catégorie.

   La condition peut être basée sur n’importe quelle catégorie enfant de la [catégorie racine](../catalog/category-root.md) du magasin.

   ![ Condition de règle de prix du panier - catégorie de produits](./assets/subselection-category.png){width="600" zoomable="yes"}

1. Pour ajouter d’autres conditions, cliquez sur _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)) et définissez une autre condition.

   Vous pouvez répéter le processus autant de fois que nécessaire pour décrire les conditions qui doivent être remplies pour la règle de prix. Voici quelques exemples :

   **Exemple 1 :** Règle de prix régionale

   Pour créer une règle de prix régionale, utilisez l’un des attributs de panier suivants :

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **Exemple 2 :** Totaux du panier

   Pour baser la condition sur les totaux du panier, utilisez l’un des attributs suivants du panier :

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>Dans le cas de plusieurs promotions parallèles, la condition _Subtotal_ est appliquée au sous-total _base_ du panier **_avant_** toute remise.

>[!IMPORTANT]
>
>**Pour les commandes d’achat uniquement** : lorsqu’une règle de prix de panier est définie selon un ou plusieurs modes de paiement spécifiques, la remise est appliquée au total lors de la création d’une commande d’achat. Une fois la commande créée, la remise reste appliquée au total si le mode de paiement est remplacé par un mode qui n’est pas couvert par la règle du prix du panier.

### Ajout d’un attribut de produit aux règles de prix du panier

1. Accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**et ouvrez l’attribut product .

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Storefront Properties]**.

1. Définissez **[!UICONTROL Use for Promo Rule Conditions]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

1. Accédez à **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** et ouvrez la règle de prix du panier requise.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Condition]** et sélectionnez **[!UICONTROL Product attribute combination]**.

1. Définissez cette condition sur l’une des valeurs suivantes :

   - Cliquez sur **[!UICONTROL FOUND]** et sélectionnez `FOUND` ou `NOT FOUND`.

   - Cliquez sur **[!UICONTROL ALL]** et sélectionnez `ALL` ou `ANY`.

1. Cliquez sur l’icône _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)) et sélectionnez l’ **[!UICONTROL Product Attribute]** que vous avez configuré pour les conditions des règles promotionnelles.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Lors de l’utilisation de la condition `is not one of` avec un attribut de produit _SKU_ et un produit configurable, les SKU du produit parent et enfant doivent être sélectionnés. Pour éviter de répertorier tous les SKU enfants dans la règle, vous pouvez utiliser la condition `does not contain` avec les parties SKU communes d’un produit configurable et de ses produits enfants.

### Utilisation d’audiences Real-Time CDP pour définir une condition

Vous pouvez définir une condition pour une règle de prix de panier basée sur une [audience](../customers/audience-activation.md) Real-Time CDP.

1. Développez **[!UICONTROL Conditions]**, cliquez sur l’icône &quot;+&quot;, puis sélectionnez **[!UICONTROL Real-Time CDP Audience]** dans la liste.

   ![Sélectionner la condition d’audience Real-Time CDP](./assets/rtcdp-conditions.png){width="300"}

1. Sélectionnez l’icône _Plus_ (**...**), cliquez sur **[!UICONTROL Open Chooser]** et affichez toutes les audiences Real-Time CDP disponibles.

   ![Afficher les audiences Real-Time CDP](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. Sélectionnez l’audience Real-Time CDP que vous souhaitez utiliser pour la règle de prix du panier.

   | Option | Description |
   |------|-----------|
   | `ID` | Identifiant interne de l’audience utilisée dans l’Admin |
   | `Real-Time CDP Audience ID` | Identifiant unique de l’audience lorsqu’elle a été créée dans Experience Platform |
   | `Name` | Nom de l’audience, par exemple `Orders over $50` |
   | `Description` | Description de l’audience, par exemple `People who placed an order over $50 in the last month.`. |
   | `Source` | Indique d’où provient l’audience, par exemple `Experience Platform`. |
   | `Website` | Indique le site web que vous avez lié à la banque de données qui contient les audiences. Vous créez ce lien lorsque vous connectez votre instance Commerce à l’Experience Platform par le biais de l’extension [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html). |

   {style="table-layout:auto"}

À l’étape suivante, vous définissez l’action à effectuer lorsque la condition est remplie.

## Etape 3 : définir les actions

Les actions de la règle de prix du panier décrivent comment les prix sont mis à jour lorsque les conditions sont remplies.

1. Faites défiler l’écran jusqu’à **[!UICONTROL Actions]**, puis développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png).

   ![ Règle de prix du panier - actions ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Apply]** sur l’une des options de remise suivantes :

   | Option | Description |
   |------|-----------|
   | `Percent of product price discount` | Remise l&#39;article en soustrayant un pourcentage du prix d&#39;origine. La remise s’applique à chaque article éligible du panier. Par exemple : saisissez `10` dans [!UICONTROL Discount Amount] pour un prix mis à jour qui est 10 % inférieur au prix d’origine. |
   | `Fixed amount discount` | Remise un article en soustrayant un montant fixe du prix d’origine de chaque article admissible dans le panier. Par exemple : saisissez `10` dans [!UICONTROL Discount Amount] pour un prix mis à jour qui est 10 $ de moins que le prix d’origine. |
   | Remise de montant fixe pour le panier entier | Remplace l’intégralité du panier en soustrayant un montant fixe du total du panier. Par exemple : saisissez 10 dans [!UICONTROL Discount Amount] pour soustraire 10 $ du total du panier. Par défaut, la remise ne s&#39;applique qu&#39;au sous-total du panier. Pour appliquer la remise au sous-total et aux frais d’expédition séparément, utilisez l’option _[!UICONTROL Apply to Shipping Amount]_. |
   | `Buy X get Y free` | Définit une quantité X que le client doit acheter pour recevoir gratuitement une quantité Y **du même produit/variation**. (Le [!UICONTROL Discount Amount] est Y.) Une quantité totale de X+Y de cet article doit être présente/ajoutée au panier pour que la remise soit appliquée. |

   {style="table-layout:auto"}

   - Saisissez le **[!UICONTROL Discount Amount]** comme nombre, sans symboles. Par exemple, selon l’option de remise sélectionnée, le nombre 10 peut indiquer un pourcentage, un montant fixe ou une quantité d’articles.

   - Pour obtenir une remise _Acheter X avec Y gratuit_, saisissez la quantité dans le champ **[!UICONTROL Discount Qty Step (Buy X)]** d’un seul produit/SKU/article que le client doit acheter pour recevoir la remise sur la quantité Y. Les valeurs X et Y font référence aux quantités d’un même SKU, et cette quantité spécifique (les variantes d’un produit configurable sont comptabilisées séparément) de l’article doit être ajoutée manuellement au panier.

   - Dans le champ **[!UICONTROL Maximum Qty Discount is Applied To]** , saisissez la quantité maximale du même produit pouvant bénéficier de la remise au cours du même achat.

   - Définissez **[!UICONTROL Apply to Shipping Amount]** (![Bascule Option](../assets/toggle-yes.png)) comme suit :

     | Option | Description |
     |------|-----------|
     | `Yes` | Applique le montant de la remise séparément au sous-total et aux frais de livraison. |
     | `No` | Applique le montant de la remise uniquement au sous-total. |

     {style="table-layout:auto"}

   - Pour arrêter le traitement d’autres règles après l’application de cette règle, définissez **[!UICONTROL Discard Subsequent Rules]** (![Bascule d’option](../assets/toggle-yes.png)) sur `Yes`. Ce paramètre empêche l’application de plusieurs remises au même produit.

     | Option | Description |
     |------|-----------|
     | `Yes` | Empêche l’application de toute autre règle de prix pouvant s’appliquer à un produit. Lorsque plusieurs règles de tarification s’appliquent au même produit, seule la règle de tarification avec la priorité définie la plus élevée (dans un champ de règle [!UICONTROL Priority]) est appliquée au produit admissible. Cela évite que plusieurs règles de tarification ne soient empilées et ne fournissent des remises supplémentaires inattendues. |
     | `No` | Permet à plusieurs règles de tarification de s’appliquer au même produit. Cela peut entraîner un empilement et fournir plusieurs remises appliquées au prix de votre offre. |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >Pour ignorer les règles suivantes, une règle de tarification doit utiliser les priorités définies dans le champ Priorité de chaque règle, et plusieurs règles ne doivent pas avoir la même priorité définie . Voir **[!UICONTROL Priority]** à l’étape _Ajouter une nouvelle règle_ .

1. Pour définir les produits **_exacts_** du panier qui sont affectés par la règle de prix du panier, ajoutez les conditions **_supplémentaires_** nécessaires à l’action.

   Pour déterminer si la livraison gratuite est appliquée aux commandes qui répondent aux conditions, définissez **[!UICONTROL Free Shipping]** sur l’une des options suivantes :

   | Option | Description |
   |------|-----------|
   | `No` | La livraison gratuite n’est pas disponible. |
   | `For matching items only` | La livraison gratuite est disponible uniquement pour les éléments qui correspondent aux conditions de la règle. |
   | `For shipment with matching items` | La livraison gratuite est disponible pour toute livraison incluant des articles correspondants. La méthode de remise [Livraison gratuite](../stores-purchase/shipping-free.md) doit être activée pour utiliser cette option. |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour **[!UICONTROL Add Rewards Points]**, saisissez le nombre fixe de points que le client gagne **_une fois_** par commande chaque fois que la règle de prix du panier est appliquée.

   Si les points de récompense ne sont pas activés, laissez ce champ vide.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save and Continue Edit]**.

## Étape 4 : renseigner les libellés

Le libellé apparaît dans la section des totaux de la commande pour identifier la remise. Le texte de l’étiquette est inclus entre parenthèses, après le mot `Discount`. Vous pouvez saisir un libellé par défaut pour toutes les vues de magasin ou un libellé différent pour chaque vue.

![Panier de vitrine - étiquettes de remise](./assets/order-totals-section-discount-special.png){width="600"}

1. Faites défiler l’écran jusqu’à **[!UICONTROL Labels]** et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) .

1. Saisissez le texte que vous souhaitez utiliser comme **[!UICONTROL Default Rule Label for All Store Views]**.

   ![Règle de prix du panier - étiquette par défaut](./assets/label-default.png){width="600" zoomable="yes"}

1. Si votre boutique comporte plusieurs vues ou plusieurs sites web avec plusieurs vues, saisissez le texte d’étiquette approprié pour chacune d’elles.

   Par exemple, si chaque vue de magasin est dans une langue différente, saisissez la traduction du libellé pour chaque vue.

   ![ Étiquettes spécifiques au magasin ](./assets/label-store-specific.png){width="600" zoomable="yes"}

## Étape 5 : Ajout de blocs dynamiques associés (facultatif)

{{ee-feature}}

[Blocs dynamiques](../content-design/dynamic-blocks.md) associés à la règle apparaissent dans le storefront chaque fois que les conditions sont remplies.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Related Dynamic Blocks]** .

1. Utilisez les [filtres de recherche](../getting-started/admin-workspace.md) pour localiser les blocs que vous souhaitez associer à la règle.

1. Cochez la case dans la première colonne pour associer le bloc à la règle.

   Pour en savoir plus, voir [Blocs dynamiques dans les règles de prix](../content-design/dynamic-blocks-price-rules.md).

## Étape 6 : enregistrer et tester la règle

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Rule]**.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.

   Les règles de prix sont automatiquement traitées avec d’autres règles système chaque nuit. Lorsque vous créez une règle de prix, laissez suffisamment de temps pour qu’elle entre dans le système. Testez également la règle pour vous assurer qu’elle fonctionne correctement. A mesure que de nouvelles règles sont ajoutées, Commerce recalcule les prix et les priorités en conséquence.

## Démonstration de la règle de prix du panier

Regardez cette vidéo pour en savoir plus sur la création de règles de prix de panier :

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## Descriptions des champs

### [!UICONTROL Rule Information]

| Champ | Description |
|--- |--- |
| [!UICONTROL Rule Name] | (Obligatoire) Le nom de la règle est à titre de référence interne. |
| [!UICONTROL Description] | Une description de la règle doit inclure l’objectif de la règle et expliquer comment elle est utilisée. |
| [!UICONTROL Active] | (Obligatoire) Détermine si la règle est active dans le magasin. Options : `Yes` / `No` |
| [!UICONTROL Websites] | (Obligatoire) Identifie les sites web sur lesquels la règle peut être utilisée. |
| [!UICONTROL Customer Groups] | (Obligatoire) Identifie les groupes de clients auxquels s’applique la règle. |
| [!UICONTROL Coupon] | (Obligatoire) Indique si un coupon est associé à la règle. Options : <br/>**[!UICONTROL No Coupon]**- Aucun coupon n’est associé à la règle.<br/>**[!UICONTROL Specific Coupon]** - Un coupon spécifique est associé à la règle. <br/>**[!UICONTROL Coupon Code]**- Lorsque vous y êtes invité, saisissez le code de bon que le client doit saisir pour profiter de la promotion.<br/>**[!UICONTROL Use Auto Generation]** - Cochez la case pour générer automatiquement plusieurs codes de bon qui peuvent être utilisés avec la promotion. <br/>**[!UICONTROL Auto]**- Affiche la section _[!UICONTROL Manage Coupon Codes]_pour définir le format des codes de coupon à générer. |
| [!UICONTROL Uses per Coupon] | Détermine le nombre de fois où le code de coupon peut être utilisé. Si aucune limite n’est définie, laissez le champ vide. |
| [!UICONTROL Uses per Customer] | Détermine le nombre de fois où la règle de prix du panier peut être utilisée par le même client enregistré qui appartient à un groupe de clients sélectionné. Ne s’applique pas aux acheteurs invités qui sont membres du groupe de clients NON CONNECTÉS , ni aux clients qui achètent sans se connecter à leurs comptes. Pour aucune limite, laissez vide. |
| [!UICONTROL Priority] | Un nombre qui indique la priorité de cette règle par rapport aux autres. Les priorités du plus haut au plus bas sont `0,1,2,3...` |
| [!UICONTROL Public in RSS Feed] | Détermine si la promotion est incluse dans le flux RSS public de votre magasin. Options :  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Date de première utilisation du coupon. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Dernière date à laquelle le coupon peut être utilisé. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Indique les conditions qui doivent être remplies avant que la règle de prix du panier ne prenne effet. Si rien n’est indiqué, la règle s’applique à tous les produits du panier. Les conditions peuvent être basées sur n’importe quelle combinaison d’attributs de panier et de produit. Cependant, les [options personnalisables](../catalog/settings-advanced-custom-options.md) ne peuvent pas être référencées dans les conditions des règles de prix du panier.

| Champ | Description |
|--- |--- |
| [!UICONTROL **Attribut d’élément de panier**] |  |
| [!UICONTROL Price in cart] | Prix du produit. La règle s’applique si le prix du produit dans la condition du panier est satisfait. |
| [!UICONTROL Quantity in cart] | Quantité de produit. La règle s’applique si la quantité de produit dans le panier est remplie. |
| [!UICONTROL Row total in cart] | Total de la ligne du produit. La règle s’applique si le total de la ligne du produit dans la condition du panier est satisfait. |
| [!UICONTROL **Attribut de produit**] |  |
| [!UICONTROL Attribute Set] | Jeu d’attributs de produit. La règle s’applique si le produit respecte la condition d’attribut du produit. |
| [!UICONTROL Category/Other attribute] | Catégorie de produit/autre attribut. La règle s’applique si le produit lui-même ou les enfants répondent à la condition de catégorie/autre attribut. [!UICONTROL Use for Promo Rule Conditions] doit être défini sur `Yes` pour l’attribut. |
| [!UICONTROL Category/Other attribute (Children Only)] | Catégorie de produit enfant/autre attribut. La règle s’applique si seuls les enfants de produit répondent à la condition de catégorie/autre attribut (le produit lui-même n’est pas vérifié ici). L’attribut doit avoir [!UICONTROL Use for Promo Rule Conditions] sur `Yes`. |
| [!UICONTROL Category/Other attribute (Parent Only)] | Catégorie de produit parente/autre attribut. La règle s’applique si seul le produit répond à la condition de catégorie/autre attribut (les produits enfants ne sont pas vérifiés ici). [!UICONTROL Use for Promo Rule Conditions] doit être défini sur `Yes` pour l’attribut. |
| [!UICONTROL **Attribut au panier**] |  |
| [!UICONTROL Subtotal (Excl. Tax)] | Sous-total du panier (hors taxe). La règle s’applique si le panier respecte la condition de sous-total (hors taxe). |
| [!UICONTROL Subtotal (Incl. Tax)] | Sous-total du panier (taxes comprises). La règle s’applique si le panier respecte la condition de sous-total (y compris la taxe). |
| [!UICONTROL Subtotal] | Sous-total du panier. La règle s’applique si le panier respecte une condition de sous-total. Cochez la case inclut ou exclut la taxe en fonction des paramètres de taxe actuels. |
| [!UICONTROL Total Items Quantity] | Quantité totale de tous les produits du panier. La règle s’applique si le panier respecte une condition de quantité totale d’articles. |
| [!UICONTROL Total Weight] | Poids total de tous les produits du panier. La règle s’applique si le panier respecte la condition de poids total. |
| [!UICONTROL Payment Method] | Mode de paiement sélectionné lors de l’extraction. La règle s’applique si la condition du mode de paiement est remplie. |
| [!UICONTROL Shipping Method] | Mode de livraison sélectionné lors du passage en caisse. La règle s’applique si la condition du mode de livraison est remplie. |
| [!UICONTROL Shipping Postcode] | Code postal de l’adresse d’expédition. La règle s’applique si l’adresse de livraison respecte la condition du code postal. |
| [!UICONTROL Shipping Region] | Région de l’adresse d’expédition. La règle s’applique si l’adresse de livraison respecte la condition de région. |
| [!UICONTROL Shipping State/Province] | Etat/province de l’adresse d’expédition. La règle s’applique si l’adresse de livraison respecte la condition Etat/province. |
| [!UICONTROL Shipping Country] | Pays de l’adresse d’expédition. La règle s’applique si l’adresse de livraison respecte la condition du pays. |
| [!UICONTROL Customer Segment] | La règle s’applique si un client enregistré ou invité remplit la condition de segment du client. |

### [!UICONTROL Actions]

| Champ | Description |
|--- |--- |
| [!UICONTROL Apply] | Détermine le type de calcul appliqué à l’achat. Options : <br/>**[!UICONTROL Percent of product price discount]**- article de remise en soustrayant un pourcentage du prix d’origine. Par exemple : saisissez `10` dans _[!UICONTROL Discount Amount]_pour un prix mis à jour qui est 10 % inférieur au prix d’origine.<br/>**[!UICONTROL Fixed amount discount]**- Remise un article en soustrayant un montant fixe du prix d’origine de chaque article éligible dans le panier. Par exemple : saisissez `10` dans_[!UICONTROL Discount Amount]_ pour un prix mis à jour qui est 10 $ de moins que le prix d’origine. <br/>**[!UICONTROL Fixed amount discount for whole cart]**- Remplace l’intégralité du panier en soustrayant un montant fixe du sous-total du panier. Par exemple : saisissez `10` dans _[!UICONTROL Discount Amount]_pour soustraire 10 $ du sous-total du panier. Par défaut, la remise ne s&#39;applique qu&#39;au sous-total du panier. Pour appliquer la remise au sous-total et aux frais d’expédition séparément, voir_Appliquer au montant d’expédition _.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**- Définit une quantité que le client doit acheter pour recevoir gratuitement une quantité. (La valeur_[!UICONTROL Discount Amount]_ est Y.) |
| [!UICONTROL Discount Amount] | (Obligatoire) Montant de la remise proposée. |
| [!UICONTROL Maximum Qty Discount is Applied To] | Définit le nombre maximal de produits auxquels la remise peut être appliquée au cours du même achat. |
| [!UICONTROL Discount Qty Step (Buy X)] | Définit le nombre de produits représentés par `X` dans une promotion `Buy X Get Y Free`. Définit également le nombre de produits à ajouter au panier ensemble par lots pour appliquer des promotions `Fixed amount discount` et `Percent of product price discount`. |
| [!UICONTROL Apply to Shipping Amount] | Détermine si la remise est appliquée séparément au sous-total et aux montants d’expédition. Sinon, elle s’applique uniquement au sous-total. Options : `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | Détermine si des règles de priorité inférieure (1 est la priorité la plus élevée) peuvent être appliquées au produit lorsque cette règle de prix de panier est une correspondance. Activez cette option pour empêcher que plusieurs remises ne soient appliquées au même produit. Options : `Yes` / `No` |
| [!UICONTROL Free Shipping] | Détermine si la livraison gratuite est incluse dans la promotion et, le cas échéant, pour quels éléments. Options : <br/>**[!UICONTROL No]**- La livraison gratuite n’est pas disponible pour la règle actuelle.<br/>**[!UICONTROL For matching items only]** - La livraison gratuite est disponible uniquement pour des articles spécifiques du panier qui correspondent à la règle. <br/>**[!UICONTROL For shipment with matching items]**- La livraison gratuite est disponible pour tous les articles du panier. La méthode de remise [Livraison gratuite](../stores-purchase/shipping-free.md) doit être activée pour utiliser cette option. |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indique le nombre de [points de récompense](rewards-loyalty.md) gagnés par le client lors de l’application de la règle de prix. |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| Champ | Description |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | Libellé par défaut qui identifie la remise et peut être utilisé pour toutes les vues de magasin. |
| [!UICONTROL Store View Specific Labels] | Le cas échéant, spécifie un libellé différent pour identifier la remise pour chaque vue de magasin. |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifie tous les [blocs dynamiques](../content-design/dynamic-blocks.md) associés à la règle.
