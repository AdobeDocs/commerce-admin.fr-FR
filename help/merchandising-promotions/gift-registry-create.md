---
title: Configuration du registre des cadeaux
description: Découvrez comment configurer des types de registre de cadeaux pour vos clients de magasin.
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Configuration du registre des cadeaux

{{ee-feature}}

Un registre des cadeaux peut être créé pour tout type d’événement, tel qu’un mariage, un anniversaire, un anniversaire, un nouveau bébé ou toute autre occasion spéciale. Par défaut, Adobe Commerce inclut les événements spéciaux suivants :

- Bébé
- Anniversaire
- Mariage

Lorsque vous créez un registre, il devient une option dans la liste des types de registre des cadeaux du compte du client.

Vous pouvez utiliser l’un des trois registres de cadeaux préparés ou créer votre propre registre personnalisé. Chaque type de registre des cadeaux comprend plusieurs attributs, qui sont les champs de saisie de données qu’un client remplit pour créer un registre des cadeaux. Les attributs fournissent des informations supplémentaires sur l’événement, l’heure et l’emplacement, ou toute autre information nécessaire. Selon le type d’entrée, certains attributs disposent de plusieurs options. Par exemple, le type de registre des cadeaux `Wedding` a l’attribut `Role`, avec les options `Bride`, `Groom` et `Partner`. Pour en savoir plus sur les attributs et les types d’entrée, voir [Attributs](../customers/attribute-properties.md).

