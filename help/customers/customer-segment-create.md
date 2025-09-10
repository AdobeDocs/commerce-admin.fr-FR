---
title: Créer et supprimer des segments de clients
description: Les clients peuvent consulter les informations sur le remboursement associées à la commande dans leur tableau de bord de compte client.
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 079aef1f4d90ecba649ac43e7cbab812da79871a
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 1%

---

# Créer et supprimer des segments de clients

{{ee-feature}}

La création d’un segment client est similaire à la création d’une [règle de prix de panier](../merchandising-promotions/price-rules-cart.md), sauf que les options incluent [attributs spécifiques au segment client](../customers/customer-segments.md).

![Liste des segments clients](assets/customer-segments.png){width="700" zoomable="yes"}

_&#x200B;**[!UICONTROL Customer Segments]une grille &#x200B;** _

| Colonne | Description |
|--- |--- |
| **[!UICONTROL ID]** | Identifiant unique du segment client. |
| **[!UICONTROL Segment]** | Nom du segment client. |
| **[!UICONTROL Status]** | Indique si le segment client est _[!UICONTROL Active]_&#x200B;ou&#x200B;_[!UICONTROL Inactive]_. |
| **[!UICONTROL Website]** | Indique le site web auquel appartient le segment client. |

{style="table-layout:auto"}

## Prérequis : activer les segments de clients

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Customer Segments]** .

