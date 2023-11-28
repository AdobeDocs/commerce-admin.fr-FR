---
title: Comptes d’entreprise
description: Découvrez comment les comptes d’entreprise gérés dans votre boutique Adobe Commerce permettent de rejoindre plusieurs acheteurs appartenant à la même société dans un seul compte d’entreprise.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Comptes d’entreprise

Lorsque vous incorporez des comptes d’entreprise B2B dans votre boutique, vous pouvez simplifier l’expérience d’achat d’entreprise en permettant aux entreprises de créer plusieurs sous-comptes avec des autorisations flexibles en fonction des rôles d’utilisateur dans leur entreprise. Selon l’entreprise, un administrateur de magasin peut ajuster les promotions et les prix en fonction de ses besoins, et créer des offres hautement personnalisées qui répondent aux besoins des acheteurs et augmentent les commandes. Ajout d’une association de compte d’entreprise à une norme [individu](../customers/account-create.md) permet au client d’utiliser les workflows d’achat spécifiques définis pour la société.

Avantages d’un compte d’entreprise :

- Offres illimitées [utilisateurs de l’entreprise](account-company-users.md) et la création de comptes supplémentaires, ce qui simplifie les achats d’entreprise.

- Inclut la prise en charge d’un _smart_ hiérarchie des comptes d’entreprise avec différentes [rôles et autorisations](account-company-roles-permissions.md) pour passer des commandes.

- Fournit un mécanisme pour que les marchands augmentent leurs revenus en proposant [crédit de boutique d’entreprise](credit-company.md) comme mode de paiement.

- Prise en charge de la variable [gestion](account-company-manage.md) de tous les comptes de société dans l’administrateur.

## Affichage des comptes d’entreprise

La variable _Entreprises_ grid répertorie tous les comptes d’entreprise actifs et les demandes en attente, quel que soit le paramètre d’état. Il fournit également des outils pour [création](account-company-create.md) et [gestion](account-company-manage.md) des comptes de société. Utilisez les contrôles de grille standard pour filtrer la liste et ajuster la disposition des colonnes. Pour obtenir la liste des descriptions des colonnes, voir la section _Descriptions des colonnes_ dans [Gestion des comptes d’entreprise](account-company-manage.md).

Les clients peuvent créer un compte d’entreprise à partir du storefront ou un commerçant peut en créer un à partir de l’administrateur. Par défaut, la possibilité de créer des comptes d’entreprise à partir du storefront est activée. S’il est autorisé par la configuration, un visiteur du magasin peut demander l’ouverture d’un compte de société. Une fois le compte de l’entreprise approuvé, l’administrateur de l’entreprise peut configurer la structure de l’entreprise et les utilisateurs avec différents niveaux d’autorisation.

Dans le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grille des entreprises](./assets/companies-grid.png){width="700" zoomable="yes"}

La variable [!UICONTROL Companies] grid répertorie toutes les entreprises, quel que soit leur statut. L&#39;exemple qui s&#39;affiche montre les comptes de deux sociétés : la société &quot;ACME&quot; et la société &quot;Vandelay&quot;.

## Administrateur d’entreprise

L’exemple suivant illustre la variable _Clients_ grille avec les comptes administrateur de la société initiaux.

![Grille des clients avec compte administrateur de l’entreprise](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Il est possible que la personne qui est administrateur de la société ait plusieurs rôles au sein de la société. Si une adresse électronique distincte est saisie pour l’administrateur de l’entreprise, la structure initiale de l’entreprise inclut l’administrateur de l’entreprise ainsi qu’un compte utilisateur individuel au nom de l’administrateur de l’entreprise. Dans ce cas, l’administrateur de l’entreprise peut se connecter au compte en tant qu’entreprise ou utilisateur individuel.

Après la création du compte, l’administrateur de l’entreprise définit la structure de l’entreprise de [équipes](account-company-structure.md), configure le [utilisateurs de l’entreprise](account-company-users.md), et établit [rôles et autorisations](account-company-roles-permissions.md) pour chacun d’eux.

### Définition du mot de passe de l’administrateur de la société avant la première connexion

1. L’administrateur de la société trouve un e-mail de bienvenue dans le magasin.

   ![Exemple de courrier électronique de bienvenue](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Les cibles et le contenu de l’email sont déterminés par les options spécifiées dans la variable [options de messagerie de l’entreprise](email-company-configuration.md) configuration.

1. Suivez les instructions et les clics [!UICONTROL **link**] pour définir leur mot de passe.

1. Entre dans une [!UICONTROL **Nouveau mot de passe**] pour leur compte et pour confirmer.

   Le mot de passe doit contenir au moins trois des types de caractères suivants :

   - Caractères minuscules (abc..)
   - Caractères majuscules (ABC...)
   - Nombres (1234567890)
   - Caractères spéciaux (!@#$...)

1. Clics [!UICONTROL **Définir un nouveau mot de passe**].

   ![Connexion client - administrateur de la société](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Lorsque la variable [!UICONTROL Customer Login] s’affiche, le client entre dans la [!UICONTROL **Email**] et [!UICONTROL **Password**].

1. Clics [!UICONTROL **Se connecter**] pour accéder au tableau de bord de leur compte.

   ![Tableau de bord du compte - société](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Structure de l&#39;entreprise

Un compte d’entreprise peut être configuré pour refléter la structure de l’entreprise. Au départ, la structure de l’entreprise inclut uniquement l’administrateur de l’entreprise, mais peut être développée pour inclure des équipes d’utilisateurs. Les utilisateurs peuvent être associés à des équipes ou organisés au sein d’une hiérarchie de divisions et de subdivisions au sein de l’entreprise. La structure est conçue pour prendre en charge l’utilisation de la fonction [règles de validation](account-dashboard-approval-rules.md) pour [commandes d’achat](purchase-order-flow.md) (PO) associés au compte de la société.

![Structure de l’entreprise avec des divisions](./assets/company-structure-diagram.svg){width="450"}

Dans le tableau de bord du compte de l’administrateur de l’entreprise, la structure de l’entreprise est représentée sous la forme d’une arborescence et se compose initialement uniquement de l’administrateur de l’entreprise.

![Structure de l’entreprise avec l’administrateur de l’entreprise](./assets/company-structure-tree-admin.png){width="600"}

Lors de la création du compte, l’administrateur de l’entreprise peut utiliser l’adresse électronique de l’entreprise ou se voir attribuer une autre adresse électronique.

Dans l’exemple suivant, la structure initiale de l’entreprise inclut l’administrateur de l’entreprise ainsi qu’un compte utilisateur individuel au nom de l’administrateur de l’entreprise. Mais les fonctions d’administrateur de l’entreprise (telles que la structure de l’entreprise et les règles d’approbation) ne sont disponibles que lorsqu’elles sont connectées au compte utilisateur désigné comme administrateur de l’entreprise.

![Structure de l’entreprise avec un compte administrateur et utilisateur](./assets/company-structure-tree-admin-user.png){width="600"}
