Since: 2021-10-27

# Cahier des charges fonctionnelles et techniques

## Descriptif FCI

La BDD est destinée à rassembler, décrire avec des métadonnées  appropriées toutes les sources mobilisées et les contenus documentaires  produits dans le cadre du partenariat (redéploiements de collections  (axe 1), archives citoyennes (axe 2), dépouillement des dossiers  d’acquisition et des politiques institutionnelles (axe 3 et 4), et de  rassembler les sources visuelles et audiovisuelles pour la préparation  de l’Encyclopédie). Il s’agit d’un système de gestion documentaire  multi-utilisateurs qui permet l’archivage, le signalement et le partage  de la documentation à travers des interfaces faciles d’emploi et qui  sert de plateforme de travail collaborative pour tous les chercheurs et  les auxiliaires de recherche engagés dans le projet.

La base de données sera produite par un prestataire externe  spécialisé dans les applications bibliothéconomiques en utilisant le  gestionnaire de contenus libre et open source [Omeka-S](https://omeka.org/s/) qui offre les fonctionnalités nécessaires pour la description des  ressources culturelles avec des métadonnées métiers (Dublin Core  qualifié, BIBO, LIDO, BIO-CRM) et permet l’utilisation de vocabulaires  structurés au format SKOS. Omeka-S permet d’alimenter un entrepôt  OAI-PMH à destination des moteurs de recherche spécialisés en sciences  humaines ainsi qu’une interface programmable (API REST) pour connecter  les ressources avec l’Encyclopédie.

## Rétroplanning (hypothèse 2021-10)

- 2021-06 livrable
- 2021-03 contrat
- 2021-01 appel d’offre
- 2021-12 cahier des charges fonctionnelles et techniques

## Proposition initiale

La publication de l’Encyclopédie numérique de CIÉCO nécessite la création d’une chaîne éditoriale structurée adossée à une base de données documentaire destinée à rassembler et décrire tous les contenus produits dans le cadre du partenariat. Celle-ci constitue **l’infrastructure numérique et collaborative**  du projet de recherche.

Il s’agit donc de développer une **plateforme de travail et une base de données multi-utilisateurs** (+++) destinée à l’ensemble du partenariat de recherche. Les coûts propres à la publication du site web de présentation du projet et de l’Encyclopédie (design graphique, implémentation web, et travail éditorial) sont affectés distinctement au financement du partenariat par le CRSH.

Les développements informatiques reposent principalement sur l’assemblage de **briques logicielles libres et open source** (+++), l’utilisation de standards et de modèles de métadonnées ouverts (++), afin de faciliter la pérennisation à long terme de l’information numérique et le signalement des ressources en contexte culturel et académique.

Base de données documentaire

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

## Exemples

- https://open.nytimes.com/we-built-a-collaborative-documentation-site-deploy-your-own-with-the-push-of-a-button-134de99c42fc

