---
title: Affecter un administrateur d’entreprise
description: Découvrez comment affecter un compte d’utilisateur d’entreprise en tant qu’administrateur d’entreprise désigné pour le compte d’entreprise.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 274
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

