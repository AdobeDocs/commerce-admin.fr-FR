---
source-git-commit: bb5da9eea16601303b62ccc06327c6a832062c49
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%
---
# Problèmes résolus Adobe Commerce B2B (v1.5.4-alpha1)

## B2B v1.5.4-alpha1

*13 octobre 2026*

23 problèmes ont été résolus dans le code Adobe Commerce B2B 1.5.4-alpha1. Un sous-ensemble des problèmes résolus inclus dans cette version est décrit ci-dessous.

### Interface utilisateur d’administration

#### [B2B] Les quantités de produits groupés ne sont pas conservées après la mise à jour des prix dans les devis principaux

Correction d’un problème en raison duquel la quantité d’un article groupé dans un devis négociable par l’administrateur revenait à sa valeur précédente après modification de la quantité dans la grille à la suite d’une modification de configuration via la boîte de dialogue Configurer.

_ACP2E-5005_

### B2B

#### La page Détails du devis [B2B] (storefront et admin) perd les informations article/produit lorsque le produit associé est supprimé du catalogue

Correction du problème où les produits non vendables disparaissaient des devis négociables finalisés

_ACP2E-4680_

#### Quantité de produit groupée non mise à jour correctement après l’envoi du devis depuis le serveur principal

Correction d’un problème en raison duquel les quantités d’options de produit groupé n’étaient pas mises à jour lors de la reconfiguration d’un devis négociable à partir du panneau d’administration. Auparavant, les modifications apportées aux quantités des options de groupement via le bouton Configurer étaient ignorées silencieusement.

_ACP2E-4801_

#### La grille [CLOUD] [B2B] Admin Companies provoque une CPU MySQL élevée — requête corrélée type_société / NOMBRE

Correction du problème en raison duquel la grille Admin Companies (Clients → Entreprises) entraînait une utilisation élevée de MySQL CPU et des sessions de base de données longues. Auparavant, la détermination du type d&#39;entreprise (parent/enfant/entreprise) pour chaque ligne nécessitait une sous-requête corrélée par rapport à la table company_relation qui se déclenchait une fois par ligne d&#39;entreprise, ce qui rendait à la fois les requêtes de liste et de nombre total O(N²) à l&#39;échelle ; le correctif remplace cela par une seule JOIN préagrégée qui s&#39;exécute une fois quelle que soit la taille du jeu de données.

_ACP2E-4846_

#### Paiement sur le compte (B2B) - Bouton Modifier la commande manquant pour les commandes en attente alors que visible pour le contre-remboursement

Le bouton Modifier la commande est désormais disponible pour les commandes passées avec paiement en compte. Auparavant, il n’était pas possible de modifier une commande passée avec paiement en compte lorsque la commande est en attente

_ACP2E-4877_

#### Délai d’expiration PHP permettant d’économiser l’entreprise B2B avec un super utilisateur multisociété

Enregistrer une société B2B ou charger la page du super-utilisateur de la société dans l&#39;administrateur ne dépasse plus le temps d&#39;exécution maximal PHP lorsque le super-utilisateur de la société est affecté à un très grand nombre de sociétés.

_ACP2E-4967_

#### [ON-PREM] devis négociables non mis à jour comme prévu

Correction du problème en raison duquel les devis négociables n&#39;étaient pas mis à jour lorsqu&#39;un produit présent dans un devis négociable actif était supprimé.

_ACP2E-5001_

#### Chèques supplémentaires « Paiement sur compte » volatils

Correction du problème en raison duquel Paiement sur compte, un mode de paiement destiné exclusivement aux membres de l’entreprise B2B, pouvait être sélectionné par des clients individuels (B2C) lors du passage en caisse. Auparavant, ces clients étaient autorisés à tort à procéder au paiement sur le compte au lieu de recevoir une erreur de type « Mode de paiement non disponible ».

_ACP2E-5013_

#### L’action d’enregistrement de l’assistant de catalogue partagé efface la structure de tarification d’un catalogue partagé

Correction d’un problème en raison duquel l’action d’enregistrement de l’assistant de catalogue partagé effaçait la structure de tarification d’un enregistrement de catalogue partagé

_ACP2E-5015_

