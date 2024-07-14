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

_Taux fixe_ est une charge fixe prédéfinie qui peut être appliquée par article ou par envoi. Le prix plat est une solution de livraison simple, surtout lorsqu&#39;il est utilisé avec un emballage à prix fixe disponible auprès de certains opérateurs. Lorsque cette option est activée, le _taux plat_ apparaît comme une option lors de l’extraction. Comme aucun opérateur spécifique n’est spécifié, vous pouvez utiliser un opérateur de votre choix.

## Configuration de l’expédition à taux fixe

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **Taux d’aplatissement** .

   ![Taux d’aplatissement](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Flat Rate](../configuration-reference/sales/delivery-methods.md#flat-rate) dans le _Guide de référence de configuration_.

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

   Le taux plat apparaît comme une option dans la section Estimer l’expédition et la taxe du panier, ainsi que dans la section Expédition lors du passage en caisse.

1. Saisissez un **[!UICONTROL Title]** descriptif pour la méthode Flat Rate.

1. Saisissez un **Nom de méthode** pour afficher le taux calculé en regard du panier.

   Le nom de la méthode par défaut est `Fixed`. Si vous facturez des frais de gestion, vous pouvez modifier ce texte en `Plus Handling` ou autre chose qui convient.

1. Pour décrire l&#39;utilisation de l&#39;expédition à taux fixe, définissez **Type** sur l&#39;une des options suivantes :

   - `None` - Désactive le type de paiement. L’option Taux plat est répertoriée dans le panier, mais avec un taux de zéro, ce qui revient à la même livraison gratuite.
   - `Per Order` - Facture un seul taux forfaitaire pour l’ensemble de la commande.
   - `Per Item` - Facture un seul prix forfaitaire pour chaque article. Le taux est multiplié par le nombre d’articles dans le panier, qu’il y ait plusieurs quantités d’un même article ou de différents articles.

1. Saisissez le **Prix** que vous souhaitez facturer pour l’expédition à taux fixe.

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Pour **Calculate Handling Fee**, sélectionnez la méthode à utiliser pour calculer les frais de gestion :

      - `Fixed`
      - `Percent`

   - Pour le **frais de gestion**, indiquez le montant à prélever, en fonction de la méthode de calcul choisie.

     Par exemple, si le coût est basé sur des frais fixes, saisissez le montant sous forme de décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage du coût de livraison, saisissez le montant en pourcentage. Par exemple, si vous facturez six pour cent des frais d’expédition, entrez la valeur `6`.

1. Si nécessaire, modifiez le **message d’erreur affiché**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si l’option Expédition à taux plat devient indisponible.

1. Définissez **Ship to Applicable Countries** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définissez **Afficher la méthode si non applicable** :

   - `Yes` - Affiche toujours la méthode Flat Rate, même lorsqu’elle n’est pas applicable.
   - `No` - Affiche la méthode Flat Rate uniquement le cas échéant.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’expédition à taux plat s’affiche lorsqu’elle est répertoriée avec d’autres méthodes de livraison lors du passage en caisse.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.
