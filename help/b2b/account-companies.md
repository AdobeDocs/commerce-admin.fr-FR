---
title: Comptes d’entreprise
description: Découvrez comment les comptes d’entreprise gérés dans votre boutique Adobe Commerce permettent de regrouper plusieurs acheteurs appartenant à la même société en un seul compte d’entreprise.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
TQID: https://experienceleague.adobe.com/gHdiA49ndaE4yFfIPAPaCUOhWnkkZIg2WKfSeSrwBQQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 753
ht-degree: 0%

---

# Comptes d’entreprise

Lorsque vous incorporez des comptes d’entreprise B2B dans votre boutique, vous pouvez simplifier l’expérience d’achat en permettant aux entreprises de créer plusieurs sous-comptes avec des autorisations flexibles basées sur les rôles utilisateur dans leur organisation.

Selon l&#39;entreprise, un administrateur de magasin peut ajuster les promotions et les prix en fonction de ses besoins et créer des offres hautement personnalisées qui répondent aux demandes des acheteurs et augmentent les commandes.

L&#39;ajout d&#39;une association de comptes de société à un [individu](../customers/account-create.md) standard permet au client d&#39;utiliser les workflows d&#39;achat spécifiques définis pour la société.

Avantages d&#39;un compte d&#39;entreprise :

- Offre un nombre illimité [utilisateurs de l’entreprise](account-company-users.md) et la création de comptes supplémentaires, ce qui simplifie les achats de l’entreprise.

- Inclut la prise en charge d’une hiérarchie de comptes d’entreprise _intelligente_ avec différents [rôles et autorisations](account-company-roles-permissions.md) pour passer des commandes.

- Fournit un mécanisme permettant aux commerçants d&#39;augmenter leurs revenus en offrant [crédit de magasin de l&#39;entreprise](credit-company.md) comme mode de paiement.

- Prend en charge la [gestion](account-company-manage.md) de tous les comptes de société de l’administrateur.

## Afficher les comptes société

La grille _Entreprises_ répertorie tous les comptes d’entreprise actifs et les demandes en attente, quel que soit le paramètre de statut. Il fournit également les outils nécessaires à la [création](account-company-create.md) et [gestion](account-company-manage.md) des comptes d’entreprise. Utilisez les commandes de grille standard pour filtrer la liste et ajuster la disposition des colonnes. Pour obtenir une liste des descriptions des colonnes, reportez-vous à la section _Descriptions des colonnes_ dans [Gestion des comptes d’entreprise](account-company-manage.md).

Les clients peuvent créer un compte d’entreprise à partir du storefront ou un commerçant peut en créer un à partir de l’administrateur. Par défaut, la possibilité de créer des comptes d’entreprise à partir du storefront est activée. Si la configuration le permet, un visiteur du magasin peut demander l’ouverture d’un compte d’entreprise. Une fois le compte d’entreprise approuvé, l’administrateur de l’entreprise peut configurer la structure de l’entreprise et les utilisateurs avec différents niveaux d’autorisation.

Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grille des sociétés](./assets/companies-grid.png){width="700" zoomable="yes"}

La grille [!UICONTROL Companies] répertorie toutes les sociétés, quel que soit leur statut. La liste des sociétés indique si une société est associée à une [hiérarchie de société](manage-company-hierarchy.md) et fournit des [informations détaillées](/help/b2b/account-company-manage.md#company-options-and-columns) sur la société, l&#39;administrateur de la société et d&#39;autres informations. Personnalisez l’affichage à l’aide des contrôles de grille d’administration [Admin](../getting-started/admin-grid-controls.md) pour définir des filtres, des options d’affichage des colonnes, etc.

## Administrateur d’entreprise

L’exemple suivant illustre la grille _Clients_ avec les comptes d’administration initiaux de la société.

![Grille des clients avec compte d’administrateur d’entreprise](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Chaque société a un seul administrateur d’entreprise identifié par l’adresse e-mail du compte et le prénom et le nom de l’administrateur. L’administrateur peut être affecté à d’autres sociétés en tant qu’utilisateur, mais il ne peut être administrateur que d’une seule société.

Après avoir créé le compte, l’administrateur ou l’administratrice d’entreprise définit la structure de l’entreprise [équipes](account-company-structure.md), configure les [utilisateurs de l’entreprise](account-company-users.md) et établit les [rôles et autorisations](account-company-roles-permissions.md) pour chacun.

### Définir le mot de passe de l&#39;administrateur d&#39;entreprise avant la première connexion

1. L’administrateur de la société trouve un e-mail de bienvenue dans le magasin .

   ![Exemple de courrier électronique de bienvenue](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Les adresses e-mail cibles et le contenu de l’e-mail sont déterminés par les options spécifiées dans la configuration [options d’e-mail de la société](email-company-configuration.md).

1. Suit les instructions et clique sur [!UICONTROL **lien**] pour définir son mot de passe.

1. Saisit un [!UICONTROL **Nouveau mot de passe**] et une confirmation de mot de passe pour son compte.

   Le mot de passe doit comporter au moins trois des types de caractères suivants :

   - Caractères minuscules (abc...)
   - Caractères en majuscules (ABC...)
   - Nombres (1234567890)
   - Caractères spéciaux (!@#$...)

1. Clique sur [!UICONTROL **Définir un nouveau mot de passe**].

   ![Connexion client - administrateur de la société](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Lorsque la page de [!UICONTROL Customer Login] s’affiche, le client saisit ses [!UICONTROL **E-mail**] et [!UICONTROL **Mot de passe**].

1. Clique sur [!UICONTROL **Se connecter**] pour accéder au tableau de bord de son compte.

   ![Tableau de bord du compte - Société](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Structure de l&#39;entreprise

Un compte d’entreprise peut être configuré pour refléter la structure de l’entreprise. Au départ, la structure de l’entreprise comprend uniquement l’administrateur ou l’administratrice de l’entreprise, mais peut être étendue pour inclure des équipes d’utilisateurs et utilisatrices. Les utilisateurs peuvent être associés à des équipes ou organisés dans une hiérarchie de divisions et de subdivisions au sein de la société. La structure est conçue pour prendre en charge l’utilisation de [&#x200B; règles d’approbation &#x200B;](account-dashboard-approval-rules.md) pour les [&#x200B; commandes fournisseur &#x200B;](purchase-order-flow.md) associées au compte de la société.

![Structure d’entreprise avec divisions](./assets/company-structure-diagram.svg){width="450"}

Dans le tableau de bord du compte de l&#39;administrateur de la société, la structure de la société est représentée sous la forme d&#39;une arborescence et n&#39;est initialement constituée que de l&#39;administrateur de la société.

![Structure de l’entreprise avec l’administrateur d’entreprise](./assets/company-structure-tree-admin.png){width="600"}

Lors de la création du compte, l’administrateur ou l’administratrice de la société peut utiliser l’adresse e-mail de la société ou se voir attribuer une autre adresse e-mail.

Dans l&#39;exemple suivant, la structure initiale de l&#39;entreprise comprend l&#39;administrateur de l&#39;entreprise et un compte utilisateur individuel au nom de l&#39;administrateur de l&#39;entreprise. Cependant, les fonctions d’administrateur d’entreprise (telles que la structure de l’entreprise et les règles d’approbation) ne sont disponibles que lorsqu’elles sont connectées au compte utilisateur désigné comme administrateur de l’entreprise.

![Structure d’entreprise avec administrateur et compte utilisateur](./assets/company-structure-tree-admin-user.png){width="600"}
