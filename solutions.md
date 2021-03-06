# Solutions possibles




## Islandora

[web](https://islandora.ca/), [sandbox demo](https://islandora.ca/try), [git repo](https://github.com/Islandora/islandora), [documentation](https://islandora.github.io/documentation/)

- **Islandora**  is an open-source software framework designed to help institutions and organizations and their audiences  collaboratively manage, and discover digital assets using a  best-practices framework
- Drupal CMS as interface. Build in website front-end. Feodra as storage layer
- Islandora 7: Drupal as presentation layer, Islandora makes drupal manage the fedora contents. Options to add custom "toppings"
- Islandora 8: more modular application. All components can be removed and repalces easily. Customisation through the UI
- Exploration du sandbox: interface très complexe, il faudrait l'explorer avec un use case plus clair pour comprendre ses forces et ses limites. Notes une liste de fonctionnalités à tester?


### Specs

- code en php
- JSON-LD et support IIIF
- 1st release: avril 2017, latest release: 28 oct 2021
- beaucoup de modules et dépendances mais toutes garanties libres et open source: **Islandora and all of its components are free to use and always will be.**
- installation avec Docker ou Ansible

Avantages
- solution existante avec une communauté d’utilisateurs étendue
- respect des standards de métadonnées
- signalement des ressources (JSONLD OAI-PMH)
- Moteur de recherche SolR
- orienté préservation numérique
- libre et open source
- IIIF
- API

Inconvénients
- PHP
- dépendance à Drupal
- plus orienté conservation durable que travail
- interface complexe et un peu datée

Solution robuste avec de riches fonctionnalités mais peu user-friendly. Comme on craint que la solution soit peu adoptée par les utilisateurs, il n’est pas certain qu’Islandora soit le meilleur choix. A fortiri lorsque nous n’avons pas d’attentes importantes en termes de pérennisation ou de signalement. 

## Library (NYTimes)

[demo](https://nyt-library-demo.herokuapp.com/), [git repo](https://github.com/nytimes/library), [documentation](https://nyt-library-demo.herokuapp.com/how-to-use-library)

- Library is a Collaborative Documentation Site (wiki) powered by a Google Docs backend
- Google Drive API to retrieve the content from each document and render it inside the wiki: makes ifrom Google Docs searchable and renders its contents, creates a clean interface for viewing and navigating between those documents.
- editing interface handled by Google Docs
- Documents in Library are searchable (recherche plein texte), taggable, and can be grouped by desks or categories.
- formats supportés: text, images et gif
- most Library users would be looking for documentation by keyword or  phrase, so we placed a search bar as a prominent element on each page.  When a user searches for a document, the results will include relevant  documents, annotated with information about who last edited it, and  where in Library the document is stored
- With a little code knowledge, you can customize the site language, create themes or use a specific authentication method. Library can be deployed with or without an additional customization layer, and we encourage you to explore [the example](http://nyt-library-demo.herokuapp.com/) to see how easy it is to use.

### Specs

- code en javascript, avec scss et ejs
- Licence: Library a une licence Apache 2.0 mais se base sur Google Drive
- 1st release printemps 2019, latest relesase: 1.4.2, novembre 2021
- [Liste de dépendances](https://github.com/nytimes/library/blob/main/package.json) non négligeable, dont pusieurs services google
- [requiert](https://github.com/nytimes/library#development-workflow) Google Cloud Database products (peut devenir [payant](https://cloud.google.com/datastore/pricing) au-delé d'une certaine utilisation)
- [deploy](https://github.com/nytimes/library#deploying-the-app) avec [Heroku](https://www.heroku.com/pricing) (mais ils disent qu'on peut le faire avec la version gratuite), Google App Engine, Docke ou autonome (standard VPS)

## GoogleDrive CMS

[demo](https://docs.google.com/spreadsheets/d/12BJi_Ln7z5Q5KIuJcPNwPRKwUQg3G7B7NNO7APFWUQk/edit#gid=0), [git repo](https://github.com/max-barry/google-drive-cms)

- Google Drive CMS is a Google Sheet with a custom menu option to publish the content of that spreadsheet to your site's API

### Specs

- last commit: 6 years ago. **No longer maintained**: recommends projects like [Prismic.io](https://prismic.io/) and [Contentful](https://www.contentful.com/) that tackle similar problems
  - prismic est quand même [cher](https://prismic.io/pricing). Licence: Apache 2
  - Contentful  Licence: MIT
- Licence MIT, mais se base sur les services google

## Google Drive for Developers

[Developer products](https://developers.google.com/workspace/products?hl=fr), [code samples](https://github.com/googleworkspace)

- [Drive API ](https://developers.google.com/drive/api?hl=fr)

- [Google Workspace developer products](https://developers.google.com/workspace/products?hl=fr)

  

## Startin'blox

[documentation générale](https://docs.startinblox.com/), [git repo](https://git.startinblox.com/framework/sib-core)

- Startin’Blox est un framework de web components qui se branchent sur des sources de données Solid avec une importance accordée à la simplicité  d’usage de la technologie.  mais cette complexité est totalement masquée pour l’utilisateur final
- plateforme pour aider à gérer la collaboration entre pairs
- outil qui permet également de développer des applications facilement et de les interconnecter avec les standards existants
- vous pourrez alors vous connecter et échanger de l’information très  simplement avec d’autres plateformes, tout en gardant le contrôle de vos données


### Specs

- code en typescript
- first release: il y a trois ans, last release: ~septembre 2021
- licence: MIT
- [Liste des dépendences](https://git.startinblox.com/framework/sib-core/-/blob/master/package.json)
- standards ouverts: implémente les standards d’échange de données [SoLiD](https://solid.inrupt.com/) et ceux des [Web components](https://www.webcomponents.org/)
- Startin’Blox is a front framework, based on a server named [DjangoLDP](https://git.startinblox.com/djangoldp-packages/djangoldp/) and based on [Django](https://www.djangoproject.com/).The DjangoLDP server is adapted to be compatible with Linked Datas convention.

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


## OSF

[doc](https://cosdev.readthedocs.io/en/latest/), [git repo](https://github.com/CenterForOpenScience/osf.io)

- Find papers, data, and materials to inspire your next research  prooject. Search public projects to build on the work of others and find  new collaborators.
- Start a project and add collaborators, giving them access to protocols  and other research materials. Built-in version control tracks the  evolution of your study.
- Store data, code, and other materials in OSF Storage, or connect your  Dropbox or other third-party account. Every file gets a unique,  persistent URL for citing and sharing.
- Share papers in OSF Preprints or a community-based preprint provider, so others can find and cite your work. Track impact with metrics like  downloads and view counts.

### Specs

- Javascript et python
- Licence: Apache 2

## HSS Commons

- publications, blog entries, collections of resources/links, tagged content
- groups to share content and conversation, privatly or openly (members, blog, calendar, collections, forum ...)
- each project has a wiki area, to-do list management, microblogging tool, option to publish data and manage publications

[terms](https://hsscommons.ca/aboutus/terms)

- Le Canadian HSS Commons est une initiative de partenariat  d’Environnements d’implémentation de nouvelles connaissances (INKE), en  partenariat avec l’Institut canadien de connaissance sociale, CANARIE,  Calcul Canada, le Laboratoire de cultures textuelles électroniques, la  Fédération des sciences humaines, l’Association du langage moderne (MLA) et autres
- Le site web de https://hsscommons.ca est exploité par une communauté de chercheurs et hébergé par l’Université de Victoria
- https://hsscommons.ca is available to researchers and scholars at  CAF-member institutions. It is intended for researchers studying in the  Humanities or Social Sciences that are in current, good standing at  their home institution. Upon leaving your university, your access to the Site may be revoked. If you would like assistance transitioning your  content to another community, please contact us via [hsscommons@uvic.ca](mailto:hsscommons@uvic.ca).

<!-- website restructuring in progress, completion planned by Dec. 10. Don't see any chances on jan 10 2022-->

### Specs

- free
- ORCID integration

<!--Erudit est nommé comme partenaire, on peut leur demander s'ils s'en servent?-->






## Google Drive
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

## WebDAV

Avantages
- fine gestion des droits
- collaboration

Inconvénients
- pas de collaboration sur l’édition des documents
- interface technique est limitée

Solution possible

## Omeka-S

Avantage
- solution prédéfinie
- respect des standards
- possibilité d’utiliser des vocabulaires contraints
- flexibilité des modèles de métadonnées
- compatibilité Zotero et Trello
- API OAI-PMH

Inconvénients
- PHP
- interfaces standard peu accessibles
- plutôt obsolète et petite communauté

Questions
- quid de la gestion des images

## Strapi + client web

Avantages
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
- on voudrait des champs de saisies plus ergonomiques
- gestion des utilisateurs payante (abonnement) mais gratuité pour l'éducation
- logiciels tiers créent une dette technologique assez forte: node.js, environnement pas très stable (beaucoup de dépendances plugins et npms, obsolescence rapide) + interface construite avec React
- durée de vie plutôt courte des CMS
- difficulté à trouver un client pour un headless CMS? trouver un développeur pour le faire
- pas de gestion des notes de bas de page, ni  des typographie fine (exposants)

Solution possible
- Créer des formulaires pour chaque type de ressources, qu'on peut adapter au fur et à mesure des besoins
  

Questions à poser
- peut-on créer des structures arborescentes? 
- jusqu'à quel point peut-on personnaliser les métadonnées? 
- peut-on faire un entrepôt OAI-PMH? 
- aeut-on configurer l'exposition JSON? (JSONLD)
- gestion des images

## Base de données XML native + client web

Avantages
- compatibilité avec les standards de métadonnées
- flexibilité de l’API
- authentification
- libre et open source et basé sur des standards
- compatibilité possible avec une chaîne éditoriale
- pas de backend
- produit plus personnalisé et plus extensible
- stabilité
- moteur de recherche plein-texte intégré
- Emmanuel est heureux :)

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

### bdd locale + Svelte

Svelte - client, communique avec une base de données avec un point d'accès REST.

Serveur (baseX , express NodeJs): 

- quand tu reçois ce type de requête, tu fais x 
- quand tu reçois ce type de requête, tu fais y (image --> serveur de stockage d'image type cantaloupe)

Possibilité d'avoir une interface unifiée avec BaseX qui gère les fiches (modèle documentaire: XQuery pour manipuler les langages structurés)

Stocker les fichiers dans des bases de données spécifiques (webDav)

hors ligne: encapsuler Svelte dans un composant electron pour avoir une app locale mais il faudrait développer un module pour la synchronisation avec le serveur (Native Svelte)

option mobile: charger les photos directement depuis le téléphone? 



## Cantaloupe

### version lourde
version alimentée par une API
- cantaloupe est le serveur d'image
- webDav pour les fichiers
- client web qui fait toutes les interactions (en svelte ou react)
    - authentification (module à réutiliser pour tout le partenariat)

### version légère
version parasite Bernard l'hermitte
- on squatte des services web (qui propose une API) et on se crée un client pour s'y connecter
- outils low tech orchestrés par notre client

## Zotero

suite aux rencontre d'équipes axe1 et axe3: orientation vers [Zotero](https://www.zotero.org/support/)

Avantages: 

- client desktop MacOS + windows + linux + web (& data syncing)
- extension navigateur
- API
- produit des bibliographies et modèle de citation
- retrieve PDF metadata + PDF indexing can be enabled (At this time, only PDF full text content (and plain text files) can be  indexed by Zotero. Other document types (e.g., .docx, .odt, .epub)  cannot be indexed by Zotero. ) + annotations (zotfile)
- Feed RSS pour faire des états de l'art etc.
- tags, notes, relations (zutilo plugin)
- proxy pour lecture de contenus avec accès institutionnel

À discuter: 

- si on utilise Zotero, on héberge sur Zotero directement aussi? Où on héberge dans un service distinct qui crée (par exemple) des url pérennes? 
  - Zotero lab: $30 per user, with a minimum of 15 users.
  - Zotero institution: universitaire, mais pourrait peut-être fonctionner pour le Partenariat comme groupe de recherche
  - [Zotero + webDav](https://www.zotero.org/support/preferences/sync#file_syncing)
- quels formats (attachements) ne sont pas pris en charge? à tester?
- [importation](https://www.zotero.org/support/kb/importing_standardized_formats): formats bibliographiques standardisés type RDF, CSL JSON et BibText
- versionnement? 
- explorer les [plugin](https://www.zotero.org/support/plugins)

Ajouts : développements "par dessus"

- "formulaires" modèle types (exposition, document d'archive....)
- droits différenciés plus complexes
  - In order to start using OAuth to create API keys on behalf of users, you must [register your application with Zotero](https://www.zotero.org/oauth/apps) to obtain a Client Key and Client Secret for use during all future  OAuth handshakes between your application/website and zotero.org. Note  that after you obtain an API key for a particular user these client  credentials are not required for further Zotero API requests.

- visualisation
- vue par image / édition / annotation des images? 
- éditeur de texte (markdown? versionner le texte?)
- diffusion RSS



Étapes de travail: 

- mise en place dans les projets actuels
  - définir les "utilisations de bases", liste de bonnnes pratiques à respecter
  - définir architecture (qui crée des collections pour des droits d'accès bien gérés: group member vs group admin → library reading, library editing, file editing)
- phases de développement d'un outil plus avancé 
