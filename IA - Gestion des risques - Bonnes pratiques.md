# Intelligence artificielle - Bonnes pratiques

## Objet du document
**Ce document propose une liste de bonnes pratiques qui permettent de respecter les critères de confiance que tout système d’intelligence artificielle (IA) devrait respecter**.
Il harmonise les différents critères ou objectifs, ainsi que les bonnes pratiques associées, qui figurent dans les nombreux documents de références en matière d'IA.
Il peut être directement utilisé dans le cadre des projets de nouveaux services qui reposent sur l’IA pour comparer ce qui est prévu ou mis en œuvre aux bonnes pratiques, et peut également être intégré à une démarche de gestion des risques.

[Avant-propos](#avant-propos)<br>
[Introduction](#introduction)<br>
[1. Gouvernance responsable](#1-gouvernance-responsable)<br>
[2. Fiabilité et sûreté](#2-fiabilité-et-sûreté)<br>
[3. Équité](#3-équité)<br>
[4. Transparence](#4-transparence)<br>
[5. Sécurité de l'information](#5-sécurité-de-linformation)<br>
[6. Protection des droits et libertés](#6-protection-des-droits-et-libertés)<br>
[7. Maintenabilité et évolutivité](#7-maintenabilité-et-évolutivité)<br>
[8. Interopérabilité](#8-interopérabilité)<br>
[9. Respect de l'environnement](#9-respect-de-lenvironnement)<br>
[10. Accessibilité](#10-accessibilité)<br>
[Annexe : déclaration d'applicabilité (DdA)](#annexe--déclaration-dapplicabilité-dda)<br>

## Avant-propos
Ce document s’inscrit dans un [ensemble de documents méthodologiques](https://github.com/matthieu-grall/ai) en amélioration continue, destinés à aider les organismes à gérer les risques liés à l’IA, et qui peuvent être utiles ensemble ou séparément.
Les [documents de référence](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Documents%20de%20r%C3%A9f%C3%A9rence.md) sont utilisés entre crochets dans le corps du document.

Il est placé sous la **licence** suivante :
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

Les principaux **contributeurs** sont les suivants :
- Matthieu GRALL ;
- Cécile LAMARQUE.

Les **versions** du document sont les suivantes :
| <center>**Version**</center> | <center>**Action**</center> | <center>**Éditeur**</center> | 
| --- | --- | --- | 
| 06/04/2025 (v0.1) | Création du document | Matthieu GRALL |
| 10/04/2025 (v0.2) | Rédaction de l’introduction, réorganisation et harmonisation des bonnes pratiques, ajout de l’annexe, corrections mineures (reformulations, mises en cohérences) | Matthieu GRALL |
| 30/04/2025 (v0.3) | Transformation du document en _markdown_ | Cécile LAMARQUE |
| 07/05/2025 (v0.4) | Harmonisation du document avec les autres | Matthieu GRALL |
| 07/05/2025 (v1.0) | Finalisation d'une première version complète, cohérente, et en _markdown_ | Matthieu GRALL |
| 11/07/2025 (v1.1) | Simplification et harmonisation des chapitres introductifs, corrections mineures | Matthieu GRALL |
| 20/07/2025 (v1.2) | Ajout de _tags_ pour indiquer la correspondance avec les mesures de l'[ISO/IEC 42001], les phases du cycle de vie de la [Recommandation de l'OCDE], des observables illustratifs et des fonctions types concernées, transformation des bonnes pratiques en tableaux, corrections mineures | Matthieu GRALL |
| 02/10/2025 (v1.3) | Intégration du contenu du document qui définissait indépendamment les critères de confiance, ajout de références à [ISO/IEC 27090] et [IEC 61508], correction des liens de retour des références | Matthieu GRALL |
| 23/10/2025 (v1.4) | Corrections mineures (mise en cohérence des libellés courts des documents de référence qui ont été changés, harmonisation des balises "br", correction des notes de bas de page) | Matthieu GRALL |
| 06/11/2025 (v1.5) | Ajout de risques liés à la protection des droits fondamentaux dans chaque section, ajout de références au [Règlement IA] dans les bonnes pratiques concernées, ajout de mesures additionnelles dans la DdA, amélioration de la lisibilité des tableaux | Matthieu GRALL |

## Introduction
**Pour obtenir une liste de critères de confiance des systèmes basés sur l’IA, on se heurte à la pluralité des principaux documents de référence**<sup><a href="#note1" id="ref1">[1]</a></sup> qui comprennent des exigences, règles et recommandations liées à l’IA ou applicables à l’IA (objectifs de l'[ISO/IEC 42001], principes des [Recos OCDE], etc.). Ils ne sont pas vraiment cohérents, que ce soit en termes de champs d’application, de formulations, de classements, et de langue. On a donc de nombreuses redondances dans l’ensemble et de nombreux manques dans chaque, si on souhaite une vision globale.

**Toutefois, les idées convergent toutes, ou se complètent plutôt bien**. On peut donc faire émerger une liste de ces critères de confiance, exhaustive et « non recouvrante », qui traite de l’ensemble des aspects qui peuvent devoir être considérés quand on crée un système basé sur l’IA.

Ainsi, un système basé sur l’IA devrait :
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

**La mise en oeuvre de bonnes pratiques contribue à respecter chacun de ces critères de confiance**. Mais la **multiplicité des documents de référence** qui comportent des bonnes pratiques, spécifiques à l’IA<sup><a href="#note2" id="ref2">[2]</a></sup> ou applicables à tous les systèmes<sup><a href="#note3" id="ref3">[3]</a></sup>, **apporte de la confusion** chez ceux qui doivent ou souhaitent les appliquer.

Ils peuvent en effet sembler :
-	**chacun incomplet**, car leurs périmètres diffèrent (par domaines comme la sécurité de l’information ou la protection des droits et libertés, par techniques d’IA comme les LLM<sup><a href="#note4" id="ref4">[4]</a></sup> , par phases comme le développement, etc.). Ceci est notamment dû au fait que les problématiques liées à l’IA imposent une vision globale, alors que les périmètres de compétences et spécialités des organismes émetteurs sont restreints ;

-	**tous incohérents**, car leurs structures, bonnes pratiques et terminologies diffèrent, mêmes si elles ont des similarités, et que les normes internationales<sup><a href="#note5" id="ref5">[5]</a></sup> ne sont pas encore matures.

Or, quand on veut mettre en œuvre un système basé sur l’IA, on peut devoir ou souhaiter **respecter l’ensemble des références applicables, et ce, de manière cohérente !**

Ainsi, ce document **propose des bonnes pratiques harmonisées**, organisées selon les 10 critères de confiance de l’IA.

La portée de chaque critère de confiance et les principaux risques qu'il contribuent à traiter sont précisés.

Des _tags_ sont ajoutés, à titre indicatif, pour orienter vers :
- les principales mesures de l'annexe A de l'[ISO/IEC 42001] correspondantes ;
- les principales phases du cycle de vie des [Recos OCDE] concernées ;
- des exemples de preuve de mise en œuvre observables ;
- les principales fonctions types d'entreprise concernées.

L'Annexe [« Déclaration d'applicabilité »](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md#annexe---d%C3%A9claration-dapplicabilit%C3%A9-) peut être utilisée pour présenter les pratiques mises en œuvre en comparaison aux bonnes pratiques.

Note : un renvoi vers les documents de référence est privilégié quand cela est opportun.

## 1. Gouvernance responsable
<ins>Portée</ins> : pilotage éthique, transparent et responsable, incluant la mise en place de mécanismes de contrôle, de _reporting_ et de gestion des conflits d’intérêts.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (dignité humaine, droit à une bonne administration, et droit à un recours collectif, cf. Art. 1, 41 et 47 de la [Charte UE]), décisions unilatérales, conflits d’intérêts, manque de supervision, opacité décisionnelle.

<ins>Objectif</ins> : instaurer un cadre de gouvernance qui permet de partager et contrôler l’éthique des processus mis en œuvre dans les projets qui reposent sur l’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recos UE], [ISO/IEC 42001].

**BP01.	Formaliser les responsabilités des parties intéressées**

Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA.

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| BP01. Formaliser les responsabilités des parties intéressées | Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA. | [Recos OCDE] :<br> - Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.3.2. Rôles et responsabilités IA<br>- A.3.4. Implication des parties intéressées<br>[Règlement IA] :<br>- Art. 17 sur le système de gestion de la qualité | - Lettres de missions<br>- Organigrammes ou matrices RACI<br>- Compte-rendus de réunions | - Direction<br>- Personne en charge de la conformité<br>- Personne en charge du projet IA |
| BP02. Partager les valeurs éthiques | Impliquer, voire former, les parties intéressées pour assurer que les technologies liées à l'IA sont produites et utilisées conformément à des valeurs éthiques, en surveillant les préjugés, la confidentialité et les abus, tout en promouvant l'innovation et la confiance. | [Recos OCDE] :<br>- Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.7.2. Formation et sensibilisation<br>- A.6.2. Communication sur les valeurs | - Matériel de formation<br>-Enregistrements liés aux sensibilisations<br>- Chartes éthiques signées | - Direction<br>- Personne en charge de l'éthique<br>- Ressources humaines |
| BP03. Déterminer des mécanismes de contrôle | Trouver et mettre en œuvre le(s) moyen(s) le(s) plus efficace(s), c’est-à-dire cohérent(s) avec la taille, la maturité et les processus existants de l’organisme, pour vérifier régulièrement que l’éthique est effectivement considérée dans les projets qui reposent sur de l’IA (ex : reporting, revue annuelle, indicateurs basés sur des objectifs prédéfinis, audits, rapports de gouvernance, comité d’éthique). | [Recos OCDE] :<br>- Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.4.2. Mécanismes de gouvernance IA<br>- A.12.1. Suivi et audit des systèmes IA<br>[Règlement IA] :<br>- Art. 61-65 sur la conformité et le contrôle post-commercialisation | - Rapports d’audit<br>- Comptes-rendus de comité d’éthique<br>- Indicateurs liés aux contrôles | - Direction<br>- Personne en charge de la sécurité de l'information<br>- Personne en charge de la conformité |

## 2. Fiabilité et sûreté
<ins>Portée</ins> : robustesse, performance, stabilité, résilience, précision, absence d'erreurs, capacité à fonctionner correctement, sans mettre en danger la vie humaine, les biens ou l'environnement, dans des conditions variées, incertaines ou inattendues, même en conditions de stress ou d’attaque.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (dignité humaine, protection de la santé, et protection des consommateurs, cf. Art. 1, 35 et 38 de la [Charte UE]), défaillances techniques / dysfonctionnements, accidents, attaques malveillantes.

<ins>Objectif</ins> : assurer la robustesse des systèmes qui reposent sur l’IA afin d’améliorer leur fiabilité et la sécurité des biens et des personnes.

<ins>Principale(s) référence(s)</ins> : [IEC 61508], [Règlement IA], [Recos UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| BP04. Vérifier les données d’entrée possibles | Vérifier les particularités des données futures, par exemple à l’aide de modules spécifiques dans la chaîne de traitements de données. | [Recos OCDE] :<br>- Collecte et traitement des données<br>[ISO/IEC 42001] :<br>- A.8.3. Qualité des données<br>- A.8.2. Gestion des données d'entrée | - Journaux d'événements<br>- Scripts de validation des données<br>- Résultats de tests de qualité | - _Data engineer_<br>-  _Data scientist_<br>- Personne en charge de la qualité des données |
| BP05. Vérifier la robustesse du modèle | Vérifier que le modèle ne peut pas être attaqué pour produire un résultat indésirable, par exemple dans le cadre d’une chaîne de modèles. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.3. Sécurité du modèle IA<br>- A.11.3. Robustesse du modèle<br>[Règlement IA] :<br>- Art. 15 sur la robustesse, précision et cybersécurité | - Rapports de tests d’attaque<br>- Indicateurs de robustesse | - _Data scientist_<br>- Expert sécurité IA |
| BP06. Éprouver les limites du système dans sa globalité | Mettre en place des mesures pour éprouver et consolider le système d’IA (tests de charge et de stress, simulations d’attaques, redondances techniques, procédures de réponse aux incidents) en considérant l’amont et l’aval du système d’IA. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.11.1. Tests de résistance et de robustesse<br>- A.12.4. Gestion des incidents | - Rapports de tests de charge et de stress<br>- Journaux d’incidents<br>- Simulations documentées | - Personne en charge de la qualité<br>- _Data scientist_<br>- Personne en charge de la sécurité de l'information |
| BP07. Évaluer les performances du système | Faire des mesures quantitatives pour évaluer les performances du modèle dans diverses conditions de stress, notamment les attaques contradictoires, le bruit et les changements de distribution des données. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>[ISO/IEC 42001] :<br>- A.10.2. Mesure et suivi des performances<br>- A.11.2. Analyse des résultats | - Rapports d’évaluation<br>- Indicateurs de performance<br>- Rapports d’audits techniques | - _Data scientist_<br>- Personne en charge de la qualité<br>- Analyste |
| BP08. Mettre en place les mesures de sûreté nécessaires | Tester et valider le système d’IA pour répondre aux normes de sûreté et aux exigences réglementaires, intégrer plusieurs mesures redondantes pour gérer les pannes sans causer de dommages, laisser la main à l’humain pour intervenir ou guider les actions de l'IA si nécessaire. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.11.5. Sécurité et sûreté<br>- A.7.7. Supervision humaine | - Rapports de validation de sûreté<br>- Procédures de supervision humaine<br>- Plans de contingence | - Personne en charge de la sûreté<br>- _Data scientist_<br>- Opérateur métier |

## 3. Équité
<ins>Portée</ins> : fonctionnement de l’IA sans biais, traitement impartial et équitable des usagers, non-discrimination.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (égalité devant la loi, non-discrimination, égalité entre hommes et femmes, cf. Art. 20, 21 et 23 de la [Charte UE]), discrimination, traitement inéquitable, exclusion, du fait de biais :
- dans la formulation des cas d’usages<sup><a href="#note6" id="ref6">[6]</a></sup> ;
- liés à l’algorithme d’entrainement / à l’architecture du modèle<sup><a href="#note9" id="ref9">[9]</a></sup> ;
- liés aux données d’entrainement et de validation<sup><a href="#note8" id="ref8">[8]</a></sup> ;
- liés aux données d’entrée<sup><a href="#note7" id="ref7">[7]</a></sup> ;
- liés aux données de sortie<sup><a href="#note10" id="ref10">[10]</a></sup>.

<ins>Objectif</ins> : détecter et corriger les biais par des mécanismes de vérification et d’audit des algorithmes.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recos CNIL], [Guide France IA].

### 3.1. Réduction des biais liés à la formulation du cas d'usage

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP09. Définir clairement le(s) cas d’usage(s)** | Décrire précisément le cas d’usage, les limitations et les exceptions, et s’assurer que les personnes en charge de la conception et du développement des outils en ont connaissance et les comprennent. | [Recos OCDE] :<br>- Planification et conception<br>[ISO/IEC 42001] :<br>- A.5.1. Définition du périmètre et des usages<br>- A.6.2. Communication des exigences | - Cahiers des charges<br>- Spécifications fonctionnelles<br>- Documents de conception | - Personne en charge du projet<br>- Analyste métier<br>- Architecte IA | 

### 3.2. Réduction des biais liés aux données d'entrée

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP10. Diversifier les données d’entrée** | Utiliser des sources de données diverses et représentatives. | [Recos OCDE] :<br>- Collecte et traitement des données<br>[ISO/IEC 42001] :<br>- A.8.3. Qualité des données<br>- A.8.2. Gestion des données d’entrée<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données | - Catalogue des sources de données<br>- Rapports de couverture de données<br>- Audits de représentativité | - _Data engineer_<br>- _Data scientist_<br>- Personne en charge de la qualité des données | 
| **BP11. Rendre les données exploitables** | Limiter les données qu’à celles qui seront traitées, les transformer / intégrer de façon cohérente (ex : via une ontologie qui sert de pivot), et les nettoyer de manière approfondie, afin de faciliter leur traitement, de ne pas traiter de données inutilisables, inutiles, sujettes à des règles internes ou externes, ou qu’on ne souhaite pas traiter. | [Recos OCDE] :<br>- Collecte et traitement des données<br>[ISO/IEC 42001] :<br>- A.8.3. Gestion de la qualité des données<br>- A.8.5. Traitement cohérent des données<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données | - Processus de nettoyage documentés<br>- Ontologie utilisée<br>- Rapports de qualité des données | - _Data engineer_<br>- _Data steward_<br>- Personne en charge de la qualité des données | 

### 3.3. Réduction des biais liés aux données d'entrainement

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP12. S’assurer de la qualité des données d’entrainement** | Vérifier la pertinence des données par rapport au problème à résoudre, leur fiabilité (crédibles et/ou de sources objectives), et la légalité de leur collecte et de leur traitement. | [Recos OCDE] :<br>- Collecte et traitement des données<br>[ISO/IEC 42001] :<br>- A.8.3. Contrôle qualité des données d’entrainement<br>- A.9.1. Conformité légale<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données | - Audits de qualité<br>- Certificats de conformité<br>- Procédures de validation | - _Data scientist_<br>- Juriste<br>- Personne en charge de la conformité | 
| **BP13. Faire des échantillonnages équilibrés des données d’entrainement** | Respecter les bonnes pratiques d’échantillonnage pour que les échantillons soient équilibrés. | [Recos OCDE] :<br>- Collecte et traitement des données<br>[ISO/IEC 42001] :<br>- A.8.3. Equilibrage des données<br>- A.11.1. Gestion des biais<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données | - Rapports d’échantillonnage<br>- Analyses statistiques<br>- Tests d’équilibre | - _Data scientist_<br>- Analyste statistique<br>- Personne en charge de la qualité | 
| **BP14. Corriger les corrélations indésirables** | Identifier les corrélations entre les caractéristiques ou les variables, évaluer leur impact et gérer ceux qui ne sont pas acceptables. | [Recos OCDE] :<br>- Construction ou adaptation du modèle<br>[ISO/IEC 42001] :<br>- A.11.2. Analyse des dépendances<br>- A.11.1. Gestion des biais<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données | - Rapports d’analyse des corrélations<br>- Actions correctives documentées | - _Data scientist_<br>- Statisticien<br>- Personne en charge de la qualité | 
| **BP15. Collecter de nouvelles données dès que cela est nécessaire** | Recourir à de nouvelles données d’entrée jusqu’à avoir l’assurance que les biais sont suffisamment réduits. | [Recos OCDE] :<br>- Collecte et traitement des données<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.8.3. Surveillance de la qualité des données<br>- A.10.2. Gestion des évolutions des données | - Rapports de nouvelles collectes<br>- Indicateurs d’équité<br>- Documents d’ajustement des jeux de données | - _Data scientist_<br>- _Data engineer_<br>- Personne en charge de la qualité | 

### 3.4. Réduction des biais liés à l'agorithme d'entrainement / Architecture du modèle

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP16. Évaluer la qualité du modèle** | Mesurer l'équité à l’aide de modèles mathématiques, comme l'indépendance statistique, les intervalles de confiance, l'étude de séparation et l'étude de suffisance. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>[ISO/IEC 42001] :<br>- A.10.2. Évaluation de la performance des modèles<br>- A.11.1. Gestion des biais | - Rapports d’évaluation d’équité<br>- Analyses statistiques<br>- Documentations d’audits | - _Data scientist_<br>- Analyste qualité<br>- Personne en charge de l'éthique | 
| **BP17. Évaluer les performances du modèle** | Évaluer les performances de l'algorithme de manière régulière. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.2. Surveillance continue des performances<br>- A.10.4. Revue des modèles IA | - Tableaux de bord de suivi<br>- Rapports périodiques<br>- Plans d’amélioration | - _Data scientist_<br>- Personne en charge de la qualité<br>- Analyste | 
| **BP18. Faire auditer le modèle** | Réaliser un audit pour identifier et corriger les biais. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>[ISO/IEC 42001] :<br>- A.12.1. Audit des systèmes IA<br>- A.11.1. Gestion des risques IA | - Rapports d’audit<br>- Plans d’action corrective<br>- Attestations d’audit | - Auditeur IA<br>- Personne en charge de la conformité<br>- _Data scientist_ | 

### 3.5. Réduction des biais liés aux données de sortie

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP19. Valider les données de sorties** | Valider les résultats produits, si possible de manière continue, voire consulter des experts en éthique et inclusion. | [Recos OCDE] :<br>- Test, évaluation et vérification<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.3. Validation des résultats<br>- A.3.4. Implication des experts<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données<br>[Règlement IA] :<br>- Art. 14 sur la supervision humaine | - Rapports de validation<br>- Comptes rendus de consultations<br>- Tableaux de suivi | - _Data scientist_<br>- Expert éthique<br>- Personne en charge de la qualité | 
| **BP20. Obtenir les retours des usagers** | Collecter régulièrement les commentaires et retours d'expérience des usagers, pour détecter et corriger les biais dans les résultats. | [Recos OCDE] :<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.7.3. Gestion des retours utilisateurs<br>- A.10.5. Surveillance des impacts<br>[Règlement IA] :<br>- Art. 14 sur la supervision humaine | - Rapports d’enquête<br>- Comptes rendus d’atelier utilisateurs<br>- Tickets de support | - Personne en charge du support aux usagers<br>- Personne en charge du projet<br>- Personne en charge de la qualité | 

## 4. Transparence
<ins>Portée</ins> : compréhension des processus et décisions, explicabilité, traçabilité des données, possibilité de contester et vérifier le fonctionnement.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (droit à la protection des données à caractère personnel, liberté d'expression et d'information, et droit d'accès aux documents, cf. Art. 8, 11 et 42 de la [Charte UE]), opacité, incompréhension des mécanismes, perte de confiance.

<ins>Objectif</ins> : rendre explicites les algorithmes et les processus de décision via une documentation accessible, des interfaces interactives et des explications techniques adaptées aux différents publics.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recos UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP21.	Documenter les éléments utiles à la transparence** | Élaborer les explications<sup><a href="#note11" id="ref11">[11]</a></sup>, nécessaires à la transparence<sup><a href="#note12" id="ref12">[12]</a></sup>, notamment pour expliquer d’où les données proviennent les données, la forme qu’elles prennent et leur utilisation par l’organisme, et les faire connaître<sup><a href="#note13" id="ref13">[13]</a></sup> aux personnes chargées de créer et de maintenir les modèles et les flux de données, aux usagers, et aux autorités compétentes. | [Recos OCDE] :<br>- Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.6.2. Documentation et communication<br>- A.8.7. Transparence des données<br>[Règlement IA] :<br>- Art. 11 sur la documentation technique<br>- Art. 13 sur la transparence et la fourniture d'information | - Documents de transparence<br>- Rapports d’audit<br>- Supports de formation | - Personne en charge de la conformité<br>- Personne en charge du projet<br>- _Data scientist_ |

## 5. Sécurité de l'information
<ins>Portée</ins> : protection de la disponibilité, de l’intégrité et de la confidentialité des données, gestion des risques liés à la sécurité de l’information engendrés par les systèmes d’IA (au-delà du critère de confiance de fiabilité).

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (respect de la vie privée et familiale, et droit à la protection des données à caractère personnel, cf. Art. 7 et 8 de la [Charte UE]), cyberattaques, fuites de données, corruption de systèmes.

<ins>Objectif</ins> : appliquer les bonnes pratiques de sécurité de l’information au système d’IA, pour réduire les risques sur l’organisme en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données, tout le long du cycle de vie du système.

<ins>Principale(s) référence(s)</ins> : [Recos ANSSI], [ISO/IEC 27090], [Guide France IA].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP22.	Respecter les recommandations de l’ANSSI** | Appliquer les [Recos ANSSI] (chapitre 5 de celles de 2024) applicables dans le cas d’un système d’IA générative et les [Recos ANSSI] (annexe I de celles de 2025). | [Recos OCDE] :<br>- Construction ou adaptation du modèle<br>Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.1. Sécurité des systèmes<br>- A.11.4. Gestion des vulnérabilités<br>[Règlement IA] :<br>- Art. 12 sur la tenue des enregistrements<br>- Art. 15 sur la robustesse, précision et cybersécurité | - Rapports de conformité<br>- Plans d’action<br>- Tests de sécurité | - Personne en charge de la sécurité de l'information<br>- Personne en charge des systèmes informatiques |
| **BP23.	Adopter des bonnes pratiques de sécurité de l’information** | Appliquer la politique de sécurité des systèmes d’information, ou les bonnes pratiques de sécurité de l’information applicables selon la maturité de l’organisme en la matière (ex : [Guide sécurité de la CNIL], [Guide d'hygiène], [ISO/IEC 27002]). | [Recos OCDE] : toutes les phases<br>[ISO/IEC 42001] :<br>- A.2.2. Politique de sécurité<br>- A.9.1. Contrôle d’accès<br>- A.8.1. Protection des actifs<br>[Règlement IA] :<br>- Art. 12 sur la tenue des enregistrements<br>- Art. 15 sur la robustesse, précision et cybersécurité | - Politiques formalisées<br>- Rapports d’audit | - Personne en charge de la sécurité de l'information<br>- Personne en charge des systèmes informatiques |

## 6. Protection des droits et libertés
<ins>Portée</ins> : respect de la vie privée, protection des données à caractère personnel et des droits fondamentaux, gestion des risques sur les droits et libertés des personnes concernées engendrés par les systèmes d’IA (au-delà du critère de confiance d’équité).

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (respect de la vie privée et familiale, droit à la protection des données à caractère personnel, et non-discrimination, cf. Art. 7, 8 et 21 de la [Charte UE]), atteintes à la vie privée, usage abusif des données personnelles.

<ins>Objectif</ins> : appliquer les grands principes de la protection de la vie privée au traitement de données par IA, pour réduire les risques sur les personnes concernées en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données.

<ins>Principale(s) référence(s)</ins> : [Recos CNIL], [Loi I&L], [RGPD].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP24.	Respecter les recommandations de la CNIL** | Appliquer les [Recos CNIL] applicables dans le cas d’une phase de développement. | [Recos OCDE] :<br>- Collecte et traitement des données<br>- Construction ou adaptation du modèle<br>[ISO/IEC 42001] :<br>- A.9.2. Protection des données personnelles<br>- A.9.1. Conformité réglementaire<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données<br>- Art. 13 sur la transparence<br>- Art. 14 sur la supervision humaine<br>- Art. 61-65 sur la conformité et la surveillance post-commercialisation | - Rapports de conformité<br>- Registres (des traitements, des violations, etc.)<br>- AIPD | - Personne en charge de la protection de la vie privée<br>- Personne en charge de la conformité |
| **BP25.	Mettre le traitement en conformité avec la réglementation** | Formaliser les éléments nécessaires<sup><a href="#note14" id="ref14">[14]</a></sup> à la personne / au service en charge de la protection de la vie privée pour bâtir la conformité du traitement de données à caractère personnel à la [Loi I&L] / au [RGPD]. | [Recos OCDE] :<br>- Collecte et traitement des données<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.9.1. Conformité réglementaire<br>- A.9.3. Gestion des risques liés à la vie privée<br>[Règlement IA] :<br>- Art. 10 sur la gouvernance des données<br>- Art. 13 sur la transparence<br>- Art. 14 sur la supervision humaine<br>- Art. 61-65 sur la conformité et la surveillance post-commercialisation | - Registres de traitement<br>- Rapports de conformité<br>- AIPD | - Personne en charge de la protection de la vie privée<br>- Personne en charge de la conformité |

## 7. Maintenabilité et évolutivité
<ins>Portée</ins> : maintien en conditions opérationnelle et de sécurité, adaptation du système d’IA au fil du temps pour résoudre des problèmes et être utilisé pour de nouveaux besoins.

<ins>Principaux risques traités</ins> : obsolescence logicielle, incompatibilités, pertes de performance.

<ins>Objectif</ins> : assurer performances, maintien en conditions opérationnelle et de sécurité, intégration de nouvelles fonctionnalités, et comptabilité ascendante, tout le long du cycle de vie du système d’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [ISO/IEC 42001].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP26.	Adopter un principe de modularité et de réutilisabilité** | Mettre en œuvre une conception modulaire du système d'IA, pour réutiliser/remplacer les composants de la chaîne sans affecter l'ensemble du système. | [Recos OCDE] :<br>- Planification et conception<br>- Construction ou adaptation du modèle<br>[ISO/IEC 42001] :<br>- A.6.4. Architecture modulaire<br>- A.10.4. Gestion des changements | - Schémas d’architecture<br>- Documentation des modules<br>- Gestion de versions | - Personne en charge de l'architecture des logiciels<br>- Personne en charge du développement<br>- Personne en charge du projet |
| **BP27.	Documenter le système** | Élaborer une documentation complète, qui comprend des commentaires sur le code, des manuels d'utilisation et une documentation sur le prétraitement des données, la formation des modèles et les processus de déploiement. | [Recos OCDE] : toutes les phases<br>[ISO/IEC 42001] :<br>- A.6.2. Documentation complète<br>- A.7.3. Gestion des connaissances | - Documentation technique<br>- Manuels usagers<br>- Historiques des modifications | - Personne en charge du développement<br>- Personne en charge du projet |
| **BP28.	Contrôler la qualité du code** | Appliquer les bonnes pratiques de développement pour produire un code de haute qualité, notamment des conventions de nommage appropriées, un style cohérent et des algorithmes efficaces. | [Recos OCDE] :<br>- Construction ou adaptation du modèle<br>[ISO/IEC 42001] :<br>- A.10.1. Contrôle qualité du code<br>- A.10.3. Revue de code | - Revues de code<br>- Rapports d’analyse statique<br>- Tests unitaires | - Personne en charge du développement<br>- Personne en charge de la qualité |
| **BP29.	Permettre l’évolutivité** | Concevoir le système pour gérer des charges accrues et évoluer selon les besoins. Ceci implique également le maintien des performances et la gestion des ressources. | [Recos OCDE] :<br>- Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.5. Scalabilité<br>- A.11.6. Gestion des ressources | - Tests de charge<br>- Rapports de performance<br>- Plans d’évolution | - Personne en charge de l'architecture des logiciels<br>- Personne en charge des systèmes informatiques<br>- Personne en charge de la qualité |
| **BP30.	Maîtriser les évolutions** | Mettre en œuvre un processus de gestion des évolutions, qui intègre la veille technologique, les tests de comptabilité ascendante, l’automatisation des correctifs et mises à jour, le contrôle des versions<sup><a href="#note15" id="ref15">[15]</a></sup> , et la surveillance des performances. | [Recos OCDE] :<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.10.4. Gestion des changements<br>- A.10.2. Surveillance des performances<br>[Règlement IA] :<br>- Art. 61-65 sur la conformité et la surveillance post-commercialisation | - Historique des versions<br>- Rapports de veille<br>- Procédures de mise à jour | - Personne en charge du projet<br>- Personne en charge du développement<br>- Personne en charge des systèmes informatiques |

## 8. Interopérabilité
<ins>Portée</ins> : compatibilité entre différents systèmes d'IA, intégration du système d’IA avec d’autres outils et normes existants, capacité à échanger des informations.

<ins>Principaux risques traités</ins> : verrouillage technologique, incompatibilités de formats<sup><a href="#note16" id="ref16">[16]</a></sup>.

<ins>Objectif</ins> : risques sur les droits fondamentaux (liberté d'information, cf. Art. 11 de la [Charte UE]) assurer l’interopérabilité fluide des données et des technologies sur lesquelles elles reposent.

<ins>Principale(s) référence(s)</ins> : [RGI].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP31.	Assurer la comptabilité des données** | Identifier les sources de données, les données consommées, les traitements de données effectués et les données produites, vérifier que ces données sont référencées (ex : dans une ontologie pivot) pour faciliter leur interopérabilité et leur réutilisation. | [Recos OCDE] :<br>- Collecte et traitement des données<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.8.6. Traçabilité des données<br>- A.8.7. Gestion des métadonnées | - Registres de données<br>- Ontologie(s)<br>- Rapports d’audit | - _Data engineer_<br>- _Data steward_<br>- Personne en charge de l'architecture des données |
| **BP32.	Adopter des bonnes pratiques d’interopérabilité** | Appliquer les bonnes pratiques applicables du [RGI] et, le cas échéant, vérifier la conformité aux outils autorisés en interne pour favoriser l’interopérabilité des technologies<sup><a href="#note17" id="ref17">[17]</a></sup>. | [Recos OCDE] :<br>- Construction ou adaptation du modèle<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.8.7. Standards d’interopérabilité<br>- A.6.4. Gestion des interfaces<br>[Règlement IA] :<br>- Art. 11 sur la documentation technique | - Documentation des API<br>Rapports de conformité<br>- Tests d’intégration | - Personne en charge de l'architecture des logiciels<br>- Personne en charge des systèmes informatiques<br>- Personne en charge du développement |

## 9. Respect de l’environnement
<ins>Portée</ins> : maîtrise de l’empreinte écologique globale associée au développement, au déploiement et à l’exploitation de technologies d’IA, maîtrise de la consommation énergétique, gestion des risques sur l’environnement engendrés par les systèmes d’IA.

<ins>Principaux risques traités</ins> : consommation excessive d’énergie, émissions de CO₂.

<ins>Objectif</ins> : risques sur les droits fondamentaux (protection de l'environnement, cf. Art. 37 de la [Charte UE]),  réduire globalement les besoins en ressources matérielles et énergétiques et les impacts environnementaux associés.

<ins>Principale(s) référence(s)</ins> : [RGESN], [RGIAF].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP33.	Adopter des bonnes pratiques d’écoconception** | Identifier la consommation d'énergie des centres de données (_data centers_) lors de l’entrainement des modèles, l'économie circulaire du matériel, l'empreinte carbone, l'obsolescence et les déchets électroniques, et appliquer les bonnes pratiques applicables du [RGESN] ou du [RGIAF]. | [Recos OCDE] :<br>- Exploitation et maintenance<br>- Décommisionnement et mise au rebut<br>[ISO/IEC 42001] :<br>- A.13.1. Gestion de l’impact environnemental<br>- A.13.2. Optimisation des ressources | - Bilans énergétiques<br>- Rapports RSE<br>- Certificats d’éco-conception | - Personne en charge de la responsabilité sociétale<br>- Personne en charge des systèmes informatiques<br>- Personne en charge du projet |

## 10. Accessibilité
<ins>Portée</ins> : accès aux systèmes d'IA, notamment pour les personnes handicapées, gestion des risques d’inégalités engendrés par les systèmes d’IA.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (non-discrimination, et intégration des personnes handicapées, cf. Art. 21 et 26 de la [Charte UE]), exclusion numérique, inégalités d’accès, manque de compatibilité avec les technologies d’assistance.

<ins>Objectif</ins> : intégrer les principes d’accessibilité numérique dès la conception et tester régulièrement l’interface pour garantir une utilisation inclusive.

<ins>Principale(s) référence(s)</ins> : [RGAA], [EN 301 549], [WCAG].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondances**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP34.	Adopter des bonnes pratiques d’accessibilité** | Se conformer au [RGAA] en appliquant les bonnes pratiques applicables de l’[EN 301 549] ou des [WCAG]<sup><a href="#note18" id="ref18">[18]</a></sup>, en visant l'accessibilité et l'autonomisation des usagers, pour favoriser une expérience d'IA positive et inclusive pour tous les usagers. | [Recos OCDE] :<br>- Planification et conception<br>- Exploitation et maintenance<br>[ISO/IEC 42001] :<br>- A.6.5. Accessibilité numérique<br>- A.9.1. Conformité réglementaire<br>[Règlement IA] :<br>- Art. 13 sur la transparence et les informations à l'utilisateur | - Rapports d’audit d’accessibilité<br>- Tests usagers<br>- Guides de bonnes pratiques | - Personne en charge du projet<br>Personne en charge de l'accessibilité<br>- Personne en charge du développement |

## Annexe : déclaration d'applicabilité (DdA)
<ins>Notes</ins> :
-	l’objectif est d’une part de vérifier qu’on n’a rien oublié, et d’autre part d’apporter des éléments nécessaires à la prise de décision d’accepter ou non la mise en exploitation du système d’IA ;

-	les bonnes pratiques ne sont pas toutes applicables à un projet donné : certaines ne sont pas applicables (ex : si elles concernent un type d’IA qui n’est pas celui considéré), n’ont pas besoin d’être appliquées (ex : si le sujet est traité par ailleurs), ou sont exclues par l’organisation.

### Gouvernance responsable
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Formaliser les responsabilités des parties intéressées | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Partager les valeurs éthiques | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Déterminer des mécanismes de contrôle | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Fiabilité et sûreté
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Vérifier les données d’entrée possibles | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Vérifier la robustesse du modèle | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Éprouver les limites du système dans sa globalité | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Évaluer les performances du système | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Mettre en place les mesures de sûreté nécessaires | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Équité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Définir clairement le(s) cas d’usage(s) | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Diversifier les données d’entrée | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Rendre les données exploitables | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| S’assurer de la qualité des données d’entrainement | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Faire des échantillonnages équilibrés des données d’entrainement | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Corriger les corrélations indésirables | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Collecter de nouvelles données dès que cela est nécessaire | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Évaluer la qualité du modèle | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Évaluer les performances du modèle | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Faire auditer le modèle | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Valider les données de sorties | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Obtenir les retours des usagers | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Transparence
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Formaliser les éléments utiles à la transparence | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Sécurité de l'information
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Respecter les recommandations de l’ANSSI | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Adopter des bonnes pratiques de sécurité de l’information | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Protection des droits et libertés
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Respecter les recommandations de la CNIL | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Mettre le traitement en conformité avec la réglementation | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Maintenabilité et évolutivité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Adopter un principe de modularité et de réutilisabilité|☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Documenter le système | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Contrôler la qualité du code | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Permettre l’évolutivité | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Maîtriser les évolutions | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Interopérabilité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Assurer la comptabilité des données | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Adopter des bonnes pratiques d’interopérabilité | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Respect de l’environnement
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Adopter des bonnes pratiques d’écoconception | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Accessibilité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Adopter des bonnes pratiques d’accessibilité | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

<br>
<br>
<a id="note1">[1]</a> Notamment [Règlement IA], [ISO/IEC 42001], [Recos UE], [Loi I&L], [NIST AI RMF], [Recos OCDE], [Recos  ANSSI, [Recos CNIL], [RGAA], [RGESN], [RGI], et [RGIAF]. <a href="#ref1">↩</a>
<br>
<br>
<a id="note2">[2]</a> Notamment [ISO/IEC 42001], [Guide France IA], [Recos OCDE], [Recos ANSSI], [Recos CNIL], [Règlement IA] et [RGIAF]. <a href="#ref2">↩</a>
<br>
<br>
<a id="note3">[3]</a> Notamment [Loi I&L] (dont [RGPD]), [RGAA], [RGESN], et [RGI]. <a href="#ref3">↩</a>
<br>
<br>
<a id="note4">[4]</a> LLM : <i>large language models</i> (grands modèles linguistiques). <a href="#ref4">↩</a>
<br>
<br>
<a id="note5">[5]</a> Ex : [ISO/IEC 42001]. <a href="#ref5">↩</a>
<br>
<br>
<a id="note6">[6]</a> Manque d’équité par défaut de cadrage du cas d’usage. <a href="#ref6">↩</a>
<br>
<br>
<a id="note7">[7]</a> Prises de décisions basées sur des données incomplètes ou non équilibrées. <a href="#ref7">↩</a>
<br>
<br>
<a id="note8">[8]</a> Biais dans les données de l'échantillon (si l'ensemble de données d’entrainement n'est pas représentatif de la population), identification et transformation des caractéristiques sensibles (si un groupe défavorisé est présent dans l'échantillon, modifier les pondérations du modèle de manière à modifier le résultat pour ce groupe défavorisé), biais dans la représentation des différentes classes ou catégories de données (ce qui peut entraîner des résultats non représentatifs, inexacts ou injustes), biais dans les corrélations entre les caractéristiques ou les variables utilisées (ce qui peut conduire à des prédictions biaisées). <a href="#ref8">↩</a>
<br>
<br>
<a id="note9">[9]</a> Biais introduits à la suite de la conception du modèle, donnant des résultats trompeurs même à partir de données fiables et de qualité, du fait de la construction du modèle (l'architecture du modèle elle-même peut présenter des problèmes inhérents, entraînant des biais tels que le biais de régression, le biais de classification, le biais de clustering, etc. ; il peut y avoir des erreurs de calcul dans les paramètres du modèle, entraînant des modèles sur/sous-ajustés, qui introduisent des biais et du bruit dans les données de sortie) ou de la dérive du modèle (le cas d’usage peut évoluer avec le temps, de sorte que le modèle peut devenir obsolète et nécessiter une re-modélisation et un recyclage au fil du temps, réintroduisant les biais mentionnés ci-dessus à chaque étape). Les impacts potentiels concernent des décisions discriminatoires ou injustes basées sur des caractéristiques personnelles ou des groupes de personnes spécifiques, la partialité ou les préjugés dans les résultats produits par l'algorithme. <a href="#ref9">↩</a>
<br>
<br>
<a id="note10">[10]</a> Risque de produire des résultats de sortie discriminatoires ou injustes, qui peuvent avoir un impact négatif sur les utilisateurs ou les parties prenantes concernées, risque de renforcer les stéréotypes ou les préjugés existants à travers les résultats produits par l'IA. <a href="#ref10">↩</a>
<br>
<br>
<a id="note11">[11]</a> L’explicabilité peut reposer sur des méthodes agnostiques ou spécifiques, intrinsèques ou <i>post-hoc</i>, locales ou globales, <i>a priori</i> ou <i>a posteriori</i>. Des outils tels que LIME ou SHAP peuvent notamment contribuer à cette explicabilité. <a href="#ref11">↩</a>
<br>
<br>
<a id="note12">[12]</a> La transparence s’applique aux algorithmes (logique et modèle), aux interactions (via l’interface utilisateur), et à la société (impact social de cette interaction). <a href="#ref12">↩</a>
<br>
<br>
<a id="note13">[13]</a> Ex : publier de la documentation technique, développer des interfaces explicatives, créer des tutoriels et guides d’usage, organiser des ateliers d’information. <a href="#ref13">↩</a>
<br>
<br>
<a id="note14">[14]</a> Finalité, données traitées, durées de conservation, destinataires, mesures prévues pour assurer la minimisation et la qualité des données, mesures prévues pour assurer l’information et les droits des personnes concernées (le cas échéant, d’accès, à la portabilité, de rectification, d’effacement, de limitation et d’opposition) et, le cas échéant, mesures prévues pour encadrer la sous-traitance et le transfert en dehors de l’UE. <a href="#ref14">↩</a>
<br>
<br>
<a id="note15">[15]</a> Recourir à un système de contrôle de version permet de suivre les modifications, de collaborer avec d'autres et de revenir aux versions précédentes si nécessaire. <a href="#ref15">↩</a>
<br>
<br>
<a id="note16">[16]</a> Comme tout service numérique, ceux qui reposent sur l’IA peuvent ne pas pouvoir interagir avec les autres si les technologies ou les données utilisées ne sont pas cohérentes ou compatibles entre elles. <a href="#ref16">↩</a>
<br>
<br>
<a id="note17">[17]</a> Notamment : utiliser des standards ouverts, respecter les API publiques, favoriser la portabilité des données, assurer la documentation des interfaces. <a href="#ref17">↩</a>
<br>
<br>
<a id="note18">[18]</a> Cela implique notamment de concevoir des interfaces ergonomiques, ou plusieurs modes d’interactions, en tenant compte de facteurs tels que la diversité linguistique et l’accessibilité pour les personnes handicapées, et de les tester avec des usagers en situation de handicap. <a href="#ref18">↩</a>
