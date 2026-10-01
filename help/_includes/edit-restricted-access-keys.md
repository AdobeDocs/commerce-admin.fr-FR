---
title: Modifier les clés d’accès restreintes
description: Procédure réutilisée pour la modification des clés d'accès restreint
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%
---
# Modifier les clés d’accès restreintes

Attribuez ou annulez l’attribution des clés d’une vue de catalogue, et non de la grille de [!UICONTROL Restricted Access Keys] principale. Vous pouvez effectuer cette modification à partir de l’onglet _[!UICONTROL Catalog Views]_&#x200B;du catalogue partagé ou de la section&#x200B;_[!UICONTROL Catalog Views]_ de l’entreprise associée : les deux répertorient les mêmes vues de catalogue et les affectations de clés actuelles.

Une vue de catalogue doit comporter au moins une clé et peut en contenir trois. Si vous essayez d’attribuer une quatrième clé, l’enregistrement échoue avec un message vous indiquant d’en supprimer une en premier.

1. Ouvrez la grille de _[!UICONTROL Catalog Views]_&#x200B;de la vue de catalogue que vous souhaitez mettre à jour à l’aide de l’un des chemins suivants :

   - _À partir du catalogue partagé_ — Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**. Pour le catalogue partagé, sélectionnez **[!UICONTROL General Settings]** dans la colonne **[!UICONTROL Action]** . Ensuite, dans le panneau _[!UICONTROL Shared Catalog Information]_, sélectionnez **[!UICONTROL Catalog Views]**.
   - _De l’entreprise_ — Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**. Pour la société, sélectionnez **[!UICONTROL Edit]** dans la colonne **[!UICONTROL Action]** . Développez ensuite la section **[!UICONTROL Catalog Views]** .

   Les deux grilles répertorient les vues de catalogue créées pour le catalogue partagé affecté à l’entreprise, y compris leurs clés affectées.

1. Sélectionnez **[!UICONTROL Edit Restricted Access Keys]** pour la vue du catalogue que vous souhaitez mettre à jour.

   ![Sélecteur Modifier les clés d’accès restreint affichant les clés affectées à une vue de catalogue](/help/systems/assets/restricted-access-key-selector.png){width="500" zoomable="yes"}

1. Dans le champ **[!UICONTROL Access Keys]** , sélectionnez une clé non affectée par la valeur [!UICONTROL Key ID].

   Les clés déjà affectées à une autre vue de catalogue sont libellées en conséquence.

1. Sélectionnez **[!UICONTROL Done]** pour affecter la clé à la vue Catalogue.

1. Pour supprimer une clé du champ de **[!UICONTROL Access Keys]** `x`, sélectionnez-la dans l’entrée du nom de la clé pour la supprimer.

1. Cliquez sur **[!UICONTROL Save]**.
