---
title: Vues du magasin
description: Découvrez comment ajouter et modifier une vue de magasin.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# Vues du magasin

Les vues de magasin sont généralement utilisées pour rendre le magasin disponible dans différents paramètres régionaux. Les acheteurs peuvent utiliser le sélecteur de langues dans l’en-tête du magasin pour modifier la vue du magasin.

![Portée : plusieurs vues de magasin](./assets/scope-multiview.svg){width="550"}

## Ajout d’une vue de magasin

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Toutes les boutiques](./assets/stores-all.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Create Store View]**.

   ![Créer une vue de magasin](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Store]** au magasin parent de cette vue.

1. Saisissez un **[!UICONTROL Name]** pour cette vue de magasin.

   Le nom apparaît dans le sélecteur de langues de l’en-tête du magasin. Par exemple: `Spanish`.

1. Pour **[!UICONTROL Code]**, saisissez le code qui identifie la vue (en minuscules).

   Par exemple: `spanish`.

1. Pour activer la vue, définissez **[!UICONTROL Status]** to `Enabled`.

1. (Facultatif) Saisissez un **[!UICONTROL Sort Order]** nombre pour déterminer la séquence dans laquelle cette vue est répertoriée avec d’autres vues.

1. Cliquez sur **[!UICONTROL Save Store View]**.

## Modifier une vue de magasin

Comme le nom de la vue s’affiche dans le sélecteur de langues, vous pouvez éventuellement modifier le nom de la vue par défaut pour le rendre plus explicite. La variable _Nom_ est simplement un libellé qui peut être facilement modifié.

Si votre installation Adobe Commerce ou Magento Open Source dispose d’une configuration multi-site ou multi-magasin, ne modifiez pas le champ de code de magasin sans vérifier que la valeur n’est pas référencée dans la variable `index.php` fichier . Si vous n’avez pas accès au serveur pour examiner le fichier, demandez de l’aide à un développeur.

| Champ | Valeur d’origine | Valeur mise à jour |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Dans le _[!UICONTROL Store View]_de la grille, cliquez sur le nom de la vue à modifier.

   Lors de la modification de la vue par défaut, la variable _[!UICONTROL Store]_et_[!UICONTROL Status]_ ne sont pas disponibles.

   ![Vue Boutique - Modifier la vue par défaut](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Mettez à jour les champs suivants si nécessaire :

   - **[!UICONTROL Store]** (vues autres que par défaut uniquement)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (uniquement si non utilisé dans `index.php`)
   - **[!UICONTROL Status]** (vues autres que par défaut uniquement)
   - **[!UICONTROL Sort Order]**

1. Cliquez sur **[!UICONTROL Save Store View]**.
