---
title: Positionner les blocs de contenu
description: Positionnez un bloc à un emplacement spécifique de la page, et même pour un produit ou une catégorie spécifique, sans écrire de code
exl-id: cfc9eb2c-19c8-43f1-937d-4162b5011b8a
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/BgZJJ9DGr8KD2-6XNf3yPTjo3ulGVdp0yyrJMXHWX-4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Positionner les blocs de contenu

Le code qui contrôle la mise en page et l’emplacement des blocs est écrit en XML [widgets](widgets.md). Ces widgets permettent de positionner facilement un bloc à un emplacement spécifique sur la page, et même pour un produit ou une catégorie spécifique, sans avoir à écrire de code. Vous pouvez choisir chaque option dans une liste, plutôt que d’essayer de mémoriser toutes les combinaisons possibles.

La liste suivante décrit les emplacements par type de page où les blocs sont généralement placés. Pour plus d’informations sur la définition des zones de la page, voir [Mises en page standard](page-layout.md#standard-page-layouts).

## Pages Catégorie et CMS

| Référence de bloc | Position |
|----------|-------- |
| [!UICONTROL Breadcrumbs] | L’aide à la navigation en haut de nombreuses pages qui indique votre emplacement actuel sous forme de lien. Tout contenu supplémentaire placé dans la référence de chemin de navigation flotte à droite du chemin de navigation, s’il est affiché. |
| [!UICONTROL Left Column] | Le contenu est ajouté à la colonne de gauche. |
| [!UICONTROL Main Content Area] | Le contenu est ajouté à la zone de contenu principale. |
| [!UICONTROL My Cart Extra Actions] | Le contenu s’affiche sous le _sous-total du panier_ lorsque le client clique sur l’icône du panier en haut de la page. |
| [!UICONTROL Navigation Bar] | Le contenu s’affiche sous la barre de navigation principale. |
| [!UICONTROL Page Bottom] | Le contenu s’affiche au bas de la page. |
| [!UICONTROL Page Footer] | Le contenu s’affiche au-dessus du pied de page. |
| [!UICONTROL Page Header] | Le contenu apparaît sous l’en-tête de la page. |
| [!UICONTROL Page Top] | Le contenu apparaît en haut de la page. |
| [!UICONTROL Right Column] | Le contenu s’affiche dans la colonne de droite. |
| [!UICONTROL Store Language] | Le contenu s’affiche dans le coin supérieur gauche de l’en-tête. |

{style="table-layout:auto"}

## Page de produit

| Référence de bloc | Position |
|----------|-------- |
| [!UICONTROL Alert URLs] | Le contenu s’affiche sous le titre du produit sur la page des détails du produit. |
| [!UICONTROL Bottom Block Options Wrapper] | Si des options personnalisées sont ajoutées, le contenu s’affiche sous le bouton _Ajouter au panier_. |
| [!UICONTROL Breadcrumbs] | Le contenu s’affiche à droite des chemins de navigation, l’aide à la navigation qui fournit des liens sous la forme d’un chemin d’accès présenté sous la barre de navigation. |
| [!UICONTROL Info Column Options Wrapper] | Si des options personnalisées sont ajoutées, le contenu s’affiche à droite. Le même emplacement s’applique aux options configurables. |
| [!UICONTROL Left Column] | Le contenu s’affiche sous les blocs de colonne de gauche. |
| [!UICONTROL Main Content Area] | Le contenu s’affiche sous la zone de contenu principale. |
| [!UICONTROL My Cart Extra Actions] | Le contenu s’affiche sous le _sous-total du panier_ lorsque le client clique sur l’icône du panier en haut de la page. |
| [!UICONTROL Navigation Bar] | Le contenu s’affiche sous la barre de navigation principale. |
| [!UICONTROL Page Bottom] | Le contenu s’affiche au bas de la page. |
| [!UICONTROL Page Footer] | Le contenu s’affiche au-dessus du pied de page. |
| [!UICONTROL Page Header] | Le contenu apparaît sous l’en-tête de la page. |
| [!UICONTROL Page Top] | Le contenu apparaît en haut de la page. |
| [!UICONTROL PayPal Express Checkout (Payflow Edition) Shortcut Wrapper] | Si le mode de paiement PayPal est activé, le contenu apparaît sous le bouton _Achat PayPal_. |
| [!UICONTROL PayPal Express Checkout Shortcut Wrapper] | Si le mode de paiement PayPal est activé, le contenu apparaît sous le bouton _Achat PayPal_. |
| [!UICONTROL Product Tags List] | Le contenu s’affiche sous la barre des balises de produits. |
| [!UICONTROL Product View Extra Hint] | Le contenu s’affiche sous le prix principal du produit. |
| [!UICONTROL Right Column] | Le contenu s’affiche sous les blocs de colonne de droite. |
| [!UICONTROL Store Language] | Le contenu s’affiche à droite du sélecteur de langues. |
| [!UICONTROL Tags List Before] | Le contenu s’affiche au-dessus du champ _[!UICONTROL Add Your Tags]_. |

{style="table-layout:auto"}
