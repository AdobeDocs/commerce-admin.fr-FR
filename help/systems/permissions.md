---
title: Autorisations d’administrateur
description: Découvrez les comptes d’utilisateurs administrateurs et comment les rôles sont utilisés pour accorder l’accès aux fonctions de gestion de magasin.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Autorisations d’administrateur

Adobe Commerce et Magento Open Source utilisent des rôles et des autorisations pour créer différents niveaux d’accès à l’administrateur. Lorsque votre magasin est configuré pour la première fois, vous recevez un ensemble d’informations d’identification de connexion pour le rôle Administrateur qui dispose d’autorisations complètes. Cependant, vous pouvez restreindre le niveau des autorisations selon le &quot;besoin de savoir&quot; des autres personnes qui travaillent sur votre site. Par exemple, un membre de l’équipe de conception peut avoir accès uniquement aux outils de conception de contenu, mais pas aux zones contenant des informations sur les clients et les commandes.

En outre, vous pouvez restreindre l’accès de l’administrateur à un site spécifique ou à un ensemble de sites et à leurs données associées. Si vous disposez de plusieurs marques ou unités opérationnelles avec des magasins distincts sur la même installation Commerce, vous pouvez accorder un accès administrateur à chaque unité opérationnelle, mais masquer et protéger leurs données des autres utilisateurs administrateurs.

Lorsque l’accès d’un utilisateur administrateur est limité à un site web ou à un magasin spécifique, les adresses où il n’est pas autorisé ne sont pas visibles ou apparaissent grisées. Seules les ventes et autres données des sites web et des magasins autorisés s’affichent pour l’utilisateur.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par défaut, le système consigne (enregistre) automatiquement toutes les actions effectuées par un utilisateur lorsqu’il applique les modifications à un magasin. Les actions d’administration peuvent être examinées dans le [rapport Journaux d’action](action-log-report.md). Configurez la connexion à la [journalisation des actions d’administration](action-log.md) dans les paramètres d’administration avancés de votre magasin.

![Admin - tous les comptes d’utilisateurs](./assets/users-all.png){width="700" zoomable="yes"}
