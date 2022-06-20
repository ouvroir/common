# Common - cahier des charges fonctionnelles

Juin 2020

## Contexte et objectifs

### Contexte du laboratoire et du partenariat CIÉCO

L’**Ouvroir** d’histoire de l’art et de muséologie numériques de l’Université de Montréal, est un laboratoire de recherche destiné à soutenir le travail conduit dans le cadre du Partenariat « Des nouveaux usages des collections dans les musées d’art » ([CIÉCO](http://www.cieco.co)). Ce laboratoire fournit à l’ensemble de l’équipe un équipement de pointe pour mener la recherche mais aussi pour expérimenter et développer de nouveaux usages des collections numérisées qui utilisent le web, les techniques de visualisation 3D et la réalité virtuelle et augmentée. Il donne l’occasion de créer une infrastructure éditoriale solide pour l’Encyclopédie numérique et de produire trois développements informatiques qui seront mobilisés dans les différents axes de la recherche : d’abord avec la mise en place d’une plateforme collaborative de travail pour le travail sur les archives ; ensuite avec la création d’un outil numérique consacré à la documentation des accrochages de collections ; enfin, avec la création d’une librairie JavaScript destinée à faciliter la production et le déploiement de dispositifs d’expositions numériques et de l’illustration de l’Encyclopédie. C’est aussi une structure polyvalente qui permet de faciliter le travail collaboratif et l’organisation de téléréunions avec les partenaires muséaux et internationaux du projet. Sa création permet de doter le Canada d’un équipement de recherche dédié à l’expérimentation et le développement d’innovations dans le domaine de l’histoire de l’art et de la muséologie numérique.

<!-- piger dans la newsletter pour ajouter du contenu --->

L’Ouvroir bénéficie du soutien de l’[Université de Montréal](https://www.umontreal.ca/), du [Fonds Canadien pour l’Innovation](https://www.innovation.ca/) et de la [province du Québec](https://www.economie.gouv.qc.ca/bibliotheques/programmes/aide-financiere/programme-de-soutien-aux-organismes-de-recherche-et-dinnovation-pso/cofinancement-du-gouvernement-du-quebec-aux-programmes-de-la-fondation-canadienne-pour-linnovation-fci/fonds-dinnovation/).

### *Common*

*Common* est une infrastructure umérique pour la recherche. En tant que portail documentaire, *Common* a pour rôle de rassembler, documenter et diffuser la recherche produite par les membres du CIÉCO. 





### État de la situation

#### Qu’est-ce que la recherche en histoire de l’art et en muséologie aujourd’hui? 

La recherche menée par le Partenariat 

4 axes : chaque axe = équipe étudiante qui se renouvelle aux quelques années (~20 personnes par année)

- axe 1 : la collection exposée - Marie Fraser. Histoire des expositions de collections
  - archives des musées (expositions) → documents de montage d'exposition (texte, photographies → vues d'exposition)
  - listes (données semi-structurées) d'exposition
- axe 2 : la collectin engagée - Johanne Lamoureux. Musées et implication citoyenne
  - initiatives qui impliquent le public au sein des musées
  - recherche des traces / "archives" mais il y en a peu, sous forme très disparate (boîte avec objets hétéroclites type post-it)
- axe 3 : la collection élargie - Mélanie Boucher. Nouvelles formes d'œuvres dans les collection (art contemporain - performatif)
  - archives des musées (acquisition, conservation d'œuvres de la performance)
  - numérique  → 3D AR/VR 
- axe 4 : la collection partagée - Emmanuel Château-Dutier. le partage et ouverture des collections
  - bibliographie des initiatives 3D dans les musées (documentation de projets numériques)
  - essayer et documenter les usages d'expositions numériques partagées (AR/VR)

Co-chercheur·se·s (~20) qui viennent compléter les recherches dans les quatres axes principaux

Maximum une 50aine de personnnes qui travaillent "en même temps" (la même année scolaire), mais sur 7 ans, il va y avoir du renouvellement et des changements au sein des équipes

L'objectif → conserver les recherches effectuées de façon centralisée, pour que la recherche effectuée l'an 1 par l'étudiante x soit accessible 5 ans plus tard par Prof Y.



#### Ce qu'on veut conserver

Les chercheur·se·s effectuent des recherches dans les archives des musées. On ne veut pas numériser l'ensemble des archives du musée mais on peut souhaiter conserver des reproductions (numérisations) des documents et extraire des métadonnées pour le renseigner. 

espace de travail interne: pour les personnes qui travaillent dans le partenariat





Analyse des besoins des chercheur·se·s: recherche en cours, utilisation de Zotero, données dans des tableurs type googleSheets



### Objectifs de la prestation









### Parties concernées par le déroulement du projet et ses résultats

#### Réponses à l’appel d'offres

Adresser les réponses au Laboratoire Ouvroir: ouvroir@umontreal.ca

#### Responsable du projet: Lena Krause





#### Direction scientifique: Emmanuel Château-Dutier, Kristine Tanton



#### Direction générale: Johanne Lamoureux







## Description fonctionnelle des besoins

*description la plus générique possible, pour préciser nos besoins au fur et à mesure*

 

### Architecture - briques      

architecture de base / template d'interactions / briques



#### Créer un module d'authentification

- authentifier les chercheur·se·s qui se connectent à la plateforme
- enregistrer leurs activités de façon horodatée (voir: versionner les contenus)

#### Donner des droits d'accès différenciés

- donner des accès à des nouveaux chercheurs
- par défaut, tout est ouvert, mais on peut limiter l'accès à des contenus <!-- comment ? par individu, par "dossier" -->

Les droits sont les suivants :

- visibilité ?
- lecture
- lecture et écriture

#### Personnaliser (modifier) l'interface 

- choisir les contenus sur la page d'accueil 
- choisir les contenus dans le tableau de bord
- thème (clair / sombre)
- taille de la typo

#### Mapper des fonctionnalités à des raccourcis claviers

<!-- à détailler-->



#### Conserver l'historique de création et modification des contenus

qui a créé, importé ou modifié un contenu ou ses métadonnées





#### Importer et consulter des contenus externes (API)

Zotero

- compte Zotero instutionnel (espace stockage illimité)
- qu'est-ce qu'il arrive si les gens suppriment dans zotero? 
- 

API Google Sheets

#### Moteur de recherche

moteur de recherche plein texte sur les métadonnées

- recherche par type contenu (seulement les expositions | les images | les documents): priorité haute
- recherche au sein de l'ensemble des contenus (expositions, bibliographie, images): priorité basse

#### Serveur d'images

- Cantaloupe
- téléverser, ajouter des métadonnées, consuler
- autoriser la diffusion (à l'interne par défaut oui, à l'externe par défaut non)



#### Base de données interne (entités)

##### Structurer des données

- CIDOC-CRM + thesauri de vocabulaires structurés

##### Ajouter de données

- expositions, œuvres (acquisitions Mélanie)
- identifiants uniques

##### Consulter des données

- chaque donnée a un identifiant unique (URI)

##### Modifier les données

- modifier les métadonnées
- modifier les droits d'accès (interne)/ droits de diffusion(externe)

##### Supprimer des données

- conserver ce qui est supprimé? 







#### Tableau de bord

- vue d'ensemble des données de recherche



#### Sécurité



#### Backups



vocabulaire graphique

## Contraintes



## Conditions

### Enveloppe budgétaire

L’enveloppe budgétaire pour la réalisation du projet se situe entre $[   ] et $[    ].
C’est la raison pour laquelle ce cahier des charges propose des niveaux de priorités
qui permettront d’adapter le périmètre de la prestation.

### Délais

Une livraison est souhaitée d'ici décembre 2022.

### Conditions de livraison

L’ensemble de la prestation devra être réalisée sous licence libre.