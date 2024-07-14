---
title: Affectation d’un administrateur de société
description: Découvrez comment affecter un compte utilisateur de société en tant qu’administrateur désigné de société pour le compte de société.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Affectation d’un administrateur de société

L’administrateur de la société est initialement affecté lors de la création du compte de la société. Il ne peut être modifié que par un administrateur de magasin de l’administrateur.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Recherchez l’entreprise dans la liste et cliquez sur **[!UICONTROL Edit]**.

   ![Entreprises](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Company Admin]** .

   ![Administrateur de société](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Saisissez le **[!UICONTROL Job Title]** du nouvel administrateur de la société et cliquez sur **[!UICONTROL Proceed]** pour continuer.

   Cette action efface le formulaire et les champs _[!UICONTROL First Name]_et_[!UICONTROL Last Name]_ requis sont mis en surbrillance.

1. Saisissez l’adresse **[!UICONTROL Email]** du nouvel administrateur de la société.

   Si le système ne trouve pas l’adresse électronique dans la base de données, vous êtes invité à confirmer que vous souhaitez remplacer l’administrateur de la société.

   - Si aucun compte utilisateur n’existe pour le nouvel administrateur de la société, le système crée un compte de type `Company Admin`.

   - Si le compte utilisateur existe dans le système, il est déplacé vers le poste d’administrateur de l’entreprise dans la structure de l’entreprise.

1. Saisissez les **[!UICONTROL First Name]** et **[!UICONTROL Last Name]**, ainsi que toute autre information applicable pour le nouvel administrateur de la société.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   Le compte individuel de l’ancien administrateur de l’entreprise reste dans le système en tant que compte utilisateur individuel actif dans la structure de l’entreprise, affecté au rôle utilisateur par défaut.

   Le système envoie une notification par courrier électronique de la modification aux nouveaux administrateurs et aux anciens administrateurs de l’entreprise.
