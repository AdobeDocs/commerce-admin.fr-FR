---
title: '[!DNL Google Analytics]'
description: Découvrez comment utiliser [!DNL Google Analytics] pour rassembler des mesures utiles pour vos sites Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] vous permet de définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions avec les applications mobiles et hors ligne et l’accès aux mises à jour en cours. [!DNL Google Analytics] 4 est la solution de mesure de nouvelle génération Google et remplace [!DNL Universal Analytics]. Le 1er juillet 2023, les propriétés Universal Analytics standard cesseront de traiter de nouveaux accès.

>[!NOTE]
>
>Si votre entreprise est soumise à des réglementations de confidentialité telles que la variable [Règlement général sur la protection des données](../getting-started/compliance-gdpr.md) et/ou [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), voir [Paramètres de confidentialité de Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Si vous activez la variable [Mode de restriction des cookies](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] ne collecte pas de données sur les visiteurs, sauf s’ils ont accepté des cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Étape 1 : configuration [!UICONTROL Google Analytics] 4

Si vous n’avez pas déjà une [!DNL Google Analytics] 4 configuration pour votre site, procédez comme suit :

- [Configuration de la collecte de données Analytics pour la première fois](https://support.google.com/analytics/answer/9304153)
- [Ajout de Google Analytics 4 à un site avec [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Étape 2 : terminer la configuration Commerce

1. Connectez-vous à l’administrateur de votre boutique Commerce.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Google GTag]** .

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Google Analytics4]** et procédez comme suit :

   - Définir **[!UICONTROL Enable]** to `Yes`.

   - Laissez le champ **[!UICONTROL Account type]** as `Google Analytics4`.

   - Saisissez votre **[!UICONTROL Measurement ID]**. Pour en savoir plus, voir [Aide pour les Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Si vous souhaitez effectuer des tests A/B et d’autres tests de performance sur votre contenu, définissez **Expériences de contenu** to `Yes`.

   ![Configuration des ventes - API Google pour les Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>À compter du 1er juillet 2023, les propriétés Universal Analytics standard ne traiteront plus les données. Si vous comptez toujours sur [!DNL Universal Analytics], il est recommandé de [préparation à l’utilisation des Google Analytics 4](https://support.google.com/analytics/answer/10759417) à venir.

### Étape 1 : configuration de Google Universal Analytics

Visitez le site web de Google et inscrivez-vous à une [Google Universal Analytics][1] compte .

### Étape 2 : terminer la configuration Commerce

1. Connectez-vous à l’administrateur de votre boutique Commerce.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Google Analytics]** et procédez comme suit :

   - Définir **[!UICONTROL Enable]** to `Yes`.

   - Saisissez votre [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Si vous souhaitez effectuer des tests A/B et d’autres tests de performance sur votre contenu, définissez **[!UICONTROL Content Experiments]** to `Yes`.

   ![Configuration des ventes - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Amélioration de l’e-commerce

Enhanced Ecommerce est un module externe pour [!DNL Google Universal Analytics] qui vous donne des informations sur le comportement d’achat et d’achat de vos clients. Vous pouvez utiliser l’e-commerce amélioré pour générer des rapports sur les activités clés des clients, par exemple lorsque les clients ajoutent des articles au panier, commencent le processus de passage en caisse ou effectuent un achat. Vous pouvez également identifier et analyser les schémas des acheteurs qui abandonnent leur panier sans faire d’achat.

Les instructions suivantes expliquent comment configurer [!DNL Google Tag Manager] avec [!DNL Universal Analytics] pour produire des données et des rapports d’e-commerce améliorés.

### Étape 1. S’inscrire à des comptes Google

1. Inscrivez-vous à un [Gestionnaire de balises de Google](google-tag-manager.md) et effectuez la configuration Commerce.

1. Inscrivez-vous à une nouvelle [Google Universal Analytics][1] compte .

### Étape 2. Configurer le commerce électronique amélioré

1. Connectez-vous à votre compte Google Universal Analytics.

1. Créez une propriété pour l’analyse d’e-commerce améliorée avec les paramètres suivants :

   - État : activé
   - Produits associés : ACTIVÉ
   - Activer les rapports d’e-commerce améliorés : activé
   - Étiquetage du passage en caisse : (non requis)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Submit]**.

### Étape 3. Création de balises et de déclencheurs

1. Se connecter à [!DNL Google Tag Manager] et créez les déclencheurs suivants :

   | Nom | Type d’événement | Filtrer |
   |--- |--- |--- |
   | `addToCart` | Événement personnalisé |  |
   | `checkout` | Événement personnalisé |  |
   | `checkout only` | Page vue | L’URL de page correspond à RegEx /checkout/.* |
   | `checkoutOption` | Événement personnalisé |  |
   | `gtm.dom` | Événement personnalisé |  |
   | `productClick` | Événement personnalisé |  |
   | `promotionClick` | Événement personnalisé |  |
   | `removeFromCart` | Événement personnalisé |  |

   >[!NOTE]
   >
   >La variable [!UICONTROL Checkout] est déclenché pour les méthodes de paiement de base intégrées de Commerce uniquement (telles que `Check / Money Order` et `Cash On Delivery Payment`). Cet événement n’est pas exécuté pour `PayPal checkout` et d&#39;autres modes de paiement externes, qui utilisent la redirection vers le passage en caisse à partir de ressources externes.

1. Créez les balises Universal Analytics suivantes avec la même configuration de base.

   - Balises Analytics universelles

     | Nom | Type | Déclencheurs |
     |--- |--- |--- |
     | `Add to cart tracking` | Analyses universelles | addToCart |
     | `Checkout option tracking` | Analyses universelles | checkoutOption |
     | `Checkout tracking` | Analyses universelles | passage en caisse |
     | `Pageview tracking` | Analyses universelles | gtm.dom |
     | `Product click tracking` | Analyses universelles | productClick |
     | `Promo click tracking` | Analyses universelles | promotionClick |
     | `Remove from cart tracking` | Analyses universelles | removeFromCart |

   - Configuration de base des balises

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Analyses universelles |
     | [!UICONTROL Tracking ID] | UA-XXX (ID de suivi de votre compte Analytics universel.) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. Effectuez les différentes configurations de suivi.

   - Saisissez ce qui suit : **[!UICONTROL Add to Cart]** paramètres de suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | eCommerce |
     | [!UICONTROL Action] | Ajouter au panier |
     | [!UICONTROL Trigger] | addToCart |

   - Saisissez ce qui suit : **[!UICONTROL Checkout option]** paramètres de suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | eCommerce |
     | [!UICONTROL Action] | Option de passage en caisse |
     | [!UICONTROL Trigger] | checkoutOption |

   - Saisissez ce qui suit : **[!UICONTROL PageView]** paramètres de suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Procédez comme suit : **[!UICONTROL Product Click]** configuration du suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | eCommerce |
     | [!UICONTROL Action] | Clic sur le produit |
     | [!UICONTROL Trigger] | productClick |

   - Procédez comme suit : **[!UICONTROL Promotion Click]** configuration du suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | eCommerce |
     | [!UICONTROL Action] | Clic sur la promotion |
     | [!UICONTROL Trigger] | promotionClick |

   - Procédez comme suit : **[!UICONTROL Remove from Cart]** configuration du suivi :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | eCommerce |
     | [!UICONTROL Action] | Supprimer du panier |
     | [!UICONTROL Trigger] | removeFromCart |

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Preview]** et vérifiez que les balises fonctionnent correctement.

1. Après avoir vérifié les paramètres, cliquez sur **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