#### GraphQL customer.role renvoie une « erreur de serveur interne » pour les clients B2C sans entreprise

Correction du problème en raison duquel l’interrogation du client { role {...} } via GraphQL renvoie une « erreur de serveur interne » pour les clients B2C qui ne sont affectés à aucune société. Auparavant, cette requête déclenchait une erreur de type PHP, car un ID d’entreprise nul était transmis à une méthode avec un conseil de type entier strict.

_ACP2E-5017_

#### [B2B] La remise article du bundle n&#39;est pas appliquée lorsque les quantités d&#39;option sont mises à jour dans les devis principaux

Correction du problème en raison duquel une remise au niveau de l&#39;article appliquée à un produit groupé de prix dynamiques dans l&#39;administrateur de devis principal n&#39;était pas reflétée dans le sous-total ou le sous-total (sauf Colonnes de taxe) lorsque les quantités d’options du lot ont été mises à jour via la boîte de dialogue Configurer. Auparavant, la remise apparaissait dans la colonne remise mais ne réduisait pas le sous-total cité.

_ACP2E-5034_

#### La section Demande se recharge à chaque navigation de page

Correction du problème en raison duquel la section de demande d’approvisionnement déclenchait un rechargement AJAX inutile sur chaque navigation de page de produit et de catégorie. Auparavant, la section était rechargée à chaque chargement de page pour tout client dont les données de liste de demandes d&#39;approvisionnement n&#39;étaient pas vides, même si aucune modification n&#39;avait été apportée.

_ACP2E-5037_

#### [B2B] Erreur lorsque des données de région sont manquantes pour l’adresse de la société

Correction d’un problème en raison duquel la page Profil d’entreprise et la page Modifier le client d’administration affichaient une erreur lorsqu’une adresse d’entreprise faisait ajouter une région à son pays après l’enregistrement de l’adresse sans région. Désormais, l’adresse retourne correctement au texte de la région stockée au lieu de provoquer une erreur.

_ACP2E-5092_

#### Mise à jour de la société sur l’administrateur avec des paramètres régionaux non anglais réinitialisant la limite de crédit

Correction d’un problème en raison duquel la modification des détails d’une société B2B pouvait involontairement réinitialiser la limite de crédit configurée sur 0 lorsque les paramètres régionaux de l’administrateur différaient des paramètres régionaux par défaut. La limite de crédit est maintenant conservée correctement, sauf si elle est explicitement modifiée.

_ACP2E-5127_

#### [CLOUD] L’administration restreinte à un site web ne peut pas supprimer les clients lorsque leur user_id entre en conflit avec un entity_id client inaccessible

Auparavant, lorsqu’un administrateur restreint à un site web tentait de supprimer un client, le plug-in de vérification des autorisations du système comparait le propre ID utilisateur de l’administrateur à
ID d’entité client pour appliquer les restrictions hiérarchiques de la société, sans vérifier que l’utilisateur intérimaire était bien un client ; si l’ID d’utilisateur de l’administrateur s’est produit
pour coïncider avec l’ID d’entité d’un client non lié sur un site web auquel l’administrateur n’a pas pu accéder, le plug-in a tenté de charger cet enregistrement client inaccessible
et la suppression a échoué avec une erreur « d’autres autorisations sont nécessaires », même si l’administrateur disposait de droits valides sur le client en cours de suppression. Ce problème a été résolu
en ajoutant une condition pour que la comparaison des ID de client s’exécute uniquement lorsque l’utilisateur par intérim est véritablement un client, ce qui signifie que les suppressions lancées par l’administrateur contournent désormais entièrement cette vérification. les administrateurs restreints peuvent à nouveau supprimer des clients dans leur ou leurs sites web attribués sans être bloqués par des enregistrements de clients non liés et inaccessibles

_ACP2E-5146_

#### La commande B2B affiche un nom de société incorrect dans les commandes client d’administration

Correction d’un problème en raison duquel un nom de société incorrect était affiché pour les commandes fournisseur B2B dans les commandes client d’administration lorsqu’un utilisateur était affecté à plusieurs sociétés.
Le nom de la société s’affiche désormais correctement en fonction de la société associée à la commande.

_B2B-4656_

### B2B, panier et passage en caisse

