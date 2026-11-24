---
title: Notes de mise à jour de la découverte de produits d’IA
description: Consultez les notes de mise à jour de la découverte de produits AI pour les fonctionnalités d’enrichissement de catalogue et de PDP, les correctifs, les conseils de mise à niveau, les versions de Commerce prises en charge et les problèmes connus.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# Notes de mise à jour d’AI Product Discovery

Ces notes de mise à jour couvrent les mises à jour de l’enrichissement du catalogue et de l’enrichissement de la PDP, y compris les nouvelles fonctionnalités, les correctifs, les exigences de mise à niveau et les problèmes connus. Chaque entrée de version identifie l’extension ou le workflow affecté.

![Nouvelles](../assets/new.svg) Nouvelles fonctionnalités
![Correctif](../assets/fix.svg) et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

## Version 2.1.3 {#release-2-1-3}

*30 Novembre 2026*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 et 2.4.7 sur PHP 8.3 à 8.5. [!DNL Adobe Commerce as a Cloud Service]

La version 2.1.3 combine l’enrichissement de la page des détails du produit avec l’enrichissement du catalogue dans un nouvel élément du menu d’administration appelé **Découverte de produit IA**. En outre, la prise en charge s’étend à [!DNL Adobe Commerce as a Cloud Service].

## Version 2.1.2 {#release-2-1-2}

*22 Octobre 2026*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 et 2.4.7 sur PHP 8.3 à 8.5.

La version 2.1.2 de fait de l’enrichissement du catalogue une extension autonome. Elle comprend désormais tout ce qui était auparavant fourni par l’extension [!DNL Adobe Brand Visibility] distincte (`magento/llm-optimizer`) : application des suggestions approuvées au catalogue, restauration de celles-ci et protection de vos propres modifications contre le remplacement.

### Mise à niveau à partir de versions antérieures {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>La version 2.1.2 ne peut pas être installée avec l’extension [!DNL Adobe Brand Visibility]. Si vous l’avez installé, supprimez-le dans le cadre de la mise à niveau.

1. Supprimez l’extension [!DNL Adobe Brand Visibility], si elle est installée :

   ```bash
   composer remove magento/llm-optimizer
   ```

   Si l’extension a été installée en copiant ou en liant symboliquement `Magento/LlmoCatalog` dans `app/code`, supprimez ce répertoire. Ne désactivez pas uniquement le module : un module désactivé qui se trouve toujours sur le disque peut entraîner l&#39;abandon par `setup:upgrade` du tableau qui stocke les valeurs d&#39;origine des produits enrichis.

1. Mettez à jour l’enrichissement du catalogue et appliquez les modifications :

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   Videz le cache après la mise à niveau. La mise à niveau déplace les autorisations d’accès existantes vers de nouvelles ressources d’autorisation, et ces autorisations ne prennent effet que lorsque le cache est effacé.

### Conditions requises

![Nouveau](../assets/new.svg) **PHP 8.3 et [!DNL Adobe Commerce] 2.4.7 ou version ultérieure**—PHP 8.1 est en fin de vie et PHP 8.2 atteint sa fin de vie le 31 décembre 2026, donc ni l&#39;un ni l&#39;autre n&#39;est pris en charge. [!DNL Adobe Commerce] 2.4.6 et versions antérieures ne sont pas pris en charge.

### Nouvelles fonctionnalités

![Nouveau](../assets/new.svg) **[!UICONTROL AI Product Discovery]menu** : les pages d’enrichissement du catalogue ont désormais leur propre section dans la barre latérale d’administration. Accédez à **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. Auparavant, la page se trouvait sous **[!UICONTROL Catalog]**.

![Nouveau](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Pas encore disponible pour tous"} **[!UICONTROL Product Details Page Enrichment (Beta)]** : une nouvelle page sous **[!UICONTROL AI Product Discovery]** pour examiner les suggestions d’enrichissement pour les pages de détails du produit. L’enrichissement de la page des détails du produit est en version bêta et n’est pas encore disponible en général.

![Nouveau](../assets/new.svg) **Appliquer et restaurer les suggestions approuvées** : les mises à jour de nom et de description approuvées sont écrites dans le catalogue par cette extension. Commerce enregistre la valeur d’origine de chaque attribut enrichi la première fois qu’il est modifié. Une restauration restaure donc toujours la valeur que vous aviez avant l’enrichissement, même après l’application de plusieurs suggestions au même attribut.

![Nouveau](../assets/new.svg) **Vos modifications sont respectées**—Lorsque vous modifiez un nom ou une description enrichis dans le formulaire de produit Admin, avec **[!UICONTROL Update Attributes]**, ou par le biais d&#39;une importation, votre valeur est conservée et la suggestion associée est marquée *Obsolète*. Une modification apportée à l’étendue par défaut affecte uniquement les vues de magasin qui héritent de la valeur.

![Nouveau](../assets/new.svg) **L’accès en lecture seule au catalogue pour les suggestions**—[!DNL Commerce Catalog Agent] peut lire les données de produit, de catégorie, d’ensemble d’attributs et de type de produit pour sélectionner les produits à analyser. La lecture renvoie uniquement les attributs marqués **[!UICONTROL Used in Product Listing]**, ainsi que les attributs qui peuvent être enrichis. Il ne peut pas modifier les données du catalogue.

### Correctifs et améliorations

![Problème résolu](../assets/fix.svg) **La nouvelle tentative d&#39;application des rapports a réussi**—Si une demande d&#39;application des modifications est relancée alors qu&#39;elle est déjà terminée, la nouvelle tentative signale désormais les modifications comme appliquées au lieu de signaler qu&#39;aucune modification n&#39;a été apportée. Rien n&#39;est écrit deux fois.

![Problème résolu](../assets/fix.svg) **Seuls les services approuvés peuvent modifier le catalogue**—Appliquer et restaurer acceptent uniquement les requêtes provenant de [!DNL Commerce Catalog Agent]. Auparavant, tout jeton Adobe IMS valide était accepté. Le même contrôle s’applique désormais aux requêtes SOAP.

![Correction d’un problème](../assets/fix.svg) **Erreurs plus claires**—Une panne d’Adobe IMS renvoie désormais `401` au lieu de `500`, de sorte que la requête n’est pas retentée sur le catalogue et qu’un environnement Adobe IMS non reconnu est rejeté au lieu d’être traité comme une étape.

![Correction d’un problème](../assets/fix.svg) **Environnement Adobe IMS** : l’enrichissement du catalogue se connecte désormais par défaut à l’environnement Adobe IMS de production, y compris sur les instances connectées à un espace de données [!DNL Commerce Services] hors production. Auparavant, ces instances étaient envoyées à l’environnement d’évaluation.

![Problème](../assets/fix.svg) **Connexion après le changement de domaine [!DNL Adobe Brand Visibility]** : la page d’enrichissement du catalogue se charge désormais à partir de `abv.adobe.com`, ce qui corrige une boucle de connexion après que le domaine précédent a commencé à rediriger.

### Problèmes connus

![Problème connu](../assets/bug.svg) **Rôles avec un accès complet à [!UICONTROL Catalog]** : un rôle d’utilisateur enregistré avant cette version avec tous les **[!UICONTROL Catalog]** accordés conserve l’accès à la ressource **[!UICONTROL Catalog Enrichment Service API]**. Passez en revue ces rôles dans **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** et effacez cette ressource lorsqu’elle n’est pas nécessaire.

## Version 1.0.2 {#release-1-0-2}

Version initiale de la page d’administration de l’enrichissement du catalogue. Exige que l’extension [!DNL Adobe Brand Visibility] applique des suggestions au catalogue.
