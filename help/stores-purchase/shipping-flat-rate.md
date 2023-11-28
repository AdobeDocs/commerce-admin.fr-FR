---
title: Expédition à taux plat
description: Découvrez comment configurer une option d’expédition à tarif fixe pour votre magasin.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Expédition à taux plat

_Taux d&#39;aplati_ est une charge fixe et prédéfinie qui peut être appliquée par article ou par envoi. Le prix plat est une solution de livraison simple, surtout lorsqu&#39;il est utilisé avec un emballage à prix fixe disponible auprès de certains opérateurs. Lorsqu’elle est activée, _Taux d&#39;aplatissement_ apparaît comme option lors du passage en caisse. Comme aucun opérateur spécifique n’est spécifié, vous pouvez utiliser un opérateur de votre choix.

## Configuration de l’expédition à taux fixe

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **Taux d&#39;aplatissement** .

   ![Taux d&#39;aplatissement](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Taux d&#39;aplatissement](../configuration-reference/sales/delivery-methods.md#flat-rate) dans le _Guide de référence de configuration_.

1. Définir **[!UICONTROL Enabled]** to `Yes`.

   Le taux plat apparaît comme une option dans la section Estimer l’expédition et la taxe du panier, ainsi que dans la section Expédition lors du passage en caisse.

1. Saisissez un texte descriptif. **[!UICONTROL Title]** pour la méthode Flat Rate.

1. Saisissez un **Nom de méthode** s’affiche en regard du taux calculé dans le panier.

   Le nom de la méthode par défaut est `Fixed`. Si vous facturez des frais de traitement, vous pouvez modifier ce texte en `Plus Handling`ou autre chose qui convient.

1. Pour décrire l’utilisation de l’expédition à taux fixe, définissez **Type** à l’une des options suivantes :

   - `None` - Désactive le type de paiement. L’option Taux plat est répertoriée dans le panier, mais avec un taux de zéro, ce qui revient à la même livraison gratuite.
   - `Per Order` - Facture un seul taux forfaitaire pour l’ensemble de la commande.
   - `Per Item` - Facture un seul taux forfaitaire pour chaque article. Le taux est multiplié par le nombre d’articles dans le panier, qu’il y ait plusieurs quantités d’un même article ou de différents articles.

1. Saisissez le **Prix** que vous souhaitez facturer pour les frais d&#39;expédition à taux fixe.

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Pour **Frais de gestion des calculs**, sélectionnez la méthode à utiliser pour calculer les frais de gestion :

      - `Fixed`
      - `Percent`

   - Pour **Gestion des frais**, indiquez le montant à imputer, en fonction de la méthode de calcul choisie.

     Si, par exemple, les frais sont calculés à partir d’une somme fixe, saisissez la valeur décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage du coût de livraison, saisissez le montant en pourcentage. Par exemple, si vous facturez 6 % des frais de livraison, saisissez la valeur `6`.

1. Si nécessaire, modifiez la variable **Message d’erreur affiché**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si l’option Expédition à taux plat devient indisponible.

1. Définir **Expédier aux pays applicables**:

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la variable _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définir **Afficher la méthode si cela n’est pas applicable**:

   - `Yes` - Affiche toujours la méthode Flat Rate, même lorsqu’elle n’est pas applicable.
   - `No` : affiche la méthode Flat Rate uniquement lorsque cela est possible.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’expédition à taux plat apparaît lorsqu’elle est répertoriée avec d’autres méthodes de livraison lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.