1. Vérifiez que **[!UICONTROL Enable Customer Segment Functionality]** est défini sur `Yes`.

   ![Configuration des clients - segments de clients](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. (Facultatif) Pour désactiver la validation en temps réel des segments clients, définissez **[!UICONTROL Real-time Check if Customer is Matched by Segment]** sur `No`.

   Lorsque vous désactivez la validation en temps réel, les segments de clients sont validés par une requête SQL à condition combinée unique. La désactivation de cette fonction améliore les performances de validation des segments en présence d’un grand nombre de segments client dans le système. Cependant, la validation ne fonctionne pas avec une base de données fractionnée ou en l’absence de clients enregistrés.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Création d’un segment

Les étapes suivantes utilisent un exemple de création d’un segment client qui cible les clientes de Los Angeles.

### Étape 1 : ajouter un segment client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Segment]**.

1. Saisissez un **[!UICONTROL Segment Name]** qui identifie le segment client lors de l’utilisation dans l’Administration.

1. Saisissez un bref **[!UICONTROL Description]** qui explique l’objectif du segment.

1. Définissez **[!UICONTROL Assigned to Website]** sur le site web où le segment client peut être utilisé.

1. Définissez le **[!UICONTROL Status]** sur _Actif_ ou _Inactif_.

1. Pour identifier les types de clients que vous souhaitez utiliser pour appliquer le segment, définissez **[!UICONTROL Apply to]** sur l’un des types de clients suivants :

   - `Visitors and Registered Customers` - Inclut tous les acheteurs, qu’ils soient connectés ou non à un compte.
   - `Registered Customers` - Inclut uniquement les acheteurs connectés à un compte.
   - `Visitors` - Inclut uniquement les acheteurs qui ne sont pas connectés à un compte.

   >[!TIP]
   >
   >Si vous créez un segment en fonction des attributs du client stockés dans un compte client, il est recommandé d’appliquer le segment uniquement aux clients enregistrés.

   >[!NOTE]
   >
   > Si un segment s’applique à `Visitors and Registered Customers`, le [!UICONTROL Matched Customers] affiche uniquement les `Registered Customers`. C’est le cas même si les visiteurs peuvent être ciblés selon les conditions qui leur sont applicables. Pour les segments `Visitors` uniquement, aucun onglet `Matched Customers` n’est affiché.


1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

   Une fois le segment _[!UICONTROL General Properties]_&#x200B;enregistré, d’autres options sont disponibles dans le panneau de gauche.

   ![Propriétés du segment](assets/customer-segment-saved.png){width="600" zoomable="yes"}

**_[!UICONTROL General Properties]_**

| Champ | Description |
|--- |---|
| **[!UICONTROL Segment Name]** | Nom qui identifie le segment à des fins de référence interne. |
| **[!UICONTROL Description]** | Brève description qui explique l’objectif du segment à des fins de référence interne. |
| **[!UICONTROL Assigned to Website]** | Site web unique sur lequel le segment peut être utilisé. |
| **[!UICONTROL Status]** | Active et désactive le segment. Toutes les règles de prix et bannières associées sont désactivées lorsque le segment est désactivé. Options : `Active` / `Inactive` |
| **[!UICONTROL Apply to]** | Définit les types de clients auxquels le segment est appliqué. La sélection influence l’ensemble des conditions disponibles pour la création du segment. Le paramètre ne peut pas être modifié une fois le segment enregistré. |

{style="table-layout:auto"}

### Etape 2 : définition des conditions

>[!NOTE]
>
> Pour les visiteurs, seules les conditions suivantes s’appliquent : Conditions du panier (montant du sous-total du panier, articles du panier et quantité de produits du panier), Règles de produit (produits figurant dans le panier et l’historique des produits) et combinaisons de ces articles. Si un segment doit s’appliquer à la fois aux visiteurs et aux clients enregistrés, les visiteurs sont suivis uniquement sur la base des conditions répertoriées.

Les conditions possibles sont organisées dans les groupes suivants :

| Groupe | Description |
|--- |--- |
| **[!UICONTROL Customer]** | Conditions basées sur les attributs du compte client. Disponible uniquement si le segment s’applique aux clients enregistrés. |
| **[!UICONTROL Shopping Cart]** | Conditions basées sur le contenu du panier. Ces conditions sont disponibles pour tous les types de segment. |
| **[!UICONTROL Products]** | Conditions basées sur les produits du panier ou l’historique de navigation des produits. Ces conditions sont disponibles pour tous les types de segment. |
| **[!UICONTROL **Sales]** | Conditions basées sur les commandes terminées. Disponible uniquement si le segment s’applique aux clients enregistrés. |

1. Dans le volet de gauche, cliquez sur **[!UICONTROL Conditions]**.

   La condition par défaut commence par _[!UICONTROL If ALL of these conditions are TRUE:]_&#x200B;sur la page.

   ![Conditions ](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. Créez une condition qui cible les clientes :

   - Cliquez sur l&#39;icône **[!UICONTROL Add]** pour afficher la liste des conditions et sélectionnez `Gender`.

   - Laissez l’option de contrôle de condition **is** par défaut.

   - Cliquez sur **...** et sélectionnez `female`.

   ![Ligne de condition 1](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. Créez une autre condition qui cible les habitants de Los Angeles :

   - Sur la ligne suivante, cliquez sur l’icône **[!UICONTROL Add]** et sélectionnez `Customer Address`.

     Cette action crée une condition parent dans laquelle vous pouvez définir un ou plusieurs champs d’adresse à faire correspondre.

   - Cliquez sur l&#39;icône **[!UICONTROL Add]** pour afficher la liste des champs de l&#39;adresse et sélectionnez `City`.

   - Cliquez sur **is** pour afficher les options de contrôle des conditions et sélectionnez `contains`.

   - Cliquez sur **...** et saisissez `Los Angeles`.

   - Sur la ligne suivante, cliquez sur l’icône **[!UICONTROL Add]** et sélectionnez `State/Province`.

   - Laissez l’option de contrôle de condition **is** par défaut.

   - Cliquez sur **...** et sélectionnez `United States > California`.

   ![Conditions pour les femmes à Los Angeles, California](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

### Étape 3 : vérifier la liste des clients correspondants

1. Dans le volet de gauche, cliquez sur **[!UICONTROL Matched Customers]** pour afficher tous les clients qui correspondent à la condition.

   ![Clients correspondants](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. Si la liste des clients atteint votre objectif, cliquez sur **[!UICONTROL Save]** pour terminer le segment de clients.

1. Le segment client peut désormais être utilisé pour le ciblage des promotions, du contenu et du publipostage.

_&#x200B;**[!UICONTROL Matched Customers]une grille &#x200B;** _

| Colonne | Description |
|--- |--- |
| **[!UICONTROL ID]** | ID de client d’un client enregistré. |
| **[!UICONTROL Name]** | Nom d’un client enregistré. |
| **[!UICONTROL Email]** | Adresse e-mail d’un client enregistré. |
| **[!UICONTROL Group]** | Groupe de clients auquel le client est affecté. |
| **[!UICONTROL Phone]** | Numéro de téléphone du client. |
| **[!UICONTROL ZIP]** | Code postal du client. |
| **[!UICONTROL Country]** | Pays dans lequel le client est situé. |
| **[!UICONTROL State / Province]** | État ou province où se trouve le client. |
| **[!UICONTROL Customer Since]** | Date et heure de création du compte client. |

{style="table-layout:auto"}

## Supprimer un segment client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Recherchez le segment à supprimer et sélectionnez-le.

1. Dans la barre de menus, cliquez sur **[!UICONTROL Delete]** bouton.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Retourne à la page _[!UICONTROL Customer Segments]_&#x200B;sans enregistrer les modifications. |
| **[!UICONTROL Delete]** | Supprime le segment client actuel. Les clients ou les commandes terminées associés au client dans le segment ne sont pas supprimés. |
| **[!UICONTROL Reset]** | Réinitialise toutes les modifications non enregistrées dans le formulaire de segment client à leurs valeurs précédentes. |
| **[!UICONTROL Refresh Segment Data]** | Actualise les données de segment aux valeurs les plus récemment enregistrées. Pertinent si des données de segment sont indisponibles ou obsolètes. |
| **[!UICONTROL Save and Continue Edit]** | Enregistre les modifications et maintient le segment client ouvert. |
| **[!UICONTROL Save]** | Enregistre les modifications et ferme le segment client. |

{style="table-layout:auto"}

## Démonstration des segments client

Regardez cette vidéo pour une démonstration de la création de segments de clients :

>[!VIDEO](https://video.tv.adobe.com/v/3410189/?quality=12&learn=on&captions=fre_fr)
