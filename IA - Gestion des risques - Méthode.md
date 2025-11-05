# Intelligence artificielle (IA) - Méthode de gestion des risques

## Objet du document
**Ce document propose une démarche pour gérer les risques spécifiques aux produits et services qui reposent sur des systèmes l'intelligence artificielle (IA)**.
Il a pour vocation à s'inscrire dans les démarches existantes au sein des organismes, notamment les processus d'homologation de systèmes, mais peut également être directement utilisé.

[Avant-propos](#avant-propos)<br>
[Introduction](#introduction)<br>
[Étape 1. Cadrer le contexte](#étape-1-cadrer-le-contexte)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 1.1. Cadrer l'étude](#action-11-cadrer-létude)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 1.2. Estimer le niveau de risque que l'objet de l'étude est susceptible d'engendrer](#action-12-estimer-le-niveau-de-risque-que-lobjet-de-létude-est-susceptible-dengendrer)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 1.3. Déterminer les suites à donner](#action-13-déterminer-les-suites-à-donner)<br>
[Étape 2. l'approche par conformité](#étape-2-lapproche-par-conformité)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 2.1. Choisir son référentiel](#action-21-choisir-son-référentiel)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 2.2. Évaluer la conformité aux bonnes pratiques](#action-22-évaluer-la-conformité-aux-bonnes-pratiques)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 2.3. Améliorer la conformité aux bonnes pratiques](#action-23-améliorer-la-conformité-aux-bonnes-pratiques)<br>
[Étape 3. l'approche par scénarios](#étape-3-lapproche-par-scénarios)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 3.1. Établir le contexte](#action-31-établir-le-contexte)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 3.2. Apprécier les risques](#action-32-apprécier-les-risques)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[Action 3.3. Traiter les risques](#action-33-traiter-les-risques)<br>

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
| 23/10/2025 (v1.3) | Corrections mineures (mise en cohérence des libellés courts des documents de référence qui ont été changés, harmonisation des balises "br", correction d'une phrase) | Matthieu GRALL |
| 05/11/2025 (v1.4) | Développement de la méthode et d'une étude de cas (en cours) | Matthieu GRALL |

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
1. décrit le cas d'usage et estime _a priori_ un **niveau de risque** sur l'organisme, sur les personnes et sur l'environnement ;
2. compare les pratiques envisagées aux bonnes pratiques via une **approche par conformité** ;
3. pour les systèmes d'IA susceptibles d'engendrer les risques les plus élevés, explique comment les apprécier et les traiter via une **approche par scénarios**.

Cette méthode :
- s'inscrit dans les démarches d'homologation existantes (cf. [Guide d'homologation]) ;
- repose sur la méthode [EBIOS _Risk Manager_] ;
- respecte donc les principes de gestion des risques ([ISO 31000], [ISO/IEC 27005], etc.) ;
- contribue à satisfaire les exigences afférentes des systèmes de management ([ISO/IEC 27001], [ISO/IEC 42001], [ISO 14001]).

## Étape 1. Cadrer le contexte
L'objectif est de **proportionner l'étude au niveau de risque que le cas d'usage est susceptible d'engendrer**.

Note : le cas échéant, le résultat de cette étape peut utilement être intégré à la stratégie d'homologation.

### Action 1.1. Cadrer l'étude

Il convient tout d'abord d'identifier clairement :
- l’**objet de l’étude** : le cas d'usage / traitement de données considéré (cas d'usage seul ou périmètre plus large, de manière intelligible pour que toutes les parties intéressées comprennent bien de quoi il s'agit) ;
- l’**objectif de l’étude** (ex : homologuer un système) ;
- les **destinataires de l’étude** (ex : commission d’homologation) ;

<i>

> Exemple :
> - objet de l'étude : contrôler l’accès à une zone sécurisée à l'aide d'un dispositif de reconnaissance faciale ;
> - objectifs de l'étude : évaluer la sécurité du dispositif, bâtir la conformité au [RGPD] et au [Règlement IA] ;
> - destinataires de l'étude : commission d'homologation interne, délégué à la protection des données (DPO) et, le cas échéant, les autorités compétentes.

</i>

### Action 1.2. Estimer le niveau de risque que l'objet de l'étude est susceptible d'engendrer

La gravité des conséquences des risques que l'objet de l'étude est susceptible d'engendrer devrait être estimée _a priori_ afin de pouvoir proportionner la profondeur de l'étude.

Pour ce faire, il convient de :
- **choisir les sujets à considérer** : protection des droits fondamentaux (cf. [Règlement IA]), protection de la vie privée (cf. [RGPD]), sécurité de l'information (cf. [ISO/IEC 27001]), protection de l'environnement (cf. [ISO 14001]), etc. ;
- **définir une/des échelle(s)** qui décri(ven)t les niveaux de risque pour chaque sujet considéré ;
- **situer l'objet de l'étude dans la/les échelle(s) définie(s)**, au regard des conséquences imaginables :
    - de son fonctionnement nominal : sa finalité, les données traitées, la nature et le volume de personnes concernées, les technologies utilisées ;
	- de son dysfonctionnement ;
	- et surtout, des risques liés à la sécurité des données : disparition, modification non désirée ou accès non autorisé ;
- **retenir le niveau le plus élevé**.

Notes :
- selon le contexte, on peut choisir de considérer tous les sujets possibles (pour avoir une vision globale) ou uniquement certains, voire un seul (ex : périmètre de compétence limité) ;
- cette démarche ne préjuge en rien des obligations et interdictions applicables (ex : « IA à risque inacceptable » interdite par le [Règlement IA]).

>_Exemple : il est choisi d'adopter une vision globale, et donc de définir des échelles permettant d'estimer les conséquences sur les personnes, sur l'organisme, et sur l'environnement (voir ci-dessous) ; le niveau des risque est jugé comme élevé sur les personnes et l'organisme, mais plutôt faible sur l'environnement ; le niveau de risque retenu est donc 3. Élevé._

<i>

| <center>**Niveau de risque**<br><br>(et correspondance avec le [Règlement IA])</center> | <center>**Conséquences potentielles sur les personnes**<br><br>(cf. [Guide PIA-3])</center> | <center>**Conséquences potentielles sur l'organisme**<br><br>(cf. [EBIOS _Risk Manager_])</center> | <center>**Conséquences potentielles sur l'environnement**<br><br>(inspirées de [ISO 14004] et [NF X30-205])</center> |
| --- | --- | --- | --- |
| 1. Minimal<br><br>("Risque minimal ou nul", ex : filtres anti-spam, IA gadget) | 1. Négligeable : les personnes concernées ne seront pas impactées ou pourraient connaître quelques désagréments, qu'elles surmonteront sans difficulté<br>Ex : perte de temps pour réitérer des démarches ou pour attendre de les réaliser, réception de courriers non sollicités (ex. : _spams_), sentiment d'atteinte à la vie privée sans préjudice réel ni objectif (ex : intrusion commerciale) | G1. Mineure : conséquences négligeables pour l'organisation (aucun impact opérationnel ni sur les performances de l'activité ni sur la sécurité des personnes et des biens, l'organisation surmontera la situation sans trop de difficultés (consommation des marges))<br>Ex : perturbation très limitée, aucune donnée sensible, rétablissement rapide, aucun impact légal ou réputationnel | 1. Minime : impact négligeable ou localisé (effets réversibles, faibles, sans conséquence durable, ne nécessite aucune action de remédiation environnementale, faible consommation énergétique, pas d'entraînement intensif, empreinte carbone négligeable, impact potentiellement positif)<br>Ex : IA utilisée pour l'optimisation d'un processus numérique sans augmentation significative de ressources, test d'un modèle IA sur un échantillon restreint en local sans usage massif de cloud |
| 2. Faible<br><br>("Risque limité", ex : chatbot, IA générative non critique) | 2. Limitée : les personnes concernées pourraient connaître des désagréments significatifs, qu'elles pourront surmonter malgré quelques difficultés<br>Ex : affection physique mineure (ex. : maladie bénigne suite au non respect de contre-indications), élévation de coûts (ex. : augmentation du prix d'assurance), difficultés relationnelles avec l'entourage personnel ou professionnel (ex. : image, réputation ternie, perte de reconnaissance) | G2. Significative : conséquences significatives mais limitées pour l'organisation (dégradation des performances de l'activité sans impact sur la sécurité des personnes et des biens, l'organisation surmontera la situation malgré quelques difficultés (fonctionnement en mode dégradé))<br>Ex : dégradation temporaire, données peu sensibles, intervention rapide | 2. Faible : impact modéré ou indirect (impact localisé, non permanent, nécessite des mesures correctrices simples ou des bonnes pratiques, utilisation modérée du cloud, empreinte maîtrisable, usage de données/matériel à faible intensité, compensation possible)<br>Ex : déploiement d'un assistant IA consommant modérément des ressources cloud (CPU, bande passante), utilisation de capteurs IA générant un surplus d'énergie ou de données traitées sans recyclage |
| 3. Élevé<br><br>("Risque élevé", ex : IA pour santé, emploi, justice) | 3. Importante : les personnes concernées pourraient connaître des conséquences significatives, qu'elles devraient pouvoir surmonter, mais avec des difficultés réelles et significatives<br>Ex : affection physique grave causant un préjudice à long terme (ex. : aggravation de l'état de santé suite à une mauvaise prise en charge, ou au non respect de contre-indications), interdiction bancaire, affection psychologique grave (ex. : dépression, développement d'une phobie) | G3. Grave : conséquences importantes pour l'organisation (forte dégradation des performances de l'activité, avec d'éventuels impacts significatifs sur la sécurité des personnes et des biens, l'organisation surmontera la situation avec de sérieuses difficultés (fonctionnement en mode très dégradé), sans impact sectoriel ou étatique)<br>Ex : compromission de données sensibles, interruption prolongée, gestion de crise nécessaire, risques juridiques et réputationnels | 3. Élevé : Impact étendu ou cumulatif (effets significatifs sur les ressources ou les émissions, potentiellement persistants, peut contribuer à la pression sur les écosystèmes ou au dérèglement climatique, calculs intensifs, stockage/énergie importants, pression sur ressources matérielles, impact environnemental notable)<br>Ex : entraînement de modèles LLM sur GPU à haute intensité énergétique, IA dans des objets connectés non recyclables produits à grande échelle |
| 4. Maximal<br><br>("Risque inacceptable", ex : notation sociale, manipulation, surveillance biométrique de masse) | 4. Maximale : les personnes concernées pourraient connaître des conséquences significatives, voire irrémédiables, qu'elles pourraient ne pas surmonter<br>Ex : décès (ex : meurtre, suicide, accident mortel), impossibilité de travailler, affection psychologique de longue durée ou permanente | G4. Critique : conséquences désastreuses pour l'organisation avec d'éventuels impacts sur l'écosystème (incapacité pour l'organisation d'assurer la totalité ou une partie de son activité, avec d'éventuels impacts graves sur la sécurité des personnes et des biens, l'organisation ne surmontera vraisemblablement pas la situation (sa survie est menacée), les secteurs d'activité ou étatiques dans lesquels elle opère seront susceptibles d'être légèrement impactés, sans conséquences durables) et G5. Catastrophique : conséquences sectorielles ou régaliennes au-delà de l'organisation (écosystème(s) sectoriel(s) impacté(s) de façon importante, avec des conséquences éventuellement durables, et/ou difficulté pour l'État, voire incapacité, d'assurer une fonction régalienne ou une de ses missions d'importance vitale, et/ou : impacts critiques sur la sécurité des personnes et des biens (crise sanitaire, pollution environnementale majeure, destruction d'infrastructures essentielles, etc.)<br>Ex : fuite massive de données critiques, dysfonctionnement généralisé, impact légal/réputationnel majeur, risque pour la pérennité | 4. Maximal : Impact critique ou irréversible (effets à grande échelle, à long terme ou irréversibles, dégradation majeure des écosystèmes, contribution significative à des risques systémiques environnementaux, modèles massifs, consommation énergétique élevée, externalisation des impacts, pas de compensation)<br>Ex : déploiement mondial d'un système IA nécessitant des centres de données à forte intensité carbone dans plusieurs pays, IA pilotant des chaînes de production entraînant surconsommation de matières premières rares ou polluantes |

</i>

### Action 1.3. Déterminer les suites à donner

**Les suites à donner sont déterminées en fonction du niveau de risque** :

| <center>**Niveau de risque**</center> | <center>**Approche par conformité (étape 2)**</center> | <center>**Approche par scénario (étape 3)**</center> |
| --- | --- | --- |
| 1. Minimal | Pas utile | Pas utile |
| 2. Faible | Conseillée | Pas utile |
| 3. Élevé | Oui | Oui |
| 4. Maximal | Oui | Oui |

>_Exemple : avec un niveau de risque 3. Élevé, les approches par conformité et par scénarios devraient être mises en œuvre._

## Étape 2. L'approche par conformité
L'approche par conformité devrait être mise en œuvre à partir du niveau de risque 3. Élevé (également conseillée pour 2. Faible).

Elle permet de **gérer les risques standards**, y compris ceux de cause accidentelle, **et les attaques cyber non ciblées**.

L'objectif est de **comparer les pratiques mises en oeuvre ou prévues pour le cas d'usage aux bonnes pratiques**, afin d'éclairer la prise de décision.

Notes :
- cette approche correspond à la « déclaration d'applicabilité » de l'[ISO/IEC 27001] et à l'« évaluation du socle de règles » de l'atelier 1 d'[EBIOS _Risk Manager_] ;
- le cas échéant, le résultat de cette étape peut être intégré au dossier d'homologation.

### Action 2.1. Choisir son référentiel

Parmi les nombreux référentiels de bonnes pratiques, il convient de **choisir le(s) plus pertinent(s) selon son contexte**, notamment :
- pour avoir une vision synthétique et globale, ou à défaut d'un choix précis de référentiel(s), il est possible d'utiliser tout ou partie des [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) ;
- si une politique interne est censée couvrir les référentiels applicables à l'organisation, il peut être pertinent d'en choisir les règles applicables au cas d'usage ;
- si le périmètre de compétence est limité (ex : si on ne peut traiter que de sécurité de l'information, il peut être pertinent de choisir le [Guide d'hygiène] ou le [Guide sécurité de la CNIL] (selon le niveau de maturité), et les [Recos ANSSI]) ;
- si certains référentiels doivent être employés (ex : s'il y a des données à caractère personnel, il peut être pertinent de choisir les [Lignes directrices AIPD], le [Guide sécurité de la CNIL] et les [Recos CNIL]) ;
- etc.

>_Exemple : s'agissant de mettre en place un système d'IA traitant des données à caractère personnelle, il est choisi de restreindre le champ des référentiels à ceux qui concernent le [Règlement IA] et le [RGPD] ; ces textes n'étant pas des référentiels de bonnes pratiques, il est choisi d'utiliser les [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md), qui intègre les obligations afférentes._

### Action 2.2. Évaluer la conformité aux bonnes pratiques

Pour ce faire, **évaluer chacune des bonnes pratiques retenues** :
- **si elle est jugée comme applicable** :
	- **si elle est appliquée, comment ?** L'explication fournie doit permettre d'évaluer le respect de la bonne pratique ;
	- **si elle n'est pas appliquée, quelles sont les mesures compensatoires ?** L'explication fournie doit permettre d'évaluer que les mesures prévues sont suffisantes pour atteindre un niveau de confiance aussi bon que si la bonne pratique était appliquée ;
- **si elle est jugée comme non applicable, pourquoi ?** L'explication fournie doit permettre de juger de son inapplicabilité (un chapitre entier peut être exclu s'il est traité par ailleurs ou en dehors de sa responsabilité, une bonne pratique sur un LLM n'est applicable qu'aux LLM, etc.).
 
La déclaration d'applicabilité en annexe des [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) peut être utilisée à cet effet.
 
Note : l'objectif n'est pas de respecter toutes les bonnes pratiques, mais de décrire ce qui est réellement prévu au regard de celles-ci.

> _Exemple : la déclaration d'applicabilité en annexe des [bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) est utilisée pour réaliser cette action ; l'évaluation globale met en évidence que de nombreuses bonnes pratiques sont applicables mais pas appliquées, et même que plusieurs sujets étaient éludés jusqu'à présent, notamment en matière d'interopérabilité, d'environnement et d'accessibilité._
> 
>[ /!\ à développer (DdA) /!\ ]

### Action 2.3. Améliorer la conformité aux bonnes pratiques

Pour chaque bonne pratique applicable, il convient de :
- **déterminer les mesures qui permettraient d'améliorer la conformité** aux bonnes pratiques applicables ;
- **les inscrire dans un plan de traitement des risques** ;
- si besoin, **évaluer les risques résiduels** (qui subsisteraient après application du plan de traitement des risques), de manière synthétique (ex : en formulant un événement qui pourrait se réaliser malgré les mesures prévues et ses conséquences potentielles), dans l'objectif de convaincre l'autorité que les risques résiduels ont été analysés, et qu'ils sont acceptables.

> _Exemple : pour traiter les sujes éludés, il est décidé de revoir la politique interne afin de (mieux) les intégrer ; et pour les nombreuses bonnes pratiques applicables mais non appliquées, des mesures sont déterminées et inscrites au plan de traitement des risques ; l'évaluation des risques résiduels n'est pas réalisée, car jugée trop compliquée et abstraite._
> 
>[ /!\ à développer (plan de traitement) /!\ ]

## Étape 3. L'approche par scénarios
L'approche par scénarios devrait être mise en œuvre à partir du niveau de risque 3. Élevé.

Elle permet de **gérer les attaques cyber avancées et ciblées**.

L'objectif est d'**identifier** et d'**apprécier les risques** que le cas d'usage est susceptible d'engendrer sur le(s) sujet(s) retenu(s), de **déterminer les mesures pour les traiter**, et de **présenter les risques résiduels** pour éclairer une prise de décision.

Pour ce faire, il convient de **mener une étude de risques par scénarios sur le cas d'usage avec les spécificités de l'IA**, par exemple en appliquant [EBIOS _Risk Manager_] au contexte spécifique des systèmes d'IA.

### Action 3.1. Établir le contexte

Le processus d'établissement du contexte (qui peut être réalisé avant ou pendant les processus suivants) devrait :
- détailler la description de l'**objet de l'étude** :
    - sa **mission** : la finalité du cas d’usage ;
	- ses **valeurs métier** (processus et données à protéger), notamment :
	    - ses **fonctionnalités d’IA** utilisées (voir les [cas d'usages](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Cas%20d'usages.md)) ;
		- le cas échéant, les **données d'entrainement** ;
		- les **données d'entrée** et leurs sources ;
		- les **données de sortie** et leurs destinataires ;
		- si possible, une **description fonctionnelle** (simple, ex : un schéma qui montre les sources de données, la chaine de traitements réalisés, les flux de données entre les traitements, jusqu'aux destinataires des données) ;
    - ses **biens supports** (matériels, logiciels, réseaux, personnes, organisations, canaux interpersonnels et locaux, sur lesquels reposent les valeurs métier et les mesures), notamment :
	    - les systèmes nécessaires à la mise en œuvre de l'objet de l'étude, notamment le **système d'IA** ;
		- si possible, leurs composants, notamment les **techniques d’IA** employées (voir les [cas d'usages](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Cas%20d'usages.md)) ;
		- si possible, une **description technique** (simple, ex : un schéma qui montre les systèmes utilisés, leurs interfaces et les fonctions qui peuvent y accéder) ;
	- ses **parties prenantes** (acteurs en dehors de l’objet de l’étude, qui interagissent avec celui-ci), notamment :
	    - le cas échéant, les **fournisseurs** ;
		- le cas échéant, les **clients** ;
		- autres ;
    - le cas échéant, les **éléments spécifiques requis par certains référentiels** (ex : durées d'utilisation prévues pour se conformer au [Règlement IA]) ;

- définir les **échelles de l’étude** (et qui devraient donc être adaptées au contexte, et comprises par les parties intéressées) :
    - pour **estimer la gravité des conséquences** (selon le contexte) :
		- sur les personnes ;
	    - sur l'organisation ;
		- sur les droits fondamentaux ;
		- sur l'environnement ;
		- autres ;
    - pour **estimer la vraisemblance des scénarios** ;
	- pour **évaluer les risques** et les risques résiduels.

Notes :
- cette approche emploie les outils utiles de la boîte à outils d’[EBIOS _Risk Manager_] ;
- elle correspond aux processus d' « établissement du contexte », d' « appréciation des risques » et de « traitement des risques » des normes relatives à la gestion des risques (ex : [ISO 31000], [ISO/IEC 27005]) ;
- le cas échéant, le résultat de cette étape peut constituer le cœur du dossier d'homologation.

<i>

> Exemple :
>
> Objet de l'étude :
> - mission : contrôler l’accès physique à une zone sécurisée ;
> - principales valeurs métier : données d'entrainement, empreintes biométriques, données captées, fonction de reconnaissance faciale, résultats d'identification ;
> - principaux biens supports : capteurs biométriques, réseau, algorithme de reconnaissance (modèles de Markov cachés), environnement d'entrainement, environnement de production, développeurs, administrateurs, zone sécurisée ;
> - principales parties prenantes : éditeur de l'algorithme, éditeurs des solutions logicielles (système d'exploitation, serveurs, etc.).
> 
> Échelles de l'étude (elles seront toutes utilisées) :
> 
> - pour la protection de la vie privée (cf. [RGPD]), la gravité des conséquences sur les personnes sera estimée à l'aide de l'échelle du guide [PIA-3] ;
> 
> - pour la sécurité de l'information (cf. [ISO/IEC 27005]), la gravité des conséquences sur l'organisation sera estimée à l'aide de l'échelle suivante :

| <center>**Gravité des conséquences sur l'organisation**</center> | <center>**Conséquences financières**</center> | <center>**Conséquences opérationnelles**</center> | <center>**Conséquences réputationnelles**</center> | <center>**Conséquences légales**</center> |
| --- | --- | --- | --- | --- |
| 1. Minimale | Aucun ou seulement quelques dizaines ou centaines d’euros annuels | Aucun ou seulement dégradation fonctionnelle avec peu de conséquence sur un processus | Aucun ou conséquence négligeable sur l’image | Aucun ou seulement sanction interne |
| 2. Limitée | Milliers d’euros annuels | Dégradation fonctionnelle limité sur un processus | Image impactée, mais de manière circonscrite et temporaire | Pénalités contractuelles avec des petits clients |
| 3. Importante | Dizaines de milliers d’euros annuels | Dégradation fonctionnelle limité sur plusieurs processus | Image atteinte de manière publique, mais limitée dans le temps | Pénalités contractuelles fortes (avec des grands comptes), mention dans une affaire civile ou pénale, non-respect de la loi et de la réglementation (protection de la vie privée notamment), enquête administrative, condamnation ou amende |
| 4. Maximale | Centaines de milliers d'euros annuels | Arrêt fonctionnel sur l’ensemble des processus | Image dégradée de manière profonde et durable | Non-respect majeur de la loi et de la réglementation (protection de la vie privée notamment), condamnation pénale, pénalités contractuelles avec plusieurs acteurs |

> Pour la conformité aux exigences du [Règlement AI], la gravité des conséquences sur les droits fondamentaux (cf. [Charte UE]) sera estimée à l'aide de l'échelle suivante :

| <center>**Gravité des conséquences sur les droits fondamentaux**</center> | <center>**Conséquences sur la dignité (cf. Art. 1–5)**</center> | <center>**Conséquences sur les libertés (cf. Art. 6–19)**</center> | <center>**Conséquences sur l'égalité (cf. Art. 20–26)**</center> | <center>**Conséquences sur la solidarité (cf. Art. 27–38)**</center> | <center>**Conséquences sur la citoyenneté (cf. Art. 39–46)**</center> | <center>**Conséquences sur la justice (cf. Art. 47–54)**</center> |
| --- | --- | --- | --- | --- | --- | --- |
| 1. Minimale | Expérience désagréable sans dommage physique ni moral (ex. commentaires inappropriés en ligne) | Restrictions légères ou temporaires (ex. blocage d’un contenu non critique) | Préjugé ou traitement désavantageux léger (ex. commentaires stéréotypés) | Accès limité à des ressources sociales ou protections (ex. retard dans la délivrance d’aides) | Difficultés mineures d’exercice des droits civiques (ex. problème administratif ponctuel pour voter) | Procédures lentes ou formalités complexes sans conséquence majeure (ex. retard dans le traitement d’une plainte) |
| 2. Limitée | Atteinte physique ou psychologique limitée (ex. harcèlement ciblé) | Restriction d’accès à l’information ou à la communication (ex. censure ciblée) | Discrimination ponctuelle ou limitée (ex. refus d’un service sur un critère non autorisé) | Accès partiel aux services essentiels (ex. traitement médical retardé ou incomplet) | Restrictions partielles du droit de participation ou d’information (ex. retard dans l’accès aux documents publics) | Procédures biaisées ou erreurs mineures (ex. jugement partiellement incorrect ou contestable) |
| 3. Importante | Atteinte grave à l’intégrité (ex. violence physique, contrainte coercitive) | Limitation significative des libertés fondamentales (ex. interdiction de manifestation, surveillance intrusive) | Discrimination systémique ou répétée (ex. algorithme de recrutement biaisé) | Privation significative de droits sociaux ou protections (ex. exclusion prolongée du système de santé) | Limitation grave de la participation civique ou politique (ex. incapacité de vote ou de recours judiciaire) | Procédures injustes entraînant un préjudice sérieux (ex. condamnation injustifiée, sanction disproportionnée) |
| 4. Maximale | Atteinte majeure à la vie ou à l’intégrité (ex. torture, esclavage, mise en danger de la vie) | Privation totale de libertés (ex. détention arbitraire, interdiction de parole ou de croyance) | Discrimination majeure affectant l’accès à la vie sociale ou professionnelle (ex. exclusion totale d’un emploi, logement ou service) | Privation critique entraînant un risque vital ou grave préjudice social (ex. interdiction d’accès à soins vitaux ou protection minimale) | Privation totale des droits civiques et démocratiques (ex. exclusion complète du système électoral, impossibilité d’accès à la justice) | Absence totale de recours ou violation grave des droits procéduraux (ex. condamnation arbitraire, traitement inéquitable majeur) |
 
> La **vraisemblance** sera estimée à laide de l'échelle suivante :

| <center>**Vraisemblance**</center> | <center>**Description**</center> |
| --- | --- |
| 1. Minimale | La source de risque a peu de chances d’atteindre son objectif visé selon l’une des chaînes d’attaque envisagées. La vraisemblance du scénario est faible |
| 2. Faible | La source de risque est susceptible d’atteindre son objectif visé selon l’une des chaînes d’attaque envisagées. La vraisemblance du scénario est significative |
| 3. Importante | La source de risque va probablement atteindre son objectif visé selon l’une des chaînes d’attaque envisagées. La vraisemblance du scénario est élevée |
| 4. Maximale | La source de risque va certainement atteindre son objectif visé selon l’une des chaînes d’attaque envisagées OU un tel scénario s’est déjà produit au sein de l’organisme (historique d’incidents) |

> L'évaluation des risques et des risques résiduels sera réalisée à la cartographie suivante :

| <center>**Évaluation<br>des risques**</center> |  | <center>**Vraisemblance**</center> |  |  |  |
| --- | --- | --- | --- | --- | --- |
|  |  | **1. Minimale** | **2. Limitée** | **3. Importante** | **4. Maximale** |
| **Gravité** | **4. Maximale** | Tolérable sous contrôle | Tolérable sous contrôle | Inacceptable | Inacceptable |
|  | **3. Importante** | Acceptable en l'état | Tolérable sous contrôle | Tolérable sous contrôle | Inacceptable |
|  | **2. Limitée** | Acceptable en l'état | Acceptable en l'état | Tolérable sous contrôle | Tolérable sous contrôle |
|  | **1. Minimale** | Acceptable en l'état | Acceptable en l'état | Acceptable en l'état | Tolérable sous contrôle |

</i>

### Action 3.2. Apprécier les risques

Le processus d'appréciation des risques devrait :
- apprécier les **événements redoutés** :
    - situer les conséquences potentielles d'une disparition de données, d'une modification non désirée de données et d'un accès non autorisé à des données correspondant à chaque valeur métier dans chaque échelle de gravité définie à cet effet ;
	- retenir la gravité la plus élevée ;
	- si possible, illustrer les événements redoutés ainsi analysés par un exemple parlant ;
- analyser les **sources de risques** :
    - identifier les attaquants qui sont les plus susceptibles d’engendrer chaque événement redouté ;
    - déterminer leurs objectifs visés (ils peuvent être au-delà de l'objet de l'étude) ;
- analyser les **scénarios stratégiques** :
    - identifier les différents chemins que les sources de risques identifiées sont les plus susceptibles d'emprunter au sein des parties prenantes pour mener à chaque événement redouté et atteindre leurs objectifs visés (ex : attaque directe de l’objet de l’étude, compromission d’un produit d’un fournisseur) ;
	- retenir le plus vraisemblable ;
- apprécier les **scénarios opérationnels** :
    - analyser les différentes chaînes d’attaque (séquences d'actions élémentaires qui exploitent les vulnérabilités des biens supports) que les sources de risques sont susceptibles de réaliser pour mettre en œuvre les scénarios stratégiques retenus (pour les attaques spécifiques aux systèmes d'IA, se référer aux fiches du [Guide France IA] ou à [ATLAS]) ;
	- si possible, formuler un libellé court et parlant pour les scénarios opérationnels ainsi analysés ;
    - estimer leur vraisemblance à l'aide de l'échelle définie à cet effet, compte tenu des mesures existantes ou prévues ;
	- retenir le scénario opérationnel le plus vraisemblable ;
- déterminer les **risques** :
    - constituer les risques : ils sont composés d'un événement redouté et du scénario opérationnel retenu ;
    - déterminer leurs niveaux : la gravité est celle de l’événement redouté considéré, la vraisemblance est celle du scénario opérationnel retenu ;
    - évaluer les risques : les positionner dans l'échelle définie à cet effet.

<i>

> Exemple :
> 
> Le tableau suivant présente l'appréciation des risques :

| <center>**Risque**</center> | <center>**Valeur métier**</center> | <center>**Événement redouté**</center> | <center>**Gravité** (et principales conséquences)</center> | <center>**Principale source de risque** (et objectifs visés)</center> | <center>**Principal scénario stratégique**</center> | <center>**Principal scénario opérationnel** (détail plus bas)</center> | <center>**Vraisemblance**</center> |
| --- | --- | --- | --- | --- | --- | --- | --- |
| R01 | Fonction de reconnaissance faciale | Disparition | 2. Limitée (opérationnel : accès bloqués) | Crime organisé (extorsion) | Attaque directe | Destruction physique ou logique | 2. Limitée |
| R02 | Fonction de reconnaissance faciale | Modification non désirée | **3. Importante (droits fondamentaux / vie privée : discrimination)** | Acteur étatique / concurrent (sabotage ou manipulation) | Attaque via l'éditeur du modèle | Injection de biais dans modèle | **3. Importante** |
| R03 | Fonction de reconnaissance faciale | Accès non autorisé | 1. Minimale (image) | Employé malveillant (revente) | Attaque directe | Exfiltration d’algorithme ou paramètres | 1. Minimale |
| R04 | Données d'entraînement | Disparition | 2. Limitée (coût humain et financier) | Crime organisé (sabotage ciblé) | Attaque directe | Suppression ou corruption de jeux de données | 2. Limitée |
| R05 | Données d'entraînement | Modification non désirée | 2. Limitée (droits fondamentaux / vie privée : biais, discrimination) | Concurrent (sabotage) | Attaque directe | Empoisonnement des données d’entrainement | 2. Limitée |
| R06 | Données d'entraînement | Accès non autorisé | 2. Limitée (vie privée) | Crime organisé (revente) | Attaque directe | Exfiltration de données sensibles | 1. Minimale |
| R07 | Empreintes biométriques | Disparition | 2. Limitée (opérationnel : accès bloqués) | Crime organisé (sabotage) | Attaque directe | Suppression de données | **3. Importante** |
| R08 | Empreintes biométriques | Modification non désirée | **3. Importante (sécurité : accès de personnes non autorisées)** | Acteur étatique (infiltration) | Attaque via un éditeur de logiciels | Altération de données | **4. Maximale** |
| R09 | Empreintes biométriques | Accès non autorisé | **4. Maximale (droits fondamentaux / vie privée : usurpations, empreinte inutilisable à vie)** | Crime organisé (usurpation) | Attaque directe | Exfiltration via API | **3. Importante** |
| R10 | Données captées | Disparition | 2. Limitée (opérationnel : accès bloqués) | Vandale (idéologie) | Attaque directe | Sabotage des caméras | 2. Limitée |
| R11 | Données captées | Modification non désirée | **3. Importante (sécurité : accès de personnes non autorisées, opérationnel : accès bloqués)** | Acteur étatique (infiltration) | Attaque directe | Injection de fausses données | 2. Limitée |
| R12 | Données captées | Accès non autorisé | 2. Limitée (vie privée) | Acteur étatique (espionnage) | Attaque directe | Exfiltration de flux vidéo | **3. Importante** |
| R13 | Résultats d'identification | Disparition | 2. Limitée (opérationnel : accès bloqués) | Crime organisé (extorsion) | Attaque directe | Suppression de données | 3. Importante |
| R14 | Résultats d'identification | Modification non désirée | **3. Importante (sécurité : accès de personnes non autorisées)** | Acteur étatique (infiltration) | Attaque directe | Modification de résultats | 2. Limitée |
| R15 | Résultats d'identification | Accès non autorisé | **3. Importante (sécurité : rejeu pour accès de personnes non autorisées)** | Acteur étatique (infiltration) | Attaque directe | Usage de faux résultats | 2. Limitée |

> Le tableau suivant présente le détail des scénarios opérationnels :

| **Scénarios opérationnels** | **Chaînes d’attaques (_kill chain_)** |
| --- | --- |
| Destruction physique ou logique | 1. Identification des serveurs/applications ou locaux hébergeant l'algorithme <br> 2. Accès physique ou admin (compte vulnérable) <br> 3. Suppression de fichiers / container de l’algorithme <br> 4. Vérification de l'indisponibilité de l'algorithme |
| Injection de biais dans modèle | 1. Identification du _pipeline_ d’entrainement <br> 2. Compromission d'un _package_ du fournisseur (pipeline vulnérable) <br> 3. Injection de données empoisonnées <br> 4. Déploiement du modèle biaisé en production |
| Exfiltration d’algorithme ou paramètres | 1. Identification de comptes d'administrateurs <br> 2. _Phishing_ <br> 3. Téléchargement de l'algorithme ou de paramètres <br> 4. Exfiltration vers un serveur externe |
| Suppression ou corruption de jeux de données | 1. Localisation du stockage des jeux de données <br> 2. Exploitation d'une vulnérabilité du serveur <br> 3. Compromission de l'accès <br> 4. Suppression ou altération de jeux de données |
| Empoisonnement des données d’entrainement | 1. Identification de points d'ingestion de jeux de données <br> 2. Injection de données malveillantes <br> 3. Lancement de ré-entrainement automatique <br> 4. Propagation de biais du modèle |
| Exfiltration de données sensibles | 1. Identification de comptes avec accès aux jeux de données <br> 2. _Phishing_ ciblé ou compromission d’accès <br> 3. Téléchargement de jeux de données <br> 4. Exfiltration vers un serveur externe |
| Suppression de données | 1. Identification des serveurs de traitement des empreintes <br> 2. Exploitation d'une vulnérabilité applicative <br> 3. Suppression |
| Altération de données | 1. Identifier d'éditeurs de logiciels concernés <br> 2. Corruption de correctifs <br> 3. Déploiement des correctifs validés <br> 4. Accès physique à la zone sécurisée |
| Exfiltration via API | 1. Cartographie des APIs / _endpoints_ <br> 2. Exploitation d'une API non protégée <br> 3. Téléchargement de templates <br> 4. Usage _offline_ pour usurpation |
| Sabotage des caméras | 1. Localisation des caméras <br> 2. Accès physique <br> 3. Destruction physique |
| Injection de fausses données | 1. Identification des flux et protocoles utiles <br> 2. MITM / _replay frames_ <br> 3. Injection de _deepfakes_ <br> Accès physique à la zone sécurisée |
| Exfiltration de flux vidéo | 1. Identification d'équipements vulnérables <br> 2. Compromission du routeur / _switch_ <br> 3. _Sniffing_ et enregistrement des flux <br> 4. Exfiltration |
| Suppression de données | 1. Identification de services dépendants <br> 2. Compromission de la base de données en production et des sauvegardes <br> 3. Suppression de résultats d'identifications |
| Modification de résultats | 1. Identification d'administrateurs <br> 2. Chantage <br> 3. Validation frauduleuse <br> 4. Accès physique à la zone sécurisée |
| Usage de faux résultats | 1. Collecte des horaires & routines <br> 2. Compromission de l'API des résultats <br> 3. Génération de faux accès <br> 4. Accès physique à la zone sécurisée |

> La cartographie des risques est la suivante :

| <center>**Évaluation<br>des risques**</center> |  | <center>**Vraisemblance**</center> |  |  |  |
| --- | --- | --- | --- | --- | --- |
|  |  | **1. Minimale** | **2. Limitée** | **3. Importante** | **4. Maximale** |
| **Gravité** | **4. Maximale** |  |  | R09 |  |
|  | **3. Importante** |  |  | R02 R11 R14 R15 | R08 |
|  | **2. Limitée** | R06 | R01 R04 R05 R10 | R07 R12 R13 |  |
|  | **1. Minimale** | R03 |  |  |  |

</i>

### Action 3.3. Traiter les risques

Le processus de traitement des risques devrait :
- déterminer les **mesures** : si possible, tout au long de l’étude, ou sinon après l'appréciation des risques, déterminer les mesures qui contribuent à traiter les événements redoutés, les sources de risques, les scénarios stratégiques et les scénarios opérationnels (considérer les mesures spécifiques aux systèmes dIA de l’Annexe 1. III du [Guide France IA] et d'[ATLAS], ainsi que les recommandations ([Recos ANSSI], [Recos CNIL], etc.) qui n'auraient pas été retenues dans l'étape précédente) ;
- compléter le **plan de traitement des risques** : planifier les mesures déterminées ;
- réestimer la gravité et la vraisemblance des risques résiduels (qui subsistent après application des mesures) ;
- si besoin, repositionner les risques sur la **cartographie des risques** ;
- le cas échéant, **déterminer des mesures complémentaires** jusqu'à rendre les risques acceptables ou proposer d'accepter les risques tels quels.

<i>

> Exemple :
> 
> Le tableau suivant présente les mesures additionnelles prévues pour contribuer à traiter les risques, ainsi que les risques résiduels :
>
> [ /!\ à revoir à partir d'ici /!\ ]

| **Risque** | **Mesures additionnelles** | **Gravité résiduelle** | **Vraisemblance résiduelle** |
| --- | --- | --- | --- |
| R01 | Mettre en place une sauvegarde automatique chiffrée quotidienne (testée tous les 6 mois) <br> Mettre en place une authentification à double facteurs (MFA) <br> Mettre en place un outil de surveillance et d'alertes d'indisponibilité du service | = 2. Limitée | = 2. Limitée |
| R02 | Vérifier le _hash_ / la signature des _packages_ utilisés <br> Valider manuellement les modèles <br> Créer une liste blanche des sources fournisseurs | = 3. Importante | ↘ 2. Limitée |
| R03 | Renforcer la journalisation des accès et des actions <br> Revoir les droits d'accès tous les 3 mois | 3 | 2 |
| R04 | Chiffrement at-rest + clés locales <br> Backups immuables <br> Accès restreint par comptes dédiés | 2 | 2 |
| R05 | Filtrage/validation datasets entrants <br> Sandbox d’entraînement <br> Checklist humaine avant ré-entrainement | 3 | 2 |
| R06 | MFA + segmentation stockage <br> Alertes accès inhabituels <br> Logging et audits réguliers | 3 | 2 |
| R07 | Chiffrement templates <br> Accès physique restreint <br> Journaux d’accès + alertes | 3 | 2 |
| R08 | Revue modifications <br> Validation multi-acteurs <br> Logs + alertes | 3 | 2 |
| R09 | API sécurisée + rate limit <br> MFA pour API <br> Monitoring et alertes | 3 | 2 |
| R10 | Verrouillage physique des caméras <br> Surveillance <br> Backups local/central | 2 | 2 |
| R11 | Signature flux vidéo <br> Monitoring anomalies <br> Vérification humaine aléatoire | 2 | 2 |
| R12 | Chiffrement flux vidéo <br> Accès restreint <br> Journaux + alertes | 3 | 2 |
| R13 | Backups immuables <br> Revue droits DBA <br> Alertes suppression DB | 2 | 2 |
| R14 | Validation multi-acteurs <br> Logging modifications <br> Alertes automatisées | 3 | 2 |
| R15 | MFA API + tokens courts <br> Journaux + alertes <br> Surveillance physique entrée | 3 | 2 |

> Le tableau suivant présente le plan de traitement des risques :

| <center>**Priorité**</center> | <center>**Mesure**</center> | <center>**Risques traités**</center> | <center>**Service**</center> | <center>**Apport**</center> | <center>**Difficulté**</center> | <center>**Délais**</center> |
|------------|-------------------|------------|------------|----------------|-------------------------------|--------------|
|  | Mettre en place une sauvegarde automatique chiffrée quotidienne (testée tous les 6 mois) | R01, R04, R13 | DSI | 5 | 2 | 1 mois |
|  | Backups immuables | R04, R13 | DSI | 5 | 3 | 1 mois |
|  | Chiffrement at-rest + clés locales | R04, R07, R12 | DSI | 5 | 3 | 1 mois |
|  | Mettre en place une authentification à double facteurs (MFA) | R01, R03, R06 | DSI | 4 | 2 | 1 mois |
|  | MFA API + tokens courts | R09, R15, R12 | DSI | 4 | 2 | 1 mois |
|  | Vérifier le _hash_ / la signature des _packages_ utilisés | R02 | DevOps | 4 | 2 | 2 mois |
|  | Filtrage / validation datasets entrants | R05 | Data | 4 | 2 | 2 mois |
|  | Revoir les droits d'accès tous les 3 mois | R03, R06, R09, R14 | DSI / SecOps | 4 | 2 | 2 mois |
|  | Accès restreint par comptes dédiés | R04, R06, R07 | DSI | 4 | 2 | 2 mois |
|  | Sandbox d’entraînement | R05, R02 | Data | 4 | 3 | 2 mois |
|  | Mettre en place un outil de surveillance et d'alertes d'indisponibilité du service | R01, R02 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Créer une liste blanche des sources fournisseurs | R02, R05 | DevOps | 3 | 2 | 3 mois |
|  | Valider manuellement les modèles | R02 | Data | 3 | 2 | 3 mois |
|  | Renforcer la journalisation des accès et des actions | R03, R06, R09, R14, R15 | DSI | 3 | 2 | 2 mois |
|  | Alertes accès inhabituels | R03, R06, R09 | DSI | 3 | 2 | 2 mois |
|  | Logging et audits réguliers | R03, R06, R09 | DSI | 3 | 2 | 2 mois |
|  | Chiffrement templates | R07, R08, R09 | DSI | 3 | 2 | 2 mois |
|  | Accès physique restreint | R07, R10, R15 | Moyens généraux | 3 | 2 | 2 mois |
|  | Renforcer la journalisation des accès et des actions | R07, R08 | DSI | 3 | 2 | 2 mois |
|  | Revue modifications | R08, R14 | DSI / Data | 3 | 2 | 2 mois |
|  | Validation multi-acteurs | R02, R08, R14 | DSI / Data | 3 | 2 | 2 mois |
|  | API sécurisée + rate limit | R09, R15 | DevOps | 3 | 2 | 2 mois |
|  | Monitoring et alertes | R09, R12, R15 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Verrouillage physique des caméras | R10 | Moyens généraux | 3 | 2 | 1 mois |
|  | Backups local/central | R10, R11, R12 | DSI | 3 | 2 | 2 mois |
|  | Signature flux vidéo | R11, R12 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Vérification humaine aléatoire | R11, R12 | Data / SecOps | 3 | 2 | 2 mois |
|  | Chiffrement flux vidéo | R12 | DSI | 3 | 2 | 2 mois |
|  | Renforcer la journalisation des accès et des actions | R12, R14, R15 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Revue droits DBA | R13, R14 | DBA | 3 | 2 | 2 mois |
|  | Alertes suppression DB | R13 | DBA | 3 | 2 | 2 mois |
|  | Logging modifications | R08, R14 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Alertes automatisées | R08, R14 | DSI / SecOps | 3 | 2 | 2 mois |
|  | Surveillance physique entrée | R15 | Facilities / SecOps | 3 | 2 | 2 mois |

> La cartographie des risques résiduels est la suivante :

| <center>**Évaluation<br>des risques**</center> |  | <center>**Vraisemblance**</center> |  |  |  |
| --- | --- | --- | --- | --- | --- |
|  |  | **1. Minimale** | **2. Limitée** | **3. Importante** | **4. Maximale** |
| **Gravité** | **4. Maximale** |  |  | R09 |  |
|  | **3. Importante** |  |  | R02 R11 R14 R15 | R08 |
|  | **2. Limitée** | R06 | R01 R04 R05 R10 | R07 R12 R13 |  |
|  | **1. Minimale** | R03 |  |  |  |

</i>