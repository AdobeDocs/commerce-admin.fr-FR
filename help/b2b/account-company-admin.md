---
title: Affectation d’un administrateur de société
description: Découvrez comment affecter un compte utilisateur de société en tant qu’administrateur désigné de société pour le compte de société.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Affectation d’un administrateur de société

L’administrateur de la société est initialement affecté lors de la création du compte de la société. Il ne peut être modifié que par un administrateur de magasin de l’administrateur.

- Un seul administrateur peut être affecté à chaque entreprise.
- Un utilisateur de société peut être administrateur pour une seule société.
- Les modifications apportées à l’administrateur de la société affectée doivent être effectuées par un administrateur de magasin de l’administrateur.

## Modifier l’administrateur de la société affectée

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Entreprises](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Recherchez l’entreprise dans la liste, puis cliquez sur **[!UICONTROL Edit]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Company Admin]** .

   ![Administrateur de société](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Saisissez le **[!UICONTROL Job Title]** du nouvel administrateur de la société.

   Cette action efface le formulaire et les champs _[!UICONTROL First Name]_&#x200B;et&#x200B;_[!UICONTROL Last Name]_ requis sont mis en surbrillance.

1. Saisissez l’adresse **[!UICONTROL Email]** du nouvel administrateur de la société.

   Si le système ne trouve pas l’adresse électronique dans la base de données, vous êtes invité à confirmer que vous souhaitez remplacer l’administrateur de la société.

   - Si aucun compte utilisateur n’existe pour le nouvel administrateur de la société, le système crée un compte de type `Company Admin`.

   - Si le compte utilisateur existe dans le système, il est déplacé vers le poste d’administrateur de l’entreprise dans la structure de l’entreprise.

1. Saisissez les **[!UICONTROL First Name]** et **[!UICONTROL Last Name]**, ainsi que toute autre information applicable pour le nouvel administrateur de la société.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   Le compte individuel de l’ancien administrateur de la société reste dans le système en tant que compte utilisateur actif, affecté au rôle utilisateur par défaut. S’il s’agit de la seule société associée au compte utilisateur, le type de compte passe de *[!UICONTROL Company user]* à *[!UICONTROL Individual user]*.

   Le système envoie une notification par courrier électronique de la modification aux nouveaux administrateurs et aux anciens administrateurs de l’entreprise.

