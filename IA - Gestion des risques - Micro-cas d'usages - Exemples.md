# Intelligence artificielle
## Micro-cas d'usages : exemples

### Contributeurs
**Matthieu GRALL**, expert-conseil en management des données, sécurité de l’information, protection de la vie privée et nouvelles technologies

**Cécile LAMARQUE**, <titre ?>

### Versions

| <center>**Version**</center>|<center>**Action**</center>|<center>**Éditeur**</center>|<center>**État**</center>|
| --- | --- | --- | --- |
| 05/04/2025 | Création du document, ajout d’une liste empirique de cas d’usages et du tableau périodique proposée par XPRIZE | Matthieu GRALL | Document de travail |
| 10/04/2025 | Ajout d’une introduction, améliorations mineures (clarifications, compléments, mise en cohérence avec les autres documents) | Matthieu GRALL | Document de travail |
| 16/04/2025 | Transformation du document en _markdown_ | Cécile LAMARQUE | Document de travail |
| 18/04/2025 | Amélioration du _markdown_ | Matthieu GRALL | Document de travail |

### Documents de référence
Les références suivantes sont utilisées entre crochets dans le corps du document :
<center>Libellé court</center>|<center>Libellé long</center>
---|---
[RAPPORT TASK FORCE IA]|L’intelligence artificielle au service de la Défense, Rapport de la Task Force IA, ministère des Armées (2019)<br/>[Lien](<https://www.defense.gouv.fr/sites/default/files/aid/20200108-NP-Rapport de la Task Force IA Septembre.pdf>)


### Ressources utilisées

**Page de garde** : Grid, par Magic Creative, de PIXABAY.

**Tableau périodique de cas d’usages** : par XPRIZE.

### Sommaire
1.	[Objet du document](#1objet-du-document)

2.	[Introduction](#2introduction)

3.	[Exemple : liste de cas d'usages](#3exemple--liste-de-cas-dusages)

4.	[Exemple : tableau périodique de cas d'usages](#4exemple--tableau-périodique-de-cas-dusages)

 
# 1.	Objet du document
**Ce document propose des exemples de typologies de micro-cas d’usages d’utilisation de l’intelligence artificielle (IA).**

Il s’inscrit dans un ensemble de documents méthodologiques en amélioration continue, destinés à aider les organismes à gérer les risques liés à l’IA, et qui peuvent être utiles ensemble ou séparément :
1. [Exemples de micro-cas d'usages de L'IA] (Lien à mettre) ;
2.	[Critères de confiance de l'IA] (Lien à mettre);
3.	[Bbonnes pratiques de l'IA] (Lien à mettre);
4.	[Méthode de gestion des risques de l'IA] (Lien à mettre).

Il n’a pas pour vocation à servir de référence, mais à souligner la variété des cas d’usages et des techniques sous-jacentes, et il peut également être utile à la description d’un système dans une démarche de gestion des risques ou de projets.

## 2.	Introduction
[Pour le Parlement européen](https://www.europarl.europa.eu/topics/fr/article/20200827STO85804/intelligence-artificielle-definition-et-utilisation), l’IA représente tout outil utilisé par une machine afin de « _reproduire des comportements liés aux humains, tels que le raisonnement, la planification et la créativité_ ». Cette définition peut être élargie en incluant les comportements dépassant les capacités humaines, puisque les ordinateurs actuels parviennent aujourd’hui à les surpasser dans certaines tâches (bien que la compétence de l’ordinateur s’arrête généralement à l’exécution de cette tâche).

C’est un domaine de l'informatique né en 1956<sup><a href="#note1" id="ref1">[1]</a></sup> qui vise à créer des machines capables de réaliser des tâches qui nécessitent normalement l'intelligence humaine. Il s'agit de simuler des processus cognitifs tels que l'apprentissage, la résolution de problèmes, la prise de décision et la compréhension du langage naturel. Contrairement à une simple programmation de règles précises, l'IA cherche à donner aux machines la capacité d'apprendre et de s'adapter à de nouvelles situations sans être explicitement programmées pour chaque éventualité.

En synthèse, le [RAPPORT TASK FORCE IA] fournit l’explication suivante : 

*« L’IA est utilisée dans les applications où il s’agit de* :
-	*détecter/reconnaître des données (texte, sons, images, vidéos), ou prédire des données futures ;*
-	*rechercher des corrélations entre des données pour en déduire un comportement générique ou lever une alerte en cas de comportement anormal ;*
-	*optimiser des problèmes à forte combinatoire (ex : flux logistiques ou trajectoires d’aéronef) ;*
-	*raisonner sur des données symboliques pour déduire ou pour diagnostiquer.*

*Du point de vue technique<sup><a href="#note2" id="ref2">[2]</a></sup>, l’intelligence artificielle comprend deux branches majoritaires :*
-	*les approches symboliques basées sur le raisonnement (systèmes à base de règles) ; et*
-	*les approches connexionnistes plus proches de l’empirisme, fondées sur l’apprentissage à partir de grandes bases de données (réseaux de neurones). »* 

**Il est toutefois très difficile d’établir une typologie de cas d’usages détaillés**, tant les domaines de recherche et applications liées à l’IA sont nombreux, variés, parfois croisés, et en évolution permanente.

**Ce document propose donc uniquement des exemples de typologies.**

<a name="note1" id="note1">[1]</a> Cf. [conférence de Dartmouth](https://fr.wikipedia.org/wiki/Conf%C3%A9rence_de_Dartmouth). [↩](#ref1)

<a name="note2" id="note2">[2]</a> L'étendue de l'IA est vaste et englobe plusieurs branches interdépendantes. On retrouve l'apprentissage automatique (machine learning), où les systèmes apprennent à partir de données sans être explicitement programmés, l’apprentissage profond (deep learning), utilisant des réseaux neuronaux artificiels à plusieurs couches pour traiter des informations complexes, le traitement du langage naturel (TLN - NLP) permettant aux machines de comprendre et de générer du langage humain, la vision par ordinateur (computer vision) permettant aux machines de "voir" et d'interpréter des images, et la robotique, combinant l'IA avec des systèmes physiques pour créer des robots intelligents. [↩](#ref2)

## 3.	Exemple : liste de cas d'usages
Le tableau suivant présente une liste non exhaustive de cas d’usages qui reposent sur de l’IA, en indiquant les principales techniques d’IA mises en œuvre et des exemples d’outils qui les mettent effectivement en œuvre :
<center>**Micro-cas d’usages**</center>|<center>**Principales techniques d’IA**</center>|<center>**Exemples d’outils**</center>
---|---|---
Détecter certains types de sons dans un signal audio (alarmes, moteurs, dispositifs spécifiques)|Apprentissage supervisé, réseaux de neurones convolutifs (CNN), modèles de reconnaissance sonore|	SONARWORKS, GOOGLE AudioSet|
Reconnaître les visages et les états émotionnels dans des images ou vidéos|	CNN, apprentissage profond (*deep learning*), analyse des expressions faciales|	LIGHTON, AFFECTIVA, MICROSOFT Face API|
Reconnaître certains types d'objets dans des images ou vidéos|	CNN, YOLO, Mask R-CNN, transformateurs de vision (vision transformers – ViT)|	HUGGING FACE, GOOGLE Vision AI, AMAZON Rekognition|
Analyser les données du capteur pour détecter des objets et/ou situations à partir d’un signal|	Apprentissage supervisé/non supervisé, analyse de séries temporelles, fusion de capteurs|	SIEMENS MindSphere, GE DIGITAL|
Reconnaître la langue parlée et/ou les états émotionnels dans un signal audio|	Traitement automatique du langage naturel (TAL ou *natural language processing* – NLP), modèles de classification audio, transformateurs|	VOXYGEN, GOOGLE Speech API, IBM Watson Speech to Text, OPENAI Whisper|
Reconnaître une voix individuelle dans un signal audio|	Identification biométrique vocale, CNN appliqués à l’audio|	NUANCE Gatekeeper, MICROSOFT Azure Speaker Recognition|
Détecter des signatures audio spécifiques (moteur, sonnette, etc.)|	Modèles de classification audio, spectrogrammes et CNN|	ZOUNDREAM, GOOGLE AudioSet|
Reconnaître des personnes spécifiques dans des images ou vidéos|	Apprentissage supervisé, *deep learning*, bases de données d’empreintes faciales|	CLEARVIEW AI, PIMEYES|
Reconnaître un objet concret dans une image ou vidéo|	Mise en correspondance de similarités (feature matching), CNN, vision assistée|	GOOGLE Lens, APPLE Vision Pro, OPENCV|
Analyser les données pour identifier certains faits et événements|	TAL, modèles de classification, transformateurs|	PALANTIR, IBM Watson Discovery, BIGML|
Analyser des textes pour extraire des informations sur les entités, temps, lieux et faits|	TAL, reconnaissance des entités nommées (*named entity recognition* – NER), transformateurs|	SPACY, STANFORD NLP, IBM Watson NLU|
Prévoir des événements ou conditions futures	|Modèles prédictifs, réseaux de neurones, analyse de séries temporelles (*autoregressive integrated moving average* – ARIMA, *long short-term memory* – LSTM)|	PREVISION.IO, FACEBOOK Prophet, GOOGLE Forecast|
Expliquer des événements en fonction des états passés|	Modélisation causale, réseaux bayésiens, IA explicable (XAI)|	GRAKN.AI, IBM Explainable AI, MIT Model-based AI|
Utiliser des preuves pour appuyer des conclusions|	Raisonnement bayésien, inférence logique, XAI|	WOLFRAM Alpha, IBM Watson, KNOWLEDGE GRAPHS|
Créer un plan d’action basé sur des objectifs et la connaissance des actions|	Planification automatique, apprentissage par renforcement (*reinforcement learning* – RL, modèles décisionnels|	OPENAI Gym, DEEP MIND AlphaZero, AUTOGPT|
Créer une solution à un problème|	Algorithmes heuristiques, génération de solutions|	IBM Solver CPLEX, GOOGLE OR-Tools|
Choisir une direction ou solution basée sur les faits|	Systèmes de recommandation, IA décisionnelle|	SALESFORCE Einstein, IBM Watson Decision Platform, GOOGLE Optimize|
Créer des textes et/ou des explications en langage naturel|	TAL, grands modèles linguistiques (*large language models* – LLM), IA générative|	LIGHTON, OPENAI ChatGPT, GOOGLE Bard|
Créer une représentation sémantique du sens d'un texte|	Modèles de représentation sémantique, graphes de connaissances (*knowledge graphs*)|	GOOGLE Knowledge Graph, WORD2VEC, CONCEPTNET|
Reconnaître les relations entre caractéristiques visibles et cachées|	Apprentissage non supervisé, division en groupes (*clustering*), IA causale|	SCIKIT-LEARN, TENSORFLOW, PYCARET|
Reconnaître de nouvelles catégories de valeurs sémantiques|	Apprentissage non supervisé, *clustering* (K-Means, DBSCAN)|	H2O.AI, BIGML, RAPIDMINER|
Répondre à des connaissances ou règles existantes|	Raisonnement basé sur règles, ontologies, *knowledge graphs*|	CYC, IBM Watson Knowledge Studio, NEO4J|
Contrôler des véhicules autonomes en interaction avec d'autres véhicules|	*Deep learning*, RL, télédétection par laser (*light detection and ranging* – LIDAR), perception multimodale|	NAVYA, TESLA Autopilot, WAYMO, CRUISE|
Contrôler des robots qui interagissent avec des humains en zones intérieures|	Vision par ordinateur, RL, NLP	|ALDEBARAN Robotics (NAO, Pepper), BOSTON DYNAMICS Spot, NVIDIA Isaac|
Manipuler des objets dans un environnement collaboratif avec les humains|	Robotique cognitive, préhension adaptative, vision par ordinateur|	UNIVERSAL ROBOTS (UR Cobot), ABB YuMi, EVERYDAY ROBOTS (GOOGLE)|
Faciliter la communication Homme-machine|	NLP, assistants virtuels (*chatbots*, interfaces vocales)|	VIVOKA, GOOGLE Assistant, APPLE Siri, AMAZON Alexa|
Contrôler d'autres machines sans action physique nécessaire (ex. commerce automatisé)|	IA décisionnelle, algorithmes de commerce (*trading*), automatisation logicielle|	BLOOMBERG Terminal, TRADE IDEAS AI, KENSHO|
 
## 4.	Exemple : tableau périodique de cas d'usages
Les cas d’usages de systèmes basés sur l’IA peuvent aussi être représentés sous la forme d’un tableau périodique, comme le propose [XPRIZE](https://community.digilogic.africa/resource/the-periodic-table-of-ai/) :

![XPRIZE AI periodic table](https://danielschristian.com/learning-ecosystems/wp-content/uploads/2017/01/AI-PeriodicTable-Dec2016.jpg)

<center>**Acron.**</center>|<center>**Cas d'usage**</center>|<center>**Description synthétique**</center>
---|---|---
Ar|	*Audio Recognition*|	Détecter certains types de sons (alarmes, contrainte du dispositif, automoteur) dans un signal audio|
Fr	|*Face Recognition*|	Reconnaître les visages et les états émotionnels dans les images ou les signaux vidéo|
Ir	|*Image Recognition*|	Reconnaître certains types d'objets dans des images ou des signaux vidéo|
Gr	|*General Recognition*	|Analyser les données du capteur pour détecter les types d'objets et/ou les situations seules à partir du signal|
Sr|*Speech Recognition*|	Reconnaître la langue parlée et/ou des états émotionnels en général dans un signal audio|
Si|	*Speech Identification*|	Reconnaître une voix individuelle dans un signal audio|
Ai|	*Audio Identification*	|Détecter les signatures audio (un moteur spécifique ou une sonnette spécifique) à partir de signaux audio|
Fi	|*Face Identification*|	Reconnaître des personnes concrètes dans des images ou des signaux vidéo|
Ii	|*Image Identification*	|Reconnaître un objet concret dans une image ou une vidéo|
Gi	|*General Identification*	|Analyser les données du capteur pour détecter des objets et/ou des situations uniquement à partir du signal|
Da	|*Data Analytics*|	Analyser les données pour identifier certains faits et/ou événements qui représentent les données|
Te|	*Text Extraction*|	Analyser des textes pour extraire des informations sur les entités, temps, lieux et faits qui sont inclus exclusivement dans le texte|
Pi	|*Predictive Inference*|	Prévoir des événements ou conditions à l'avenir basée sur la compréhension d'un état actuel du monde et son fonctionnement|
Ei	|*Explanatory Inference*|	Expliquer des événements ou des États dans le monde réel sur la base de la compréhension des États précédents|
Sy|	*Synthetic Reasoning*	|Utiliser des preuves à l'appui de conclusions sur l'état réel du monde, une prédiction ou une explication|
Pl|	*Planning*	|Créer un plan d'action fondé sur un ensemble d'objectifs, une compréhension de l'état réel du monde et la connaissance des actions et de leurs conséquences|
Ps	|*Problem Solving*|	Créer une solution à un problème qui peut être lié ou non à l'utilisation d'actions|
Dm	|*Decision Making*|	Choisir une direction ou solution particulière sur la base des faits disponibles, d'autres solutions et d'un certain nombre d'objectifs|
Lg	|*Language Generation*|	Créer des textes et/ou des explications en langage naturel basés sur une certaine compréhension du monde|
Lu	|*Language Understanding*|	Créer une représentation sémantique du sens d'un texte qui montre le contexte et une certaine compréhension du fonctionnement du monde|
Lr	|*Relationship Learning*|	Reconnaître les relations entre les caractéristiques qui peuvent être utilisées pour prédire la présence d'un ensemble de caractéristiques cachées si d'autres sont visibles|
Lc	|*Category Learning*	|Reconnaître les nouvelles catégories de valeurs sémantiques fondées sur les collections de caractéristiques|
Lt	|*Knowledge Refinement*|	Répondre aux connaissances ou aux règles qui existent déjà en réponse à l'utilisation pour soutenir des actions ou des conclusions|
Ml	|*Mobility Large*	|Contrôler des véhicules autonomes qui interagissent avant tout avec d'autres véhicules|
Ms	|*Mobility Small*|Contrôler les robots qui se déplacent à travers les zones intérieures, travaillant et interagissant avec les gens|
Ma	|*Manipulation*|	Manipuler des objets avec lesquels les gens travaillent régulièrement|
Cm	|*Communication*|	Soutenir l'exécution de différentes formes de communication entre l'Homme et la machine|
Cn|	*Control*	|Contrôler d'autres machines lorsqu'aucune action n'est nécessaire dans le monde physique (ex : commerce automatisé)|
