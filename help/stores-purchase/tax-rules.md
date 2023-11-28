---
title: Règles fiscales
description: Découvrez comment définir les règles fiscales à l’aide de la classe de produits, de la classe de clients et du taux d’imposition.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Règles fiscales

Les règles fiscales intègrent une combinaison de catégories de produits, de catégories de clients et de taux d’imposition. Chaque client est affecté à une classe de clients et chaque produit se voit attribuer une classe de produits. Commerce analyse le panier de chaque client et calcule la taxe appropriée en fonction des catégories de clients et de produits, ainsi que de la région. La région est basée sur l’adresse de livraison, l’adresse de facturation ou l’origine de livraison du client.

>[!NOTE]
>
>Lorsque de nombreux taux d&#39;imposition doivent être définis, vous pouvez simplifier le processus en les important.

![Règles fiscales](./assets/tax-rules.png){width="600" zoomable="yes"}

## Etape 1 : renseigner les informations sur les règles fiscales

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Tax Rule]**.

1. Sous _Informations sur les règles fiscales_, saisissez une **[!UICONTROL Name]** pour la nouvelle règle.

   ![Informations sur les règles fiscales](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Choisissez la **[!UICONTROL Tax Rate]** qui s’applique à la règle.

   Pour modifier un taux de taxe existant, procédez comme suit :

   - Passez la souris sur le taux de la taxe et cliquez sur le _Modifier_ ![Icône Crayon](../assets/icon-edit-pencil.png) Icône

   - Mettez à jour le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

1. Pour saisir les taux d&#39;imposition, utilisez l&#39;une des méthodes suivantes :

### Méthode 1 : saisie manuelle des taux de taxe

1. Cliquez sur **[!UICONTROL Add New Tax Rate]**.

1. Remplissez le formulaire selon vos besoins (voir [Zones et taux d&#39;imposition](tax-zones-rates.md)).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   ![Nouveau taux d&#39;imposition](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Méthode 2 : taux de taxe à l’importation

1. Faites défiler jusqu’à la section située au bas de la page.

1. Pour importer des taux de taxe, procédez comme suit :

   - Cliquez sur **[!UICONTROL Choose File]** et accédez au fichier CSV contenant les taux de taxe à importer.

   - Cliquez sur **[!UICONTROL Import Tax Rates]**.

1. Pour exporter des taux de taxe, cliquez sur **[!UICONTROL Export Tax Rates]** (voir [Taux de taxe d’importation/exportation](../systems/data-transfer-tax-rates.md)).

![Importer/exporter des taux de taxe](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Etape 2 : paramétrage supplémentaire

1. Pour ouvrir la section, cliquez sur **[!UICONTROL Additional Settings]**.

   ![Paramètres supplémentaires pour la règle de taxe](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Choisissez la **[!UICONTROL Customer Tax Class]** à laquelle la règle s’applique.

   - Pour modifier une classe de taxe client, cliquez sur le bouton _Modifier_ ![Icône Crayon](../assets/icon-edit-pencil.png) , mettez à jour le formulaire suivant les besoins, puis cliquez sur **[!UICONTROL Save]**.

   - Pour créer une classe de taxe, cliquez sur **[!UICONTROL Add New Tax Class]**, remplissez le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

1. Choisissez la **[!UICONTROL Product Tax Class]** à laquelle la règle s’applique.

   - Pour modifier une classe de taxe sur les produits, cliquez sur le bouton _Modifier_ ![Icône Crayon](../assets/icon-edit-pencil.png) , mettez à jour le formulaire suivant les besoins, puis cliquez sur **[!UICONTROL Save]**.

   - Pour créer une classe de taxe, cliquez sur **[!UICONTROL Add New Tax Class]**, remplissez le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

1. Lorsque plusieurs taxes s’appliquent, saisissez un nombre pour indiquer la priorité de cette taxe pour **[!UICONTROL Priority]**.

   Si deux règles fiscales de même priorité s&#39;appliquent, les taxes sont ajoutées. Si deux taxes avec des paramètres de priorité différents s’appliquent, les taxes sont aggravées.

1. Si vous souhaitez que les taxes soient basées sur le sous-total de la commande, sélectionnez la variable **[!UICONTROL Calculate off Subtotal Only]** .

1. Pour **[!UICONTROL Sort Order]**, saisissez un numéro pour indiquer l&#39;ordre de cette règle de taxe lorsqu&#39;elle est répertoriée avec d&#39;autres personnes.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Rule]**.

## Démonstration des règles de devise et de taxe

Découvrez la gestion des règles de devise et de taxe en regardant cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
