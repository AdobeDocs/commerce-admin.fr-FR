---
title: Règles fiscales
description: Découvrez comment définir les règles fiscales à l’aide de la classe de produits, de la classe de clients et du taux d’imposition.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Règles fiscales

Les règles fiscales intègrent une combinaison de catégories de produits, de catégories de clients et de taux d’imposition. Chaque client est affecté à une classe de clients et chaque produit se voit attribuer une classe de produits. Commerce analyse le panier de chaque client et calcule la taxe appropriée en fonction des catégories de clients et de produits, ainsi que de la région. La région est basée sur l’adresse de livraison, l’adresse de facturation ou l’origine de livraison du client.

>[!NOTE]
>
>Lorsque de nombreux taux d&#39;imposition doivent être définis, vous pouvez simplifier le processus en les important.

![Règles fiscales](./assets/tax-rules.png){width="600" zoomable="yes"}

## Etape 1 : renseigner les informations sur les règles fiscales

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Tax Rule]**.

1. Sous _Informations sur la règle fiscale_, saisissez un **[!UICONTROL Name]** pour la nouvelle règle.

   ![Informations sur les règles fiscales](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Sélectionnez le **[!UICONTROL Tax Rate]** qui s’applique à la règle.

   Pour modifier un taux de taxe existant, procédez comme suit :

   - Passez la souris sur le taux de taxe et cliquez sur l&#39;icône _Modifier_ ![Crayon](../assets/icon-edit-pencil.png) .

   - Mettez le formulaire à jour selon les besoins et cliquez sur **[!UICONTROL Save]**.

1. Pour saisir les taux d&#39;imposition, utilisez l&#39;une des méthodes suivantes :

### Méthode 1 : saisie manuelle des taux de taxe

1. Cliquez sur **[!UICONTROL Add New Tax Rate]**.

1. Remplissez le formulaire selon vos besoins (voir [Zones fiscales et taux](tax-zones-rates.md)).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   ![Nouveau taux d’imposition](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Méthode 2 : taux de taxe à l’importation

1. Faites défiler jusqu’à la section située au bas de la page.

1. Pour importer des taux de taxe, procédez comme suit :

   - Cliquez sur **[!UICONTROL Choose File]** et accédez au fichier CSV contenant les taux de taxe à importer.

   - Cliquez sur **[!UICONTROL Import Tax Rates]**.

1. Pour exporter des taux de taxe, cliquez sur **[!UICONTROL Export Tax Rates]** (voir [Taux de taxe d&#39;importation/exportation](../systems/data-transfer-tax-rates.md)).

![Taux de taxe d’importation/exportation](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Etape 2 : paramétrage supplémentaire

1. Pour ouvrir la section, cliquez sur **[!UICONTROL Additional Settings]**.

   ![Paramètres supplémentaires de la règle fiscale](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Sélectionnez le **[!UICONTROL Customer Tax Class]** auquel s&#39;applique la règle.

   - Pour modifier une classe de taxe client, cliquez sur l’icône _Modifier_ ![&#x200B; &#x200B;](../assets/icon-edit-pencil.png), mettez à jour le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

   - Pour créer une classe de taxe, cliquez sur **[!UICONTROL Add New Tax Class]**, remplissez le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

1. Sélectionnez le **[!UICONTROL Product Tax Class]** auquel s&#39;applique la règle.

   - Pour modifier une classe de taxe de produit, cliquez sur l’icône _Modifier_ ![&#x200B; &#x200B;](../assets/icon-edit-pencil.png), mettez à jour le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

   - Pour créer une classe de taxe, cliquez sur **[!UICONTROL Add New Tax Class]**, remplissez le formulaire selon les besoins, puis cliquez sur **[!UICONTROL Save]**.

1. Lorsque plusieurs taxes s&#39;appliquent, saisissez un nombre pour indiquer la priorité de cette taxe pour **[!UICONTROL Priority]**.

   Si deux règles fiscales de même priorité s&#39;appliquent, les taxes sont ajoutées. Si deux taxes avec des paramètres de priorité différents s’appliquent, les taxes sont aggravées.

1. Si vous souhaitez que les taxes soient basées sur le sous-total de la commande, cochez la case **[!UICONTROL Calculate off Subtotal Only]** .

1. Pour **[!UICONTROL Sort Order]**, saisissez un numéro pour indiquer l&#39;ordre de cette règle de taxe lorsqu&#39;elle est répertoriée avec d&#39;autres personnes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Rule]**.

## Démonstration des règles de devise et de taxe

Découvrez la gestion des règles de devise et de taxe en regardant cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3410211/?quality=12&learn=on&captions=fre_fr)
