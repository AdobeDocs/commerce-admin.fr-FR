---
title: Sécurité
description: Découvrez les outils disponibles pour sécuriser vos magasins et vos données, ainsi que les directives d’un plan d’action de sécurité si vous détectez une compromission.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# Sécurité

Il existe plusieurs façons de sécuriser votre boutique et de maintenir la sécurité de vos données :

- Configurer [authentification à deux facteurs](security-two-factor-authentication.md)
- Implémenter [CAPTCHA](security-captcha.md) ou [reCAPTCHA](security-google-recaptcha.md)
- Configurez un [Analyse de sécurité](security-scan.md) pour chaque domaine de votre installation Adobe Commerce ou Magento Open Source.

>[!NOTE]
>
>Les magasins qui ont activé l’authentification [!DNL Adobe Identity Management Services] (IMS) ont Adobe Commerce et Magento Open Source 2FA natifs désactivés. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification Adobe n’ont pas besoin de s’authentifier à nouveau pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir Présentation de l’intégration [[!DNL Adobe Identity Management Service] (IMS)](../getting-started/adobe-ims-integration-overview.md).

Visitez le [Centre de sécurité](https://helpx.adobe.com/fr/security.html){:target="_blank"} pour obtenir les dernières informations sur les vulnérabilités potentielles, enregistrez-vous pour les notifications de sécurité d’Adobe et accédez au Centre de gestion de la confidentialité d’Adobe.

![&#x200B; Centre de sécurité &#x200B;](./assets/product-security-home.png){width="700" zoomable="yes"}

Pour plus d’informations sur les bonnes pratiques de sécurité, consultez la section [Sécurisation du site et de l’infrastructure Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=fr) du _guide d’implémentation_.

## Plan d’action pour la sécurité

Si vous pensez que votre site Adobe Commerce ou Magento Open Source est compromis, suivez ce plan d’action sans délai.

1. **Diagnostic** : exécutez une analyse pour établir le statut de sécurité de votre boutique Commerce. Commerce [Security Scan](security-scan.md) est un service gratuit proposé par Adobe. Il vous permet de surveiller vos sites Commerce à la recherche de risques de sécurité et de programmes malveillants connus, et de recevoir des notifications de sécurité.

1. **Clean** : embauchez un [consultant qualifié](https://solutionpartners.adobe.com/s/directory/?partner_type=1) ou un service en ligne pour nettoyer votre site de tout code malveillant. Certains membres de la communauté Commerce recommandent [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Recherchez le code exécutable restant dans le dossier `/media`. Supprimez tous les utilisateurs administrateurs inconnus et réinitialisez tous les mots de passe d’administration.

1. **Protection** : maintenez votre installation de Commerce à jour avec la version la plus récente. Si vous utilisez une ancienne version, appliquez tous les correctifs de sécurité dès qu’ils sont disponibles. Examinez et suivez les [bonnes pratiques de sécurité de &#x200B;](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Abonnez-vous aux [alertes de sécurité &#x200B;](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport** : si vous pensez avoir détecté une vulnérabilité spécifique dans Commerce, [signalez-le à Adobe](https://hackerone.com/adobe?type=team) en fournissant les détails techniques nécessaires.

1. **Mise à niveau** : pour une tranquillité d’esprit accrue, grâce à une prise en charge 24h/24 et 7j/7, planifiez dès maintenant votre mise à niveau vers [Adobe Commerce sur notre architecture cloud](https://business.adobe.com/fr/products/magento/cloud-delivery.html).
