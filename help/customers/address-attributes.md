---
title: Attributs d’adresse du client
description: Découvrez les attributs d’adresse du client et comment configurer ces propriétés d’attribut.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Attributs d’adresse du client

{{ee-feature}}

L’ensemble d’attributs Customer Address détermine les propriétés des adresses de rue qui sont saisies dans le [carnet d’adresses](account-dashboard-address-book.md) à partir du compte du client ou pendant le [passage en caisse](../stores-purchase/checkout-process.md).

Les attributs d’adresse personnalisés peuvent être configurés pour fournir des informations supplémentaires, telles qu’une adresse électronique facultative, un compte Skype, un numéro de téléphone alternatif, un bâtiment ou un département. L’attribut personnalisé peut ensuite être incorporé dans le [modèle d’adresse](address-templates.md) utilisé pour produire des documents de vente. Le processus de création d’un attribut d’adresse personnalisé est presque identique à la création d’un [attribut du client](attribute-properties.md).

Les attributs d’adresse du client sont utilisés dans les formulaires suivants :

- [Enregistrement de l’adresse du client](account-create.md)
- [Adresse du compte client](account-dashboard-address-book.md)

![Admin - Attributs de l’adresse client](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Étape 1 : propriétés de l’attribut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Propriétés d’attribut du client](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Dans la section **[!UICONTROL Attribute Properties]** , procédez comme suit :

   - Saisissez un **[!UICONTROL Default Label]** qui identifie l’attribut lors de la saisie des données.

   - Saisissez un **[!UICONTROL Attribute Code]** qui identifie l’attribut dans le système.

     Le code d’attribut doit commencer par une lettre et peut inclure toute combinaison de lettres minuscules (a-z) et de nombres (0-9). Le code doit comporter moins de 30 caractères et ne peut pas contenir de caractères spéciaux ni d’espaces. Le caractère de soulignement (_) peut être utilisé pour indiquer un espace.

     >[!TIP]
     >
     >**_Raccourci :_** Pour remplir uniquement les champs requis, faites défiler l’écran jusqu’à [!UICONTROL Storefront Properties], saisissez le [!UICONTROL Sort Order] et enregistrez.

1. Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Input Type]** sur l’un des paramètres suivants :

   - `Text Field` - Champ de texte d’une seule ligne.
   - `Text Area` - Zone de texte multiligne.
   - `Multiple Line` - Crée plusieurs lignes de texte pour l’attribut, comme une adresse de rue multi-lignes. Le nombre de lignes de saisie de données distinctes peut être compris entre 2 et 20. Utilisez le `Default Value` pour spécifier la valeur initiale du champ.
   - `Date` - Affiche un champ de date avec un calendrier contextuel. Propriétés supplémentaires : utilisez `Default Value` pour spécifier la valeur initiale du champ. <br/>Utilisez `Minimal Value` pour spécifier la date la plus ancienne pouvant être saisie.  Utilisez `Maximum Value` pour spécifier la date la plus récente pouvant être saisie.
   - `Dropdown` - Liste déroulante qui accepte une seule valeur à sélectionner.
   - `Multiple Select` - Liste déroulante qui accepte plusieurs valeurs à sélectionner.
   - `Yes/No` - Champ qui ne propose que le choix des valeurs `Yes` ou `No`.
   - `File (attachment)` - Champ qui permet de charger un fichier et de l’associer à l’attribut du client en tant que pièce jointe.
   - `Image File` - Champ qui permet de charger une image dans la galerie et de l’associer à l’attribut du client.

1. Si le client doit saisir une valeur dans le champ, définissez **[!UICONTROL Values Required]** sur `Yes`.

1. Pour attribuer une valeur initiale au champ, saisissez une valeur **[!UICONTROL Default Value]**.

1. Pour vérifier la précision des données saisies dans le champ avant l’enregistrement, définissez **[!UICONTROL Input Validation]** sur le type de données à autoriser dans le champ. Les valeurs disponibles dépendent du _[!UICONTROL Input Type]_&#x200B;spécifié.

   - `None` - Le champ n’a aucune validation d’entrée lors de la saisie des données.
   - `Alphanumeric` - Accepte toute combinaison de nombres (0-9) et de caractères alphabétiques (a-z, A-Z) lors de la saisie des données. Pour inclure des caractères spéciaux, reportez-vous à la section [!UICONTROL Escape HTML Entities] à l’étape suivante.
   - `Alphanumeric with Space` - Accepte toute combinaison de nombres (0-9), de caractères alphabétiques (a-z, A-Z) et d’espaces lors de la saisie des données.
   - `Numeric Only` - Accepte uniquement les nombres (0-9) lors de la saisie des données.
   - `Alpha Only` - Accepte uniquement les caractères alphabétiques (a-z, A-Z) lors de la saisie des données.
   - `URL` - Accepte uniquement une URL lors de la saisie des données.
   - `Email` - Accepte uniquement une adresse électronique lors de la saisie des données.
   - `Length Only` : valide l’entrée en fonction de la longueur des données saisies dans le champ.

