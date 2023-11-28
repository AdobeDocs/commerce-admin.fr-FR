---
title: Configuration des guillemets
description: Découvrez la configuration des guillemets, qui contrôle le montant minimum requis de commande pour les demandes de guillemet, la durée de vie des guillemets et les pièces jointes.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Configuration des guillemets

Si les guillemets sont activés dans la variable [Fonctionnalités B2B](enable-basic-features.md), vous pouvez configurer la prise en charge des guillemets dans l’Admin. La configuration du guillemet détermine le montant de commande minimal requis pour les demandes de guillemet, la durée de vie du guillemet et les formats de fichiers pris en charge pour les fichiers joints.

>[!NOTE]
>
>Les options de configuration de devis et la possibilité d&#39;utiliser les fonctions de négociation de devis sont contrôlées à l&#39;aide de la fonction [ressources de rôle](../systems/permissions-user-roles.md#role-resources). Ces ressources de rôle doivent être sélectionnées pour le rôle d’utilisateur administrateur attribué au compte d’utilisateur administrateur. Pour accorder l’accès aux fonctions de devis dans l’administrateur, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, sélectionnez le rôle et accédez à [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] dans le_ Ressources de rôle _arborescence.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Quotes]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL General]** et procédez comme suit :

   ![Configuration des guillemets de vente - général](./assets/quotes-general.png){width="700" zoomable="yes"}

   Voir [Guillemets](../configuration-reference/sales/quotes.md) dans le _Référence de configuration_ pour obtenir la liste complète des options de la fonction Guillemets et de leurs fonctions.

   - Saisissez le **[!UICONTROL Minimum Amount]** dans le panier, qui doit être rempli avant qu’une demande de devis puisse être envoyée.

   - Pour **[!UICONTROL Minimum Amount Message]**, saisissez le message à afficher lorsque le total du panier ne correspond pas au montant minimum requis.

   - Pour **[!UICONTROL Default Expiration Period]**, saisissez le nombre de **[!UICONTROL days]**, **[!UICONTROL weeks]**, ou **[!UICONTROL months]** qu&#39;un guillemet soit valable.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Attached files]** et procédez comme suit :

   - Pour **[!UICONTROL File formats for upload]**, saisissez le suffixe de chaque type de fichier pris en charge pour les fichiers joints à un guillemet.

     Saisissez chaque suffixe de fichier en minuscules, séparé par une virgule.

     Par défaut, les formats suivants sont pris en charge : `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, et `jpeg`

   - Pour **[!UICONTROL Maximum file size]**, saisissez la taille maximale d’un fichier joint en mégaoctets.

     La valeur saisie peut être remplacée par le paramètre du serveur.

     ![Configuration des guillemets de vente - fichiers joints](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
