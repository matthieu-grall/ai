# Intelligence artificielle (IA) - Méthode de gestion des risques

## Objet du document
**Ce document propose une démarche pour gérer les risques spécifiques aux produits et services qui reposent sur des systèmes l'intelligence artificielle (IA)**.
Il a pour vocation à s'inscrire dans les démarches existantes au sein des organismes, notamment les processus d'homologation de systèmes, mais peut également être directement utilisé.

[Avant-propos](#avant-propos)<br/>
[Introduction](#introduction)<br/>
[Étape 1 : estimer le niveau de risque](#étape-1--estimer-le-niveau-de-risque)<br/>
[Étape 2 : l'approche par conformité](#étape-2--lapproche-par-conformité)<br/>
[Étape 3 : l'approche par scénarios](#étape-3--lapproche-par-scénarios)<br/>

## Avant-propos
Ce document s'inscrit dans un [ensemble de documents méthodologiques](https://github.com/matthieu-grall/ai), en amélioration continue, destinés à aider les organismes à gérer les risques liés à l'IA, et qui peuvent être utiles ensemble ou séparément.
Les [documents de référence](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Documents%20de%20r%C3%A9f%C3%A9rence.md) sont utilisés entre crochets dans le corps du document.

Il est placé sous la **licence** suivante :
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

Les principaux **contributeurs** sont les suivants :
- Matthieu GRALL, expert-conseil en management des données, sécurité de l'information, protection de la vie privée et nouvelles technologies.

Les **versions** du document sont les suivantes :
| <center>**Version**</center> | <center>**Action**</center> | <center>**Éditeur**</center> |
| --- | --- | --- |
| 28/03/2025 (v0.1) | Création du document, ajout des documents de références, du tableau périodique de cas d'usages et des critères de confiance | Matthieu GRALL |
| 05/04/2025 (v0.2) | Déplacement du tableau périodique de cas d'usages dans un autre document | Matthieu GRALL |
| 10/04/2025 (v0.3) | Déplacement des critères de confiance et des bonnes pratiques dans d'autres documents, améliorations mineures (mise en cohérence avec les autres documents) | Matthieu GRALL |
| 23/04/2025 (v0.4) | Transformation du document en _markdown_ | Matthieu GRALL |
| 07/05/2025 (v1.0) | Finalisation d'une première version complète, cohérente, et en _markdown_ | Matthieu GRALL |
| 11/07/2025 (v1.1) | Simplification et harmonisation des chapitres introductifs, corrections mineures | Matthieu GRALL |
| 20/07/2025 (v1.2) | Amélioration de l'étape 1 (identification du cas d'usage et échelle), corrections mineures | Matthieu GRALL |

## Introduction
On peut autant considérer l'IA comme :
1. **une technologie comme les autres**, sur laquelle de nouveaux services numériques vont pouvoir reposer, et dont il conviendra d'apprécier et de traiter les risques spécifiques ;
2. **une réelle opportunité d'améliorer nos capacités cyber** dans tous les domaines de lutte ;
3. **un levier démultiplicateur des capacités offensives adverses**, contre lesquelles on va devoir lutter.

Pour les deux premiers points, l'enjeu est le même : **améliorer la confiance envers l'IA** !

Or, un système d'IA est susceptible d'engendrer des **risques qui ne se limitent pas à la sécurité de l'information, et qui sont amplifiés par la frénésie actuelle** qui réduit la prise de recul :
- **sur les organismes**, du fait de défauts de qualité des données et légalité de leur obtention / traitement, et de technologies qui apportent leurs lots de vulnérabilités ;
- **sur les personnes**, avec notamment des biais sur les données d'entrainement, d'entrée et de sortie, qui peuvent mener à des discriminations ;
- **sur l'environnement**, car les technologies sur lesquelles reposent les outils d'IA sont parfois très gourmandes en ressources.

Ce document propose donc une **méthode de gestion des risques liés à l'IA**, qui :
1. estime _a priori_ un **niveau de risque** sur l'organisme, sur les personnes et sur l'environnement ;
2. compare les pratiques envisagées aux bonnes pratiques via une **approche par conformité** ;
3. pour les systèmes d'IA susceptibles d'engendrer les risques les plus élevés, explique comment les apprécier et les traiter via une **approche par scénarios**.

Cette méthode :
- s'inscrit dans les démarches d'homologation existantes (cf. [Guide d'homologation de l'ANSSI]) ;
- repose sur la méthode [EBIOS _Risk Manager_] ;
- respecte donc les principes de gestion des risques ([ISO 31000], [ISO/IEC 27005], etc.) ;
- contribue à satisfaire les exigences afférentes des systèmes de management ([ISO/IEC 27001], [ISO/IEC 42001], [ISO 14001]).

## Étape 1 : estimer le niveau de risque
L'objectif est de **proportionner l'étude au niveau de risque que le système d'IA est susceptible d'engendrer**.

Pour ce faire, il convient de :

1. **décrire le cas d'usage considéré**, notamment en termes de finalités, de fonctionnalités d'IA et de techniques d'IA (voir les [cas d'usages](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Cas%20d'usages.md)) ;

2. **situer le cas d'usage** dans chaque colonne de l'échelle suivante :

| <center>**Niveau de risque**<br/><br/>(et correspondance avec le [Règlement IA]</center> | <center>**Conséquences potentielles sur les personnes**<br/><br/>(cf. [Guide PIA-3])</center> | <center>**Conséquences potentielles sur l'organisme**<br/><br/>(cf. [EBIOS _Risk Manager_])</center> | <center>**Conséquences potentielles sur l'environnement**<br/><br/>(inspirées de [ISO 14004] et [NF X30-205])</center> |
| --- | --- | --- | --- |
| 1. Minimal<br/><br/>("Risque minimal ou nul", ex : filtres anti-spam, IA gadget) | 1. Négligeable : les personnes concernées ne seront pas impactées ou pourraient connaître quelques désagréments, qu'elles surmonteront sans difficulté<br/>Ex : perte de temps pour réitérer des démarches ou pour attendre de les réaliser, réception de courriers non sollicités (ex. : _spams_), sentiment d'atteinte à la vie privée sans préjudice réel ni objectif (ex : intrusion commerciale) | G1. Mineure : conséquences négligeables pour l'organisation (aucun impact opérationnel ni sur les performances de l'activité ni sur la sécurité des personnes et des biens, l'organisation surmontera la situation sans trop de difficultés (consommation des marges))<br/>Ex : perturbation très limitée, aucune donnée sensible, rétablissement rapide, aucun impact légal ou réputationnel | 1. Minime : impact négligeable ou localisé (effets réversibles, faibles, sans conséquence durable, ne nécessite aucune action de remédiation environnementale, faible consommation énergétique, pas d'entraînement intensif, empreinte carbone négligeable, impact potentiellement positif)<br/>Ex : IA utilisée pour l'optimisation d'un processus numérique sans augmentation significative de ressources, test d'un modèle IA sur un échantillon restreint en local sans usage massif de cloud |
| 2. Faible<br/><br/>("Risque limité", ex : chatbot, IA générative non critique) | 2. Limitée : les personnes concernées pourraient connaître des désagréments significatifs, qu'elles pourront surmonter malgré quelques difficultés<br/>Ex : affection physique mineure (ex. : maladie bénigne suite au non respect de contre-indications), élévation de coûts (ex. : augmentation du prix d'assurance), difficultés relationnelles avec l'entourage personnel ou professionnel (ex. : image, réputation ternie, perte de reconnaissance) | G2. Significative : conséquences significatives mais limitées pour l'organisation (dégradation des performances de l'activité sans impact sur la sécurité des personnes et des biens, l'organisation surmontera la situation malgré quelques difficultés (fonctionnement en mode dégradé))<br/>Ex : dégradation temporaire, données peu sensibles, intervention rapide | 2. Faible : impact modéré ou indirect (impact localisé, non permanent, nécessite des mesures correctrices simples ou des bonnes pratiques, utilisation modérée du cloud, empreinte maîtrisable, usage de données/matériel à faible intensité, compensation possible)<br/>Ex : déploiement d'un assistant IA consommant modérément des ressources cloud (CPU, bande passante), utilisation de capteurs IA générant un surplus d'énergie ou de données traitées sans recyclage |
| 3. Élevé<br/><br/>("Risque élevé", ex : IA pour santé, emploi, justice) | 3. Importante : les personnes concernées pourraient connaître des conséquences significatives, qu'elles devraient pouvoir surmonter, mais avec des difficultés réelles et significatives<br/>Ex : affection physique grave causant un préjudice à long terme (ex. : aggravation de l'état de santé suite à une mauvaise prise en charge, ou au non respect de contre-indications), interdiction bancaire, affection psychologique grave (ex. : dépression, développement d'une phobie) | G3. Grave : conséquences importantes pour l'organisation (forte dégradation des performances de l'activité, avec d'éventuels impacts significatifs sur la sécurité des personnes et des biens, l'organisation surmontera la situation avec de sérieuses difficultés (fonctionnement en mode très dégradé), sans impact sectoriel ou étatique)<br/>Ex : compromission de données sensibles, interruption prolongée, gestion de crise nécessaire, risques juridiques et réputationnels | 3. Élevé : Impact étendu ou cumulatif (effets significatifs sur les ressources ou les émissions, potentiellement persistants, peut contribuer à la pression sur les écosystèmes ou au dérèglement climatique, calculs intensifs, stockage/énergie importants, pression sur ressources matérielles, impact environnemental notable)<br/>Ex : entraînement de modèles LLM sur GPU à haute intensité énergétique, IA dans des objets connectés non recyclables produits à grande échelle |
| 4. Maximal<br/><br/>("Risque inacceptable", ex : notation sociale, manipulation, surveillance biométrique de masse) | 4. Maximale : les personnes concernées pourraient connaître des conséquences significatives, voire irrémédiables, qu'elles pourraient ne pas surmonter<br/>Ex : décès (ex : meurtre, suicide, accident mortel), impossibilité de travailler, affection psychologique de longue durée ou permanente | G4. Critique : conséquences désastreuses pour l'organisation avec d'éventuels impacts sur l'écosystème (incapacité pour l'organisation d'assurer la totalité ou une partie de son activité, avec d'éventuels impacts graves sur la sécurité des personnes et des biens, l'organisation ne surmontera vraisemblablement pas la situation (sa survie est menacée), les secteurs d'activité ou étatiques dans lesquels elle opère seront susceptibles d'être légèrement impactés, sans conséquences durables) et G5. Catastrophique : conséquences sectorielles ou régaliennes au-delà de l'organisation (écosystème(s) sectoriel(s) impacté(s) de façon importante, avec des conséquences éventuellement durables, et/ou difficulté pour l'État, voire incapacité, d'assurer une fonction régalienne ou une de ses missions d'importance vitale, et/ou : impacts critiques sur la sécurité des personnes et des biens (crise sanitaire, pollution environnementale majeure, destruction d'infrastructures essentielles, etc.)<br/>Ex : fuite massive de données critiques, dysfonctionnement généralisé, impact légal/réputationnel majeur, risque pour la pérennité | 4. Maximal : Impact critique ou irréversible (effets à grande échelle, à long terme ou irréversibles, dégradation majeure des écosystèmes, contribution significative à des risques systémiques environnementaux, modèles massifs, consommation énergétique élevée, externalisation des impacts, pas de compensation)<br/>Ex : déploiement mondial d'un système IA nécessitant des centres de données à forte intensité carbone dans plusieurs pays, IA pilotant des chaînes de production entraînant surconsommation de matières premières rares ou polluantes |

3. **retenir le niveau le plus élevé** de toutes les colonnes ;

4. **déterminer les suites à donner** en fonction de ce niveau :

| <center>**Niveau de risque**</center> | <center>**Approche par conformité (étape 2)**</center> | <center>**Approche par scénario (étape 3)**</center> |
| --- | --- | --- |
| 1. Minimal | Pas utile | Pas utile |
| 2. Faible | Conseillée | Pas utile |
| 3. Élevé | Oui | Conseillée |
| 4. Maximal | Oui | Oui |

Notes :
- cette approche correspond à la qualification des systèmes d'IA du [Règlement IA], en l'élargissant, la précisant et la rendant plus pratique ; 
- elle ne préjuge en rien des obligations et interdictions applicables (ex : « IA à risque inacceptable » interdite par le [Règlement IA]) ;
- le cas échéant, le résultat de cette étape peut être intégré à la stratégie d'homologation.

## Étape 2 : l'approche par conformité
L'approche par conformité, à mettre en œuvre dans le cas d'un niveau 3. Élevé (également conseillée pour 2. Faible ), permet de **gérer les risques standards**, y compris ceux de cause accidentelle, **et les attaques cyber non ciblées**.

L'objectif est d'**évaluer la conformité du cas d'usage aux [Bonnes pratiques de l'IA]**, qui contribuent à respecter les [critères de confiance de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Crit%C3%A8res%20de%20confiance.md) d'un système d'IA, afin d'éclairer la prise de décision.

Pour ce faire, évaluer chacune des [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) :
- **si elle est jugée comme applicable** :
	- **si elle est appliquée, comment ?** L'explication fournie doit permettre d'évaluer le respect de la bonne pratique ;
	- **si elle n'est pas appliquée, quelles sont les mesures compensatoires ?** L'explication fournie doit permettre d'évaluer que les mesures prévues sont suffisantes pour atteindre un niveau de confiance aussi bon que si la bonne pratique était appliquée ;
- **si elle est jugée comme non applicable, pourquoi ?** L'explication fournie doit permettre de juger de son inapplicabilité (un chapitre entier peut être exclu s'il est traité par ailleurs ou en dehors de sa responsabilité, une bonne pratique sur un LLM n'est applicable qu'aux LLM, etc.).
 
La déclaration d'applicabilité en annexe des [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) peut être utilisée à cet effet.
 
Notes :
- l'objectif n'est pas de respecter toutes les bonnes pratiques, mais de décrire ce qui est réellement prévu au regard de celles-ci ;
- cette approche correspond à la « déclaration d'applicabilité » de l'[ISO/IEC 27001] et à l'« évaluation du socle de règles » de l'atelier 1 d'[EBIOS _Risk Manager_] ;
- le cas échéant, le résultat de cette étape peut être intégrée au dossier d'homologation.

## Étape 3 : l'approche par scénarios
L'approche par scénarios, à mettre en œuvre dans le cas d'un niveau 4. Maximal (également conseillée pour le niveau 3. Élevé ), permet de **gérer les attaques cyber avancées et ciblées**.

L'objectif est d'**identifier** et d'**apprécier les risques** que le cas d'usage est susceptible d'engendrer sur l'organisme, les personnes et l'environnement, de **déterminer les mesures pour les traiter**, et de **présenter les risques résiduels** pour éclairer la prise de décision.

Pour ce faire, **mener une étude de risques par scénarios sur le cas d'usage avec les spécificités de l'IA**. Par exemple,  avec [EBIOS _Risk Manager_] :
- dans l'atelier 1 :
	- considérer le **cas d'usage** comme « objet de l'étude » ;
	- considérer sa **finalité** comme « mission » ;
	- intégrer les **fonctionnalités d'IA, données d'entrée, d'entrainement et de sortie** dans les « valeurs métier » ;
	- intégrer le **système d'IA**, notamment les techniques d'IA (ex : l'algorithme utilisé), dans les « biens supports » ;
	- considérer les **conséquences sur l'organisme**, mais aussi **sur les personnes** et **sur l'environnement**, et l'échelle proposée dans l'étape 1 dans les « événements redoutés » ;
- dans l'atelier 2 : pas de spécificité ;
- dans l'atelier 3 : pas de spécificité ;
- dans l'atelier 4 : considérer les **attaques spécifiques aux systèmes d'IA** (ex : [Guide de France IA] ou [ATLAS]) dans les « scénarios opérationnels » ;
- dans l'atelier 5 : considérer les **mesures spécifiques aux systèmes d'IA** (ex : [Guide de France IA] ou [ATLAS]) dans les « mesures », ainsi que les recommandations ([Recommandations IA de l'ANSSI - 2024], [Recommandations IA de l'ANSSI - 2025], [Recommandations IA de la CNIL], etc.) qui n'auraient pas été retenues dans l'étape précédente.

Notes :
- cette approche correspond à l'ensemble ateliers d'[EBIOS _Risk Manager_] et aux processus d' « établissement du contexte », d' « appréciation des risques » et de « traitement des risques » des normes relatives à la gestion des risques (ex : [ISO 31000], [ISO/IEC 27005]) ;
- le cas échéant, le résultat de cette étape peut constituer le cœur du dossier d'homologation.
