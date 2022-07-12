# Common - cahier des charges fonctionnelles

Juin 2020

## Contexte et objectifs

### Contexte du laboratoire et du partenariat CIÉCO

L’**Ouvroir** d’histoire de l’art et de muséologie numériques de l’Université de Montréal, est un laboratoire de recherche destiné à soutenir le travail conduit dans le cadre du Partenariat « Des nouveaux usages des collections dans les musées d’art » ([CIÉCO](http://www.cieco.co)). Ce laboratoire fournit à l’ensemble de l’équipe un équipement de pointe pour mener la recherche mais aussi pour expérimenter et développer de nouveaux usages des collections numérisées qui utilisent le web, les techniques de visualisation 3D et la réalité virtuelle et augmentée. Il donne l’occasion de créer une infrastructure éditoriale solide pour l’Encyclopédie numérique et de produire trois développements informatiques qui seront mobilisés dans les différents axes de la recherche : d’abord avec la mise en place d’une plateforme collaborative de travail pour le travail sur les archives ; ensuite avec la création d’un outil numérique consacré à la documentation des accrochages de collections ; enfin, avec la création d’une librairie JavaScript destinée à faciliter la production et le déploiement de dispositifs d’expositions numériques et de l’illustration de l’Encyclopédie. C’est aussi une structure polyvalente qui permet de faciliter le travail collaboratif et l’organisation de téléréunions avec les partenaires muséaux et internationaux du projet. Sa création permet de doter le Canada d’un équipement de recherche dédié à l’expérimentation et le développement d’innovations dans le domaine de l’histoire de l’art et de la muséologie numérique. L’Ouvroir bénéficie du soutien de l’[Université de Montréal](https://www.umontreal.ca/), du [Fonds Canadien pour l’Innovation](https://www.innovation.ca/) et de la [province du Québec](https://www.economie.gouv.qc.ca/bibliotheques/programmes/aide-financiere/programme-de-soutien-aux-organismes-de-recherche-et-dinnovation-pso/cofinancement-du-gouvernement-du-quebec-aux-programmes-de-la-fondation-canadienne-pour-linnovation-fci/fonds-dinnovation/).

### *Common*

*Common* est une infrastructure numérique à concevoir pour soutenir la recherche en histoire de l’art et en muséologie. En tant que portail documentaire, *Common* a pour rôle de rassembler, structurer et diffuser la recherche produite par les membres du CIÉCO. 

#### Qu’est-ce que la recherche en histoire de l’art et en muséologie aujourd’hui? 

La recherche menée par le Partenariat est s’organise en 4 axes. La description des quatre axes nous semblent importante car ils seront repris pour présenter les cas d’usage particuliers auxquels l’outil devra répondre.

> **Axe 1: «la collection exposée»** (dir. Marie Fraser) concerne l’histoire des expositions de collections. À partir des documents d’archives des musées partenaires (documents de montage d’exposition, textes, photographies de vues d’exposition), la recherche prend forme à deux échelles dans *common*. D’une part, il s’agit de documenter l’histoire des expositions en créant des entrées (sous la forme de données structurées) pour chaque exposition. Ces données offriront la possibilité d’avoir une vue d’ensemble ainsi que de produire une analyse quantitative. D’autre part, certaines expositions seront analysées en profondeur, ce qui requiert d’accumuler et de produire des métadonnées à propos de nombreux documents d‘archive qui concernent une même exposition. 
>
> **Axe 2: «la collection engagée»** (dir. Johanne Lamoureux) s’intéresse à l’implication citoyenne dans les musées, c’est-à-dire aux initiatives qui impliquent le public lors d’exposition ou d’événements. L’équipe recherche et souhaite documenter des archives, ou du moins des traces, de ces initiatives. Il y en a toutefois très peu (à date), sous forme très disparates dont des boîtes contenant des objets hétéroclites tels que des post-it.
>
> **Axe 3: «la collection élargie»** (dir. Mélanie Boucher)a pour sujet les nouvelles formes d’œuvres dans les collections, particulièrement en art contemporain performatif. La recherche dans les archives muséale se concentrera sur des œuvres particulières, dont les dossiers d’acquisition et de conservation seront étudiés de près. De plus, certains projets numériques (3D, AR, VR) feront parfois partie de la documentation de ces œuvres.
>
> **Axe 4 : «la collection partagée»** (Emmanuel Château-Dutier) explore le partage et l’ouverture des collections muséales. La documentation des projets numériques prend tout d’abord la forme d’une bibliographie commentée, mais se prolongera également en essais et documentation des formes et usages d’expositions numériques en AR ou VR notamment.

#### Organisation du travail

Chaque axe est dirigé par un·e professeur·e, quelques co-chercheur·se·s et une équipe étudiante qui se renouvelle sur une base réguilère (estimation: ~20 personnes qui contribuent activement par année). 

*Common* sert comme espace de travail interne, il ne doit être accessible que pour les personnes impliquées dans le partenariat

#### Analyse des besoins

Suite à l’analyse des besoins effectuée à l’hiver 2022, nous avons relevés les points suivants pour ce cahier des charges: 

- la recherche en cours, 
- utilisation de Zotero
- données dans des tableurs type googleSheets





### Objectifs de la prestation

Conserver les recherches effectuées de façon centralisée, pour que la recherche effectuée l’an 1 par l’étudiante x soit accessible 5 ans plus tard par Prof Y.



#### Rassembler

Les chercheur·se·s effectuent des recherches dans les archives des musées. On ne veut pas numériser l’ensemble des archives du musée mais on peut souhaiter conserver des reproductions (numérisations) des documents et extraire des métadonnées pour le renseigner. 



#### Structurer

Produire des métadonnées 



#### Diffuser

Produire des liens pérenne pour le matériel sélectionné qui sera cité et partagé dans des publications, notamment dans l’Encylopédie. 



### 











### Parties concernées par le déroulement du projet et ses résultats

#### Réponses à l’appel d’offres

Adresser les réponses au Laboratoire Ouvroir: ouvroir@umontreal.ca

#### Responsable du projet: Lena Krause





#### Direction scientifique: Emmanuel Château-Dutier, Kristine Tanton



#### Direction générale: Johanne Lamoureux







## Description fonctionnelle des besoins

*description la plus générique possible, pour préciser nos besoins au fur et à mesure*

 

### Architecture - briques      

architecture de base / template d’interactions / briques



#### Créer un module d’authentification

- authentifier les chercheur·se·s qui se connectent à la plateforme
- enregistrer leurs activités de façon horodatée (voir: versionner les contenus)

#### Donner des droits d’accès différenciés

- donner des accès à des nouveaux chercheurs
- par défaut, tout est ouvert, mais on peut limiter l’accès à des contenus <!-- comment ? par individu, par "dossier" -->

Les droits sont les suivants :

- visibilité ?
- lecture
- lecture et écriture

#### Personnaliser (modifier) l’interface 

- choisir les contenus sur la page d’accueil 
- choisir les contenus dans le tableau de bord
- thème (clair / sombre)
- taille de la typo

#### Mapper des fonctionnalités à des raccourcis claviers

<!-- à détailler-->



#### Conserver l’historique de création et modification des contenus

qui a créé, importé ou modifié un contenu ou ses métadonnées





#### Importer et consulter des contenus externes (API)

Zotero

- compte Zotero instutionnel (espace stockage illimité)
- qu’est-ce qu’il arrive si les gens suppriment dans zotero? 
- 

API Google Sheets

#### Moteur de recherche

moteur de recherche plein texte sur les métadonnées

- recherche par type contenu (seulement les expositions | les images | les documents): priorité haute
- recherche au sein de l’ensemble des contenus (expositions, bibliographie, images): priorité basse

#### Serveur d’images

- Cantaloupe
- téléverser, ajouter des métadonnées, consuler
- autoriser la diffusion (à l’interne par défaut oui, à l’externe par défaut non)



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
- modifier les droits d’accès (interne)/ droits de diffusion(externe)

##### Supprimer des données

- conserver ce qui est supprimé? 







#### Tableau de bord

- vue d’ensemble des données de recherche



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

Une livraison est souhaitée d’ici décembre 2022.

### Conditions de livraison

L’ensemble de la prestation devra être réalisée sous licence libre.