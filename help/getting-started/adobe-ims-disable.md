---
title: Désactivation de l’intégration d’administration Commerce à Adobe ID
description: Suivez cette procédure facultative pour désactiver l’intégration d’administration d’Adobe Commerce avec Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Désactivation de l’intégration d’administration Commerce à Adobe ID

{{ee-feature}}

Les commerçants qui ont intégré leur instance Commerce au workflow d’authentification Adobe IMS peuvent être amenés à désactiver cette intégration facultative.

Les déploiements de Commerce reviennent aux politiques de mot de passe et de workflow d’authentification Commerce par défaut une fois l’intégration IMS désactivée. Seuls les workflows utilisateur administrateur sont affectés lorsque cette intégration est activée ou désactivée.

Voir [Votre compte d’administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=fr) pour une présentation de la connexion d’administrateur Commerce.

## Étape 1 : désactivation de l’intégration

Vous ne pouvez pas désactiver cette intégration à partir de l’administration. Pour désactiver l’intégration d’Adobe IMS à Commerce et rétablir l’authentification Commerce à son état par défaut, vous devez désactiver l’intégration à partir de l’interface de ligne de commande.

Pour désactiver l’intégration :

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce affiche le message suivant en cas de succès :

```
Admin Adobe IMS integration is disabled.
```

## Étape 2 : création ou récupération de votre mot de passe Commerce

Après la désactivation de l’intégration, les utilisateurs administrateurs doivent utiliser un mot de passe Commerce pour se connecter à l’administrateur.

* Les utilisateurs administrateurs de Commerce qui se souviennent de leur mot de passe Commerce préexistant (c’est-à-dire un mot de passe Commerce créé avant l’intégration IMS) peuvent l’utiliser pour se connecter à l’administrateur.

* Les utilisateurs administrateurs de Commerce qui ne disposent pas d’un mot de passe Commerce préexistant ou qui l’ont oublié doivent en créer un nouveau. Pour créer un mot de passe, les utilisateurs administrateurs peuvent utiliser la fonction [!UICONTROL Forgot your password?] de la page de connexion de Commerce. Voir [&#x200B; Réinitialiser les mots de passe client &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=fr). Commerce n’accepte pas un champ de mot de passe vide.

## Après la désactivation de l’intégration

Le workflow d’authentification par défaut de Commerce reprend une fois l’intégration IMS désactivée et les utilisateurs administrateurs sont à nouveau invités à saisir leur mot de passe.

La désactivation de l’intégration IMS supprime les informations d’identification saisies lors de l’activation de l’intégration (valeurs `Organization ID`, `Client ID` et `Client Secret`) des fichiers de configuration de Commerce.
