---
title: Journal
since: 2021-11-30

---
# Journal *common*

## Séance de travail (22 mars 2022)

utilisation de Zotero pour les pdfs et archives

architecture client-serveur basée sur la consommation d'API qui permet de gérer des ressources avec Zotero, des images avec IIIF et un entrepot IIIF. On investit l'argent sur la construction d'une infrastructure qui serait un client web (associé à une base de données) qui permet de gérer un tableau de bord, d'entrer des données qui ne sont pas gérables par Zotero (événements historiques) et de les mettre en lien avec les ressources documentaires stockées dans Zotero et autres services web (serveur d'images cantaloupe)

peut-on faire un moteur de recherche avec des documents stockés en pdf? 

- restocker les documents
- héberger zotero: faire notre propre zotero, permet de raffiner l'autentification? 
- auto-héberger l'API Zotero?

https://www.zotero.org/blog/

auto-hébergement semble difficile faute de documentation, à vérifier en contactant Sean Takats (sean.takats@uni.lu)

```
Cher Sean,

Nous travaillons actuellement sur un projet de recherche pour lequel nous envisageons une utilisation plutôt intensive de Zotero au sein de l’équipe de recherche. Pour certaines fonctionnalités, nous nous demandons s’il ne pourrait pas être intéressant d’auto-héberger un serveur Zotero et éventuellement d’en augmenter les fonctionnalités.

Pourrais-tu, s’il te plaît, m’indiquer quelle est votre roadmap actuelle sur cet aspect du projet ? Avez-vous prévu à court ou moyen terme des évolutions de cette partie du logiciel dont il faudrait tenir compte ? Serait-il possible de contribuer utilement au logiciel d’une manière ou d’une autre ?

D’après la recherche préliminaire que nous avons faites dans le forum et la documentation, voici les ressources identifies.

Est-ce que c’est bien toujours ce repo qu’il faut utiliser
https://github.com/zotero/dataserver

Il était question d’une distribution Docker, où se trouve-t-elle ?
https://github.com/gfacciol/zotero_dataserver-docker

Nous avons-vu que la synchronisation des fichiers impliquait un serveur WebDAV sur Amazon.
```



La documentation est assez sommaire sur Github. Existe

https://forums.zotero.org/discussion/73721/zotero-self-hosted
https://forums.zotero.org/discussion/comment/309275
https://forums.zotero.org/discussion/comment/316306

https://github.com/zotero/dataserver
https://github.com/mrtcode/zotero-server
https://github.com/gfacciol/zotero_dataserver-docker





développeurs? 

- conjoint de Marina
- envoyer une demande sur Astro

- [ ] préparer une question pour le forum pour l'autohébergement + système de fichier avec webDav? 
- [ ] décrire ce que ferait le client, à quoi il doit correspondre
  - [ ] description la plus générique possible, pour préciser nos besoins au fur et à mesure
  - [ ] architecture de base / template d'interactions
  - [ ] vocabulaire graphique (composants, hayden designer? )
  - [ ] briques qui pourront évoluer selon les projets
- [ ] proposer une rencontre (demander à Josée un lundi qui pourrait fonctionner: 11 avril?) 
  - présenter le scénario Zotero
  - d'ici là, avancer au maximum sur le cahier des charges pour présenter les orientations principales
  - ateliers spécialisés pour chaque axe?

## Séance de travail (8 mars 2022)

### Tests Zotero
- utiliser l'API, semble fonctionner de façon complète (toutes les fonctionnalités logicielles)
- créer une couche par dessus pour ce qu'il manque (événements)


Svelte: permettrait de tweaker l'API Zotero
- utiliser svelte pour requêter l'API (js / graphql) 

Trouver un composant de base de données qui serait "directement pluggable"

### Quel format pour les données
#### couchDB et Mango DB
avantage: options hors ligne
inconvénient: SQL (ne fait pas de json)

### XML: language standardisé de manipulation de données 
- requis pour l'édition numérique
- 



## Séance de travail (7 mars 2022)



### Tests HSS commons

Création d'un projet et ajout de ressources externes

- lien vers le drive: difficulté à paramétrer
  - seule option = current directory... 
- github: ne fonctionne pas... (404 pour https://github.com/ouvroir/labouvroir)

Todo: old school mais fonctionnel

Notes: versionnement + commentaires, éditeur wiki markup, tags

Je me sens décidemment surveillée dans l'onglet *Updates*...

Proposition de rencontre le 17 mars, préparer une liste de questions d'ici là

### Test API

<!-- @lenamk start Postman_ cd ~/opt/Postman → ./Postman -->

#### Zotero

- [Client API javascript](https://github.com/tnajdek/zotero-api-client)
- requêtes de base très facile

#### Google

- on peut prendre un document et "publish to the web" mais ce serait public
- pour créer une API → Google Cloud Project
  - Google Cloud : 300$ free credits to explore and conduct an assessment of Google cloud platform
  - 20+ free products, up to monthly limits: [details and full program](https://cloud.google.com/free/docs/gcp-free-tier)
  - enable GoogleSheets API
  - create credentials 
    - Are you planning to use this API with Compute Engine, Kubernetes Engine, App Engine, or Cloud Functions? Applications running on GCE, GKE, GAE, and GCF can use Application Default Credentials and don't require that you create a credential.
  - 

### Installation cantaloupe

todo





## Rencontre de travail (3 mars 2022)

Penser malin, ne pas chercher nécessairement une solution qui fait tout.

- Quid des logiciels identifiés ? (bilan sur les recherches déjà faites)
- Quid des besoins exprimés par l’équipe ?
  - très changeants
- De quoi pourraient-ils avoir besoin auxquels ils ne pensent pas ?
- Comment se positionner en support à nos chercheurs ?
- Quels scénarios (Zotero) ?

### Quid des logiciels identifiés ? (bilan sur les recherches déjà faites)

#### Solutions logicielles dédiées pour le partage de documents ou de contenus en contexte de recherche


Il existe plusieurs solutions logicielles dédiées pour le partage de documents ou de contenus en contexte de recherche.
- Islandora (drupal)
- HSS Commons (HubZéro)
- Omeka-S

Ce sont des solutions libres développées en contexte académique qui présentent donc un certain nombre de caractéristiques intéressantes pour le travail que nous voulons mener :
- utilisation de standards de métadonnées descriptives
- exposition des données OAI-PMH
- orientation préservation et archivage à long terme
- compatibilité avec certains services d’identité numérique (ORCID, etc.)
- compatibilité avec certains outils de travail des chercheurs (Zotero)

Dans le cas d’Islandora et de HSS Commons, il s’agit de suites logicielles relativement complexes qui présentent plusieurs dépendances logicielles. L’utilisation des logiciels est plus ou moins ergonomique et nécessite sans doute un apprentissage important (tout particulièrement Islandora). Le modèle de plateforme pour les chercheurs développé par HSS Commons autour de HubZéro permet de disposer gratuitement des fonctionnalités administrées par un établissement de recherche au Canada. Toutefois HubZéro est surtout centré sur le partage de l’information scientifique et la création de communauté et est moins adapté qu’Islandora pour le travail sur la documentation figurée et les documents d’archives. Les fonctionnalités de gestion de fichiers restent très limités dans HubZéro qui mise plus sur le dialogue scientifique. 

Omeka-S est un système de gestion de contenu (CMS) particulièrement flexible qui permet l’utilisation de standards de description de métadonnées et offre une compatibilité avec Zotero et une API. Mais ses interfaces génériques sont peu ergonomiques à moins d’un investissement important dans le design d’interfaces. Les retours d’utilisateurs de plusieurs collègues utilisant le logiciel sont contrastés. Le logiciel repose sur une conception web relativement ancienne, et la nouvelle version ne bénéficie pas de développement très actifs depuis quelques années. Nombre de plugins initialement disponibles pour Omeka n’ont pas été portés dans Omeka-S.

Les trois solutions offrent une gestion fine des droits d’utilisateurs. L’interface d’administration d’Omeka ne permet pas de contrôler l’accès aux ressources qui restent visibles pour tous les utilisateurs.

Aucune des solutions passées en revue n’est réellement satisfaisante pour une approche visuelle des contenus. Les fonctionnalités d’affichage restent largement déterminées par l’outil ou le cadre technique utilisé par le logiciel.

- Islandora est une solution trop lourde à mettre en œuvre pour nos besoins et qui risque de présenter des difficultés importantes d’adoption. L’infrastructure repose sur Drupal et plusieurs dépendances.
- HSS Commons, ne constitue pas en soi une solution entièrement satisfaisante pour la gestion des fichiers et particulièrement des images mais ses fonctionnalités de communautés de recherche pourraient être mises à profit pour le projet. Il n’est pas très clair si le projet canadien dispose déjà d’une API. Les métadonnées sont très limités.
- Omeka-S présente un réel intérêt en raison de sa flexibilité et de sa compatibilité avec Zotero. La gestion des droits restent limité et plusieurs retours utilisateurs nous alertent sur les limites du logiciel. L’API utilise JSONLD mais avec des fonctionnalités très limitées.

#### Cantaloupe

##### version lourde
version alimentée par une API
- cantaloupe est le serveur d'image
- webDav pour les fichiers
- client web qui fait toutes les interactions (en svelte ou react)
    - authentification (module à réutiliser pour tout le partenariat)

##### version légère
version parasite Bernard l'hermitte
- on squatte des services web (qui propose une API) et on se crée un client pour s'y connecter
- outils low tech orchestrés par notre client

Ne pas démultiplier les recours aux prestataires de services pour éviter la surcharge.
Pb rédaction cahier des charges.

#### Développer un système de style

Exemple de [Carbon Design System](https://www.carbondesignsystem.com/)

Trouver une personne qui serait capable de créer des composants ou faire un thème à partir du système existant.
Faire appel à William pour faire l'intégration à l'interne. Créer l'API est léger.


#### Strapi
Inconvénients
- interface pas très commode, 
- gestion de format pdf


#### Google Doc
utiliser l'API pour récupérer les données dans le tableur

#### Standford IIIF services
Utilisation de IIF pour toutes les images?
Que faire des images de mauvaises qualités et des numérisation directement en PDF? PDF sur Zotero


#### Solution d’un client web
Outil de gestion des documents interne
- tableau de bord et dataviz (aiderait beaucoup à l'adoption)
- créer soi-même formulaire de saisies (fiches signalétiques)
- Zotero servirait pour le stockage des PDFs et les références bibliographiques
- gérer les interactions avec les APIs
- IIIF: visionneuse , annotations
- signalement des ressources
- authentification
- sécuriser le tout
- option en ligne/hors-ligne avec un client web qui peut être déployé comme une application avec Electron (multiplateforme), se connecte à une BD locale (compatible hors-ligne).


#### XML
Avantage:
- facilité pour Emmanuel pour faire des modifs
Inconvénient: 
- difficulté à trouver un dev

#### CouchDB
Avantages: 
- BD orientée document, en JSON
- facile d'utilisation
- crée des GraphQL
Inconvénients: 
- requiert langage intermédiaire SQL 

HSS commons comme outil de communication

### Plan 

d'ici fin mars

- cahier des charges
- justifier les choix


- explorer API Zotero

- lire la doc cantaloupe

- session installation locale de Cantaloupe (15 mars?) attention: config Java ou sinon, Docker

  

___

## Suivi de l'évaluation des besoins

Cas d’utilisations et sondage des fonctionnalités

#### Formats d’importation
Les besoins de gestion de fichiers sont très divers et incluent des fichiers bureautiques, des images.
- PNG, JPG, TIF
- PDF
- MSWord et Excel
- liens (renvois vers d’autres archives type radio-canada ou CCA)
- 3D (sketchUp)
- fichiers audio et vidéo
- Markdown

Les fichiers 3D et vidéos doivent être pris en charge optionnellement car ils peuvent être mieux gérés sur des applications dédiées.

#### Images

Les chercheur·se·s du projet manipulent abondamment des contenus visuels. Le travail sur ce matériau réclame des outils spécifiques pour travailler de manière commode.
- régularité - uniformité 
- prévoir l'uniformisation et le traitement minimal des images (bonnes pratiques pour scanner avec le téléphone)
- annotation des images : tout le monde y est favorable. À quel niveau peut-on l’implémenter ? Faire une recherche des plugins/outils libres

Se concentrer sur le signalement?

#### Vues 

- gestion des structures arborescentes
- chronologique, avec tags visibles

Importance d'expérimenter avec des mots-clés, la catégorisation, la création de concepts ou de notion. Permettre l'édition en batch pour attribuer ou enlever des *tags*? 

Pour analyse comparative: 
- prévoir la possibilité de visualiser deux ressources côte-à-côte pour les comparer (divise l'écran divisé en 2 fenêtres)
- sélection de ressources en une sous-collection 

#### Entités 

Est-ce une arborescence? Un document doit pouvoir être rattaché à plusieurs institutions/projets/événements tout comme à aucun (événement annulé ou qui n'a pas lieu. Document hors norme)

Axe de recherche <!--classer le contenu complet par axe? que faire de ce qui se recoupe?-->

Institution/établissement: 

- projet ? (exposition/médiation-initiative/acquisition/projet numérique...) <!-- que serait une politique (muséale ou gouvernementale)? --> 
- document <!-- Johanne: n'a pas nécessairement des documents "bien constitués"-->
- événement <!-- inclut les occurrences d'expositions?-->
- œuvre <!-- mais c'est typiquement le type d'entité qui est floue dans les cas d'études de l'axe 3-->

Si on pense cartographie, il faut penser le degré de description de l'emplacement de chaque entité

Liens avec de la bibliographie: par entité? (= un sous-dossier Zotero?)

Métriques (indicateurs) pour chaque entité? (utile pour les rapports CRSH notamment, mais aussi pour avoir un retour sur l'emploi de la recherche primaire par la recherche secondaire)

#### Méthodes de travail

Comment permettre la répartition des tâches, simplifier/aider à déléguer?

Importance de la confidentialité des documents: préciser les droits (accès, édition, partage...). Identifier les stratégies (qui, combien de temps, quelle utilisation, qui a le droit de publier en premier...)

Travail collaboratif - mode hors ligne: à discuter/réfléchir d'avantage

- consulter une page/entité en même temps? toujours possible. La modifier en même temps? non si ce n'est pas de la colalboration en temps réel, git permettrait de gérer une partie mais pas tout
- veut-on des feuilles de calcul et des tableaux directement dans la BDD? Si oui, préférable d'avoir la collaboration en temps réel puisque plusieurs personnes peuvent vouloir travailler dessus en même temps

Versionnement du travail <!--si ce sont des fichiers word ou excel, on fait comment?-->

Annotations type Hypothesis <!-- pour que ça fonctionne, se base sur l'URL-->

Saisie: champs structurés et typés <!--quelle méthode pour la validation? -->





## Rencontre du 11 janvier 2022

Discussion de solutions possibles avec Svelte ou Islandora
évaluation de la solution Svelte

## Recherche sur les solutions actuelles - 10 janvier 2022

évaluation d'Islandora


## Recherche sur les solutions actuelles - 7 décembre

Library (NYTimes)
GoogleDrive CMS
Google Drive for Developers
OSF
HSS Commons

## Discussion du 30 novembre 2021

### Fonctionnalités

#### Identification et gestion de rôles utilisateurs

Rôles
- admin
- multiutilisateur
- groupes d’utilisateurs
- droits différentiés selon les répertoires
- Identité fédérée

#### Stockage de fichiers dans différents formats

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

#### OCRisation des documents

#### Moteur de recherche

#### Gestion des métadonnées

- renseignement mandataire des métadonnées
- formulaires personnalisés selon les types de ressources
- exposition des métadonnées (DC, autres formats, OAI-PMH)

#### Fonctionnalités de partage de contenus et de communication

- Annotation des contenus et commentaires
- Discussions, etc.
- Importation des documents dans Zotero

#### Interfaces

- Exposition par l’intermédiaire d’API (Rest, graphql)
- compatibilité IIIF
- API pour populer

### Ce qu’il ne faut pas faire

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