![Types de registre des cadeaux](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## Utiliser une liste de cadeaux préparée

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   Les registres d&#39;anniversaire, de mariage et de naissance sont prêts à être utilisés par les clients à partir de leurs comptes.

1. Veillez à terminer la [configuration de modèle d&#39;email](../systems/email-templates.md#configure-email-templates) afin qu&#39;elles reflètent votre marque.

## Créer un registre des cadeaux personnalisé

1. Dans la barre latérale Admin, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Gift Registry Type]**.

1. Sous **[!UICONTROL General Information]**, procédez comme suit :

   - Saisissez un **[!UICONTROL Code]** unique pour identifier le registre des cadeaux en interne.

     Le code doit commencer par une lettre minuscule. Le reste du code peut être n’importe quelle combinaison de lettres minuscules (a-z), de nombres (0-9) et de traits de soulignement (`_`).

   - Pour **[!UICONTROL Label]**, saisissez un nom pour le registre des cadeaux tel que vous souhaitez le voir apparaître dans le magasin.

     Cette étiquette est une option de la liste des types de registre des cadeaux disponibles pour le client.

   - Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel ce registre des cadeaux s’affiche lorsqu’il est répertorié avec d’autres types.

   - Pour activer le registre des cadeaux, définissez **[!UICONTROL Is Listed]** sur `Yes`.

     ![Registre cadeau - informations générales](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. Examinez chaque section du registre des cadeaux pour déterminer le type d’informations à inclure.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Attributes]** et cliquez sur **[!UICONTROL Add Attribute]**.

   ![Registre cadeau - nouvel attribut](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. Pour chaque attribut, procédez comme suit :

   - Attribuez un **[!UICONTROL Code]** unique pour identifier l’attribut en interne. Le code peut contenir jusqu’à 15 caractères et doit commencer par une lettre minuscule. Le reste du code peut inclure des lettres minuscules (`a`-`z`), des nombres (`0`-`9`) et le caractère de soulignement (`_`) pour séparer les mots.

   - Sélectionnez le **[!UICONTROL Input Type]** à utiliser pour la saisie des données. Vous pouvez utiliser un type personnalisé ou statique.

   - Si le type d’entrée comporte plusieurs options, cliquez sur **[!UICONTROL Add New Option]** et renseignez les informations de chaque option.

     Certains types de saisie possèdent des propriétés supplémentaires. Par exemple, l’ emplacement de l’événement comporte des propriétés supplémentaires pour rendre l’événement consultable et inclus dans la liste publique des registres de cadeaux de votre boutique.

      - Définissez **[!UICONTROL Attribute Group]** sur la section du registre des cadeaux où vous souhaitez que l’attribut apparaisse.

      - Pour **[!UICONTROL Label]**, saisissez un nom pour identifier le champ de saisie de données dans le registre.

      - Si le client doit effectuer une sélection ou saisir une valeur dans le champ, définissez **[!UICONTROL Is Required]** sur `Yes`.

      - Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel ce registre des cadeaux s’affiche lorsqu’il est répertorié avec d’autres registres de cadeaux qui peuvent être disponibles dans le magasin.

1. Pour ajouter une autre option, cliquez sur **Ajouter une nouvelle option**.

   Chaque nouvelle option ajoutée apparaît dans une nouvelle section dans la partie supérieure. Répétez cette procédure pour le nouvel attribut .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Descriptions des champs

### [!UICONTROL General Information]

| Champ | Description |
|--- |--- |
| [!UICONTROL Code] | Nom unique permettant d’identifier le type de registre des cadeaux en interne. Le premier caractère du code doit être une lettre minuscule. Le reste du code peut être n’importe quelle combinaison de lettres minuscules (a-z), de nombres (0-9) et de caractères de soulignement (`_`). |
| [!UICONTROL Label] | Nom du type de registre des cadeaux qui apparaît dans le magasin. |
| [!UICONTROL Sort Order] | Détermine la séquence dans laquelle ce type de registre des cadeaux s’affiche lorsqu’il est répertorié avec d’autres types. |
| [!UICONTROL Is Listed] | Détermine si le type de registre des cadeaux est disponible pour les clients du magasin. Options : `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| Champ | Description |
|--- |--- |
| [!UICONTROL Code] | Nom unique permettant d’identifier l’attribut en interne. Le code peut inclure toute combinaison de lettres minuscules (a-z), de nombres (0-9) et de caractères de soulignement (`_`). |
| [!UICONTROL Input Type] | Détermine le type de données et le contrôle d’entrée associés à l’attribut, selon le type. |
| [!UICONTROL Attribute Group] | Sélectionnez le groupe dans lequel l’attribut est répertorié dans le registre des cadeaux. |
| [!UICONTROL Label] | Nom qui identifie l’attribut dans le tableau de bord du compte du client. |
| [!UICONTROL Is Required] | Indique si l’attribut est une entrée obligatoire. Le registre des cadeaux ne peut pas être enregistré tant que tous les attributs requis ne sont pas terminés. Options : `Yes` / `No`. |
| [!UICONTROL Sort Order] | Détermine la séquence dans laquelle l’attribut apparaît lorsqu’il est répertorié avec d’autres attributs. |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

Sélectionnez le type de données et le contrôle d’entrée associés à l’attribut.

**_[!UICONTROL Custom Types]_**

| Champ | Description |
|--- |--- |
| [!UICONTROL Text] | Affiche l’attribut sous forme de champ de texte. |
| [!UICONTROL Select] | Affiche l’attribut sous la forme d’une liste déroulante. Cliquez sur **[!UICONTROL Add New Option]** pour ajouter d’autres conditions à la liste déroulante :<br/>**[!UICONTROL Code]**- Nom unique permettant d’identifier l’attribut en interne.<br/>**[!UICONTROL Label]** - Nom qui identifie l’attribut dans le tableau de bord du compte du client.<br/>**[!UICONTROL Is Default]**- Définissez ce commutateur pour sélectionner la condition par défaut.<br/>**[!UICONTROL Delete Option]** - Cliquez pour supprimer l’option. |
| [!UICONTROL Date] | Affiche l’attribut sous forme de champ de date. Options : `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | Affiche l’attribut sous la forme d’une liste déroulante de pays. Définissez **[!UICONTROL Show Region]** sur : `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| Champ | Description |
|--- |--- |
| [!UICONTROL Event Date] | Détermine la manière dont l’attribut date est utilisé dans le magasin. Options : <br/>**[!UICONTROL Searchable]**- Détermine si l’attribut est disponible pour la recherche avancée. Options : `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Détermine si l’événement est inclus dans la liste des événements disponibles dans le magasin. Options : `Yes` / `No`. <br/>**[!UICONTROL Date Format]**- Détermine le format de la date de l’événement. Options : `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | Affiche l’attribut sous la forme d’une liste de pays. Options : <br/>**[!UICONTROL Searchable]**- Détermine si l’attribut est disponible pour la recherche avancée. Options : `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - Détermine si l’événement est inclus dans la liste des événements disponibles dans le magasin. Options : `Yes` / `No`. <br/>**[!UICONTROL Show Region]**- Détermine la région de l’événement. |
| [!UICONTROL Event Location] | Emplacement de l’événement lié au registre des cadeaux. <br/> Définissez **[!UICONTROL Is Searcheable]** sur : `Yes` / `No` <br/> **[!UICONTROL Is Listed]** sur : `Yes` / `No` |
| [!UICONTROL Role] | Le rôle qui identifie le destinataire du cadeau. Par exemple, `Bride`, `Groom` ou `Partner`.<br/>**[!UICONTROL Is Searcheable]**- Défini sur `Yes`/ `No`<br/>** Est répertorié&#x200B;**- Défini sur `Yes` / `No`<br/>**[!UICONTROL Add New Option]** - Cliquez pour ajouter d’autres conditions au menu déroulant :<br/>**Code** - Un nom unique pour identifier l’attribut en interne.<br/>**[!UICONTROL Label]**- Nom qui identifie l’attribut dans le tableau de bord du compte du client.<br/>**[!UICONTROL Is Default]** - Définissez ce commutateur pour sélectionner la condition par défaut.<br/>**[!UICONTROL Delete Option]**- Cliquez pour supprimer l’option. |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

Sélectionnez le groupe dans lequel l’attribut est répertorié dans le registre des cadeaux.

| Champ | Description |
|--- |--- |
| [!UICONTROL Event Information] | Groupe tous les attributs du registre des cadeaux qui ajoutent des informations sur l’événement du registre des cadeaux, son heure, son lieu, etc. |
| [!UICONTROL Gift Registry Properties] | Combine tous les attributs qui ajoutent des informations directement sur le registre des cadeaux. |
| [!UICONTROL Privacy Settings] | Répertorie les attributs qui ajoutent des informations sur la confidentialité des événements du registre des cadeaux. |
| [!UICONTROL Recipients Information] | Groupe les attributs qui fournissent des informations sur la personne qui crée un registre des cadeaux. |
| [!UICONTROL Shipping Address] | Combine les attributs qui ajoutent des informations sur l’adresse d’expédition de l’événement de registre des cadeaux. |

{style="table-layout:auto"}
