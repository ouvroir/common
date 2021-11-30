---
title: Journal
since: 2021-11-30

---

# Discussion du 30 novembre 2021

## Fonctionnalités

### Identification et gestion de rôles utilisateurs

Rôles
- admin
- multiutilisateur
- groupes d’utilisateurs
- droits différentiés selon les répertoires
- Identité fédérée

### Stockage de fichiers dans différents formats

- arborescence de dossiers
- gestion des droits
- versionner (??)
- historique des interventions

Types de fichiers supportés
- fichiers images : jpg, svg, png, tiff, etc.
- vidéos, sons (optionnel)
- documents bureautiques (docx, odt, csv, md)
- fichiers pdf

Fonctionnalités d’importation
- glissé-déposé
- importation par lot
- API ou consommation d’API

### OCRisation des documents

### Moteur de recherche

### Gestion des métadonnées

- renseignement mandataire des métadonnées
- formulaires personnalisés selon les types de ressources
- exposition des métadonnées (DC, autres formats, OAI-PMH)

### Fonctionnalités de partage de contenus et de communication

- Annotation des contenus et commentaires
- Discussions, etc.
- Importation des documents dans Zotero

### Interfaces

- Exposition par l’intermédiaire d’API (Rest, graphql)
- compatibilité IIIF
- API pour populer

## Ce qu’il ne faut pas faire

Se contenter de définir des règles de nommage qui ne seront pas suivies

Une interface compliquée qui créée plus d’embuches que de faciliter le travail

« Une base de données »

Redocumenter les collections muséales (charger les documents individuellement et refaire des notices)


## Ce que l’on pourrait faire

Incorporer les processus dans l’interface

Accompagner les besoins

Faciliter la découverte, le classement et le partage des documents

Faciliter l’adoption de la solution présentée à partir de démonstration de fonctionnalités utiles


## Solutions à explorer
- Google Drive
- OneDrive / Sharedocs / Dropbox = WebDAV Web Distributed Authoring and Versioning
- [Strapi](https://strapi.io/)
- Zotero/Tropy/Omeka
- Bdd relationnelle personnalisée
- Bdd XML native
- Solid


### Google Drive
Avantages
- Familiarité
- Édition collaborative des documents
- Diversité des formats de fichiers supportés
- Gestion des droits / Partage / Annotation
- Versionning
- Compatibilité avec de nombreux services
- API

Inconvénients
- Propriétaire
- Manque de finesse dans la gestion des droits (version gratuite)
- Dépendance aux évolutions de l’API Google

Solution possible
- Création de pages pour la gestion des documents
- Formulaires qui populent l’API pour l’édition des documents

Ex : 

[*library*](https://open.nytimes.com/we-built-a-collaborative-documentation-site-deploy-your-own-with-the-push-of-a-button-134de99c42fc) New York Times 
- essentiellement une interface de recherche
- permet d'utiliser les documents directement

Google Drive CMS

### WebDAV

Avantages
- fine gestion des droits
- collaboration

Inconvénients
- pas de collaboration sur l’édition des documents
- interface technique est limitée

Solution possible

### Omeka-S

Avantage
- solution prédéfinie
- respect des standards
- possibilité d’utiliser des vocabulaires contraires
- flexibilité des modèles de métadonnées
- compatibilité Zotero et Trello
- API OAI-PMH

Inconvénients
- PHP
- interfaces standard peu accessibles
- plutôt obsolète et petite communauté

Questions
- quid de la gestion des images

### Strapi 

Avantage
- couche applicative (gestion utilisateurs, gestion des contenus, téléchargement des ressources, ...
- possibilité de créer toutes sortes d'entités (granularité assez proche de Drupal: unités de contenus configurables à la demande) Content Type Builder
- équivalent d'une base de données relationnelle mais avec une interface graphique
- vues configurables pour organiser le travail
- interface d'édition correcte, markdown
- back-end pour un headless CMS 
- API donc contenus exportables (JSON et GraphQL)
- possibilité de lier le site web du projet avec common, expots etc.
- libre et open source, beaucoup d'utilisateurs
- v4 

Inconvénients
- interface d'édition générique, n'est pas l'interface de publication (on édite les contenus sur un backend)
- gestion des utilisateurs payante (abonnement) mais gratuité pour l'éducation
- logiciels tiers créent une dette technologique assez forte: node.js, environnement pas très stable (beaucoup de dépendances plugins et npms, obsolescence rapide) + interface construite avec React
- durée de vie plutôt courte des CMS
- difficulté à trouver un client pour un headless CMS? trouver un développeur pour le faire

Solution possible
- Créer des formulaires pour chaque type de ressources, qu'on peut adapter au fur et à mesure des besoins
  
Questions à poser
- peut-on créer des structures arborescentes? 
- jusqu'à quel point peut-on personnaliser les métadonnées? 
- peut-on faire un entrepôt OAI-PMH? 
- aeut-on configurer l'exposition JSON? (JSONLD)
- gestion des images

### Base de données XML native

Avantage
- compatibilité avec les standards de métadonnées
- flexibilité de l’API
- authentification
- libre et open source et basé sur des standards
- compatibilité possible avec une chaîne éditoriale
- pas de backend
- produit plus personnalisé et plus extensible
- stabilité
- moteur de recherche plein-texte intégré
- Emmanuel est heureux

Inconvénients
- pas d’API standardisée
- partir de zéro (pas tout à fait, précédents emcd)
- créer les interfaces (glisser déposer, édition) mais il existe des libraires
- identité fédérée (Shiboleth, OpenID: Google, Github) à développer
- environnement Java

Questions
- quid de la gestion des images

 
Solution possible
- organisation client/serveur.
- RestXQ + BaseX + XForms ou un framework JavaScript.

### Solid 

Avantage
- moderne
- architecture Solid
- flexibilité
- composabilité
- composants pré-existants
- coopératif et libre

Inconvénients
- très expérimental
- possibilité d’usine à gaz

solution possible

Exemple: happy-dev.fr briques logicielles déjà conçues, Startin'blox: framework Solid et webComponents