#### [ON PREM] [B2B] Le chargeur de commandes rapides se fige lors de la tentative de chargement d’un fichier binaire se terminant par l’extension .CSV

Correction du problème en raison duquel le téléchargeur de fichiers de commande rapide acceptait tout fichier renommé avec une extension .csv, y compris les fichiers binaires. Auparavant, aucune validation de type MIME ou de contenu n’était effectuée, de sorte que les fichiers non CSV (par exemple les exécutables) pouvaient être chargés et traités comme s’il s’agissait de listes de SKU/QTÉ valides.

_ACP2E-5212_

### B2B, GraphQL

#### Inexactitude du nombre total de listes de demandes d&#39;approvisionnement GQL

Correction du problème lorsque la requête GraphQL requisition_lists renvoyait une valeur total_count incorrecte qui reflétait uniquement le nombre d&#39;éléments sur la page actuelle au lieu du nombre total d&#39;entités de liste de demandes correspondant aux critères de requête.

_ACP2E-4799_

### B2B, Commande

#### Aide sur le nettoyage des tables de devis de plus de 59M (impossible d&#39;exécuter sales_clean_quotes)

Correction du problème en raison duquel la tâche cron `sales_clean_quotes` expirait sur les instances comportant des tables de guillemets volumineuses. Auparavant, la requête de nettoyage sélectionnait inutilement toutes les colonnes de la table `negotiable_quote`, ce qui entraînait l’exécution par MySQL d’un tri de fichiers complet sur des millions de lignes ; et chaque citation était supprimée individuellement via la couche de modèle PHP, ce qui augmentait le coût de la performance.

_ACP2E-4891 - [contribution du code GitHub](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, Performances

#### [CLOUD] Suivi de ACSD-70033 : blocage de la table magento_catalogpermissions_index_product. continuation

Auparavant, la réindexation des autorisations de catalogue avec le catalogue partagé activé pouvait entraîner une erreur d’interblocage, entraînant l’échec de la réindexation. Désormais, la réindexation s’exécute correctement même lorsque plusieurs processus d’indexation s’exécutent simultanément.

_ACP2E-4844_

### Contenu

#### Les pages CMS créées pour différents sites web affichent des pages incorrectes dans frontend

Auparavant, dans les configurations multi-sites web, la clé de cache de la page de destination de la restriction du site web n’était pas définie par site web, ce qui entraînait la diffusion d’une page CMS incorrecte sur le storefront du site web secondaire. La clé de cache dans WebsiteRestriction/Controller/Index/Stub.php inclut désormais correctement l’ID de site web actuel résolu via le gestionnaire de magasin.

_ACP2E-4593_

### Framework

#### [B2B] Les commandes fournisseur ne sont pas converties automatiquement en commande client avec ActiveMQ

Correction d’un problème en raison duquel les consommateurs démarrés par cron ne traitaient pas les messages lorsqu’ActiveMQ était utilisé avec le protocole STOMP. Par conséquent, les commandes fournisseur approuvées automatiquement n&#39;ont pas été converties en commandes client. Le traitement des messages pour les files d’attente STOMP est désormais plus fiable et cohérent avec les implémentations des files d’attente DB et AMAP.

_ACP2E-4349 - [Contribution du code GitHub](https://github.com/magento/magento2/commit/08b91f1a) - [Contribution du code GitHub](https://github.com/magento/inventory/commit/239464da)_

### Installer et administrer

#### [Cloud] Correction des codes de subdivision ISO existants obsolètes

Mise à jour des codes de région pour 13 pays afin qu’ils correspondent à la norme ISO 3166-2. Auparavant, certains codes de région ne correspondaient pas à la norme, ce qui pouvait entraîner des problèmes au niveau des intégrations tierces et de la conformité internationale. Ajout de nouvelles régions pour la Belgique, la Colombie, l’Espagne, la France, l’Italie et la Lettonie. Codes de région mis à jour pour l’Autriche, la Colombie, le Costa Rica, l’Allemagne, l’Estonie, l’Espagne, la Finlande, la France, l’Inde, l’Islande et la Lettonie.

_ACP2E-4495 - [contribution du code GitHub](https://github.com/magento/magento2/commit/9b6a8bd9)_
