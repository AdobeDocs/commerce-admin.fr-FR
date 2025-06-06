---
title: Propriétés d’attribut du client
description: Découvrez comment configurer les propriétés d’attributs du client.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# Propriétés d’attribut du client

{{ee-feature}}

Les attributs du client fournissent les informations nécessaires à la prise en charge des processus de gestion des commandes, de l’exécution et des clients. Étant donné que votre entreprise est unique, il se peut que vous ayez besoin de champs en plus des éléments par défaut fournis par le système. Vous pouvez ajouter des attributs personnalisés aux sections Informations du compte, Carnet d’adresses et Informations de facturation du compte du client. Les [attributs d&#39;adresse](address-attributes.md) du client peuvent également être utilisés dans la section _Informations de facturation_ lors de l&#39;extraction ou lorsque les invités s&#39;inscrivent à un compte.

![Attributs du client](./assets/attributes-customer.png){width="700" zoomable="yes"}

## Étape 1 : Propriétés de l’attribut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Propriétés d’attribut du client](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. Dans la section **[!UICONTROL Attribute Properties]** , procédez comme suit :

   - Saisissez un **[!UICONTROL Default Label]** qui identifie l’attribut lors de la saisie des données.

   - Saisissez un **[!UICONTROL Attribute Code]** qui identifie l’attribut dans le système.

   Le code d’attribut doit commencer par une lettre et peut inclure toute combinaison de lettres minuscules (a-z) et de nombres (0-9). Le code doit comporter moins de 30 caractères et ne peut pas contenir de caractères spéciaux ni d’espaces. Le caractère de soulignement (`_`) peut être utilisé pour indiquer un espace.

   >[!TIP]
   >
   >**Raccourci :** Pour remplir uniquement les champs requis, faites défiler l’écran jusqu’à _[!UICONTROL Storefront Properties]_, saisissez le&#x200B;_[!UICONTROL Sort Order]_ et enregistrez.

1. Renseignez les propriétés de saisie des données :

   - Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Input Type]** sur l’un des paramètres suivants :

     | Type | Description |
     |----|-----------|
     | `Text Field` | Champ de texte d’une seule ligne. |
     | `Text Area` | Champ de saisie multi-lignes permettant de saisir des paragraphes de texte, comme une description de produit. Vous pouvez utiliser l’éditeur WYSIWYG pour mettre en forme le texte avec des balises d’HTML ou saisir les balises directement dans le texte. |
     | `Multiple Line` | Crée plusieurs lignes de texte pour l’attribut, comme une adresse de rue multi-lignes. Le nombre de lignes de saisie de données distinctes peut être compris entre 2 et 20. Utilisez le `Default Value` pour spécifier la valeur initiale du champ. |
     | `Date` | Affiche une valeur de date dans le format de date et le fuseau horaire de votre choix. Les valeurs de date peuvent être sélectionnées à partir d’une liste ou d’un calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ). <br/><br/>**_Remarque :_**&#x200B;Selon la configuration de votre système, les utilisateurs de_Admin _peuvent saisir des dates directement dans un champ ou sélectionner une date dans le calendrier ou la liste. Pour plus d&#39;informations sur la spécification des valeurs de date et d&#39;heure, voir [Options de date et d&#39;heure](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | Affiche une liste déroulante avec des options prédéfinies `Yes` et `No`. |
     | `Dropdown` | Affiche une liste déroulante de valeurs qui n’acceptent qu’une seule sélection. Le type d’entrée Liste déroulante est un composant clé de [produits configurables](../catalog/product-create-configurable.md). |
     | `Multiple Select` | Liste déroulante qui accepte plusieurs valeurs à sélectionner. |
     | `File (attachment)` | Champ qui permet de charger un fichier et de l’associer à l’attribut du client en tant que pièce jointe. |
     | `Image File` | Champ qui permet de charger une image dans la galerie et de l’associer à l’attribut du client. |

   - Si le client doit saisir une valeur dans le champ, définissez **[!UICONTROL Values Required]** sur `Yes`.

   - Pour attribuer une valeur initiale au champ, saisissez une valeur **[!UICONTROL Default Value]**.

   - Pour vérifier la précision des données saisies dans le champ avant l’enregistrement, définissez **[!UICONTROL Input Validation]** sur le type de données à autoriser dans le champ. Les valeurs disponibles dépendent du [!UICONTROL Input Type] spécifié.

     | Valeur | Description |
     |-----|-----------|
     | `None` | Le champ n’a aucune validation d’entrée lors de la saisie des données. |
     | `Alphanumeric` | Accepte toute combinaison de nombres (0-9) et de caractères alphabétiques (a-z, A-Z) lors de la saisie des données. Pour inclure des caractères spéciaux, reportez-vous à la section _Escape HTML Entities_. |
     | `Alphanumeric with Space` | Accepte toute combinaison de nombres (0-9), de caractères alphabétiques (a-z, A-Z) et d’espaces lors de la saisie des données. |
     | `Numeric Only` | Accepte uniquement les nombres (0 à 9) lors de la saisie des données. |
     | `Alpha Only` | Accepte uniquement les caractères alphabétiques (a-z, A-Z) lors de la saisie des données. |
     | `URL` | Accepte uniquement une URL lors de la saisie des données. |
     | `Email` | Accepte uniquement une adresse électronique lors de la saisie des données. |
     | `Length Only` | Valide l&#39;entrée en fonction de la longueur des données saisies dans le champ. |

   - Pour limiter la taille des types d’entrée Champ de texte et Zone de texte, saisissez les valeurs **[!UICONTROL Minimum Text Length]** et **[!UICONTROL Maximum Text Length]**.

   - Pour appliquer un filtre de prétraitement aux valeurs saisies dans un champ de texte, une zone de texte ou un type d’entrée multi-lignes, définissez **[!UICONTROL Input/Output Filter]** sur l’une des options suivantes :

     | Valeur | Description |
     |-----|-----------|
     | `None` | N’applique pas de filtre au texte saisi dans le champ. |
     | `Strip HTML Tags` | Supprime les balises HTMLS du texte. Ce filtre peut aider à nettoyer les données collées dans un champ à partir d’une autre source qui inclut des balises d’HTML. |
     | `Escape  HTML Entities` | Convertit les caractères spéciaux trouvés dans le texte en séquence d’échappement d’HTML valide, telle que `&;`. Les séquences d’échappement sont entourées d’une esperluette et d’un point-virgule. Elles sont fréquemment utilisées pour les guillemets intelligents du typographe, les symboles de copyright et de marque. Les séquences d’échappement sont également utilisées pour identifier des caractères tels que les symboles inférieur à (`<`) et supérieur à (`>`), ainsi que le caractère d’esperluette également utilisés dans le code. Ce filtre peut aider à nettoyer les caractères spéciaux qui sont parfois collés dans des champs de base de données à partir de programmes de traitement de texte. |

