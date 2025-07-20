# Intelligence artificielle - Bonnes pratiques

## Objet du document
**Ce document propose une liste de bonnes pratiques qui permettent de respecter les critères de confiance que tout système d’intelligence artificielle (IA) devrait respecter**.
Il peut être directement utilisé dans le cadre des projets de nouveaux services qui reposent sur l’IA pour comparer ce qui est prévu ou mis en œuvre aux bonnes pratiques, et peut également être intégré à une démarche de gestion des risques.

[Avant-propos](#avant-propos)<br/>
[Introduction](#introduction)<br/>
[1. Gouvernance responsable](#1-gouvernance-responsable)<br/>
[2. Fiabilité et sûreté](#2-fiabilité-et-sûreté)<br/>
[3. Équité](#3-équité)<br/>
[4. Transparence](#4-transparence)<br/>
[5. Sécurité de l'information](#5-sécurité-de-linformation)<br/>
[6. Protection des droits et libertés](#6-protection-des-droits-et-libertés)<br/>
[7. Maintenabilité et évolutivité](#7-maintenabilité-et-évolutivité)<br/>
[8. Interopérabilité](#8-interopérabilité)<br/>
[9. Respect de l'environnement](#9-respect-de-lenvironnement)<br/>
[10. Accessibilité](#10-accessibilité)<br/>
[Annexe : déclaration d'applicabilité (DdA)](#annexe--déclaration-dapplicabilité-dda)<br/>

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
- Matthieu GRALL, expert-conseil en management des données, sécurité de l’information, protection de la vie privée et nouvelles technologies ;
- Cécile LAMARQUE, sociologue.

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

## Introduction
La multiplicité des documents de référence, spécifiques à l’IA<sup><a href="#note1" id="ref1">[1]</a></sup>  ou applicables à tous les systèmes<sup><a href="#note2" id="ref2">[2]</a></sup>, apporte de la confusion chez ceux qui doivent ou souhaitent les appliquer.

Ils peuvent en effet sembler :
-	**chacun incomplet**, car leurs périmètres diffèrent (par domaines comme la sécurité de l’information ou la protection des droits et libertés, par techniques d’IA comme les LLM<sup><a href="#note3" id="ref3">[3]</a></sup> , par phases comme le développement, etc.). Ceci est notamment dû au fait que les problématiques liées à l’IA imposent une vision globale, alors que les périmètres de compétences et spécialités des organismes émetteurs sont restreints ;

-	**tous incohérents**, car leurs structures, bonnes pratiques et terminologies diffèrent, mêmes si elles ont des similarités, et que les normes internationales<sup><a href="#note4" id="ref4">[4]</a></sup>  ne sont pas encore matures.

Or, quand on veut mettre en œuvre un système basé sur l’IA, on doit ou on souhaite **respecter l’ensemble des références applicables, et ce, de manière cohérente !**

Ainsi, ce document **propose des bonnes pratiques harmonisées**, organisées selon les [Critères de confiance de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Crit%C3%A8res%20de%20confiance.md), qui considèrent les différents [Exemples de micro-cas d'usages de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Micro-cas%20d'usages%20-%20Exemples.md), et qui peuvent être utilisées dans le cadre de la [Méthode de gestion des risques de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20M%C3%A9thode.md).
Des _tags_ sont ajoutés, à titre indicatif, pour orienter vers :
- les principales mesures de l'annexe A de l'[ISO/IEC 42001] correspondantes ;
- les principales phases du cycle de vie de la [Recommandation de l'OCDE] concernées ;
- des exemples de preuve de mise en œuvre observables ;
- les principales fonctions types d'entreprise concernées.

L'Annexe [« Déclaration d'applicabilité »](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md#annexe---d%C3%A9claration-dapplicabilit%C3%A9-) peut être utilisée pour présenter les pratiques mises en œuvre en comparaison aux bonnes pratiques.

Note : un renvoi vers les documents de référence est privilégié quand cela est opportun.

## 1. Gouvernance responsable
<ins>Objectif</ins> : instaurer un cadre de gouvernance qui permet de partager et contrôler l’éthique des processus mis en œuvre dans les projets qui reposent sur l’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE], [ISO/IEC 42001].

**BP01.	Formaliser les responsabilités des parties intéressées**

Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA.

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP01. Formaliser les responsabilités des parties intéressées** | Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA. | A.3.2 Rôles et responsabilités IA<br>A.3.4 Implication des parties intéressées | Planification et conception<br>Exploitation et maintenance | Organigrammes des responsabilités<br>Matrices RACI<br>Procès-verbaux de réunions de gouvernance | Direction<br>Responsable conformité<br>Chef de projet IA |  
| **BP02. Partager les valeurs éthiques** | Impliquer, voire former, les parties intéressées pour assurer que les technologies liées à l'IA sont produites et utilisées conformément à des valeurs éthiques, en surveillant les préjugés, la confidentialité et les abus, tout en promouvant l'innovation et la confiance. | A.7.2 Formation et sensibilisation<br>A.6.2 Communication sur les valeurs | Planification et conception<br>Exploitation et maintenance | Matériel de formation<br>Comptes rendus de sessions de sensibilisation<br>Chartes éthiques signées | Direction<br>Responsable éthique<br>Ressources humaines |  
| **BP03. Déterminer des mécanismes de contrôle** | Trouver et mettre en œuvre le(s) moyen(s) le(s) plus efficace(s), c’est-à-dire cohérent(s) avec la taille, la maturité et les processus existants de l’organisme, pour vérifier régulièrement que l’éthique est effectivement considérée dans les projets qui reposent sur de l’IA (ex : reporting, revue annuelle, indicateurs basés sur des objectifs prédéfinis, audits, rapports de gouvernance, comité d’éthique). | A.4.2 Mécanismes de gouvernance IA<br>A.12.1 Suivi et audit des systèmes IA | Planification et conception<br>Exploitation et maintenance | Rapports d’audit<br>Procès-verbaux de comité d’éthique<br>Indicateurs de performance documentés | Direction<br>RSSI<br>Responsable conformité |  

## 2. Fiabilité et sûreté
<ins>Objectif</ins> : assurer la robustesse des systèmes qui reposent sur l’IA afin d’améliorer leur fiabilité et la sécurité des biens et des personnes.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP04. Vérifier les données d’entrée possibles** | Vérifier les particularités des données futures, par exemple à l’aide de modules spécifiques dans la chaine de traitements de données. | A.8.3 Qualité des données<br>A.8.2 Gestion des données d'entrée | Collecte et traitement des données | Logs de vérification<br>Scripts de validation des données<br>Résultats de tests de qualité des données | Data engineer<br>Data scientist<br>Responsable qualité des données |  
| **BP05. Vérifier la robustesse du modèle** | Vérifier que le modèle ne peut pas être attaqué pour produire un résultat indésirable, par exemple dans le cadre d’une chaine de modèles. | A.10.3 Sécurité du modèle IA<br>A.11.3 Robustesse du modèle | Test, évaluation et vérification<br>Exploitation et maintenance | Rapports de tests d’attaque<br>Résultats d’évaluations adversariales<br>Journalisation des tests de robustesse | Data scientist<br>RSSI<br>Expert sécurité IA |  
| **BP06. Éprouver les limites du système dans sa globalité** | Mettre en place des mesures pour éprouver et consolider le système d’IA (ex : tests de charge et de stress, simulations d’attaques, redondances techniques, procédures de réponse aux incidents) en considérant l’amont et l’aval du système d’IA. | Tests de résistance et de robustesse (A.11.1)<br>Gestion des incidents (A.12.4) | Test, évaluation et vérification<br>Exploitation et maintenance | Rapports de tests de charge et de stress<br>Journaux d’incidents<br>Simulations documentées | Responsable qualité<br>Data scientist<br>RSSI |  
| **BP07. Évaluer les performances du système** | Faire des mesures quantitatives pour évaluer les performances du modèle dans diverses conditions de stress, notamment les attaques contradictoires, le bruit et les changements de distribution des données (ex : taux de faux positifs/négatifs, étude de l’erreur quadratique moyenne – MSE, distance de Wasserstein, score de Brier). | Mesure et suivi des performances (A.10.2)<br>Analyse des résultats (A.11.2) | Test, évaluation et vérification | Rapports d’évaluation<br>Tableaux de bord de performance<br>Résultats d’audits techniques | Data scientist<br>Responsable qualité<br>Analyste |  
| **BP08. Mettre en place les mesures de sûreté nécessaires** | Tester et valider le système d’IA pour répondre aux normes de sûreté et aux exigences réglementaires dans les applications où la sûreté est primordiale (ex : véhicules autonomes, soins de santé), intégrer plusieurs mesures redondantes pour gérer les pannes sans causer de dommages ni de perturbations significatives, laisser la main à l’humain, en particulier dans le cadre de prises de décisions critiques, pour intervenir, outrepasser ou guider les actions de l'IA si nécessaire. | Sécurité et sûreté (A.11.5)<br>Supervision humaine (A.7.7) | Test, évaluation et vérification<br>Exploitation et maintenance | Rapports de validation de sûreté<br>Procédures de supervision humaine<br>Plans de contingence | Responsable sûreté<br>Data scientist<br>Opérateur métier |  

## 3. Équité
<ins>Objectif</ins> : détecter et corriger les biais par des mécanismes de vérification et d’audit des algorithmes.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recommandations IA de la CNIL], [Guide de France IA].

### 3.1. Réduction des biais liés à la formulation du cas d'usage

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP09. Définir clairement le(s) cas d’usage(s)** | Décrire précisément le cas d’usage, les limitations et les exceptions, et s’assurer que les personnes en charge de la conception et du développement des outils en ont connaissance et les comprennent. | Définition du périmètre et des usages (A.5.1)<br>Communication des exigences (A.6.2) | Planification et conception | Cahiers des charges<br>Spécifications fonctionnelles<br>Documents de conception | Chef de projet<br>Analyste métier<br>Architecte IA |  

### 3.2. Réduction des biais liés aux données d'entrée

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP10. Diversifier les données d’entrée** | Utiliser des sources de données diverses et représentatives. | Qualité des données (A.8.3)<br>Gestion des données d’entrée (A.8.2) | Collecte et traitement des données | Catalogue des sources de données<br>Rapports de couverture de données<br>Audits de représentativité | Data engineer<br>Data scientist<br>Responsable qualité données |  
| **BP11. Rendre les données exploitables** | Limiter les données qu’à celles qui seront traitées, les transformer / intégrer de façon cohérente (ex : via une ontologie qui sert de pivot), et les nettoyer de manière approfondie, afin de faciliter leur traitement, de ne pas traiter de données inutilisables, inutiles, sujettes à des règles internes ou externes, ou qu’on ne souhaite pas traiter. | Gestion de la qualité des données (A.8.3)<br>Traitement cohérent des données (A.8.5) | Collecte et traitement des données | Processus de nettoyage documentés<br>Ontologies utilisées<br>Rapports de qualité des données | Data engineer<br>Data steward<br>Responsable qualité données |  

### 3.3. Réduction des biais liés aux données d'entrainement

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP12. S’assurer de la qualité des données d’entrainement** | Vérifier la pertinence des données par rapport au problème à résoudre, leur fiabilité (crédibles et/ou de sources objectives), et la légalité de leur collecte et de leur traitement. | Contrôle qualité des données d’entrainement (A.8.3)<br>Conformité légale (A.9.1) | Collecte et traitement des données | Audits de qualité<br>Certificats de conformité<br>Procédures de validation | Data scientist<br>Juriste<br>Responsable conformité |  
| **BP13. Faire des échantillonnages équilibrés des données d’entrainement** | Respecter les bonnes pratiques d’échantillonnage pour que les échantillons soient équilibrés. | Equilibrage des données (A.8.3)<br>Gestion des biais (A.11.1) | Collecte et traitement des données | Rapports d’échantillonnage<br>Analyses statistiques<br>Tests d’équilibre | Data scientist<br>Analyste statistique<br>Responsable qualité |  
| **BP14. Corriger les corrélations indésirables** | Identifier les corrélations entre les caractéristiques ou les variables, évaluer leur impact et gérer ceux qui ne sont pas acceptables. | Analyse des dépendances (A.11.2)<br>Gestion des biais (A.11.1) | Construction ou adaptation du modèle | Rapports d’analyse des corrélations<br>Actions correctives documentées | Data scientist<br>Statisticien<br>Responsable qualité |  
| **BP15. Collecter de nouvelles données dès que cela est nécessaire** | Recourir à de nouvelles données d’entrée jusqu’à avoir l’assurance que les biais sont suffisamment réduits. | Surveillance de la qualité des données (A.8.3)<br>Gestion des évolutions des données (A.10.2) | Collecte et traitement des données<br>Exploitation et maintenance | Rapports de nouvelles collectes<br>Indicateurs d’équité<br>Documents d’ajustement des jeux de données | Data scientist<br>Data engineer<br>Responsable qualité |  

### 3.4. Réduction des biais liés à l'agorithme d'entrainement / Architecture du modèle

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP16. Évaluer la qualité du modèle** | Mesurer l'équité à l’aide de modèles mathématiques, comme l'indépendance statistique, les intervalles de confiance, l'étude de séparation et l'étude de suffisance. | Évaluation de la performance des modèles (A.10.2)<br>Gestion des biais (A.11.1) | Test, évaluation et vérification | Rapports d’évaluation d’équité<br>Analyses statistiques<br>Documentations d’audits | Data scientist<br>Analyste qualité<br>Responsable éthique |  
| **BP17. Évaluer les performances du modèle** | Évaluer les performances de l'algorithme de manière régulière. | Surveillance continue des performances (A.10.2)<br>Revue des modèles IA (A.10.4) | Test, évaluation et vérification<br>Exploitation et maintenance | Tableaux de bord de suivi<br>Rapports périodiques<br>Plans d’amélioration | Data scientist<br>Responsable qualité<br>Analyste |  
| **BP18. Faire auditer le modèle** | Réaliser un audit pour identifier et corriger les biais. | Audit des systèmes IA (A.12.1)<br>Gestion des risques IA (A.11.1) | Test, évaluation et vérification | Rapports d’audit<br>Plans d’action corrective<br>Attestations d’audit | Auditeur IA<br>Responsable conformité<br>Data scientist |  

### 3.5. Réduction des biais liés aux données de sortie

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |  
|---|---|---|---|---|---|  
| **BP19. Valider les données de sorties** | Valider les résultats produits, si possible de manière continue, voire consulter des experts en éthique et inclusion. | Validation des résultats (A.10.3)<br>Implication des experts (A.3.4) | Test, évaluation et vérification<br>Exploitation et maintenance | Rapports de validation<br>Comptes rendus de consultations<br>Tableaux de suivi | Data scientist<br>Expert éthique<br>Responsable qualité |  
| **BP20. Obtenir les retours des usagers** | Collecter régulièrement les commentaires et retours d'expérience des usagers, pour détecter et corriger les biais dans les résultats. | Gestion des retours utilisateurs (A.7.3)<br>Surveillance des impacts (A.10.5) | Exploitation et maintenance | Rapports d’enquête<br>Comptes rendus d’atelier utilisateurs<br>Tickets de support | Support utilisateur<br>Chef de projet<br>Responsable qualité |  

## 4. Transparence

<ins> Objectif </ins> : rendre explicites les algorithmes et les processus de décision via une documentation accessible, des interfaces interactives et des explications techniques adaptées aux différents publics.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP21.	Formaliser les éléments utiles à la transparence** | Élaborer les explications<sup><a href="#note5" id="ref5">[5]</a></sup>,  nécessaires à la transparence<sup><a href="#note6" id="ref6">[6]</a></sup>, notamment pour expliquer d’où les données proviennent les données, la forme qu’elles prennent et leur utilisation par l’organisme, et les faire connaître<sup><a href="#note7" id="ref7">[7]</a></sup>  aux personnes chargées de créer et de maintenir les modèles et les flux de données, aux usagers, et aux autorités compétentes. | Documentation et communication (A.6.2)<br>Transparence des données (A.8.7) | Planification et conception<br>Exploitation et maintenance | Documents de transparence<br>Rapports d’audit<br>Supports de formation | Responsable conformité<br>Chef de projet<br>Data scientist |

## 5. Sécurité de l'information
<ins>Objectif</ins> : appliquer les bonnes pratiques de sécurité de l’information au système d’IA, pour réduire les risques sur l’organisme en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données, tout le long du cycle de vie du système.

<ins>Principale(s) référence(s)</ins> : [Recommandations IA de l'ANSSI - 2024], [Recommandations IA de l'ANSSI - 2025], [Guide de France IA].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP22.	Respecter les recommandations de l’ANSSI** | Appliquer les [Recommandations IA de l'ANSSI - 2024] (chapitre 5) applicables dans le cas d’un système d’IA générative et les [Recommandations IA de l'ANSSI - 2025] (annexe I). | Sécurité des systèmes (A.10.1)<br>Gestion des vulnérabilités (A.11.4) | Construction ou adaptation du modèle<br>Exploitation et maintenance | Rapports de conformité ANSSI<br>Plans d’action<br>Tests de sécurité | RSSI<br>Responsable sécurité IA<br>DSI |
| **BP23.	Adopter des bonnes pratiques de sécurité de l’information** | Appliquer la politique de sécurité des systèmes d’information, ou les bonnes pratiques de sécurité de l’information applicables selon la maturité de l’organisme en la matière (ex : [Guide sécurité de la CNIL], [Guide d'hygiène de l'ANSSI], [ISO/IEC 27002]). | Politique de sécurité (A.2.2)<br>Contrôle d’accès (A.9.1)<br>Protection des actifs (A.8.1) | Toutes phases | Politiques formalisées<br>Rapports d’audit<br>Logs d’accès | RSSI<br>DSI<br>Responsable sécurité |

## 6. Protection des droits et libertés
<ins>Objectif</ins> : appliquer les grands principes de la protection de la vie privée au traitement de données par IA, pour réduire les risques sur les personnes concernées en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données.

<ins>Principale(s) référence(s)</ins> : [Recommandations IA de la CNIL], [Loi I&L], [RGPD].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP24.	Respecter les recommandations de la CNIL** | Appliquer les [Recommandations IA de la CNIL] applicables dans le cas d’une phase de développement. | Protection des données personnelles (A.9.2)<br>Conformité réglementaire (A.9.1) | Collecte et traitement des données<br>Construction ou adaptation du modèle | Rapports de conformité CNIL<br>Registres des traitements<br>DPIA | DPO<br>Juriste<br>Responsable conformité |
| **BP25.	Mettre le traitement en conformité avec la réglementation** | Formaliser les éléments nécessaires<sup><a href="#note8" id="ref8">[8]</a></sup>  à la personne / au service en charge de la protection de la vie privée pour bâtir la conformité du traitement de données à caractère personnel à la [Loi I&L] / au [RGPD]. | Conformité réglementaire (A.9.1)<br>Gestion des risques liés à la vie privée (A.9.3) | Collecte et traitement des données<br>Exploitation et maintenance | Registres de traitement<br>Rapports de conformité<br>Preuves de DPIA | DPO<br>Responsable conformité<br>Juriste |

## 7. Maintenabilité et évolutivité
<ins>Objectif</ins> : assurer performances, maintien en conditions opérationnelle et de sécurité, intégration de nouvelles fonctionnalités, et comptabilité ascendante, tout le long du cycle de vie du système d’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [ISO/IEC 42001].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP26.	Adopter un principe de modularité et de réutilisabilité** | Mettre en œuvre une conception modulaire du système d'IA, pour réutiliser/remplacer les composants de la chaîne sans affecter l'ensemble du système. | Architecture modulaire (A.6.4)<br>Gestion des changements (A.10.4) | Planification et conception<br>Construction ou adaptation du modèle | Diagrammes d’architecture<br>Documentation des modules<br>Gestion de versions | Architecte logiciel<br>Développeur<br>Chef de projet |
| **BP27.	Documenter le système** | Élaborer une documentation complète, qui comprend des commentaires sur le code, des manuels d'utilisation et une documentation sur le prétraitement des données, la formation des modèles et les processus de déploiement. | Documentation complète (A.6.2)<br>Gestion des connaissances (A.7.3) | Toutes phases | Documentation technique<br>Manuels utilisateurs<br>Historiques des modifications | Développeur<br>Chef de projet<br>Analyste |
| **BP28.	Contrôler la qualité du code** | Appliquer les bonnes pratiques de développement pour produire un code de haute qualité, notamment des conventions de nommage appropriées, un style cohérent et des algorithmes efficaces. | Contrôle qualité du code (A.10.1)<br>Revue de code (A.10.3) | Construction ou adaptation du modèle | Revues de code<br>Rapports d’analyse statique<br>Tests unitaires | Développeur<br>Responsable qualité |
| **BP29.	Permettre l’évolutivité** | Concevoir le système pour gérer des charges accrues et évoluer selon les besoins. Ceci implique également le maintien des performances et la gestion des ressources. | Scalabilité (A.10.5)<br>Gestion des ressources (A.11.6) | Planification et conception<br>Exploitation et maintenance | Tests de charge<br>Rapports de performance<br>Plans d’évolution | Architecte logiciel<br>DSI<br>Responsable qualité |
| **BP30.	Maîtriser les évolutions** | Mettre en œuvre un processus de gestion des évolutions, qui intègre la veille technologique, les tests de comptabilité ascendante, l’automatisation des correctifs et mises à jour, le contrôle des versions<sup><a href="#note9" id="ref9">[9]</a></sup> , et la surveillance des performances. | Gestion des changements (A.10.4)<br>Surveillance des performances (A.10.2) | Exploitation et maintenance | Historique des versions<br>Rapports de veille<br>Procédures de mise à jour | Chef de projet<br>Développeur<br>DSI |

## 8. Interopérabilité
<ins>Objectif</ins> : assurer l’interopérabilité fluide des données et des technologies sur lesquelles elles reposent.

<ins>Principale(s) référence(s)</ins> : [RGI].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP31.	Assurer la comptabilité des données** | Identifier les sources de données, les données consommées, les traitements de données effectués et les données produites, vérifier que ces données sont référencées (ex : dans une ontologie pivot) pour faciliter leur interopérabilité et leur réutilisation. | Traçabilité des données (A.8.6)<br>Gestion des métadonnées (A.8.7) | Collecte et traitement des données<br>Exploitation et maintenance | Registres de données<br>Ontologies documentées<br>Rapports d’audit | Data engineer<br>Data steward<br>Architecte données |
| **BP32.	Adopter des bonnes pratiques d’interopérabilité** | Appliquer les bonnes pratiques applicables du [RGI] et, le cas échéant, vérifier la conformité aux outils autorisés en interne pour favoriser l’interopérabilité des technologies<sup><a href="#note10" id="ref10">[10]</a></sup>. | Standards d’interopérabilité (A.8.7)<br>Gestion des interfaces (A.6.4) | Construction ou adaptation du modèle<br>Exploitation et maintenance | Documentation des API<br>Rapports de conformité<br>Tests d’intégration | Architecte logiciel<br>DSI<br>Développeur |

## 9. Respect de l’environnement
<ins>Objectif</ins> : réduire globalement les besoins en ressources matérielles et énergétiques et les impacts environnementaux associés.

<ins>Principale(s) référence(s)</ins> : [RGESN], [RGIAF].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP33.	Adopter des bonnes pratiques d’écoconception** | Identifier la consommation d'énergie des centres de données (_data centers_) lors de l’entrainement des modèles, l'économie circulaire du matériel, l'empreinte carbone, l'obsolescence et les déchets électroniques, et appliquer les bonnes pratiques applicables du [RGESN] ou du [RGIAF]. | Gestion de l’impact environnemental (A.13.1)<br>Optimisation des ressources (A.13.2) | Exploitation et maintenance<br>Décommisionnement et mise au rebut | Bilans énergétiques<br>Rapports RSE<br>Certificats d’éco-conception | Responsable RSE<br>DSI<br>Chef de projet |

## 10. Accessibilité
<ins>Objectif</ins> : intégrer les principes d’accessibilité numérique dès la conception et tester régulièrement l’interface pour garantir une utilisation inclusive.

<ins>Principale(s) référence(s)</ins> : [RGAA], [EN 301 549], [WCAG].

| <center>**Bonne pratique**</center> | <center>**Description**</center> | <center>**[ISO/IEC 42001]**</center> | <center>**Phase(s)**</center> | <center>**Observables illustratifs**</center> | <center>**Fonctions illustratives**</center> |
|---|---|---|---|---|---|
| **BP34.	Adopter des bonnes pratiques d’accessibilité** | Se conformer au [RGAA] en appliquant les bonnes pratiques applicables de l’[EN 301 549] ou des [WCAG]<sup><a href="#note11" id="ref11">[11]</a></sup>, en visant l'accessibilité et l'autonomisation des usagers, pour favoriser une expérience d'IA positive et inclusive pour tous les usagers. | Accessibilité numérique (A.6.5)<br>Conformité réglementaire (A.9.1) | Planification et conception<br>Exploitation et maintenance | Rapports d’audit d’accessibilité<br>Tests utilisateurs<br>Guides de bonnes pratiques | Chef de projet<br>Responsable accessibilité<br>Développeur |

## Annexe : déclaration d'applicabilité (DdA)
<ins>Notes</ins> :
-	l’objectif est d’une part de vérifier qu’on n’a rien oublié, et d’autre part d’apporter des éléments nécessaires à la prise de décision d’accepter ou non la mise en exploitation du système d’IA ;

-	les bonnes pratiques ne sont pas toutes applicables à un projet donné : certaines ne sont pas applicables (ex : si elles concernent un type d’IA qui n’est pas celui considéré), n’ont pas besoin d’être appliquées (ex : si le sujet est traité par ailleurs), ou sont exclues par l’organisation.

### Gouvernance responsable
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Formaliser les responsabilités des parties intéressées | ☐ Oui ☐ Non ☐ Ne sais pas |
| Partager les valeurs éthiques | ☐ Oui ☐ Non ☐ Ne sais pas |
| Déterminer des mécanismes de contrôle | ☐ Oui ☐ Non ☐ Ne sais pas |

### Fiabilité et sûreté
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Vérifier les données d’entrée possibles | ☐ Oui ☐ Non ☐ Ne sais pas |
| Vérifier la robustesse du modèle | ☐ Oui ☐ Non ☐ Ne sais pas |
| Éprouver les limites du système dans sa globalité | ☐ Oui ☐ Non ☐ Ne sais pas |
| Évaluer les performances du système | ☐ Oui ☐ Non ☐ Ne sais pas |
| Mettre en place les mesures de sûreté nécessaires | ☐ Oui ☐ Non ☐ Ne sais pas |

### Équité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Définir clairement le(s) cas d’usage(s) | ☐ Oui ☐ Non ☐ Ne sais pas |
| Diversifier les données d’entrée | ☐ Oui ☐ Non ☐ Ne sais pas |
| Rendre les données exploitables | ☐ Oui ☐ Non ☐ Ne sais pas |
| S’assurer de la qualité des données d’entrainement | ☐ Oui ☐ Non ☐ Ne sais pas |
| Faire des échantillonnages équilibrés des données d’entrainement | ☐ Oui ☐ Non ☐ Ne sais pas |
| Corriger les corrélations indésirables | ☐ Oui ☐ Non ☐ Ne sais pas |
| Collecter de nouvelles données dès que cela est nécessaire | ☐ Oui ☐ Non ☐ Ne sais pas |
| Évaluer la qualité du modèle | ☐ Oui ☐ Non ☐ Ne sais pas |
| Évaluer les performances du modèle | ☐ Oui ☐ Non ☐ Ne sais pas |
| Faire auditer le modèle | ☐ Oui ☐ Non ☐ Ne sais pas |
| Valider les données de sorties | ☐ Oui ☐ Non ☐ Ne sais pas |
| Obtenir les retours des usagers | ☐ Oui ☐ Non ☐ Ne sais pas |

### Transparence
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Formaliser les éléments utiles à la transparence | ☐ Oui ☐ Non ☐ Ne sais pas |

### Sécurité de l'information
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Respecter les recommandations de l’ANSSI | ☐ Oui ☐ Non ☐ Ne sais pas |
| Adopter des bonnes pratiques de sécurité de l’information | ☐ Oui ☐ Non ☐ Ne sais pas |

### Protection des droits et libertés
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Respecter les recommandations de la CNIL | ☐ Oui ☐ Non ☐ Ne sais pas |
| Mettre le traitement en conformité avec la réglementation | ☐ Oui ☐ Non ☐ Ne sais pas |

### Maintenabilité et évolutivité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Adopter un principe de modularité et de réutilisabilité|☐ Oui ☐ Non ☐ Ne sais pas |
| Documenter le système | ☐ Oui ☐ Non ☐ Ne sais pas |
| Contrôler la qualité du code | ☐ Oui ☐ Non ☐ Ne sais pas |
| Permettre l’évolutivité | ☐ Oui ☐ Non ☐ Ne sais pas |
| Maîtriser les évolutions | ☐ Oui ☐ Non ☐ Ne sais pas |

### Interopérabilité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Assurer la comptabilité des données | ☐ Oui ☐ Non ☐ Ne sais pas |
| Adopter des bonnes pratiques d’interopérabilité | ☐ Oui ☐ Non ☐ Ne sais pas |

### Respect de l’environnement
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Adopter des bonnes pratiques d’écoconception | ☐ Oui ☐ Non ☐ Ne sais pas |

### Accessibilité
| <center>**Bonnes pratiques**</center> | <center>**Applicabilité**</center> | <center>**Si oui, comment ? Si non, pourquoi ?**</center> |
| --- | --- | --- |
| Adopter des bonnes pratiques d’accessibilité | ☐ Oui ☐ Non ☐ Ne sais pas |

<br/>
<br/>
<a name="note1" id="note1">[1]</a> Notamment [ISO/IEC 42001], [Guide France IA], [Recommandation IA de l'OCDE], [Recommandations IA de l'ANSSI - 2024], [Recommandations IA de l'ANSSI - 2025], [Recommandations IA de la CNIL], [Règlement IA] et [RGIAF]. [↩](#ref1)
<br/>
<br/>
<a name="note2" id="note2">[2]</a> Notamment [Loi I&L] (dont [RGPD]), [RGAA], [RGESN], et [RGI]. [↩](#ref2)
<br/>
<br/>
<a name="note3" id="note3">[3]</a> LLM : _large language models_ (grands modèles linguistiques). [↩](#ref3)
<br/>
<br/>
<a name="note4" id="note4">[4]</a> Ex : [ISO/IEC 42001]. [↩](#ref4)
<br/>
<br/>
<a name="note5" id="note5">[5]</a> L’explicabilité peut reposer sur des méthodes agnostiques ou spécifiques, intrinsèques ou _post-hoc_, locales ou globales, _a priori_ ou _a posteriori_. Des outils tels que LIME ou SHAP peuvent notamment contribuer à cette explicabilité. [↩](#ref5)
<br/>
<br/>
<a name="note6" id="note6">[6]</a> La transparence s’applique aux algorithmes (logique et modèle), aux interactions (via l’interface utilisateur), et à la société (impact social de cette interaction). [↩](#ref6)
<br/>
<br/>
<a name="note7" id="note7">[7]</a> Ex : publier de la documentation technique, développer des interfaces explicatives, créer des tutoriels et guides d’usage, organiser des ateliers d’information. [↩](#ref7)
<br/>
<br/>
<a name="note8" id="note8">[8]</a> Finalité, données traitées, durées de conservation, destinataires, mesures prévues pour assurer la minimisation et la qualité des données, mesures prévues pour assurer l’information et les droits des personnes concernées (le cas échéant, d’accès, à la portabilité, de rectification, d’effacement, de limitation et d’opposition) et, le cas échéant, mesures prévues pour encadrer la sous-traitance et le transfert en dehors de l’UE. [↩](#ref8)
<br/>
<br/>
<a name="note9" id="note9">[9]</a> Recourir à un système de contrôle de version permet de suivre les modifications, de collaborer avec d'autres et de revenir aux versions précédentes si nécessaire. [↩](#ref9)
<br/>
<br/>
<a name="note10" id="note10">[10]</a> Notamment : utiliser des standards ouverts, respecter les API publiques, favoriser la portabilité des données, assurer la documentation des interfaces. [↩](#ref10)
<br/>
<br/>
<a name="note11" id="note11">[11]</a> Cela implique notamment de concevoir des interfaces ergonomiques, ou plusieurs modes d’interactions, en tenant compte de facteurs tels que la diversité linguistique et l’accessibilité pour les personnes handicapées, et de les tester avec des usagers en situation de handicap. [↩](#ref11)
