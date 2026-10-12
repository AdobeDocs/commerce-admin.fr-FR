---
title: Autorisations d’administrateur
description: Découvrez les comptes utilisateur d’administration et comment les rôles sont utilisés pour accorder l’accès aux fonctions de gestion de magasin.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: 'https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: e439352c-5b67-587d-b34e-d2a0aa5a0242
    internal-label: Roles/Permissions
  - id: 4560f5f5-d00c-5b5d-b61b-369d85ef7a26
    internal-label: User Account
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%
---
# Autorisations d’administrateur

Adobe Commerce et Magento Open Source utilisent des rôles et des autorisations pour créer différents niveaux d’accès à l’administrateur. Lorsque votre boutique est configurée pour la première fois, vous recevez un ensemble d’informations de connexion pour le rôle d’administrateur qui dispose d’autorisations complètes. Cependant, vous pouvez restreindre le niveau des autorisations en fonction du « besoin de savoir » pour d’autres personnes qui travaillent sur votre site. Par exemple, un membre de l’équipe de conception peut accéder uniquement aux outils de conception de contenu, mais pas aux zones contenant des informations sur les clients et les commandes.

En outre, vous pouvez restreindre davantage l’accès administrateur à un site spécifique ou à un ensemble de sites et aux données associées. Si vous disposez de plusieurs marques ou unités commerciales avec des magasins distincts sur la même installation de Commerce, vous pouvez fournir un accès administrateur à chaque unité commerciale, mais masquer et protéger leurs données des autres utilisateurs administrateurs.

Lorsque l’accès d’une personne utilisatrice en charge de l’administration est limité à un site web ou à une boutique spécifique, ceux pour lesquels elle n’est pas autorisée ne sont pas visibles ou apparaissent grisés. Seules les données relatives aux ventes et autres données des sites web et magasins autorisés s’affichent pour l’utilisateur.

- ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par défaut, le système consigne automatiquement (enregistre) toutes les actions effectuées par un utilisateur lorsqu’il applique des modifications à un magasin. Les actions d’administration peuvent être consultées dans le [Rapport des journaux d’actions](action-log-report.md). Configurez la journalisation dans [Journalisation des actions d’administration](action-log.md) dans les paramètres d’administration avancés de votre boutique.

![Administrateur - Tous les comptes utilisateur](./assets/users-all.png){width="700" zoomable="yes"}
