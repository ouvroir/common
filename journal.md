---
title: Journal
since: 2021-11-30

---
# Journal

## Nouvel état de la situation

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
- 



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

Discussion de solutions possibles avec Svelete ou Islandora
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

