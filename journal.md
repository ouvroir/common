---
title: Journal
since: 2021-11-30

---
# Journal

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