1. Pour appliquer un filtre de prétraitement aux valeurs saisies dans un champ de texte, une zone de texte ou un type d’entrée multi-lignes, définissez **[!UICONTROL Input/Output Filter]** sur l’une des options suivantes :

   - `None` - N’applique pas de filtre au texte saisi dans le champ.
   - `Strip HTML Tags` - Supprime les balises HTML du texte. Ce filtre peut aider à nettoyer les données collées dans un champ à partir d’une autre source qui inclut des balises d’HTML.
   - `Escape  HTML Entities` - Convertit les caractères spéciaux trouvés dans le texte en séquence d’échappement d’HTML valide, telle que `&;`. Les séquences d’échappement sont entourées d’une esperluette et d’un point-virgule. Elles sont fréquemment utilisées pour les guillemets intelligents du typographe, les symboles de copyright et de marque. Les séquences d’échappement sont également utilisées pour identifier des caractères tels que les symboles inférieur à (`<`) et supérieur à (`>`), ainsi que le caractère d’esperluette également utilisés dans le code. Ce filtre peut aider à nettoyer les caractères spéciaux qui sont parfois collés dans des champs de base de données à partir de programmes de traitement de texte.

1. Renseignez les propriétés de grille et de segment du client :

   - Pour pouvoir inclure la colonne dans la grille Clients, définissez **[!UICONTROL Add to Column Options]** sur `Yes`.

   - Pour filtrer la grille Clients selon cet attribut, définissez **[!UICONTROL Use in Filter Options]** sur `Yes`.

   - Pour filtrer la grille Clients par attribut de texte avec différentes conditions de correspondance de filtre, définissez **[!UICONTROL Grid Filter Condition Type]** sur `Partial Match`, `Prefix Match` ou `Full Match`. Cela n’a aucune incidence sur le champ _Rechercher par mot-clé_ pour la grille.

   - Pour rechercher la grille Clients en fonction de cet attribut, définissez **[!UICONTROL Use in Search Options]** sur `Yes`.

   - Pour rendre cet attribut disponible pour les [segments client](customer-segments.md), définissez **[!UICONTROL Use in Customer Segment]** sur `Yes`.

## Étape 2 : propriétés du storefront

1. Faites défiler l’écran jusqu’à la section **[!UICONTROL Storefront Properties]**.

   ![&#x200B; Attributs d’adresse du client - Propriétés Storefront](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Pour rendre l’attribut visible aux clients, définissez **[!UICONTROL Show on Storefront]** sur `Yes`.

1. Entrez un nombre dans le champ **[!UICONTROL Sort Order]**, qui détermine son ordre d’apparition lorsqu’il est répertorié avec d’autres attributs.

1. Définissez **[!UICONTROL Forms to Use]** sur chaque formulaire devant inclure l’attribut .

   Pour choisir les deux options, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque formulaire.

   - [Enregistrement de l’adresse du client](account-create.md)
   - [Adresse du compte client](account-dashboard-address-book.md)

## Etape 3 : renseigner le libellé et enregistrer

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels/Options]**.

