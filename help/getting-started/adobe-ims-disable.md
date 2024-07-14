---
title: Désactivation de l’intégration des administrateurs Commerce avec Adobe ID
description: Suivez cette procédure facultative pour désactiver l’intégration de l’administrateur Adobe Commerce avec Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Désactivation de l’intégration des administrateurs Commerce avec Adobe ID

{{ee-feature}}

Les commerçants qui ont intégré leur instance Commerce au workflow d’authentification Adobe IMS peuvent avoir besoin de désactiver cette intégration facultative.

Les déploiements de Commerce reviennent aux stratégies d’authentification et de mot de passe par défaut de Commerce une fois l’intégration IMS désactivée. Seuls les workflows des utilisateurs administrateurs sont affectés lorsque cette intégration est activée ou désactivée.

Voir [Votre compte administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) pour une présentation de la connexion de l’administrateur Commerce.

## Étape 1 : désactivation de l’intégration

Vous ne pouvez pas désactiver cette intégration dans Admin. Pour désactiver l’intégration Adobe IMS avec Commerce et rétablir l’authentification Commerce à son état par défaut, vous devez désactiver l’intégration à partir de l’interface de ligne de commande.

Pour désactiver l’intégration :

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce affiche le message suivant en cas de succès :

```terminal
Admin Adobe IMS integration is disabled.
```

## Étape 2 : création ou récupération de votre mot de passe Commerce

Après avoir désactivé l’intégration, les utilisateurs administrateurs doivent utiliser un mot de passe Commerce pour se connecter à l’administrateur.

* Les utilisateurs administrateurs de Commerce qui se souviennent de leur mot de passe Commerce préexistant (c’est-à-dire un mot de passe Commerce qui a été créé avant l’intégration IMS) peuvent l’utiliser pour se connecter à l’administrateur.

* Les utilisateurs administrateurs de Commerce qui ne disposent pas d’un mot de passe Commerce préexistant ou qui l’ont oublié doivent créer un nouveau mot de passe. Pour créer un nouveau mot de passe, les utilisateurs administrateurs peuvent utiliser la fonction [!UICONTROL Forgot your password?] de la page de connexion de Commerce pour créer un nouveau mot de passe. Voir [Réinitialisation des mots de passe client](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce n’accepte pas de champ de mot de passe vide.

## Après désactivation de l’intégration

Le workflow d’authentification Commerce par défaut reprend une fois l’intégration IMS désactivée et les utilisateurs administrateurs sont à nouveau invités à saisir leur mot de passe.

La désactivation de l’intégration IMS supprime les informations d’identification saisies lorsque l’intégration a été activée (`Organization ID`, `Client ID` et `Client Secret`) des fichiers de configuration Commerce.
