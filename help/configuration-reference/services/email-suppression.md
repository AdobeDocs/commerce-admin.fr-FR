---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Passez en revue les paramètres de configuration sur la page [!UICONTROL Email Suppression] de [!UICONTROL Adobe Services] &gt ; de l’administrateur Commerce.
feature: Configuration, Communications
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service et Adobe Commerce Optimizer (infrastructure SaaS gérée par Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression] permet aux administrateurs de désactiver des catégories spécifiques de messagerie système automatisée sans affecter le reste de la messagerie du magasin ni nécessiter l&#39;implication des développeurs. Utilisez cette fonctionnalité pour arrêter temporairement ou définitivement certaines notifications, par exemple les e-mails de commande lors d’une migration de données ou les e-mails marketing.

>[!IMPORTANT]
>
>Les notifications des administrateurs liées à la sécurité, telles que les codes d’authentification à deux facteurs et les e-mails de réinitialisation de mot de passe administrateur, ne sont jamais supprimées par cette fonctionnalité.

Les paramètres de cette page s’appliquent par [vue de magasin](../../getting-started/websites-stores-views.md#scope-settings) afin que vous puissiez supprimer différentes catégories d’e-mails pour différents storefronts.

>[!NOTE]
>
>La désactivation de la suppression permet de restaurer immédiatement la diffusion normale des e-mails, mais les e-mails envoyés pendant la période de suppression ne sont pas mis en file d’attente.

## [!UICONTROL Email Suppression]

![Suppression d’e-mails](./assets/email-suppression.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | Affichage de la boutique | Commutateur d’activation/désactivation du Principal pour la fonction. Lorsque ce paramètre est défini sur `No` (par défaut), tous les autres paramètres de cette page sont ignorés et tous les e-mails sont envoyés normalement. |
| [!UICONTROL Disabled Functional Areas] | Affichage de la boutique | Sélectionnez une ou plusieurs catégories professionnelles dont les e-mails sont supprimés. Voir [Catégories professionnelles](#business-categories) pour connaître les éléments inclus dans chaque catégorie. |
| [!UICONTROL Disabled Template IDs] | Affichage de la boutique | Liste facultative séparée par des virgules de modèles d’e-mail spécifiques à supprimer individuellement, quelle que soit la catégorie. Utilisez le code du modèle (par exemple, `customer_password_forgot_email_template`) ou l’ID du modèle numérique pour un modèle personnalisé que vous avez créé dans l’administration. |

{style="table-layout:auto"}

### Catégories d’entreprise {#business-categories}

| Catégorie | Courriers électroniques standard inclus |
|--- |--- |
| Compte client | Création du compte, réinitialisation du mot de passe, modifications des informations du compte. |
| Order Management | Confirmation de commande, facture, expédition, avoir, annulation de commande. |
| Retours (RMA) | Retournez les notifications d’autorisation des marchandises. |
| Passage en caisse et paiement | E-mails liés au passage en caisse et au paiement par lien. |
| Marketing | Newsletters, alertes produits, partage de listes de souhaits, e-mail à un ami, rappels, invitations, registre des cadeaux. |
| Crédit et récompenses de la boutique | Cartes-cadeaux, points de récompense, modifications du solde de crédit du magasin. |
| B2B | Notifications de société, devis négociable et bon de commande. |
| Notifications système | Notifications opérationnelles telles que les e-mails de formulaires de contact, d’import et d’export planifiés. |

{style="table-layout:auto"}