1. Sous **[!UICONTROL Manage Titles]**, saisissez un libellé pour identifier l’attribut pour chaque [vue de magasin](../getting-started/websites-stores-views.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.

   ![&#x200B; Attributs d’adresse du client - étiquettes/options](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Descriptions des champs

### [!UICONTROL Attribute Properties]

| Champ | Description |
|--- |--- |
| [!UICONTROL Default Label] | Libellé par défaut qui identifie l’attribut dans l’Admin et le storefront. |
| [!UICONTROL Attribute Code] | Code unique qui identifie l’attribut dans le système. Le code peut contenir jusqu’à 21 caractères et ne peut pas contenir d’espaces ni de caractères spéciaux. Le caractère de soulignement peut être utilisé à la place d’un espace. |
| [!UICONTROL Input Type] | Détermine le [contrôle d’entrée](../catalog/attributes-input-types.md) utilisé pour la saisie de données. Options : <br/>**`Text Field`**- Champ de texte d’une seule ligne.<br/>**`Text Area`** - Zone de texte multiligne. <br/>**`Multiple Line`**- Crée plusieurs lignes de texte pour l’attribut, comme une adresse de rue multi-lignes. Le nombre de lignes de saisie de données distinctes peut être compris entre 2 et 20.<br/>**`Date`** - Affiche un champ de date avec un calendrier contextuel.<br/>**`Dropdown`**- Liste déroulante qui accepte une seule valeur à sélectionner.<br/>**`Multiple Select`** - Liste déroulante qui accepte plusieurs valeurs à sélectionner. <br/>**`Yes/No`**- Champ qui ne propose que le choix des valeurs `Yes` ou `No`.<br/>**`File (attachment)`** - Champ qui permet de charger un fichier et de l’associer à l’attribut du client en tant que pièce jointe. <br/>**`Image File`**- Champ qui permet de charger une image dans la galerie et de l’associer à l’attribut du client. |
| [!UICONTROL Values Required] | Détermine si une valeur doit être saisie dans le champ. Options : `Yes` / `No` |
| [!UICONTROL Default Value] | Indique la valeur initiale de l’attribut. |
| [!UICONTROL Input Validation] | La sélection des options est déterminée par le type d’entrée. Options : <br/>**`None`**- Le champ n’a aucune validation d’entrée lors de la saisie des données.<br/>**`Alphanumeric`** - Accepte toute combinaison de nombres (0-9) et de caractères alphabétiques (a-z, A-Z) lors de la saisie des données. <br/>**`Alphanumeric with Space`**- Permet aux espaces dans l’adresse de rue de respecter les exigences de longueur maximale du transporteur. Lors du passage en caisse, le client peut saisir n&#39;importe quelle combinaison de nombres (0-9), de caractères alphabétiques (a-z, A-Z) et d&#39;espaces dans l&#39;adresse postale du destinataire et de l&#39;expéditeur. Les espaces supplémentaires sont supprimés lors de l’enregistrement de l’adresse.<br/>**`Numeric Only`** - Accepte uniquement les nombres (0-9) lors de la saisie des données. <br/>**`Alpha Only`**- Accepte uniquement les caractères alphabétiques (a-z, A-Z) lors de la saisie des données.<br/>**&#x200B; URL &#x200B;**- Accepte uniquement une URL lors de la saisie des données.<br/>**`Email`** - Accepte uniquement une adresse électronique lors de la saisie des données. <br/>**`Length Only`**: valide l’entrée en fonction de la longueur des données saisies dans le champ. |
| [!UICONTROL Input/Output Filter] | Applique un filtre de prétraitement aux valeurs saisies dans un champ de texte, une zone de texte ou un type d’entrée multi-lignes avant l’enregistrement. Options : <br/>**`None`**- N’applique pas de filtre au texte saisi dans le champ.<br/>**`Strip HTML Tags`** - Supprime les balises HTML du texte. Ce filtre peut aider à nettoyer les données collées dans un champ à partir d’une autre source qui inclut des balises d’HTML. <br/>**`Escape HTML Entities`**- Convertit les caractères spéciaux trouvés dans le texte en séquence d’échappement d’HTML valide, telle que `amp;`. Les séquences d’échappement sont entourées d’une esperluette et d’un point-virgule. Elles sont fréquemment utilisées pour les guillemets intelligents du typographe, les symboles de copyright et les symboles de marque. Les séquences d’échappement sont également utilisées pour identifier des caractères tels que les symboles inférieur à (`<`) et supérieur à (`>`), ainsi que le caractère d’esperluette également utilisés dans le code. Ce filtre peut aider à nettoyer les caractères spéciaux qui sont parfois collés dans des champs de base de données à partir de programmes de traitement de texte. |
| [!UICONTROL Add to Column Options] | Indique si l’attribut est inclus en tant que colonne dans la grille [Customers](./customers-all.md). Options : `Yes` / `No` |
| Utilisation dans les options de filtre | Indique si l’attribut peut être utilisé comme filtre pour les opérations de recherche à partir de la grille. Options : `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Spécifie les conditions de correspondance de filtre pour les attributs dans les opérations de recherche à partir de la grille. Cela n’affecte pas le champ _[!UICONTROL Search by keyword]_&#x200B;de la grille. Options : `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Indique si la valeur d’attribut peut être utilisée comme mot-clé dans les opérations de recherche. Options : `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Détermine si l’attribut est inclus dans les conditions [segment client](./customer-segments.md). Options : `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Champ | Description |
|--- |--- |
| [!UICONTROL Show on Storefront] | Détermine si l’attribut apparaît comme un champ dans les informations sur le client dans le storefront. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Indique l’ordre de tri de cet attribut par rapport aux autres attributs du client. L’ordre de tri détermine la séquence selon laquelle les champs reçoivent le focus lors de la saisie des données lors de l’utilisation de la navigation au clavier. |
| [!UICONTROL Forms to Use in] | Détermine les pages contenant des formulaires de saisie de données où l’attribut apparaît. Options : <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
