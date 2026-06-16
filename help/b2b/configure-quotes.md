---
title: Configurer les devis
description: Découvrez la configuration de devis, qui contrôle le montant minimum de commande requis pour les demandes de devis, la durée de vie du devis et les pièces jointes.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Configurer les devis

Si les guillemets sont activés dans les fonctionnalités générales [B2B](enable-basic-features.md), vous pouvez configurer la prise en charge des guillemets dans l’Administration. La configuration du devis détermine le montant minimum de commande requis pour les demandes de devis, la durée de vie du devis et les formats de fichiers pris en charge pour les fichiers joints.

>[!NOTE]
>
>Les options de configuration de devis et la possibilité d&#39;utiliser les fonctions de négociation de devis sont contrôlées à l&#39;aide des [ressources de rôle](../systems/permissions-user-roles.md#role-resources). Ces ressources de rôle doivent être sélectionnées pour le rôle d’utilisateur administrateur attribué au compte d’utilisateur administrateur. Pour accorder l’accès aux fonctions de devis dans l’administration, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, sélectionnez le rôle, puis accédez à [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] dans l’arborescence_ Ressources de rôle _.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Quotes]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General]** et procédez comme suit :

   ![Configuration des devis - Général](./assets/quotes-general.png){width="700" zoomable="yes"}

   Voir [Quotes](../configuration-reference/sales/quotes.md) dans le _Guide de référence de configuration_ pour obtenir une liste complète des options de la fonction Quotes et de leurs fonctions.

   - Saisissez les **[!UICONTROL Minimum Amount]** du panier qui doivent être satisfaites avant qu&#39;une demande de devis puisse être soumise.

   - Par **[!UICONTROL Minimum Amount Message]**, saisissez le message que vous souhaitez afficher lorsque le total du panier ne correspond pas au montant minimum requis.

   - Par **[!UICONTROL Default Expiration Period]**, saisissez le nombre de **[!UICONTROL days]**, de **[!UICONTROL weeks]** ou de **[!UICONTROL months]** pour qu&#39;un devis reste valide.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Attached files]** et procédez comme suit :

   - Par **[!UICONTROL File formats for upload]**, saisissez le suffixe de chaque type de fichier pris en charge pour les fichiers joints à une citation.

     Saisissez chaque suffixe de fichier en minuscules et séparé par une virgule.

     Par défaut, les formats suivants sont pris en charge : `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` et `jpeg`

   - Par **[!UICONTROL Maximum file size]**, saisissez la taille maximale d’un fichier joint en mégaoctets.

     La valeur saisie peut être remplacée par le paramètre du serveur.

     ![Configuration des devis - fichiers joints](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