1. Renseignez les propriétés de grille et de segment du client :

   - Pour pouvoir inclure la colonne dans la grille Clients, définissez **[!UICONTROL Add to Column Options]** sur `Yes`.

   - Pour filtrer la grille Clients selon cet attribut, définissez **[!UICONTROL Use in Filter Options]** sur `Yes`.

   - Pour filtrer la grille Clients par attribut de texte avec différentes conditions de correspondance de filtre, définissez **[!UICONTROL Grid Filter Condition Type]** sur `Partial Match`, `Prefix Match` ou `Full Match`. Cela n’a aucune incidence sur le champ _Rechercher par mot-clé_ pour la grille.

   - Pour rechercher la grille Clients en fonction de cet attribut, définissez **[!UICONTROL Use in Search Options]** sur `Yes`.

   - Pour rendre cet attribut disponible pour les [segments client](customer-segments.md), définissez **[!UICONTROL Use in Customer Segment]** sur `Yes`.

## Étape 2 : propriétés du storefront

1. Faites défiler l’écran jusqu’à la section **[!UICONTROL Storefront Properties]**.

   ![ Attributs du client - propriétés storefront](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. Pour rendre l’attribut visible aux clients, définissez **[!UICONTROL Show on Storefront]** sur `Yes`.

1. Entrez un nombre dans le champ **[!UICONTROL Sort Order]**, qui détermine son ordre d’apparition lorsqu’il est répertorié avec d’autres attributs.

1. Définissez **[!UICONTROL Forms to Use]** sur chaque formulaire devant inclure l’attribut . Pour sélectionner plusieurs options, maintenez la touche Ctrl enfoncée et cliquez sur chaque formulaire.

   - [&quot;Enregistrement de client&quot;](customer-sign-in.md)
   - [&quot;Modification du compte client&quot;](account-create.md)
   - [&quot;Achat d’administrateur&quot;](../stores-purchase/checkout-process.md)

## Etape 3 : renseigner le libellé et enregistrer

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels/Options]**.

