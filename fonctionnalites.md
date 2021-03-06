---
Since: 2021-10-27
---

# Cahier des charges fonctionnelles et techniques

## Descriptif FCI

La BDD est destinée à rassembler, décrire avec des métadonnées appropriées toutes les sources mobilisées et les contenus documentaires produits dans le cadre du partenariat (redéploiements de collections (axe 1), citoyennes (axe 2), dépouillement des dossiers d’acquisition et des politiques institutionnelles (axe 3 et 4), et de rassembler les sources visuelles et audiovisuelles pour la préparation de l’Encyclopédie. Il s’agit d’un système de gestion documentaire multi-utilisateurs qui permet l’archivage, le signalement et le partage de la documentation à travers des interfaces faciles d’emploi et qui sert de plateforme de travail collaborative pour tous les chercheur·se·s et les auxiliaires de recherche engagé·e·s dans le projet.

La base de données sera produite par un prestataire externe spécialisé dans les applications bibliothéconomiques en utilisant le gestionnaire de contenus libre et open source [Omeka-S](https://omeka.org/s/) qui offre les fonctionnalités nécessaires pour la description des ressources culturelles avec des métadonnées métiers (Dublin Core qualifié, BIBO, LIDO, BIO-CRM) et permet l’utilisation de vocabulaires structurés au format SKOS. Omeka-S permet d’alimenter un entrepôt OAI-PMH à destination des moteurs de recherche spécialisés en sciences humaines ainsi qu’une interface programmable (API REST) pour connecter les ressources avec l’Encyclopédie.

## Rétroplanning 

### prévision 2021-10

- 2021-06 livrable
- 2021-03 contrat
- 2021-01 appel d’offre
- 2021-12 cahier des charges fonctionnelles et techniques

### prévision 2022-01

- 2021-08 livrable
- 2021-05 contrat
- 2021-03 appel d’offre
- 2022-02 cahier des charges fonctionnelles et techniques

## Proposition initiale

La publication de l’Encyclopédie numérique de CIÉCO nécessite la création d’une chaîne éditoriale structurée adossée à une base de données documentaire destinée à rassembler et décrire tous les contenus produits dans le cadre du partenariat. Celle-ci constitue **l’infrastructure numérique et collaborative** du projet de recherche.

Il s’agit donc de développer une **plateforme de travail et une base de données multi-utilisateurs** (+++) destinée à l’ensemble du partenariat de recherche. Les coûts propres à la publication du site web de présentation du projet et de l’Encyclopédie (design graphique, implémentation web, et travail éditorial) sont affectés distinctement au financement du partenariat par le CRSH.

Les développements informatiques reposent principalement sur l’assemblage de **briques logicielles libres et open source** (+++), l’utilisation de standards et de modèles de métadonnées ouverts (++), afin de faciliter la pérennisation à long terme de l’information numérique et le signalement des ressources en contexte culturel et académique.

### Base de données documentaire

La base de données documentaire du Partenariat CIÉCO est destinée à rassembler et décrire avec des métadonnées appropriées toutes les sources mobilisées et les contenus documentaires produits dans le cadre du partenariat (métadonnées sur les accrochages de collections, dépouillements d’archives, et sources visuelles et audiovisuelles).

C’est un système de gestion documentaire multi-utilisateurs qui permet l’archivage, le signalement et le partage des ressources avec des métadonnées appropriées. La base de données sera produite en utilisant le Gestionnaire de contenus libre et open source Omeka-S qui offre les fonctionnalités nécessaires pour la description des ressources avec des modèles de métadonnées métiers appropriés (Dublin Core qualifié, BIBO, LIDO, BIO-CRM, utilisation de vocabulaires SKOS [fonctionnalités offertent par défaut par Omeka-S]) tout en présentant des interfaces collaboratives facile d’emploi pour les chercheurs du projet et les auxiliaires de recherche.

Omeka-S présente des fonctionnalités par défaut pour le signalement des ressources par l’intermédiaire d’un entrepôt OAI-PMH (https://www.openarchives.org/pmh/) à destination des moteurs de recherche spécialisés en sciences humaines (https://www.rechercheisidore.fr, OAIster https://www.ocls.org/fr/oaister.html ainsi qu’une interface programmable (API) qui permet d’interfacer les ressources avec l’Encyclopédie.

Analyse des besoins (6 jours)
Déployement du CMS Omeka-S et création des rôles utilisateurs (2 jours)
Conception des modèles d’interface (7 jours)
Intégration des vocabulaires et des schémas de métadonnées (5 jours)
Programmation des interfaces et intégration des fonctionnalités (12 jours)
Validation de l’application et correction des bugs (2 jours)

## Remarques sur l’expression des besoins

- les droits peuvent être variables selon les utilisateurs
- les types de contenus à gérer sont de types variés (Biblio, pdf, images, etc.)
- idéalement on devrait pouvoir forcer l’utilisateur à renseigner certains champs
- les impératifs de signalement des ressources peuvent être discutés et sont subordonnés aux aspects fonctionnels

---

## Énoncé des fonctionnalités



### Gestion collaborative des contenus

#### Espaces de travail

Plusieurs espaces de travail différentiés. Vues configurables

#### Gestion des droits d’utilisateurs

Gestion des droits différentiée.
Tous les utilisateurs n’ont pas accès à tous les documents, certains accès sont réservés. 

Login ORCID? identité fédérée - 1 login pour tout ce qui est relié au partenariat dans l'idéal (site web..)

Les droits sont les suivants :
- visibilité ?
- lecture
- lecture et écriture



#### Interfaces de travail

- Saisie de champs obligatoires
- markdown? quel éditeur de texte
- saisie dans l'interface ou dans un back-end



- Importation en lot
- Modification en masse
- Accessibilité (handicap)

#### Travail hors ligne

L’accès réseau n’est pas toujours disponible dans les archives pour la collecte de données. L’application permet de travailler hors ligne et des mécanismes de mise à jour asynchrones sont implémentés pour synchroniser les modifications.

Priorité : moyenne



#### Versionnement 

Versionnement des modifications

priorité: moyenne

#### Collaboration en temps réel

Permettre le travail collaboratif en temps réel (type Google Drive)? 

priorité: basse?

#### Gestion des tâches

attribution de tâches à effectuer / tableau de bord (to-do list, work flow, progression)

priorité: basse

#### Communication entre les pairs

fonctionnalité de commentaire (hypothesis?)

live chat : priorité basse

#### Documentation interne

wiki pour chaque série de document (partage du protocole de recherche), structurer (*enforce*) la documentation

priorité: basse - moyenne 

#### Blog de recherche interne

publication d'entrées de blog liées aux contenus et au processus de recherche (microblogging)

priorité: base

### Moteur de recherche

Moteur de recherche plein texte sur les métadonnées

Souhaite-t-on indexer automatiquement les documents PDF ?
Appliquer de la reconnaissance automatique de caractère.

Priorité : basse

#### Partage des ressources

Gestion du partage et de la publication des documents



### Gestion des fichiers et des métadonnées

#### Types de fichiers supportés

- pdf
- jpg ? autres formats d’image: png, tiff (normaliser jpg et jpeg)
- traitements de textes, tableurs ?

#### Gestion de structures arborescentes

Les fonds archivistiques de même que les instruments de recherche présentent habitullement des structures arborescentes (dossier, sous-dossiers, et document).

Priorité : basse

#### Standards de métadonnées supportés

- Dublin Core qualifié

Formats archivistiques
- EAD
- EAC-CFP ?
- RAAD???

Comment décrire les images et les pdf, est-ce que Dublin Core suffit ?
- Images ?
- PDF 

Est-ce qu'il va y avoir des archives dans d'autres langues que le français? MBAC? 

#### Annotation des images

annotation des images

priorité: basse

#### Prise en charge des images

#### Metrics

évaluation quantitative de l'utilisation (vue, modification, partage, citation...) des documents

Priorité: basse

### Signalement et exposition des données

#### API 

avoir notre propre API? 

#### Compatibilité avec une chaine éditoriale

#### Signalement des ressource avec OAI-PMH

#### Exposition des ressources en LOD

#### Exposition des métadonnées avec Zotero

Synchronisation avec l'API de Zotero (références bibliographiques, expositions)

#### Dépôt pérenne

Priorité : basse

Requiert une solution pérenne sur 7 à 10 ans minimum, sans nécessairement sortir l'artillerie lourde en matière de pérennisation des données.

- solutions privées: risques d'arrêt de maintenance de la solution, d'augmentation exponentielle des coûts
- logiciels libres: existe-t-il des solutions "modernes" tant du point de vue technique que de l'interface utilisateur? (éviter Drupal par exemple)

URL persistant pour chaque document? (pour le partage et la citation)

#### Export des données 

prévoir une façon d'exporter les données en batch ? 

### Aspects techniques

#### Technologie

- Standards
- WebDAV
- SoLiD et Webcomponents? 
- Serveur IIIF (cantaloupe)
- Base de données orientées document / SQL

#### Serveur

- installation (Docker, Ansible)

