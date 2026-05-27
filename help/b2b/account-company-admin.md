---
title: Affecter un administrateur d’entreprise
description: Découvrez comment affecter un compte d’utilisateur d’entreprise en tant qu’administrateur d’entreprise désigné pour le compte d’entreprise.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Affecter un administrateur d’entreprise

L’administrateur d’entreprise est initialement affecté lors de la première création du compte d’entreprise et ne peut être modifié que par un administrateur de magasin à partir de l’administrateur.

- Un seul administrateur peut être affecté à chaque société.
- Un utilisateur d’entreprise ne peut être l’administrateur que d’une seule société.
- Les modifications apportées à l’administrateur d’entreprise affecté doivent être effectuées par un administrateur de magasin à partir de l’administrateur.

## Modifier l’administrateur d’entreprise affecté

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Entreprises](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Recherchez la société dans la liste, puis cliquez sur **[!UICONTROL Edit]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Company Admin]** .

   ![Administrateur d’entreprise](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Saisissez le **[!UICONTROL Job Title]** du nouvel administrateur de la société.

   Cette action efface le formulaire et les champs de _[!UICONTROL First Name]_et de_[!UICONTROL Last Name]_ requis sont mis en surbrillance.

1. Saisissez l&#39;adresse **[!UICONTROL Email]** du nouvel administrateur de la société.

   Si le système ne trouve pas l&#39;adresse e-mail dans la base de données, vous êtes invité à confirmer que vous souhaitez remplacer l&#39;administrateur de la société.

   - S’il n’existe pas de compte utilisateur pour le nouvel administrateur de la société, le système crée un compte du type `Company Admin`.

   - Si le compte utilisateur existe dans le système, il est déplacé vers le poste d’administrateur de la société dans la structure de la société.

1. Saisissez le **[!UICONTROL First Name]** et le **[!UICONTROL Last Name]**, ainsi que toute autre information applicable au nouvel administrateur de la société.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

   Le compte individuel de l’ancien administrateur d’entreprise reste dans le système en tant que compte utilisateur actif, affecté au rôle utilisateur par défaut. S’il s’agit de la seule société associée au compte utilisateur, le type de compte passe de *[!UICONTROL Company user]* à *[!UICONTROL Individual user]*.

   Le système envoie une notification par e-mail de la modification aux nouveaux et anciens administrateurs de l’entreprise.

