---
title: Création d’un compte client individuel
description: Les visiteurs peuvent facilement créer un compte client individuel pour gérer leurs achats.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Création d’un compte client individuel

Les visiteurs de votre boutique peuvent ouvrir un compte pour gérer leurs achats et leurs activités. Les clients créent généralement leurs propres comptes à partir de votre magasin. Cependant, vous pouvez également créer des comptes client directement à partir de l’Administration, ce qui est utile pour aider les clients par téléphone.

Les instructions suivantes représentent la configuration de compte client par défaut. Pour modifier la sélection et le comportement de certains champs du formulaire, voir [Configuration des comptes clients](../customers/customer-account-scope.md).

En tant qu’administrateur de magasin, vous pouvez également définir la variable [nouvelles options de compte](../customers/account-options-new.md) pour envoyer un e-mail de confirmation aux nouveaux clients enregistrés, ce qui permet de s’assurer que les comptes enregistrés sont valides.

>[!NOTE]
>
>À partir de la version 2.4.7, les clients doivent saisir à nouveau leur adresse e-mail et leur mot de passe pour se connecter à leur compte après confirmation par e-mail, quel que soit le navigateur.

## Créer un compte à partir du storefront

Un client du magasin crée un compte sur le storefront.

1. Depuis le storefront, clics **[!UICONTROL Create an Account]** dans le coin supérieur droit de l’en-tête.

   ![Création d’un compte](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. Sous **[!UICONTROL Personal Information]**, entre leur **[!UICONTROL First Name]** et **[!UICONTROL Last Name]**.

   ![Informations personnelles](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. S’il souhaite ajouter son nom et son adresse e-mail à la liste des abonnés à la newsletter, le client sélectionne l’option **[!UICONTROL Sign Up for Newsletter]** case à cocher.

   >[!INFO]
   >
   > Cette option s’affiche même si le magasin ne publie pas de newsletter.

1. S’ils souhaitent que le personnel d’assistance du magasin : [voir ce qu&#39;ils voient](../customers/login-as-customer.md) et fournir une assistance à distance, le client sélectionne l’ **[!UICONTROL Allow remote shopping assistance]** case à cocher.

1. Sous **[!UICONTROL Sign-in Information]**, entre leur **[!UICONTROL Email]** adresse.

   >[!INFO]
   >
   > Cette adresse e-mail fait désormais partie de leurs informations de connexion et ne peut pas être associée à un autre compte client.

   ![Informations de connexion](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Saisit un **[!UICONTROL Password]** cela inclut trois des types d’informations suivants :

   - Caractères minuscules
   - Caractères en majuscule
   - Nombres
   - Caractères spéciaux

   Après avoir appuyé **[!UICONTROL Enter]**, la force du mot de passe est évaluée et apparaît sous le champ. Si le mot de passe est considéré comme _Faible_, essayez-en un autre jusqu’à ce qu’il soit évalué comme _Fort_.

   ![Un mot de passe fort est recommandé](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Ensuite, le client la saisit à nouveau pour **[!UICONTROL Confirm Password]**.

1. Si nécessaire, clique sur **[!UICONTROL Show Password]** pour afficher le mot de passe saisi.

1. Une fois l’opération terminée, cliquez sur **Création d’un compte**.

Le client peut ensuite utiliser son adresse e-mail et son mot de passe pour [se connecter](../customers/customer-sign-in.md) à leur compte et compléter les informations d’adresse.

## Créer un compte à partir de l’administrateur

En tant que commerçant, vous pouvez créer un compte client à partir de l’Admin.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Clic **[!UICONTROL Add New Customer]**.

### Étape 1 : renseigner les informations sur le compte

![Informations sur le client](assets/new-information.png){width="700" zoomable="yes"}

1. Dans le **[!UICONTROL Account Information]** , procédez comme suit :

   - Pour une installation multisite, définissez **[!UICONTROL Associate to Website]** vers le site web sur lequel le compte client s’applique.
   - Le cas échéant, affectez le client à un autre **[!UICONTROL Customer Group]**.
   - Si vous utilisez [Validation du numéro de TVA](../stores-purchase/vat.md) et que vous souhaitez **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**, cochez la case.

1. Renseignez les champs obligatoires :

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Renseignez les champs facultatifs suivant les besoins :

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >Dans le respect des bonnes pratiques actuelles en matière de sécurité et de confidentialité, gardez à l&#39;esprit les risques juridiques et de sécurité potentiels associés au stockage de la date de naissance complète du client (mois, jour, année) avec d&#39;autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clientes et clients et d’utiliser l’année de naissance du client comme alternative.

1. Définir **[!UICONTROL Send Welcome Email From]** à la vue de magasin à partir de laquelle _Bienvenue_ un e-mail doit être envoyé.

   >[!INFO]
   >
   > Si le magasin propose des vues différentes [langues](../stores-purchase/store-localize.md), ce paramètre détermine la langue de l’e-mail de bienvenue.

1. Clic **[!UICONTROL Save and Continue Edit]** en haut de la page.

   >[!INFO]
   >
   >Une fois le compte client enregistré, l’ensemble complet des options s’affiche dans le panneau de gauche et dans le menu en haut de la page. Le _[!UICONTROL Customer View]_L’onglet affiche un résumé du compte.

   ![Affichage client](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Étape 2 : remplir les informations d&#39;adresse

1. Dans le panneau de gauche, choisissez **[!UICONTROL Addresses]** et cliquez sur **[!UICONTROL Add New Addresses]**.

1. Si la même adresse est utilisée pour la facturation et l’expédition, activez les deux options.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Ajout des informations d’adresse du client](assets/information-addresses.png){width="600" zoomable="yes"}

1. Faites défiler vers le bas et renseignez les champs d’adresse requis dans la deuxième colonne.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Saisir le **[!UICONTROL Phone Number]** pour cette adresse.

1. Le cas échéant, saisissez **[!UICONTROL VAT Number]** associé au client.

1. Si cette adresse est la seule nécessaire pour le compte, cliquez sur **[!UICONTROL Save]**.

   Sinon, cliquez sur **[!UICONTROL Save and Continue Edit]** et répétez les étapes précédentes pour ajouter des adresses supplémentaires.

   La nouvelle adresse s’affiche dans le [!UICONTROL Addresses] page avec le sélectionné _[!UICONTROL Default Billing]_et_[!UICONTROL Default Shipping]_ adresses situées au-dessus de la liste complète.

   ![Vue Adresses](assets/address-list.png){width="600" zoomable="yes"}

### Étape 3 : réinitialiser le mot de passe

Aucun mot de passe n’est initialement attribué aux comptes clients créés à partir de l’administrateur.

1. Recherchez le nouveau compte client dans la grille.

1. Clic **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne.

1. Dans la barre de menus en haut de la page, cliquez sur **[!UICONTROL Reset Password]**.

1. Une notification est envoyée au propriétaire du compte, avec des instructions pour définir le mot de passe.

## Barre de boutons

D’autres boutons sont disponibles lorsque le profil est enregistré pour la première fois. Pour en savoir plus, voir [Mise à jour d’un profil client](../customers/update-account.md).

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Retourne à _[!UICONTROL Customers]_sans enregistrer les modifications. |
| **[!UICONTROL Delete Customer]** | Supprime le client actuel. Les commandes terminées associées au client ne sont pas supprimées. |
| **[!UICONTROL Reset]** | Réinitialise toutes les modifications non enregistrées dans le formulaire client à leurs valeurs précédentes. |
| **[!UICONTROL Create Order]** | Crée une commande pour le client. |
| **[!UICONTROL Reset Password]** | Envoie un [réinitialiser le mot de passe](../customers/password-reset.md) lien vers le client par email. |
| **[!UICONTROL Force Sign-in]** | Révoque les jetons d’accès OAuth associés au compte client. Cette fonction ne peut être utilisée qu’avec des comptes clients auxquels des jetons OAuth ont été attribués dans le cadre d’une API web [intégration](../systems/integrations.md). Pour en savoir plus, voir [Authentification basée sur OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) dans la documentation destinée aux développeurs. |
| **[!UICONTROL Manage Shopping Cart]** | Permet à l’administrateur ou l’administratrice de gérer le panier pour le client ou la cliente. |
| **[!UICONTROL Save and Continue Edit]** | Enregistre les modifications et maintient le profil client ouvert. |
| **[!UICONTROL Save Customer]** | Enregistre les modifications et ferme le profil client. |

{style="table-layout:auto"}

## Descriptions des champs

### [!UICONTROL Account Information]

| Champ | Description |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifie le site Web associé au compte client. |
| **[!UICONTROL Group]** | Identifie l’ [groupe de clients](../customers/customer-groups.md) lorsque le client est membre. Le cas échéant, cochez la case pour désactiver le changement de groupe automatique basé sur la TVA. |
| **[!UICONTROL Name Prefix]** | S’il est utilisé, le préfixe associé au nom du client (par exemple, M., Mme ou Dr). Les valeurs de préfixe sont déterminées par l’ [configuration](../configuration-reference/customers/customer-configuration.md). Selon la configuration, le contrôle de saisie peut être un champ de texte ou une liste d’options. |
| **[!UICONTROL First Name]** | Prénom du client. |
| **[!UICONTROL Middle Name / Initial]** | Deuxième prénom ou initial du client. Ce champ n’est inclus que s’il est spécifié dans [configuration](../configuration-reference/customers/customer-configuration.md) rubrique. |
| **[!UICONTROL Last Name]** | Nom du client. |
| **[!UICONTROL Name Suffix]** | S’il est utilisé, le suffixe associé au nom du client (tel que Jr., Sr. ou III). Les valeurs de suffixe sont déterminées par [configuration](../configuration-reference/customers/customer-configuration.md). Selon la configuration, le contrôle de saisie peut être un champ de texte ou une liste déroulante d’options. |
| **[!UICONTROL Email]** | Adresse e-mail du client. |
| **[!UICONTROL Date of Birth]** | Date de naissance du client. La date de naissance est incluse si elle est spécifiée dans le [configuration](../configuration-reference/customers/customer-configuration.md) rubrique. <br><br>Dans le respect des bonnes pratiques actuelles en matière de sécurité et de confidentialité, gardez à l&#39;esprit les risques juridiques et de sécurité potentiels associés au stockage de la date de naissance complète du client (mois, jour, année) avec d&#39;autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clientes et clients et de suggérer d’utiliser leur année de naissance comme alternative. |
| **[!UICONTROL Tax / VAT Number]** | Le numéro de TVA du client, le cas échéant. |
| **[!UICONTROL Gender]** | Identifie le genre du client. Le genre est inclus si spécifié dans le [configuration](../configuration-reference/customers/customer-configuration.md). Options : `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Si vous disposez de plusieurs vues de magasin, ce paramètre identifie la vue de magasin à partir de laquelle le message de bienvenue est envoyé. Si les vues du magasin sont utilisées pour différentes langues, ce paramètre détermine la langue de l’e-mail de bienvenue. |

### [!UICONTROL Addresses]

| Champ | Description |
|--- |--- |
| **[!UICONTROL New Addresses]** | Identifie le type de nouvelle adresse. Options : `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Affiche une autre section Nouvelle adresse pour identifier le type d’adresse à saisir. |
| **[!UICONTROL Company]** | Nom de la société, le cas échéant, pour cette adresse. |
| **[!UICONTROL Street Address]** | Adresse postale du client. Une deuxième ligne de l’adresse postale est disponible si elle est spécifiée dans le champ [configuration](../configuration-reference/customers/customer-configuration.md) rubrique. |
| **[!UICONTROL City]** | Ville où se trouve l’adresse du client. |
| **[!UICONTROL Country]** | Pays dans lequel se trouve l’adresse du client. |
| **[!UICONTROL State/Province]** | État ou province où se trouve l’adresse du client. |
| **[!UICONTROL Zip/Postal Code]** | Code postal de l’adresse du client. |
| **[!UICONTROL Phone Number]** | Numéro de téléphone du client associé à l’adresse. |
| **[!UICONTROL VAT Number]** | Le cas échéant, numéro de taxe sur la valeur ajoutée qui s&#39;applique au client à cette adresse. |