1. Sous **[!UICONTROL Manage Titles]**, saisissez un libellé pour identifier l’attribut pour chaque [vue de magasin](../getting-started/websites-stores-views.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.

   ![ Attributs du client - étiquettes/options](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## Descriptions des champs

### [!UICONTROL Attribute Properties]

| Champ | Description |
|--- |--- |
| [!UICONTROL Default Label] | Libellé par défaut qui identifie l’attribut dans l’Admin et le storefront. |
| [!UICONTROL Attribute Code] | Code unique qui identifie l’attribut dans le système. Le code peut contenir jusqu’à 60 caractères et ne peut pas contenir d’espaces ni de caractères spéciaux. Le caractère de soulignement peut être utilisé à la place d’un espace. |
| [!UICONTROL Input Type] | Détermine le contrôle d’entrée utilisé pour la saisie de données. Options : <br/>**`Text Field`**- Champ de texte d’une seule ligne.<br/>**`Text Area`** - Zone de texte multiligne. <br/>**`Multiple Line`**- Crée plusieurs lignes de texte pour l’attribut, comme une adresse de rue multi-lignes. Le nombre de lignes de saisie de données distinctes peut être compris entre 2 et 20.<br/>**`Date`** - Affiche un champ de date avec un calendrier contextuel.<br/>**`Dropdown`**- Liste déroulante qui accepte une seule valeur à sélectionner.<br/>**`Multiple Select`** - Liste déroulante qui accepte plusieurs valeurs à sélectionner. <br/>**`Yes/No`**- Champ qui ne propose que le choix des valeurs `Yes` ou `No`.<br/>**`File (attachment)`** - Champ qui permet de charger un fichier et de l’associer à l’attribut du client en tant que pièce jointe. <br/>**`Image File`**- Champ qui permet de charger une image dans la galerie et de l’associer à l’attribut du client. |
| [!UICONTROL Values Required] | Détermine si une valeur doit être saisie dans le champ. Options : `Yes` / `No` |
| [!UICONTROL Default Value] | Indique la valeur initiale de l’attribut. |
| [!UICONTROL Input Validation] | La sélection des options est déterminée par le type d’entrée. Options : <br/>**`None`**- Le champ n’a aucune validation d’entrée lors de la saisie des données.<br/>**`Alphanumeric`** - Accepte toute combinaison de nombres (0-9) et de caractères alphabétiques (a-z, A-Z) lors de la saisie des données. <br/>**`Alphanumeric with Space`**- Permet aux espaces dans l’adresse de rue de respecter les exigences de longueur maximale du transporteur. Lors du passage en caisse, le client peut saisir n&#39;importe quelle combinaison de nombres (0-9), de caractères alphabétiques (a-z, A-Z) et d&#39;espaces dans l&#39;adresse postale du destinataire et de l&#39;expéditeur. Les espaces supplémentaires sont supprimés lors de l’enregistrement de l’adresse.<br/>**`Numeric Only`** - Accepte uniquement les nombres (0-9) lors de la saisie des données. <br/>**`Alpha Only`**- Accepte uniquement les caractères alphabétiques (a-z, A-Z) lors de la saisie des données.<br/>**`URL`** - Accepte uniquement une URL lors de la saisie des données. <br/>**`Email`**- Accepte uniquement une adresse électronique lors de la saisie des données.<br/>**`Length Only`** : valide l’entrée en fonction de la longueur des données saisies dans le champ. |
| [!UICONTROL Input/Output Filter] | Applique un filtre de prétraitement aux valeurs saisies dans un champ de texte, une zone de texte ou un type d’entrée multi-lignes avant l’enregistrement. Options : <br/>**`None`**- N’applique pas de filtre au texte saisi dans le champ.<br/>**`Strip HTML Tags`** - Supprime les balises HTML du texte. Ce filtre peut aider à nettoyer les données collées dans un champ à partir d’une autre source qui inclut des balises d’HTML. <br/>**`Escape HTML Entities`**- Convertit les caractères spéciaux trouvés dans le texte en séquence d’échappement d’HTML valide, telle que `amp;`. Les séquences d’échappement sont entourées d’une esperluette et d’un point-virgule. Elles sont fréquemment utilisées pour les guillemets intelligents du typographe, les symboles de copyright et les symboles de marque. Les séquences d’échappement sont également utilisées pour identifier des caractères tels que les symboles inférieur à (`<`) et supérieur à (`>`), ainsi que le caractère d’esperluette également utilisés dans le code. Ce filtre peut aider à nettoyer les caractères spéciaux qui sont parfois collés dans des champs de base de données à partir de programmes de traitement de texte. |
| [!UICONTROL Add to Column Options] | Indique si l’attribut est inclus en tant que colonne dans la grille [Customers](customers-all.md). Options : `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | Indique si l’attribut peut être utilisé comme filtre pour les opérations de recherche à partir de la grille. Options : `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Indique les conditions de correspondance de filtre pour les attributs des opérations de recherche à partir de la grille. Cela n’a aucune incidence sur le champ _Rechercher par mot-clé_ pour la grille. Options : `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Indique si la valeur d’attribut peut être utilisée comme mot-clé dans les opérations de recherche. Options : `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Détermine si l’attribut est inclus dans les conditions [segment client](customer-segments.md). Options : `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Champ | Description |
|--- |--- |
| [!UICONTROL Show on Storefront] | Détermine si l’attribut apparaît comme un champ dans les informations sur le client dans le storefront. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Indique l’ordre de tri de cet attribut par rapport aux autres attributs du client. L’ordre de tri détermine la séquence selon laquelle les champs reçoivent le focus lors de la saisie des données lors de l’utilisation de la navigation au clavier. |
| [!UICONTROL Forms to Use in] | Détermine les pages contenant des formulaires de saisie de données où l’attribut apparaît. Options : <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## Attributs de client par défaut

| Code d’attribut | Description |
| --------------- | ------------------ |
| `created_at` | Date de création du compte client. |
| `updated_at` | Date de la dernière mise à jour du compte client. |
| `website_id` | Identifiant du site web sur lequel le compte du client a été créé. |
| `store_id` | Identifiant de magasin du site sur lequel le compte client a été créé. |
| `created_in` | Vue du magasin dans lequel le compte a été créé. |
| `group_id` | Identifiant du groupe de clients auquel le client est affecté. |
| `disable_auto_group_change` | Détermine si des groupes de clients peuvent être affectés de manière dynamique lors de la [validation de l’ID de TVA](../stores-purchase/vat.md#configure-vat-id-validation). |
| `prefix` | Tout préfixe utilisé avec le nom du client (M., Mme ou Dr, par exemple). |
| `firstname` | Prénom du client. |
| `middlename` | Nom intermédiaire ou initial intermédiaire du client. |
| `lastname` | Nom du client. |
| `suffix` | Tout suffixe utilisé avec le nom du client. (par exemple, Jr., Sr. ou Esquire) |
| `email` | Adresse électronique du client. |
| `dob` | Date de naissance du client.  <br><br>**_Important :_**&#x200B;Conformément aux bonnes pratiques actuelles en matière de sécurité et de confidentialité, gardez à l’esprit tous les risques potentiels liés à la sécurité et au stockage de la date de naissance complète des clients (mois, jour, année) avec d’autres identifiants personnels. Il est recommandé de limiter le stockage des dates de naissance complètes des clients et de suggérer d’utiliser l’année de naissance du client comme alternative. |
| `taxvat` | L’ID de taxe sur la valeur ajoutée (TVA) attribué au client. Le libellé par défaut de cet attribut est `VAT Number`. Le champ Numéro de TVA est toujours présent dans toutes les adresses client d’expédition et de facturation lorsqu’il est affiché à partir de l’administrateur, mais il n’est pas obligatoire. |
| `gender` | Genre du client. |

## Démonstration des attributs du client

Pour une démonstration de la création d’attributs du client, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3410184?quality=12&learn=on&captions=fre_fr)
