# Intelligence artificielle (IA) - Critères de confiance

## Objet du document
**Ce document propose une liste de "critères de confiance", qui harmonise les différents critères ou objectifs des nombreux documents de références en matière d’intelligence artificielle (IA)**.
Il sert de base à la constitution de bonnes pratiques harmonisées, et pourrait également servir à affiner les critères utilisés dans une démarche de gestion des risques, ou pour structurer des objectifs ou des mesures.

[Avant-propos](#avant-propos)<br/>
[Introduction](#introduction)<br/>
[1. Gouvernance responsable](#1-gouvernance-responsable)<br/>
[2. Fiabilité et sûreté](#2-fiabilité-et-sûreté)<br/>
[3. Équité](#3-équité)<br/>
[4. Transparence](#4-transparence)<br/>
[5. Sécurité de l'information](#5-sécurité-de-l-information)<br/>
[6. Protection des droits et libertés](#6-protection-des-droits-et-libertés)<br/>
[7. Maintenance et évolutivité](#7-maintenance-et-évolutivité)<br/>
[8. Interopérabilité](#8-interopérabilité)<br/>
[9. Respect de l'environnement](#9-respect-de-l-environnement)<br/>
[10. Accessibilité](#10-accessibilité)<br/>

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
- Matthieu GRALL, expert-conseil en management des données, sécurité de l’information, protection de la vie privée et nouvelles technologies.

Les **versions** du document sont les suivantes :
| <center>**Version**</center> | <center>**Action**</center> | <center>**Éditeur**</center> | <center>**État**</center> |
| --- | --- | --- | ---|
| 06/04/2025 (v0.1) | Création du document | Matthieu GRALL |
| 10/04/2025 (v0.2) | Transformation des « descriptions » des critères de confiance en « Portées » (pour mieux distinguer « Portées », qui désignent ce qui est couvert, et « objectifs », qui sont présentés dans les bonnes pratiques), corrections mineures (mises en cohérence avec les autres documents) | Matthieu GRALL |
| 23/04/2025 (v0.3) | Transformation en _markdown_ | Matthieu GRALL |
| 07/05/2025 (v1.0) | Finalisation d'une première version complète, cohérente, et en _markdown_ | Matthieu GRALL |
| 11/07/2025 (v1.1) | Simplification et harmonisation des chapitres introductifs, corrections mineures | Matthieu GRALL |

## Introduction
**Pour obtenir une liste de critères de confiance des systèmes basés sur l’IA, on se heurte à la pluralité des principaux documents de référence**<sup><a href="#note1" id="ref1">[1]</a></sup> qui comprennent des exigences, règles et recommandations liées à l’IA ou applicables à l’IA. Ils ne sont pas vraiment cohérents, que ce soit en termes de champs d’application, de formulations, de classements, et de langue. On a donc de nombreuses redondances dans l’ensemble et de nombreux manques dans chaque, si on souhaite une vision globale.

**Toutefois, les idées convergent toutes, ou se complètent plutôt bien**. On peut donc faire émerger une liste de ces critères de confiance, exhaustive et « non recouvrante », qui traite de l’ensemble des aspects qui peuvent devoir être considérés quand on crée un système basé sur l’IA.

Ainsi, tout système basé sur l’IA devrait :
1. reposer sur une **gouvernance responsable** (notion d’_accountability_) ;
2. assurer la **fiabilité**, et la **sûreté** des personnes et des biens ;
3. être *équitable* (notion de _fairness_) ;
4. garantir la **transparence** ;
5. assurer la **sécurité des informations** ;
6. protéger les **droits et libertés des personnes** ;
7. assurer la **maintenabilité** et l’**évolutivité** ;
8. permettre l’**interopérabilité** ;
9. respecter l’**environnement** ;
10. assurer l’**accessibilité**.

## 1. Gouvernance responsable
Portée : pilotage éthique, transparent et responsable, incluant la mise en place de mécanismes de contrôle, de _reporting_ et de gestion des conflits d’intérêts.
<br/>
<br/>
Principaux risques : décisions unilatérales, conflits d’intérêts, manque de supervision, opacité décisionnelle.

## 2. Fiabilité et sûreté
Portée : robustesse, performance, stabilité, résilience, précision, absence d'erreurs, capacité à fonctionner correctement, sans mettre en danger la vie humaine, les biens ou l'environnement, dans des conditions variées, incertaines ou inattendues, même en conditions de stress ou d’attaque.
<br/>
<br/>
Principaux risques : dysfonctionnements, accidents, attaques malveillantes, défaillances techniques.

## 3. Équité
Portée : fonctionnement de l’IA sans biais, traitement impartial et équitable des usagers, non-discrimination.
<br/>
<br/>
Principaux risques : discriminations ou inégalités d’accès, du fait de biais dans la formulation des cas d’usages<sup><a href="#note2" id="ref2">[2]</a></sup>, liés aux données d’entrée<sup><a href="#note3" id="ref3">[3]</a></sup>, aux données d’entrainement et de validation<sup><a href="#note4" id="ref4">[4]</a></sup>, à l’algorithme d’entrainement / à l’architecture du modèle<sup><a href="#note5" id="ref5">[5]</a></sup>, aux données de sortie<sup><a href="#note6" id="ref6">[6]</a></sup>.

## 4. Transparence
Portée : compréhension des processus et décisions, explicabilité, traçabilité des données, possibilité de contester et vérifier le fonctionnement.
<br/>
<br/>
Principaux risques : opacité, incompréhension des mécanismes, perte de confiance.

## 5. Sécurité de l'information
Portée : protection de la disponibilité, de l’intégrité et de la confidentialité des données, gestion des risques liés à la sécurité de l’information engendrés par les systèmes d’IA (au-delà du critère de confiance de fiabilité).
<br/>
<br/>
Principaux risques : cyberattaques, fuites de données, corruption de systèmes.

## 6. Protection des droits et libertés
Portée : respect de la vie privée, protection des données à caractère personnel et des droits fondamentaux, gestion des risques sur les droits et libertés des personnes concernées engendrés par les systèmes d’IA (au-delà du critère de confiance d’équité).
<br/>
<br/>
Principaux risques : atteintes à la vie privée, usage abusif des données personnelles.

## 7. Maintenance et évolutivité
Portée : maintien en conditions opérationnelle et de sécurité, adaptation du système d’IA au fil du temps pour résoudre des problèmes et être utilisé pour de nouveaux besoins.
<br/>
<br/>
Principaux risques : obsolescence logicielle, incompatibilités, pertes de performance.

## 8. Interopérabilité
Portée : compatibilité entre différents systèmes d'IA, intégration du système d’IA avec d’autres outils et normes existants, capacité à échanger des informations.
<br/>
<br/>
Principaux risques : verrouillage technologique, incompatibilités de formats<sup><a href="#note7" id="ref7">[7]</a></sup>.

## 9. Respect de l’environnement
Portée : maîtrise de l’empreinte écologique globale associée au développement, au déploiement et à l’exploitation de technologies d’IA, maîtrise de la consommation énergétique, gestion des risques sur l’environnement engendrés par les systèmes d’IA.
<br/>
<br/>
Principaux risques : consommation excessive d’énergie, émissions de CO₂.

## 10. Accessibilité
Portée : accès aux systèmes d'IA, notamment pour les personnes handicapées, gestion des risques d’inégalités engendrés par les systèmes d’IA.
<br/>
<br/>
Principaux risques : exclusion numérique, inégalités d’accès, manque de compatibilité avec les technologies d’assistance.

<br/>
<br/>
<a name="note1" id="note1">[1]</a> Notamment [Règlement IA], [ISO/IEC 42001], [Lignes directrices IA de l'UE], [Loi I&L], [NIST AI RMF], [Principes de l'OCDE sur l’IA], [Recommandation IA de l’OCDE], [Recommandations IA de l’ANSSI - 2024], [Recommandations IA de l’ANSSI - 2025], [Recommandations IA de la CNIL], [RGAA], [RGESN], [RGI], et [RGIAF]. [↩](#ref1)
<br/>
<br/>
<a name="note1" id="note1">[2]</a> Manque d’équité par défaut de cadrage du cas d’usage. [↩](#ref2)
<br/>
<br/>
<a name="note1" id="note1">[3]</a> Prises de décisions basées sur des données incomplètes ou non équilibrées. [↩](#ref3)
<br/>
<br/>
<a name="note1" id="note1">[4]</a> Biais dans les données de l'échantillon (si l'ensemble de données d’entrainement n'est pas représentatif de la population), identification et transformation des caractéristiques sensibles (si un groupe défavorisé est présent dans l'échantillon, modifier les pondérations du modèle de manière à modifier le résultat pour ce groupe défavorisé), biais dans la représentation des différentes classes ou catégories de données (ce qui peut entraîner des résultats non représentatifs, inexacts ou injustes), biais dans les corrélations entre les caractéristiques ou les variables utilisées (ce qui peut conduire à des prédictions biaisées). [↩](#ref4)
<br/>
<br/>
<a name="note1" id="note1">[5]</a> Biais introduits à la suite de la conception du modèle, donnant des résultats trompeurs même à partir de données fiables et de qualité, du fait de la construction du modèle (l'architecture du modèle elle-même peut présenter des problèmes inhérents, entraînant des biais tels que le biais de régression, le biais de classification, le biais de clustering, etc. ; il peut y avoir des erreurs de calcul dans les paramètres du modèle, entraînant des modèles sur/sous-ajustés, qui introduisent des biais et du bruit dans les données de sortie) ou de la dérive du modèle (le cas d’usage peut évoluer avec le temps, de sorte que le modèle peut devenir obsolète et nécessiter une re-modélisation et un recyclage au fil du temps, réintroduisant les biais mentionnés ci-dessus à chaque étape). Les impacts potentiels concernent des décisions discriminatoires ou injustes basées sur des caractéristiques personnelles ou des groupes de personnes spécifiques, la partialité ou les préjugés dans les résultats produits par l'algorithme. [↩](#ref5)
<br/>
<br/>
<a name="note1" id="note1">[6]</a> Risque de produire des résultats de sortie discriminatoires ou injustes, qui peuvent avoir un impact négatif sur les utilisateurs ou les parties prenantes concernées, risque de renforcer les stéréotypes ou les préjugés existants à travers les résultats produits par l'IA. [↩](#ref6)
<br/>
<br/>
<a name="note1" id="note1">[7]</a> Comme tout service numérique, ceux qui reposent sur l’IA peuvent ne pas pouvoir interagir avec les autres si les technologies ou les données utilisées ne sont pas cohérentes ou compatibles entre elles. [↩](#ref7)
