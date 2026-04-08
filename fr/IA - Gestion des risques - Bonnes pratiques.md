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
[Annexe - Déclaration d'applicabilité (DdA)](#annexe---déclaration-dapplicabilité-dda)<br>
[Annexe - Couverture des droits fondamentaux de la [Charte UE]](#annexe---couverture-des-droits-fondamentaux-de-la-charte-ue)<br>
[Annexe - Couverture des exigences du [Règlement IA]](#annexe---couverture-des-exigences-du-règlement-ia)<br>

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
| 07/11/2025 (v1.6) | Ajout d'annexes relatives à la couverture des droits fondamentaux de la [Charte UE] et des exigences du [Règlement IA] par les bonnes pratiques, corrections mineures (cohérence avec l'étude de cas) | Matthieu GRALL |
| 08/04/2026 (v1.7) | Suppression des pahses du cucle de vie des [Recos OCDE] qui s'avèrent pas suffisamment utiles pour des bonnes pratiques | Matthieu GRALL |

## Introduction
**Pour obtenir une liste de critères de confiance des systèmes basés sur l’IA, on se heurte à la pluralité des principaux documents de référence**<sup><a href="#note1" id="ref1">[1]</a></sup> qui comprennent des exigences, règles et recommandations liées à l’IA ou applicables à l’IA (objectifs de l'[ISO/IEC 42001], principes des [Recos OCDE], etc.). Ils ne sont pas vraiment cohérents, que ce soit en termes de champs d’application, de formulations, de classements, et de langue. On a donc de nombreuses redondances dans l’ensemble et de nombreux manques dans chaque, si on souhaite une vision globale.

**Toutefois, les idées convergent toutes, ou se complètent plutôt bien**. On peut donc faire émerger une liste de ces critères de confiance, exhaustive et « non recouvrante », qui traite de l’ensemble des aspects qui peuvent devoir être considérés quand on crée un système basé sur l’IA.

Ainsi, un système basé sur l’IA devrait :
1. reposer sur une **gouvernance responsable** (notion d’_accountability_) ;
2. assurer la **fiabilité**, et la **sûreté** des personnes et des biens ;
3. être **équitable** (notion de _fairness_) ;
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

Des colonnes sont ajoutées, à titre indicatif, pour orienter vers :
- les principales mesures de l'annexe A de l'[ISO/IEC 42001] correspondantes ;
- des exemples de preuve de mise en œuvre observables ;
- les principales fonctions types d'entreprise concernées.

L'Annexe [« Déclaration d'applicabilité »](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md#annexe---d%C3%A9claration-dapplicabilit%C3%A9-) peut être utilisée comme modèle pour présenter les pratiques mises en œuvre en comparaison aux bonnes pratiques.

Note : un renvoi vers les documents de référence est privilégié quand cela est opportun.

## 1. Gouvernance responsable
<ins>Portée</ins> : pilotage éthique, transparent et responsable, incluant la mise en place de mécanismes de contrôle, de _reporting_ et de gestion des conflits d’intérêts.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (dignité humaine, droit à une bonne administration, et droit à un recours collectif, cf. Art. 1, 41 et 47 de la [Charte UE]), décisions unilatérales, conflits d’intérêts, manque de supervision, opacité décisionnelle.

<ins>Objectif</ins> : instaurer un cadre de gouvernance qui permet de partager et contrôler l’éthique des processus mis en œuvre dans les projets qui reposent sur l’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recos UE], [ISO/IEC 42001].

**BP001.	Formaliser les responsabilités des parties intéressées**

Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA.

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| BP01. Formaliser les responsabilités des parties intéressées | Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA. | - A.3.2. Rôles et responsabilités IA<br>- A.3.4. Implication des parties intéressées | - Lettres de missions<br>- Organigrammes ou matrices RACI<br>- Compte-rendus de réunions | - Direction<br>- Personne en charge de la conformité<br>- Personne en charge du projet IA |
| BP02. Partager les valeurs éthiques | Impliquer, voire former, les parties intéressées pour assurer que les technologies liées à l'IA sont produites et utilisées conformément à des valeurs éthiques, en surveillant les préjugés, la confidentialité et les abus, tout en promouvant l'innovation et la confiance. | - A.7.2. Formation et sensibilisation<br>- A.6.2. Communication sur les valeurs | - Matériel de formation<br>-Enregistrements liés aux sensibilisations<br>- Chartes éthiques signées | - Direction<br>- Personne en charge de l'éthique<br>- Ressources humaines |
| BP03. Déterminer des mécanismes de contrôle | Trouver et mettre en œuvre le(s) moyen(s) le(s) plus efficace(s), c’est-à-dire cohérent(s) avec la taille, la maturité et les processus existants de l’organisme, pour vérifier régulièrement que l’éthique est effectivement considérée dans les projets qui reposent sur de l’IA (ex : reporting, revue annuelle, indicateurs basés sur des objectifs prédéfinis, audits, rapports de gouvernance, comité d’éthique). | - A.4.2. Mécanismes de gouvernance IA<br>- A.12.1. Suivi et audit des systèmes IA | - Rapports d’audit<br>- Comptes-rendus de comité d’éthique<br>- Indicateurs liés aux contrôles | - Direction<br>- Personne en charge de la sécurité de l'information<br>- Personne en charge de la conformité |

## 2. Fiabilité et sûreté
<ins>Portée</ins> : robustesse, performance, stabilité, résilience, précision, absence d'erreurs, capacité à fonctionner correctement, sans mettre en danger la vie humaine, les biens ou l'environnement, dans des conditions variées, incertaines ou inattendues, même en conditions de stress ou d’attaque.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (dignité humaine, protection de la santé, et protection des consommateurs, cf. Art. 1, 35 et 38 de la [Charte UE]), défaillances techniques / dysfonctionnements, accidents, attaques malveillantes.

<ins>Objectif</ins> : assurer la robustesse des systèmes qui reposent sur l’IA afin d’améliorer leur fiabilité et la sécurité des biens et des personnes.

<ins>Principale(s) référence(s)</ins> : [IEC 61508], [Règlement IA], [Recos UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| BP04. Vérifier les données d’entrée possibles | Vérifier les particularités des données futures, par exemple à l’aide de modules spécifiques dans la chaîne de traitements de données. | - A.8.3. Qualité des données<br>- A.8.2. Gestion des données d'entrée | - Journaux d'événements<br>- Scripts de validation des données<br>- Résultats de tests de qualité | - _Data engineer_<br>-  _Data scientist_<br>- Personne en charge de la qualité des données |
| BP05. Vérifier la robustesse du modèle | Vérifier que le modèle ne peut pas être attaqué pour produire un résultat indésirable, par exemple dans le cadre d’une chaîne de modèles. | - A.10.3. Sécurité du modèle IA<br>- A.11.3. Robustesse du modèle | - Rapports de tests d’attaque<br>- Indicateurs de robustesse | - _Data scientist_<br>- Expert sécurité IA |
| BP06. Éprouver les limites du système dans sa globalité | Mettre en place des mesures pour éprouver et consolider le système d’IA (tests de charge et de stress, simulations d’attaques, redondances techniques, procédures de réponse aux incidents) en considérant l’amont et l’aval du système d’IA. | - A.11.1. Tests de résistance et de robustesse<br>- A.12.4. Gestion des incidents | - Rapports de tests de charge et de stress<br>- Journaux d’incidents<br>- Simulations documentées | - Personne en charge de la qualité<br>- _Data scientist_<br>- Personne en charge de la sécurité de l'information |
| BP07. Évaluer les performances du système | Faire des mesures quantitatives pour évaluer les performances du modèle dans diverses conditions de stress, notamment les attaques contradictoires, le bruit et les changements de distribution des données. | - A.10.2. Mesure et suivi des performances<br>- A.11.2. Analyse des résultats | - Rapports d’évaluation<br>- Indicateurs de performance<br>- Rapports d’audits techniques | - _Data scientist_<br>- Personne en charge de la qualité<br>- Analyste |
| BP08. Mettre en place les mesures de sûreté nécessaires | Tester et valider le système d’IA pour répondre aux normes de sûreté et aux exigences réglementaires, intégrer plusieurs mesures redondantes pour gérer les pannes sans causer de dommages, laisser la main à l’humain pour intervenir ou guider les actions de l'IA si nécessaire. | - A.11.5. Sécurité et sûreté<br>- A.7.7. Supervision humaine | - Rapports de validation de sûreté<br>- Procédures de supervision humaine<br>- Plans de contingence | - Personne en charge de la sûreté<br>- _Data scientist_<br>- Opérateur métier |

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

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP009. Définir clairement le(s) cas d’usage(s)** | Décrire précisément le cas d’usage, les limitations et les exceptions, et s’assurer que les personnes en charge de la conception et du développement des outils en ont connaissance et les comprennent. | - A.5.1. Définition du périmètre et des usages<br>- A.6.2. Communication des exigences | - Cahiers des charges<br>- Spécifications fonctionnelles<br>- Documents de conception | - Personne en charge du projet<br>- Analyste métier<br>- Architecte IA | 

### 3.2. Réduction des biais liés aux données d'entrée

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP010. Diversifier les données d’entrée** | Utiliser des sources de données diverses et représentatives. | - A.8.3. Qualité des données<br>- A.8.2. Gestion des données d’entrée | - Catalogue des sources de données<br>- Rapports de couverture de données<br>- Audits de représentativité | - _Data engineer_<br>- _Data scientist_<br>- Personne en charge de la qualité des données | 
| **BP011. Rendre les données exploitables** | Limiter les données qu’à celles qui seront traitées, les transformer / intégrer de façon cohérente (ex : via une ontologie qui sert de pivot), et les nettoyer de manière approfondie, afin de faciliter leur traitement, de ne pas traiter de données inutilisables, inutiles, sujettes à des règles internes ou externes, ou qu’on ne souhaite pas traiter. | - A.8.3. Gestion de la qualité des données<br>- A.8.5. Traitement cohérent des données | - Processus de nettoyage documentés<br>- Ontologie utilisée<br>- Rapports de qualité des données | - _Data engineer_<br>- _Data steward_<br>- Personne en charge de la qualité des données | 

### 3.3. Réduction des biais liés aux données d'entrainement

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP012. S’assurer de la qualité des données d’entrainement** | Vérifier la pertinence des données par rapport au problème à résoudre, leur fiabilité (crédibles et/ou de sources objectives), et la légalité de leur collecte et de leur traitement. | - A.8.3. Contrôle qualité des données d’entrainement<br>- A.9.1. Conformité légale | - Audits de qualité<br>- Certificats de conformité<br>- Procédures de validation | - _Data scientist_<br>- Juriste<br>- Personne en charge de la conformité | 
| **BP013. Faire des échantillonnages équilibrés des données d’entrainement** | Respecter les bonnes pratiques d’échantillonnage pour que les échantillons soient équilibrés. | - A.8.3. Equilibrage des données<br>- A.11.1. Gestion des biais | - Rapports d’échantillonnage<br>- Analyses statistiques<br>- Tests d’équilibre | - _Data scientist_<br>- Analyste statistique<br>- Personne en charge de la qualité | 
| **BP014. Corriger les corrélations indésirables** | Identifier les corrélations entre les caractéristiques ou les variables, évaluer leur impact et gérer ceux qui ne sont pas acceptables. | - A.11.2. Analyse des dépendances<br>- A.11.1. Gestion des biais | - Rapports d’analyse des corrélations<br>- Actions correctives documentées | - _Data scientist_<br>- Statisticien<br>- Personne en charge de la qualité | 
| **BP015. Collecter de nouvelles données dès que cela est nécessaire** | Recourir à de nouvelles données d’entrée jusqu’à avoir l’assurance que les biais sont suffisamment réduits. | - A.8.3. Surveillance de la qualité des données<br>- A.10.2. Gestion des évolutions des données | - Rapports de nouvelles collectes<br>- Indicateurs d’équité<br>- Documents d’ajustement des jeux de données | - _Data scientist_<br>- _Data engineer_<br>- Personne en charge de la qualité | 

### 3.4. Réduction des biais liés à l'agorithme d'entrainement / Architecture du modèle

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP016. Évaluer la qualité du modèle** | Mesurer l'équité à l’aide de modèles mathématiques, comme l'indépendance statistique, les intervalles de confiance, l'étude de séparation et l'étude de suffisance. | - A.10.2. Évaluation de la performance des modèles<br>- A.11.1. Gestion des biais | - Rapports d’évaluation d’équité<br>- Analyses statistiques<br>- Documentations d’audits | - _Data scientist_<br>- Analyste qualité<br>- Personne en charge de l'éthique | 
| **BP017. Évaluer les performances du modèle** | Évaluer les performances de l'algorithme de manière régulière. | - A.10.2. Surveillance continue des performances<br>- A.10.4. Revue des modèles IA | - Tableaux de bord de suivi<br>- Rapports périodiques<br>- Plans d’amélioration | - _Data scientist_<br>- Personne en charge de la qualité<br>- Analyste | 
| **BP018. Faire auditer le modèle** | Réaliser un audit pour identifier et corriger les biais. | - A.12.1. Audit des systèmes IA<br>- A.11.1. Gestion des risques IA | - Rapports d’audit<br>- Plans d’action corrective<br>- Attestations d’audit | - Auditeur IA<br>- Personne en charge de la conformité<br>- _Data scientist_ | 

### 3.5. Réduction des biais liés aux données de sortie

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP019. Valider les données de sorties** | Valider les résultats produits, si possible de manière continue, voire consulter des experts en éthique et inclusion. | - A.10.3. Validation des résultats<br>- A.3.4. Implication des experts | - Rapports de validation<br>- Comptes rendus de consultations<br>- Tableaux de suivi | - _Data scientist_<br>- Expert éthique<br>- Personne en charge de la qualité | 
| **BP020. Obtenir les retours des usagers** | Collecter régulièrement les commentaires et retours d'expérience des usagers, pour détecter et corriger les biais dans les résultats. | - A.7.3. Gestion des retours utilisateurs<br>- A.10.5. Surveillance des impacts | - Rapports d’enquête<br>- Comptes rendus d’atelier utilisateurs<br>- Tickets de support | - Personne en charge du support aux usagers<br>- Personne en charge du projet<br>- Personne en charge de la qualité | 

## 4. Transparence
<ins>Portée</ins> : compréhension des processus et décisions, explicabilité, traçabilité des données, possibilité de contester et vérifier le fonctionnement.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (droit à la protection des données à caractère personnel, liberté d'expression et d'information, et droit d'accès aux documents, cf. Art. 8, 11 et 42 de la [Charte UE]), opacité, incompréhension des mécanismes, perte de confiance.

<ins>Objectif</ins> : rendre explicites les algorithmes et les processus de décision via une documentation accessible, des interfaces interactives et des explications techniques adaptées aux différents publics.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recos UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP021.	Documenter les éléments utiles à la transparence** | Élaborer les explications<sup><a href="#note11" id="ref11">[11]</a></sup>, nécessaires à la transparence<sup><a href="#note12" id="ref12">[12]</a></sup>, notamment pour expliquer d’où les données proviennent les données, la forme qu’elles prennent et leur utilisation par l’organisme, et les faire connaître<sup><a href="#note13" id="ref13">[13]</a></sup> aux personnes chargées de créer et de maintenir les modèles et les flux de données, aux usagers, et aux autorités compétentes. | - A.6.2. Documentation et communication<br>- A.8.7. Transparence des données | - Documents de transparence<br>- Rapports d’audit<br>- Supports de formation | - Personne en charge de la conformité<br>- Personne en charge du projet<br>- _Data scientist_ |

## 5. Sécurité de l'information
<ins>Portée</ins> : protection de la disponibilité, de l’intégrité et de la confidentialité des données, gestion des risques liés à la sécurité de l’information engendrés par les systèmes d’IA (au-delà du critère de confiance de fiabilité).

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (respect de la vie privée et familiale, et droit à la protection des données à caractère personnel, cf. Art. 7 et 8 de la [Charte UE]), cyberattaques, fuites de données, corruption de systèmes.

<ins>Objectif</ins> : appliquer les bonnes pratiques de sécurité de l’information au système d’IA, pour réduire les risques sur l’organisme en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données, tout le long du cycle de vie du système.

<ins>Principale(s) référence(s)</ins> : [Guide sécurité de la CNIL], [Recos ANSSI], [ISO/IEC 27090], [Guide France IA].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP022. Piloter la sécurité des données** | Faire de la sécurité des données un enjeu porté par la direction et inscrit dans une démarche d’amélioration continue. | - A.2.2 Politique relative à l’IA<br>- A.5.2 Processus d’évaluation des impacts du système d’IA | - Politique de sécurité<br>- Revues périodiques<br>- Indicateurs de suivi | - Direction<br>- RSSI |
| **BP023. Définir un cadre d’utilisation des systèmes** | Formaliser les règles d’utilisation des systèmes et les obligations associées pour les utilisateurs. | - A.2.2 Politique relative à l’IA<br>- A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Charte informatique<br>- Procédures internes | - RH<br>- DSI |
| **BP024. Sensibiliser et former les utilisateurs** | Sensibiliser et former les personnes manipulant les données aux risques et bonnes pratiques de sécurité. | - A.3.2 Rôles et responsabilités en matière d’IA | - Plan de formation<br>- Actions de sensibilisation | - RH |
| **BP025. Authentifier les utilisateurs** | Mettre en œuvre des mécanismes d’authentification individuelle robustes pour l’accès aux systèmes. | - A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Gestion des identités<br>- Politique de mots de passe | - DSI |
| **BP026. Gérer les habilitations** | Définir, attribuer et réviser régulièrement les habilitations des utilisateurs. | - A.3.2 Rôles et responsabilités en matière d’IA<br>- A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Matrice des habilitations<br>- Revues annuelles | - DSI<br>- Managers |
| **BP027. Sécuriser les postes de travail** | Protéger les postes de travail contre les accès non autorisés et les logiciels malveillants. | - A.4.5 Ressources systèmes et de calcul | - Paramétrage sécurisé<br>- Antivirus<br>- Pare-feu local | - DSI |
| **BP028. Sécuriser l’informatique mobile** | Prendre en compte les risques spécifiques liés aux équipements mobiles et au nomadisme. | - A.4.5 Ressources systèmes et de calcul | - Chiffrement des terminaux<br>- Politique mobile | - DSI |
| **BP029. Protéger le réseau informatique** | Sécuriser les réseaux informatiques et limiter les flux au strict nécessaire. | - A.4.5 Ressources systèmes et de calcul | - Architecture réseau<br>- VPN<br>- Segmentation | - DSI |
| **BP030. Sécuriser les serveurs** | Durcir les serveurs, limiter les accès et appliquer les mises à jour de sécurité. | - A.4.5 Ressources systèmes et de calcul | - Procédures d’administration<br>- Gestion des correctifs | - DSI |
| **BP031. Sécuriser les sites web** | Protéger les sites web contre les vulnérabilités et les fuites de données. | - A.6.2.4 Vérification et validation du système d’IA | - Tests de sécurité<br>- Paramétrage TLS | - Équipe technique |
| **BP032. Encadrer les développements informatiques** | Intégrer la sécurité et la protection des données dès la conception et le développement. | - A.6.1.3 Processus de conception et de développement responsable des systèmes d’IA | - Méthodologies de développement<br>- Revues de code | - Équipe de développement |
| **BP033. Protéger les locaux** | Sécuriser physiquement les locaux hébergeant des systèmes et des données. | - A.4.2 Documentation des ressources | - Contrôles d’accès physiques | - Moyens généraux |
| **BP034. Sécuriser les échanges avec l’extérieur** | Protéger les échanges de données avec des tiers et vérifier les destinataires. | - A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Chiffrement des échanges<br>- Procédures de transmission | - DSI |
| **BP035. Gérer la sous-traitance** | Encadrer la sous-traitance par des clauses contractuelles et des contrôles adaptés. | - A.10.2 Répartition des responsabilités<br>- A.10.3 Fournisseurs | - Clauses de sécurité<br>- Audits fournisseurs | - Achats<br>- Juridique |
| **BP036. Encadrer la maintenance et la fin de vie des matériels et logiciels** | Maîtriser les opérations de maintenance et la suppression des données en fin de vie. | - A.6.2.6 Exploitation et surveillance du système d’IA | - Main courante de maintenance<br>- Procédures de mise au rebut | - DSI |
| **BP037. Tracer les opérations** | Journaliser les actions réalisées sur les systèmes et analyser régulièrement les traces. | - A.6.2.8 Enregistrement des journaux d’événements du système d’IA | - Journaux d’accès<br>- Analyses de logs | - DSI<br>- RSSI |
| **BP038. Sauvegarder les données** | Mettre en œuvre des sauvegardes régulières, sécurisées et testées. | - A.4.5 Ressources systèmes et de calcul | - Plans de sauvegarde<br>- Tests de restauration | - DSI |
| **BP039. Prévoir la continuité et la reprise d’activité** | Anticiper les incidents majeurs par des plans de continuité et de reprise. | - A.5.2 Processus d’évaluation des impacts du système d’IA | - PCA / PRA<br>- Exercices réalisés | - Direction<br>- DSI |
| **BP040. Gérer les incidents et les violations de données** | Détecter, traiter et documenter les incidents et violations de données personnelles. | - A.8.4 Communication des incidents | - Procédures d’incident<br>- Registre des violations | - RSSI<br>- DPO |
| **BP041. Réaliser une analyse de risques** | Identifier, analyser et suivre les risques pesant sur la sécurité des données. | - A.5.2 Processus d’évaluation des impacts du système d’IA | - Analyses de risques<br>- Plans d’action | - RSSI |
| **BP042. Mettre en œuvre des mécanismes de chiffrement, de hachage et de signature** | Utiliser des mécanismes cryptographiques robustes et gérer les secrets de manière sécurisée. | - A.4.3 Ressources de données | - Politiques cryptographiques<br>- Gestion des clés | - DSI |
| **BP043. Sécuriser le recours aux services cloud** | Intégrer les services cloud dans la gestion globale des risques et responsabilités. | - A.4.2 Documentation des ressources<br>- A.10.3 Fournisseurs | - Évaluations fournisseurs cloud<br>- Clauses contractuelles | - DSI<br>- Juridique |
| **BP044. Sécuriser la conception et le développement des applications mobiles** | Intégrer les contraintes de sécurité propres aux environnements mobiles. | - A.6.1.3 Processus de conception et de développement responsable des systèmes d’IA | - Spécifications mobiles<br>- Tests de sécurité | - Développeurs |
| **BP045. Sécuriser les systèmes d’intelligence artificielle** | Appliquer des mesures de sécurité adaptées aux spécificités des systèmes d’IA. | - A.6.2.4 Vérification et validation du système d’IA | - Documentation sécurité IA | - Responsable IA |
| **BP046. Sécuriser les interfaces de programmation applicative (API)** | Organiser et documenter la sécurité des accès aux API et aux données exposées. | - A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Documentation API<br>- Contrôles d’accès | - Équipe technique |
| **BP047.	Respecter les [Recos ANSSI]** | Appliquer les [Recos ANSSI] (chapitre 5 de celles de 2024) applicables dans le cas d’un système d’IA générative et les [Recos ANSSI] (annexe I de celles de 2025). | - A.10.1. Sécurité des systèmes<br>- A.11.4. Gestion des vulnérabilités | - Rapports de conformité<br>- Plans d’action<br>- Tests de sécurité | - Personne en charge de la sécurité de l'information<br>- Personne en charge des systèmes informatiques |

## 6. Protection des droits et libertés
<ins>Portée</ins> : respect de la vie privée, protection des données à caractère personnel et des droits fondamentaux, gestion des risques sur les droits et libertés des personnes concernées engendrés par les systèmes d’IA (au-delà du critère de confiance d’équité).

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (respect de la vie privée et familiale, droit à la protection des données à caractère personnel, et non-discrimination, cf. Art. 7, 8 et 21 de la [Charte UE]), atteintes à la vie privée, usage abusif des données personnelles.

<ins>Objectif</ins> : appliquer les grands principes de la protection de la vie privée au traitement de données par IA, pour réduire les risques sur les personnes concernées en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données.

<ins>Principale(s) référence(s)</ins> : [Loi I&L], [RGPD], [Recos CNIL].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP048. Mettre en œuvre une gouvernance responsable des données et des systèmes d’IA** | Mettre en place un cadre de gouvernance permettant d’assurer une prise en compte continue de la protection des données personnelles dans la conception, le déploiement et l’utilisation des systèmes d’IA. | - A.2.2 Politique relative à l’IA<br>- A.3.2 Rôles et responsabilités en matière d’IA | - Politique IA formalisée<br>- RACI IA / données<br>- Instances de pilotage | - Direction<br>- Responsable de traitement |
| **BP049. Déterminer les finalités du traitement** | Définir et documenter des finalités déterminées, explicites et légitimes avant toute mise en œuvre du système d’IA. | - A.6.1.2 Objectifs pour le développement responsable des systèmes d’IA | - Objectifs documentés<br>- Spécifications fonctionnelles | - Responsable métier<br>- Responsable projet |
| **BP050. Identifier et documenter le fondement juridique du traitement** | Identifier et documenter le fondement juridique applicable au traitement de données personnelles mis en œuvre par le système d’IA. | Aucune a priori | - Analyse de la base légale<br>- Justifications formalisées | - Responsable de traitement<br>- Juridique |
| **BP051. Minimiser les données traitées** | Limiter les données traitées au strict nécessaire au regard des finalités poursuivies par le système d’IA. | - A.7.2 Données pour le développement et l’amélioration des systèmes d’IA<br>- A.7.3 Acquisition des données | - Justification des données utilisées<br>- Spécifications des jeux de données | - Équipe data<br>- Responsable IA |
| **BP052. Garantir la qualité et l’exactitude des données** | Définir et appliquer des exigences de qualité, d’exactitude et de mise à jour des données utilisées par le système d’IA. | - A.7.4 Qualité des données pour les systèmes d’IA | - Critères de qualité<br>- Procédures de contrôle | - Équipe data |
| **BP053. Définir et appliquer des durées de conservation adaptées** | Définir et documenter des durées de conservation proportionnées aux finalités du traitement et au cycle de vie du système d’IA. | - A.6.2.6 Exploitation et surveillance du système d’IA | - Politique de conservation<br>- Procédures d’archivage / suppression | - Responsable de traitement<br>- DSI |
| **BP054. Informer les personnes concernées** | Fournir aux personnes concernées une information claire, accessible et compréhensible sur les traitements réalisés par le système d’IA. | - A.8.2 Documentation du système et informations destinées aux utilisateurs<br>- A.8.5 Informations destinées aux parties intéressées | - Notices d’information<br>- Supports utilisateurs | - Responsable de traitement<br>- Communication |
| **BP055. Recueillir et gérer le consentement lorsque requis** | Mettre en œuvre des modalités permettant de recueillir, gérer et retirer le consentement lorsque celui‑ci est requis. | Aucune a priori | - Registre des consentements<br>- Interfaces de gestion | - Responsable de traitement |
| **BP056. Permettre l’exercice des droits d’accès et de portabilité** | Mettre en place des procédures permettant aux personnes concernées d’exercer leurs droits d’accès et de portabilité. | - A.8.2 Documentation du système et informations destinées aux utilisateurs | - Procédures internes<br>- Suivi des demandes | - DPO |
| **BP057. Permettre l’exercice des droits de rectification et d’effacement** | Mettre en œuvre des mécanismes permettant la rectification ou l’effacement des données personnelles. | - A.6.2.6 Exploitation et surveillance du système d’IA | - Traces de rectification / suppression | - DPO<br>- DSI |
| **BP058. Gérer les droits de limitation du traitement et d’opposition** | Intégrer les droits de limitation et d’opposition dans les processus d’utilisation du système d’IA. | - A.9.4 Utilisation conforme à l’usage prévu du système d’IA | - Gestion des restrictions d’usage | - Responsable métier |
| **BP059. Encadrer la sous-traitance des traitements** | Identifier, formaliser et encadrer les responsabilités des sous‑traitants participant au traitement. | - A.10.2 Répartition des responsabilités<br>- A.10.3 Fournisseurs | - Contrats<br>- Clauses RGPD | - Achats<br>- Juridique |
| **BP060. Encadrer les transferts de données hors de l’Union européenne** | Identifier et encadrer les transferts de données personnelles hors UE. | - A.10.3 Fournisseurs | - Cartographie des flux<br>- Clauses contractuelles | - Juridique<br>- DPO |
| **BP061.	Respecter les [Recos CNIL]** | Appliquer les [Recos CNIL] applicables dans le cas d’une phase de développement. | - A.9.2. Protection des données personnelles<br>- A.9.1. Conformité réglementaire | - Rapports de conformité<br>- Registres (des traitements, des violations, etc.)<br>- AIPD | - Personne en charge de la protection de la vie privée<br>- Personne en charge de la conformité |

## 7. Maintenabilité et évolutivité
<ins>Portée</ins> : maintien en conditions opérationnelle et de sécurité, adaptation du système d’IA au fil du temps pour résoudre des problèmes et être utilisé pour de nouveaux besoins.

<ins>Principaux risques traités</ins> : obsolescence logicielle, incompatibilités, pertes de performance.

<ins>Objectif</ins> : assurer performances, maintien en conditions opérationnelle et de sécurité, intégration de nouvelles fonctionnalités, et comptabilité ascendante, tout le long du cycle de vie du système d’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [ISO/IEC 42001].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP062.	Adopter un principe de modularité et de réutilisabilité** | Mettre en œuvre une conception modulaire du système d'IA, pour réutiliser/remplacer les composants de la chaîne sans affecter l'ensemble du système. | - A.6.4. Architecture modulaire<br>- A.10.4. Gestion des changements | - Schémas d’architecture<br>- Documentation des modules<br>- Gestion de versions | - Personne en charge de l'architecture des logiciels<br>- Personne en charge du développement<br>- Personne en charge du projet |
| **BP063.	Documenter le système** | Élaborer une documentation complète, qui comprend des commentaires sur le code, des manuels d'utilisation et une documentation sur le prétraitement des données, la formation des modèles et les processus de déploiement. | - A.6.2. Documentation complète<br>- A.7.3. Gestion des connaissances | - Documentation technique<br>- Manuels usagers<br>- Historiques des modifications | - Personne en charge du développement<br>- Personne en charge du projet |
| **BP064.	Contrôler la qualité du code** | Appliquer les bonnes pratiques de développement pour produire un code de haute qualité, notamment des conventions de nommage appropriées, un style cohérent et des algorithmes efficaces. | - A.10.1. Contrôle qualité du code<br>- A.10.3. Revue de code | - Revues de code<br>- Rapports d’analyse statique<br>- Tests unitaires | - Personne en charge du développement<br>- Personne en charge de la qualité |
| **BP065.	Permettre l’évolutivité** | Concevoir le système pour gérer des charges accrues et évoluer selon les besoins. Ceci implique également le maintien des performances et la gestion des ressources. | - A.10.5. Scalabilité<br>- A.11.6. Gestion des ressources | - Tests de charge<br>- Rapports de performance<br>- Plans d’évolution | - Personne en charge de l'architecture des logiciels<br>- Personne en charge des systèmes informatiques<br>- Personne en charge de la qualité |
| **BP066.	Maîtriser les évolutions** | Mettre en œuvre un processus de gestion des évolutions, qui intègre la veille technologique, les tests de comptabilité ascendante, l’automatisation des correctifs et mises à jour, le contrôle des versions<sup><a href="#note15" id="ref15">[15]</a></sup> , et la surveillance des performances. | - A.10.4. Gestion des changements<br>- A.10.2. Surveillance des performances | - Historique des versions<br>- Rapports de veille<br>- Procédures de mise à jour | - Personne en charge du projet<br>- Personne en charge du développement<br>- Personne en charge des systèmes informatiques |

## 8. Interopérabilité
<ins>Portée</ins> : compatibilité entre différents systèmes d'IA, intégration du système d’IA avec d’autres outils et normes existants, capacité à échanger des informations.

<ins>Principaux risques traités</ins> : verrouillage technologique, incompatibilités de formats<sup><a href="#note16" id="ref16">[16]</a></sup>.

<ins>Objectif</ins> : risques sur les droits fondamentaux (liberté d'information, cf. Art. 11 de la [Charte UE]) assurer l’interopérabilité fluide des données et des technologies sur lesquelles elles reposent.

<ins>Principale(s) référence(s)</ins> : [RGI].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|

| **BP067. Utiliser des standards ouverts pour les échanges de données** | Utiliser des formats et protocoles ouverts afin de garantir l’interopérabilité et la pérennité des échanges. | Aucune | - Formats ouverts (JSON, XML, CSV)<br>- Protocoles standards | - DSI |
| **BP068. Éviter les formats et protocoles propriétaires** | Limiter la dépendance à des solutions propriétaires pour faciliter la réversibilité. | Aucune | - Analyse de dépendance éditeur | - DSI<br>- Achats |
| **BP069. Documenter les interfaces et services exposés** | Fournir une documentation claire et structurée des interfaces et services. | A.6.2.7 Documentation technique du système d’IA | - Documentation API<br>- Guides d’intégration | - Équipe technique |
| **BP070. Mettre en œuvre des API normalisées et interopérables** | Concevoir des API respectant des conventions et standards reconnus. | A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - API REST standardisées | - Architecte applicatif |
| **BP071.	Assurer la comptabilité des données** | Identifier les sources de données, les données consommées, les traitements de données effectués et les données produites, vérifier que ces données sont référencées (ex : dans une ontologie pivot) pour faciliter leur interopérabilité et leur réutilisation. | - A.8.6. Traçabilité des données<br>- A.8.7. Gestion des métadonnées | - Registres de données<br>- Ontologie(s)<br>- Dictionnaires de données | - _Data engineer_<br>- _Data steward_<br>- Personne en charge de l'architecture des données |
| **BP072. Assurer l’interopérabilité sémantique des données** | Garantir une compréhension homogène du sens des données échangées. | A.7.4 Qualité des données pour les systèmes d’IA | - Modèles conceptuels documentés | - Data architect |
| **BP073. Garantir la traçabilité et la provenance des données échangées** | Documenter l’origine, les transformations et l’usage des données. | A.7.5 Traçabilité et provenance des données | - Métadonnées de provenance | - Responsable données |
| **BP074. Favoriser la réutilisation des services et des données** | Concevoir des services et jeux de données réutilisables. | Aucune | - Catalogue de services | - DSI |
| **BP075. Assurer la compatibilité avec des systèmes hétérogènes** | Concevoir des systèmes capables d’interagir avec des environnements variés. | Aucune | - Tests d’intégration inter‑SI | - Architecte SI |
| **BP076. Intégrer l’interopérabilité dès la conception des systèmes d’IA** | Prendre en compte l’interopérabilité dès le cadrage et la conception des systèmes d’IA. | A.6.1.2 Objectifs pour le développement responsable des systèmes d’IA | - Exigences d’architecture | - Responsable IA |
| **BP077.	Adopter des bonnes pratiques d’interopérabilité** | Appliquer les bonnes pratiques applicables du [RGI] et, le cas échéant, vérifier la conformité aux outils autorisés en interne pour favoriser l’interopérabilité des technologies<sup><a href="#note17" id="ref17">[17]</a></sup>. | - A.8.7. Standards d’interopérabilité<br>- A.6.4. Gestion des interfaces | - Documentation des API<br>Rapports de conformité<br>- Tests d’intégration | - Personne en charge de l'architecture des logiciels<br>- Personne en charge des systèmes informatiques<br>- Personne en charge du développement |

## 9. Respect de l’environnement
<ins>Portée</ins> : maîtrise de l’empreinte écologique globale associée au développement, au déploiement et à l’exploitation de technologies d’IA, maîtrise de la consommation énergétique, gestion des risques sur l’environnement engendrés par les systèmes d’IA.

<ins>Principaux risques traités</ins> : consommation excessive d’énergie, émissions de CO₂.

<ins>Objectif</ins> : risques sur les droits fondamentaux (protection de l'environnement, cf. Art. 37 de la [Charte UE]),  réduire globalement les besoins en ressources matérielles et énergétiques et les impacts environnementaux associés.

<ins>Principale(s) référence(s)</ins> : [RGESN], [RGIAF].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP069. Qualifier la pertinence du recours à l’IA** | Évaluer si le recours à l’IA est justifié au regard des besoins et des impacts environnementaux. | Aucune a priori | - Étude d’opportunité<br>- Comparaison avec solutions non‑IA | - Responsable métier |
| **BP070. Redéfinir les besoins fonctionnels de manière frugale** | Ajuster les besoins pour limiter les exigences inutiles en données et calcul. | Aucune a priori | - Expression de besoins revisitée | - Responsable produit |
| **BP071. Limiter les objectifs de performance à l’essentiel** | Fixer des objectifs de performance proportionnés aux usages réels. | Aucune a priori | - KPI limitées et justifiées | - Responsable IA |
| **BP072. Évaluer l’impact environnemental dès la phase de cadrage** | Réaliser une première estimation des impacts environnementaux du projet IA. | - A.5.2 Processus d’évaluation des impacts du système d’IA | - Estimation d’impact initiale | - Responsable projet |
| **BP073. Concevoir des systèmes d’IA éco‑responsables** | Intégrer des principes d’éco‑conception dès la conception technique. | - A.6.1.3 Processus de conception et de développement responsable des systèmes d’IA | - Choix d’architecture argumentés | - Architecte IA |
| **BP074. Optimiser l’architecture technique** | Concevoir des architectures sobres et adaptées aux usages. | - A.6.1.3 Processus de conception et de développement responsable des systèmes d’IA | - Schémas d’architecture<br>- Justifications | - Architecte |
| **BP075. Réduire la complexité des modèles** | Adapter la complexité des modèles au strict nécessaire. | Aucune a priori | - Comparaison de modèles | - Data scientist |
| **BP076. Limiter les phases d’entraînement** | Réduire le nombre et la durée des entraînements de modèles. | Aucune a priori | - Journal des entraînements | - Équipe IA |
| **BP077. Réutiliser des modèles existants** | Favoriser l’usage de modèles pré‑entraînés lorsque pertinent. | Aucune a priori | - Liste de modèles réutilisés | - Équipe IA |
| **BP078. Mutualiser les ressources de calcul** | Mutualiser les infrastructures pour limiter l’empreinte globale. | - A.4.5 Ressources systèmes et de calcul | - Mutualisation des infrastructures | - DSI |
| **BP079. Adapter les environnements de développement** | Ajuster les environnements de test et développement pour réduire leur consommation. | - A.6.2.6 Exploitation et surveillance du système d’IA | - Paramétrage des environnements | - Équipe technique |
| **BP080. Intégrer la frugalité sur tout le cycle de vie** | Prendre en compte la frugalité à chaque étape du cycle de vie du système d’IA. | - A.6.2.2 Exigences et spécifications du système d’IA | - Documentation cycle de vie | - Responsable projet |
| **BP081. Piloter la performance environnementale** | Mesurer et améliorer la performance environnementale des systèmes d’IA. | - A.5.3 Documentation des évaluations d’impact du système d’IA | - Indicateurs environnementaux | - Direction<br>- Responsable IA |
| **BP082. Acculturer et former les parties prenantes** | Former les acteurs aux enjeux de l’IA frugale. | - A.3.2 Rôles et responsabilités en matière d’IA | - Plans de formation | - RH |
| **BP083. Documenter les impacts environnementaux** | Formaliser et conserver la documentation liée aux impacts environnementaux. | - A.5.3 Documentation des évaluations d’impact du système d’IA | - Rapports d’impact | - Responsable IA |
| **BP084. Utiliser des données pertinentes et limitées** | Sélectionner uniquement les données nécessaires aux objectifs du système. | - A.7.3 Acquisition des données | - Justification des datasets | - Équipe data |
| **BP085. Réduire la duplication des données** | Limiter les copies et redondances de données. | - A.7.5 Traçabilité et provenance des données | - Architecture des flux | - DSI |
| **BP086. Optimiser le stockage des données** | Adapter les modalités de stockage pour limiter leur impact. | - A.4.3 Ressources de données | - Politique de stockage | - DSI |
| **BP087. Utiliser des jeux de données open source en prototypage** | Utiliser des données ouvertes en phase exploratoire. | Aucune a priori | - Sources open data | - Data scientist |
| **BP088. Optimiser l’usage des équipements existants** | Privilégier l’usage des équipements existants avant renouvellement. | - A.4.5 Ressources systèmes et de calcul | - Inventaire matériel | - DSI |
| **BP089. Créer un référentiel des impacts environnementaux** | Centraliser les informations d’impact environnemental des projets IA. | - A.5.3 Documentation des évaluations d’impact du système d’IA | - Référentiel interne | - Responsable IA |
| **BP090. Outiller la mesure d’impact environnemental** | Utiliser des outils dédiés à la mesure des impacts environnementaux. | - A.5.2 Processus d’évaluation des impacts du système d’IA | - Outils de mesure | - RSSI |
| **BP091. Estimer a priori la consommation des modèles** | Évaluer la consommation énergétique estimée avant déploiement. | - A.6.2.2 Exigences et spécifications du système d’IA | - Estimation prévisionnelle | - Équipe IA |
| **BP092. Ajuster les usages aux impacts environnementaux** | Adapter les usages en fonction des impacts mesurés. | Aucune a priori | - Règles d’usage | - Responsable métier |
| **BP093. Faire évoluer les stratégies de mesure** | Adapter les indicateurs et méthodes de mesure dans le temps. | - A.5.2 Processus d’évaluation des impacts du système d’IA | - Évolution des tableaux de bord | - Direction |
| **BP094. Adopter un codage durable et réutilisable** | Mettre en œuvre des pratiques de développement durables. | - A.6.1.3 Processus de conception et de développement responsable des systèmes d’IA | - Bonnes pratiques de code | - Développeurs |
| **BP095. Rationaliser les modèles** | Simplifier les modèles afin d’améliorer leur efficience. | Aucune a priori | - Comparatif de modèles | - Data scientist |
| **BP096. Décomposer les modèles complexes** | Préférer des modèles spécialisés à un modèle unique complexe. | Aucune a priori | - Architecture multi‑modèles | - Architecte IA |
| **BP097. Réutiliser et partager les modèles entraînés** | Favoriser la réutilisation et le partage de modèles existants. | Aucune a priori | - Dépôts de modèles | - Équipe IA |
| **BP098. Privilégier des modèles plus frugaux** | Choisir des modèles moins gourmands en ressources. | Aucune a priori | - Critères de sélection | - Responsable IA |
| **BP099. Réaliser des tests A/B pour optimiser le ratio performance/ressources** | Comparer plusieurs modèles afin de retenir le meilleur compromis. | Aucune a priori | - Résultats de tests A/B | - Équipe IA |

## 10. Accessibilité
<ins>Portée</ins> : accès aux systèmes d'IA, notamment pour les personnes handicapées, gestion des risques d’inégalités engendrés par les systèmes d’IA.

<ins>Principaux risques traités</ins> : risques sur les droits fondamentaux (non-discrimination, et intégration des personnes handicapées, cf. Art. 21 et 26 de la [Charte UE]), exclusion numérique, inégalités d’accès, manque de compatibilité avec les technologies d’assistance.

<ins>Objectif</ins> : intégrer les principes d’accessibilité numérique dès la conception et tester régulièrement l’interface pour garantir une utilisation inclusive.

<ins>Principale(s) référence(s)</ins> : [RGAA], [EN 301 549], [WCAG].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**Correspondance(s) [ISO/IEC 42001]**<br>(principales)</center> | <center>**Observables**<br>(exemples)</center> | <center>**Responsables**<br>(exemples)</center> |
|---|---|---|---|---|
| **BP067. Intégrer l’accessibilité numérique dès la conception** | Intégrer les besoins d’accessibilité dès le cadrage et la conception des services numériques. | A.6.1.2 Objectifs pour le développement responsable des systèmes d’IA | - Exigences d’accessibilité intégrées | - Chef de projet |
| **BP068. Garantir une gouvernance dédiée à l’accessibilité numérique** | Mettre en place une gouvernance claire pour piloter l’accessibilité. | A.3.2 Rôles et responsabilités en matière d’IA | - Référent accessibilité identifié | - Direction |
| **BP069. Produire des contenus perceptibles par tous** | Rendre les contenus perceptibles quels que soient les handicaps. | Aucune | - Textes alternatifs<br>- Contrastes conformes | - Contributeurs |
| **BP070. Concevoir des interfaces utilisables sans dispositif spécifique** | Garantir une utilisation complète au clavier et sans gestes complexes. | A.9.4 Utilisation conforme à l’usage prévu du système d’IA | - Navigation clavier testée | - Développeurs |
| **BP071. Assurer la compréhensibilité des informations et interactions** | Garantir des contenus clairs, prévisibles et compréhensibles. | Aucune | - Messages d’erreur explicites | - UX designer |
| **BP072. Garantir la robustesse technique des services numériques** | Assurer la compatibilité avec les technologies d’assistance et navigateurs. | A.6.2.4 Vérification et validation du système d’IA | - Tests multi‑navigateurs | - Développeurs |
| **BP073. Rendre accessibles les résultats et sorties des systèmes d’IA** | Présenter les résultats générés par l’IA de manière accessible. | A.8.2 Documentation du système et informations destinées aux utilisateurs | - Alternatives textuelles | - Responsable IA |
| **BP074. Concevoir des formulaires et assistants accessibles** | Garantir l’accessibilité des formulaires et agents conversationnels. | A.9.2 Processus relatifs à l’utilisation responsable des systèmes d’IA | - Étiquettes correctement associées | - Équipe technique |
| **BP075. Évaluer régulièrement la conformité à l’accessibilité** | Auditer périodiquement l’accessibilité des services numériques. | A.5.2 Processus d’évaluation des impacts du système d’IA | - Audits réalisés | - Référent accessibilité |
| **BP076. Informer les utilisateurs et publier les informations obligatoires** | Publier les informations obligatoires et recueillir les retours utilisateurs. | A.8.5 Informations destinées aux parties intéressées | - Déclaration publiée | - Communication |
| **BP100.	Adopter des bonnes pratiques d’accessibilité** | Se conformer au [RGAA] en appliquant les bonnes pratiques applicables de l’[EN 301 549] ou des [WCAG]<sup><a href="#note18" id="ref18">[18]</a></sup>, en visant l'accessibilité et l'autonomisation des usagers, pour favoriser une expérience d'IA positive et inclusive pour tous les usagers. | - A.6.5. Accessibilité numérique<br>- A.9.1. Conformité réglementaire | - Rapports d’audit d’accessibilité<br>- Tests usagers<br>- Guides de bonnes pratiques | - Personne en charge du projet<br>Personne en charge de l'accessibilité<br>- Personne en charge du développement |

## Annexe - Déclaration d'applicabilité (DdA)
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
| Adopter des bonnes pratiques de sécurité de l’information | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Respecter les [Recos ANSSI] | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

### Protection des droits et libertés
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> | <center>**Mesures additionnelles**</center> |
| --- | --- | --- | --- |
| Mettre le traitement en conformité avec la réglementation | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |
| Respecter les {Recos CNIL] | ☐ Oui<br>☐ Non<br>☐ Ne sais pas |  |

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

## Annexe - Couverture des droits fondamentaux de la [Charte UE]

Le tableau suivant présente la couverture des droits fondamentaux de la [Charte UE] par les bonnes pratiques :

| Droit fondamental | 1. Gouvernance responsable | 2. Fiabilité & sûreté | 3. Équité | 4. Transparence | 5. Sécurité de l'information | 6. Protection des droits & libertés | 7. Maintenabilité & évolutivité | 8. Interopérabilité | 9. Respect de l’environnement | 10. Accessibilité |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Art. 1 — Dignité humaine | ✅ | ✅ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 3 — Droit à l’intégrité de la personne | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 7 — Respect de la vie privée et familiale | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 8 — Protection des données à caractère personnel | ✅ | ⚪ | ⚪ | ✅ | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 11 — Liberté d’expression et d’information | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ✅ | ⚪ | ✅ | ⚪ | ⚪ |
| Art. 20–21 — Égalité devant la loi / Non-discrimination | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ |
| Art. 23 — Égalité entre femmes et hommes | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 24 — Droits de l’enfant | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ |
| Art. 25–26 — Droits des personnes âgées et handicapées | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ |
| Art. 27–31 — Droits des travailleurs (conditions équitables, information, santé) | ✅ | ✅ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 35 — Protection de la santé | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 37 — Protection de l’environnement | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ |
| Art. 38 — Protection des consommateurs | ✅ | ✅ | ⚪ | ✅ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Art. 41 — Droit à une bonne administration | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ✅ | ✅ | ✅ | ⚪ | ⚪ |
| Art. 42–43 — Accès aux documents / Médiateur européen | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ |
| Art. 47 — Droit à un recours effectif et à un procès équitable | ✅ | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |

## Annexe - Couverture des exigences du [Règlement IA]

Le tableau suivant présente la couverture des exigences du [Règlement IA] par les bonnes pratiques :

| Exigence | 1. Gouvernance responsable | 2. Fiabilité & sûreté | 3. Équité | 4. Transparence | 5. Sécurité de l'information | 6. Protection des droits & libertés | 7. Maintenabilité & évolutivité | 8. Interopérabilité | 9. Respect de l’environnement | 10. Accessibilité |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Système de gestion de la qualité (Art. 17) | ✅ | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ |
| Gouvernance des données (Art. 10) | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Documentation technique (Art. 11) | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ |
| Tenue des enregistrements (Art. 12) | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Transparence et informations à l’utilisateur (Art. 13) | ⚪ | ⚪ | ⚪ | ✅ | ⚪ | ✅ | ⚪ | ✅ | ⚪ | ✅ |
| Supervision humaine (Art. 14) | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Robustesse, précision et cybersécurité (Art. 15) | ⚪ | ✅ | ⚪ | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ⚪ |
| Conformité et contrôle post-commercialisation (Art. 61–65) | ✅ | ✅ | ⚪ | ⚪ | ⚪ | ✅ | ✅ | ⚪ | ⚪ | ⚪ |

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
