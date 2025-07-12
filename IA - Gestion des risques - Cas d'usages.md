# Intelligence artificielle - Cas d'usages

## Objet du document
**Ce document propose des exemples de typologies de cas d’usages qui reposent sur de l’intelligence artificielle (IA).**
Il n’a pas pour vocation à servir de référence, mais à souligner la variété des cas d’usages et des techniques sous-jacentes, et il peut également être utile à la description d’un système dans une démarche de gestion des risques ou de projets.

[Avant-propos](#avant-propos)<br/>
[Introduction](#introduction)<br/>
[1. Exemple : [ISO/IEC 24030]](#1-exemple---iso-iec-24030)<br/>
[2. Exemple : liste de cas d'usages](#2-exemple--liste-de-cas-dusages)<br/>
[3. Exemple : tableau périodique de cas d'usages](#3-exemple--tableau-périodique-de-cas-dusages)<br/>

## Avant-propos
Ce document s’inscrit dans un [ensemble de documents méthodologiques](https://github.com/matthieu-grall/ai), en amélioration continue, destinés à aider les organismes à gérer les risques liés à l’IA, et qui peuvent être utiles ensemble ou séparément.
Les [documents de référence](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Documents%20de%20r%C3%A9f%C3%A9rence.md) sont utilisés entre crochets dans le corps du document.

Il est placé sous la **licence** suivante :
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

Les principaux **contributeurs** sont les suivants :
- Matthieu GRALL, expert-conseil en management des données, sécurité de l’information, protection de la vie privée et nouvelles technologies ;
- Cécile LAMARQUE, sociologue.

Les **versions** du document sont les suivantes :
| <center>**Version**</center> | <center>**Action**</center> | <center>**Éditeur**</center> | 
| --- | --- | --- | 
| 05/04/2025 (v0.1) | Création du document, ajout d’une liste empirique de cas d’usages et du tableau périodique proposée par XPRIZE | Matthieu GRALL | 
| 10/04/2025 (v0.2) | Ajout d’une introduction, améliorations mineures (clarifications, compléments, mise en cohérence avec les autres documents) | Matthieu GRALL | 
| 16/04/2025 (v0.3) | Transformation du document en _markdown_ | Cécile LAMARQUE | 
| 18/04/2025 (v0.4) | Amélioration du _markdown_ | Matthieu GRALL | 
| 07/05/2025 (v1.0) | Finalisation d'une première version complète, cohérente, et en _markdown_ | Matthieu GRALL |
| 11/07/2025 (v1.1) | Changement du titre du document, ajout d'exemples de produits et services et du pays de provenance dans la liste des cas d'usages, simplification et harmonisation des chapitres introductifs, corrections mineures | Matthieu GRALL |

Les **ressources** suivantes ont été utilisées :
- Tableau périodique de cas d’usages : par XPRIZE.

## Introduction
[Pour le Parlement européen](https://www.europarl.europa.eu/topics/fr/article/20200827STO85804/intelligence-artificielle-definition-et-utilisation), **l’IA représente tout outil utilisé par une machine afin de « _reproduire des comportements liés aux humains, tels que le raisonnement, la planification et la créativité_ »**. Cette définition peut être élargie en incluant les comportements dépassant les capacités humaines, puisque les ordinateurs actuels parviennent aujourd’hui à les surpasser dans certaines tâches (bien que la compétence de l’ordinateur s’arrête généralement à l’exécution de cette tâche).

**C’est un domaine de l'informatique né en 1956<sup><a href="#note1" id="ref1">[1]</a></sup> qui vise à créer des machines capables de réaliser des tâches qui nécessitent normalement l'intelligence humaine**. Il s'agit de simuler des processus cognitifs tels que l'apprentissage, la résolution de problèmes, la prise de décision et la compréhension du langage naturel. Contrairement à une simple programmation de règles précises, l'IA cherche à donner aux machines la capacité d'apprendre et de s'adapter à de nouvelles situations sans être explicitement programmées pour chaque éventualité.

En synthèse, le [Rapport _Task Force_ IA] fournit l’explication suivante : 

_« L’IA est utilisée dans les applications où il s’agit de :_
- _**détecter/reconnaître des données** (texte, sons, images, vidéos), ou prédire des données futures ;_
- _**rechercher des corrélations entre des données** pour en déduire un comportement générique ou lever une alerte en cas de comportement anormal ;_
- _**optimiser des problèmes à forte combinatoire** (ex : flux logistiques ou trajectoires d’aéronef) ;_
- _**raisonner sur des données symboliques pour déduire** ou pour diagnostiquer._

_Du point de vue technique<sup><a href="#note2" id="ref2">[2]</a></sup>, l’intelligence artificielle comprend deux branches majoritaires :_
- _les **approches symboliques** basées sur le raisonnement (systèmes à base de règles) ; et_
- _les **approches connexionnistes** plus proches de l’empirisme, fondées sur l’apprentissage à partir de grandes bases de données (réseaux de neurones). »_ 

**Il est toutefois très difficile d’établir une typologie de cas d’usages détaillés**, tant les domaines de recherche et applications liées à l’IA sont nombreux, variés, parfois croisés, et en évolution permanente.

**Ce document propose donc uniquement des exemples de typologies.**

## 1. Exemple : [ISO/IEC 24030]

Cette norme internationale, payante et dont le contenu ne peut être reproduit ici, recense des cas d'usage de l'IA et les classe par secteur d'activité.
Elle peut utilement servir de référence pour positionner ses projets.

## 2. Exemple : liste de cas d'usages

Le tableau suivant présente une liste non exhaustive de cas d’usages qui reposent sur de l’IA, en indiquant les principales techniques d’IA mises en œuvre et des exemples d’outils qui les mettent effectivement en œuvre :
| <center>**Micro-cas d’usages**</center> | <center>**Principales techniques d’IA**</center> | <center>**Exemples d’outils**</center> |
| --- | --- | --- |
| Détecter certains types de sons dans un signal audio (alarmes, moteurs, dispositifs spécifiques) | Apprentissage supervisé, Réseaux de neurones convolutifs (CNN), Modèles de reconnaissance sonore | IA DUST — Dust Audio Classifier (FR), SONARWORKS — Sound Calibration (EE), GOOGLE — AudioSet (US), RESEMBLE.AI — Voice Cloning (CA) |
| Reconnaître les visages et les états émotionnels dans des images ou vidéos | CNN, Deep Learning, Analyse d'expressions faciales | OPTACARE — Emotion Analytics (FR), LIGHTON — Vision Emotion (FR), AFFECTIVA — Emotion AI (US), MICROSOFT — Face API (US), NTECHLAB — FindFace (RU) |
| Reconnaître certains types d'objets dans des images ou vidéos | CNN, YOLO, Mask R-CNN, Vision Transformers (ViT) | PHOTOROOM — Object Remover (FR), HUGGING FACE — Transformers Vision (FR), GOOGLE — Vision AI (US), AMAZON — Rekognition (US), OPENCV — Computer Vision Lib (INTL) |
| Analyser les données du capteur pour détecter des objets/situations | Apprentissage supervisé/non supervisé, Séries temporelles, Fusion de capteurs | DIAGRAMS TECHNOLOGIES — Sensor Fusion (FR), NVIDIA — Isaac Sim (US), SIEMENS — MindSphere (DE), GE DIGITAL — Predix (US) |
| Reconnaître la langue parlée et/ou états émotionnels dans un signal audio | NLP, Classification audio, Transformateurs | PRIMAA — Emotion Speech API (FR), VOXYGEN — TTS/STT Solutions (FR), GOOGLE — Speech API (US), IBM — Watson Speech to Text (US), SONANTIC — Emotional Speech (UK) |
| Reconnaître une voix individuelle dans un signal audio | Biometrie vocale, CNN audio | DIGEIZ — Voice ID (FR), NUANCE — Gatekeeper (US), MICROSOFT — Azure Speaker Recognition (US) |
| Détecter des signatures audio spécifiques (moteur, sonnette, etc.) | Classification audio, CNN spectrogrammes | IA DUST — Device Sound Identifier (FR), ZOUNDREAM — BabyCry AI (FR), GOOGLE — AudioSet (US), FREESOUND — Annotated Sounds (ES) |
| Reconnaître des personnes spécifiques dans des images/vidéos | Supervised Learning, Deep Learning, Visages | PHOTOROOM — Person Finder (FR), CLEARVIEW AI — Face Search (US), PIMEYES — Face Match (PL), AMAZON — Rekognition (US) |
| Reconnaître un objet concret dans une image ou vidéo | Matching, CNN, Vision par ordinateur | PHOTOROOM — Smart Selector (FR), GOOGLE — Lens (US), APPLE — Vision Pro (US), OPENCV — Template Matching (INTL) |
| Analyser les données pour identifier des faits/événements | NLP, Classification, Transformers | GISKARD — Data Event Extractor (FR), PALANTIR — Gotham (US), IBM — Watson Discovery (US), BIGML — Predictive Modelling (ES) |
| Analyser des textes pour extraire entités, temps, lieux, faits | NLP, NER, Transformers | GISKARD — NER Tagger (FR), SPACY — NLP lib (US), STANFORD NLP — CoreNLP (US), IBM — Watson NLU (US) |
| Prévoir des événements/conditions futures | Prédiction, Réseaux neuronaux, ARIMA, LSTM | BEINK DREAM — Forecast Engine (FR), PREVISION.IO — AutoML Platform (FR), FACEBOOK — Prophet (US), AMAZON — Forecast (US), GOOGLE — Cloud Forecast (US) |
| Expliquer des événements à partir d’états passés | Causalité, Bayesian nets, XAI | SHIFT TECHNOLOGY — Claims Analytics (FR), IBM — Explainable AI (US), GRAKN.AI — Knowledge Base (UK) |
| Utiliser des preuves pour appuyer conclusions ou prédictions | Raisonnement, Logique, XAI | DOCAPOST — ProofChain (FR), WOLFRAM — Alpha (US), IBM — Watson (US), ONTOTEXT — GraphDB (BG) |
| Créer un plan d’action selon objectifs & conséquences | Planification, RL, Modèles décisionnels | MISTRAL AI — Magistral (FR), OPENAI — Gym (US), DEEPMIND — AlphaZero (UK), AUTOGPT — Goal Planning (INTL) |
| Créer une solution à un problème (avec/sans action) | Algorithmes, IA heuristique | MISTRAL AI — Codestral (FR), IBM — CPLEX (US), GOOGLE — OR-Tools (US), MICROSOFT — Solver Foundation (US) |
| Choisir une solution selon les faits & objectifs | Recommandation, IA décisionnelle | SHIFT TECHNOLOGY — Claims AI (FR), SALESFORCE — Einstein (US), IBM — Decision Platform (US), GOOGLE — Optimize (US) |
| Générer des textes ou explications en langage naturel | NLP, LLM, Génération | MISTRAL AI — Le Chat (FR), LIGHTON — Text Generator (FR), OPENAI — ChatGPT (US), GOOGLE — Gemini/Bard (US), ANTHROPIC — Claude (US) |
| Représenter le sens sémantique d’un texte | Embeddings, Graphes de connaissance | MISTRAL AI — Magistral (FR), GOOGLE — Knowledge Graph (US), WORD2VEC — Embeddings (US), CONCEPTNET — Commonsense (INTL) |
| Découvrir relations entre caractéristiques visibles et cachées | Clustering, Apprentissage non supervisé, IA causale | GISKARD — Feature Explorer (FR), SCIKIT-LEARN — Clustering (FR), TENSORFLOW — Embedding Projector (US), PYCARET — AutoML (US) |
| Découvrir de nouvelles catégories sémantiques | Clustering (K-means, DBSCAN), Non supervisé | GISKARD — Category Modeler (FR), H2O.AI — AutoML (US), BIGML — Cluster Analysis (ES), RAPIDMINER — Studio (DE) |
| Appliquer des règles pour soutenir actions/conclusions | Règles, Ontologies, Graphes | DIAGRAMS TECHNOLOGIES — Rule Engine (FR), CYC — Knowledge Engine (US), IBM — Watson Knowledge Studio (US), NEO4J — Graph DB (SE) |
| Contrôler des véhicules autonomes | RL, LIDAR, Perception visuelle | NAVYA — Autonom Shuttle (FR), TESLA — Autopilot (US), WAYMO — Driver (US), CRUISE — Origin (US) |
| Contrôler des robots en zone intérieure, avec humains | Vision, RL, NLP | DOCAPOST — Robot Pepper AI (FR), BOSTON DYNAMICS — Spot (US), NVIDIA — Isaac (US), SOFTBANK — NAO/Pepper (JP) |
| Manipuler des objets dans environnement humain | Robotique, Vision, Préhension | DIAGRAMS TECHNOLOGIES — Cobot Systems (FR), UNIVERSAL ROBOTS — UR (DK), ABB — YuMi (CH), GOOGLE — Everyday Robots (US) |
| Communiquer entre humain et machine | NLP, Chatbot, Vocale | ALBERT — Chatbot État (FR), DIGEIZ — Voice Assistant (FR), GOOGLE — Assistant (US), APPLE — Siri (US), AMAZON — Alexa (US) |
| Contrôler des systèmes non physiques (ex : commerce) | IA décisionnelle, Trading, RPA | SHIFT TECHNOLOGY — Payment Integrity (FR), BLOOMBERG — Terminal (US), TRADE IDEAS — AI Trader (US), KENSHO — Analytics (US) |

## 3. Exemple : tableau périodique de cas d'usages

Les cas d’usages de systèmes basés sur l’IA peuvent aussi être représentés sous la forme d’un tableau périodique, comme le propose [XPRIZE](https://community.digilogic.africa/resource/the-periodic-table-of-ai/) :

![XPRIZE AI periodic table](https://danielschristian.com/learning-ecosystems/wp-content/uploads/2017/01/AI-PeriodicTable-Dec2016.jpg)

| <center>**Acron.**</center> | <center>**Cas d'usage**</center> | <center>**Description synthétique**</center> |
| --- | --- | --- |
| Ar | *Audio Recognition* | Détecter certains types de sons (alarmes, contrainte du dispositif, automoteur) dans un signal audio | 
| Fr | *Face Recognition* | Reconnaître les visages et les états émotionnels dans les images ou les signaux vidéo | 
| Ir | *Image Recognition* | Reconnaître certains types d'objets dans des images ou des signaux vidéo | 
| Gr | *General Recognition* | Analyser les données du capteur pour détecter les types d'objets et/ou les situations seules à partir du signal | 
| Sr | *Speech Recognition* | Reconnaître la langue parlée et/ou des états émotionnels en général dans un signal audio | 
| Si | *Speech Identification* | Reconnaître une voix individuelle dans un signal audio | 
| Ai | *Audio Identification* | Détecter les signatures audio (un moteur spécifique ou une sonnette spécifique) à partir de signaux audio | 
| Fi | *Face Identification* | Reconnaître des personnes concrètes dans des images ou des signaux vidéo | 
| Ii | *Image Identification* | Reconnaître un objet concret dans une image ou une vidéo | 
| Gi | *General Identification* | Analyser les données du capteur pour détecter des objets et/ou des situations uniquement à partir du signal | 
| Da | *Data Analytics* | Analyser les données pour identifier certains faits et/ou événements qui représentent les données | 
| Te | *Text Extraction* | Analyser des textes pour extraire des informations sur les entités, temps, lieux et faits qui sont inclus exclusivement dans le texte | 
| Pi | *Predictive Inference* | Prévoir des événements ou conditions à l'avenir basée sur la compréhension d'un état actuel du monde et son fonctionnement | 
| Ei | *Explanatory Inference* | Expliquer des événements ou des États dans le monde réel sur la base de la compréhension des États précédents | 
| Sy | *Synthetic Reasoning* | Utiliser des preuves à l'appui de conclusions sur l'état réel du monde, une prédiction ou une explication | 
| Pl | *Planning* | Créer un plan d'action fondé sur un ensemble d'objectifs, une compréhension de l'état réel du monde et la connaissance des actions et de leurs conséquences | 
| Ps | *Problem Solving* | Créer une solution à un problème qui peut être lié ou non à l'utilisation d'actions | 
| Dm | *Decision Making* | Choisir une direction ou solution particulière sur la base des faits disponibles, d'autres solutions et d'un certain nombre d'objectifs | 
| Lg | *Language Generation* | Créer des textes et/ou des explications en langage naturel basés sur une certaine compréhension du monde | 
| Lu | *Language Understanding* | Créer une représentation sémantique du sens d'un texte qui montre le contexte et une certaine compréhension du fonctionnement du monde | 
| Lr | *Relationship Learning* | Reconnaître les relations entre les caractéristiques qui peuvent être utilisées pour prédire la présence d'un ensemble de caractéristiques cachées si d'autres sont visibles | 
| Lc | *Category Learning* | Reconnaître les nouvelles catégories de valeurs sémantiques fondées sur les collections de caractéristiques | 
| Lt | *Knowledge Refinement* | Répondre aux connaissances ou aux règles qui existent déjà en réponse à l'utilisation pour soutenir des actions ou des conclusions | 
| Ml | *Mobility Large* | Contrôler des véhicules autonomes qui interagissent avant tout avec d'autres véhicules | 
| Ms | *Mobility Small* | Contrôler les robots qui se déplacent à travers les zones intérieures, travaillant et interagissant avec les gens | 
| Ma | *Manipulation* | Manipuler des objets avec lesquels les gens travaillent régulièrement | 
| Cm | *Communication* | Soutenir l'exécution de différentes formes de communication entre l'Homme et la machine | 
| Cn | *Control* | Contrôler d'autres machines lorsqu'aucune action n'est nécessaire dans le monde physique (ex : commerce automatisé) | 

<br/>
<br/>
<a name="note1" id="note1">[1]</a> Cf. [conférence de Dartmouth](https://fr.wikipedia.org/wiki/Conf%C3%A9rence_de_Dartmouth). [↩](#ref1)
<br/>
<br/>
<a name="note2" id="note2">[2]</a> L'étendue de l'IA est vaste et englobe plusieurs branches interdépendantes. On retrouve l'apprentissage automatique (machine learning), où les systèmes apprennent à partir de données sans être explicitement programmés, l’apprentissage profond (deep learning), utilisant des réseaux neuronaux artificiels à plusieurs couches pour traiter des informations complexes, le traitement du langage naturel (TLN - NLP) permettant aux machines de comprendre et de générer du langage humain, la vision par ordinateur (computer vision) permettant aux machines de "voir" et d'interpréter des images, et la robotique, combinant l'IA avec des systèmes physiques pour créer des robots intelligents. [↩](#ref2)