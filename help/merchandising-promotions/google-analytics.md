---
title: '[!DNL Google Analytics]'
description: Découvrez comment utiliser pour rassembler  [!DNL Google Analytics]  mesures utiles pour vos sites Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] vous permet de définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions d’applications mobiles et hors ligne, et l’accès aux mises à jour en cours. Le [!DNL Google Analytics] 4 est une solution de mesure de nouvelle génération de Google qui remplace [!DNL Universal Analytics]. Le 1er juillet 2023, les propriétés Universal Analytics standard cesseront de traiter les nouveaux accès.

>[!NOTE]
>
>Si votre entreprise est soumise à des réglementations de confidentialité telles que le [Règlement général sur la protection des données](../getting-started/compliance-gdpr.md) et/ou la [Loi californienne sur la protection de la vie privée des consommateurs](../getting-started/compliance-ccpa.md), consultez [Paramètres de confidentialité de Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Si vous activez le [Mode de restriction des cookies](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] ne collecte pas de données sur les visiteurs, sauf s’ils ont accepté les cookies.

## 4 [!DNL Google Analytics]

{{gtag-api-note}}

### Étape 1 : configurer le [!UICONTROL Google Analytics] 4

Si vous ne disposez pas déjà d’une configuration [!DNL Google Analytics] 4 pour votre site, procédez de l’une des manières suivantes :

- [Configurer la collecte de données Analytics pour la première fois](https://support.google.com/analytics/answer/9304153)
- [Ajouter Google Analytics 4 à un site avec [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Étape 2 : terminer la configuration de Commerce

1. Connectez-vous à l’administration de votre boutique Commerce.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Google GTag]** .

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la sous-section **[!UICONTROL Google Analytics4]** et procédez comme suit :

   - Définissez **[!UICONTROL Enable]** sur `Yes`.

   - Laissez le **[!UICONTROL Account type]** tel `Google Analytics4`.

   - Saisissez votre **[!UICONTROL Measurement ID]**. Pour en savoir plus, voir l&#39;aide de [Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Si vous souhaitez effectuer des tests A/B et d’autres tests de performance sur votre contenu, définissez **Expériences de contenu** sur `Yes`.

   ![Configuration des ventes - API Google pour Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>À compter du 1er juillet 2023, les propriétés Universal Analytics standard ne traiteront plus les données. Si vous dépendez toujours de [!DNL Universal Analytics], il est recommandé de [se préparer à utiliser Google Analytics 4](https://support.google.com/analytics/answer/10759417) à l’avenir.

### Étape 1 : Configurer Google Universal Analytics

Visitez le site web de Google et inscrivez-vous à un compte [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Étape 2 : terminer la configuration de Commerce

1. Connectez-vous à l’administration de votre boutique Commerce.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Google Analytics]** et procédez comme suit :

   - Définissez **[!UICONTROL Enable]** sur `Yes`.

   - Saisissez votre [!DNL Google Analytics] de **[!UICONTROL Account Number]**.

   - Si vous souhaitez effectuer des tests A/B et d’autres tests de performance sur votre contenu, définissez **[!UICONTROL Content Experiments]** sur `Yes`.

   ![Configuration des ventes - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## E-commerce amélioré

L’e-commerce amélioré est un plug-in d’[!DNL Google Universal Analytics] qui vous permet d’accéder à insight pour connaître le comportement d’achat de vos clients. Vous pouvez utiliser le e-commerce amélioré pour produire des rapports sur les activités clés des clients, par exemple lorsque les clients ajoutent des articles au panier, commencent le processus de passage en caisse ou effectuent un achat. Vous pouvez également identifier et analyser les schémas des acheteurs qui abandonnent leur panier sans effectuer d’achat.

Les instructions suivantes expliquent comment configurer [!DNL Google Tag Manager] avec [!DNL Universal Analytics] pour produire des données et des rapports d’e-commerce améliorés.

### Étape 1. S’inscrire à des comptes Google

1. Inscrivez-vous à un compte [Google Tag Manager](google-tag-manager.md) et effectuez la configuration de Commerce.

1. Créez un compte [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Étape 2. Configuration d’Enhanced Ecommerce

1. Connectez-vous à votre compte Google Universal Analytics.

1. Créez une propriété pour l’analyse Enhanced Ecommerce avec les paramètres suivants :

   - Statut : ACTIVÉ
   - Produits connexes : ON
   - Activer la création de rapports d’e-commerce améliorée : ACTIVÉ
   - Étiquetage du passage en caisse : (non requis)

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

### Étape 3. Création de balises et de déclencheurs

1. Connectez-vous à votre compte [!DNL Google Tag Manager] et créez les déclencheurs suivants :

   | Nom | Type d’événement | Filtre |
   |--- |--- |--- |
   | `addToCart` | Événement personnalisé |  |
   | `checkout` | Événement personnalisé |  |
   | `checkout only` | Page vue | L’URL de la page correspond à RegEx /checkout/.* |
   | `checkoutOption` | Événement personnalisé |  |
   | `gtm.dom` | Événement personnalisé |  |
   | `productClick` | Événement personnalisé |  |
   | `promotionClick` | Événement personnalisé |  |
   | `removeFromCart` | Événement personnalisé |  |

   >[!NOTE]
   >
   >L’événement [!UICONTROL Checkout] est déclenché uniquement pour les méthodes de paiement de base intégrées de Commerce (telles que `Check / Money Order` et `Cash On Delivery Payment`). Cet événement n&#39;est pas exécuté pour les `PayPal checkout` et autres méthodes de paiement externes qui utilisent la redirection vers le passage en caisse à partir de ressources externes.

1. Créez les balises Universal Analytics suivantes avec la même configuration de base.

   - Balises Universal Analytics

     | Nom | Type | Déclenchement de déclencheurs |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | passage en caisse |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Configuration de base des balises

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (ID de suivi de votre compte Universal Analytics). |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | Vrai |
     | [!UICONTROL Use data layer] | Vrai |
     | [!UICONTROL Use Debug version] | Vrai |

1. Effectuez les différentes configurations de tracking.

   - Saisissez les paramètres de tracking **[!UICONTROL Add to Cart]** suivants :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Ajouter au panier |
     | [!UICONTROL Trigger] | addToCart |

   - Saisissez les paramètres de tracking **[!UICONTROL Checkout option]** suivants :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Option de passage en caisse |
     | [!UICONTROL Trigger] | checkoutOption |

   - Saisissez les paramètres de tracking **[!UICONTROL PageView]** suivants :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Effectuez la configuration de suivi des **[!UICONTROL Product Click]** suivante :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Clic sur le produit |
     | [!UICONTROL Trigger] | productClick |

   - Effectuez la configuration de suivi des **[!UICONTROL Promotion Click]** suivante :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Clic de promotion |
     | [!UICONTROL Trigger] | promotionClick |

   - Effectuez la configuration de suivi des **[!UICONTROL Remove from Cart]** suivante :

     | Paramètre | Valeur |
     |--- |--- |
     | [!UICONTROL Track Type] | Événement |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | Supprimer du panier |
     | [!UICONTROL Trigger] | removeFromCart |

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Preview]** et vérifiez que les balises fonctionnent correctement.

1. Après avoir vérifié les paramètres, cliquez sur **[!UICONTROL Publish]**.
