# Intelligence artificielle - Bonnes pratiques

Ce document est sous licence 
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

## Sommaire
[Contributeurs](#contributeurs)<br/>
[Versions](#versions)<br/>
[Documents de référence](#documents-de-référence)<br/>
[1. Object du document](#Object_du_document)<br/>
[2. Introduction](#2introduction)<br/>
[3. Bonnes pratiques pour l'IA](#3bonnes-pratiques-pour-lia)<br/>
[3.1. Gouvernance responsable](#31gouvernance-responsable)<br/>
[3.2. Fiabilité et sûreté](#32fiabilité-et-sûreté)<br/>
[3.3. Équité](#33équité)<br/>
[3.4. Transparence](#34transparence)<br/>
[3.5. Sécurité des informations](#35sécurité-des-informations)<br/>
[3.6. Protection des droits et libertés](#36protection-des-droits-et-libertés)<br/>
[3.7. Maintenabilité et évolutivité](#37maintenabilité-et-évolutivité)<br/>
[3.8. Interopérabilité](#38interopérabilité)<br/>
[3.9. Respect de l'environnement](#39respect-de-lenvironnement)<br/>
[3.10. Accessibilité](#310accessibilité)<br/>
[Annexe : « Déclaration d'applicabilité »](#annexe---déclaration-dapplicabilité-)<br/>

## Contributeurs
**Matthieu GRALL**, expert-conseil en management des données, sécurité de l’information, protection de la vie privée et nouvelles technologies

**Cécile LAMARQUE**, sociologue

## Versions
| <center>**Version**</center> | <center>**Action**</center> | <center>**Éditeur**</center> | <center>**État**</center> | 
| --- | --- | --- | --- | 
| 06/04/2025 (v0.1) | Création du document | Matthieu GRALL | Document de travail |
| 10/04/2025 (v0.2) | Rédaction de l’introduction, réorganisation et harmonisation des bonnes pratiques, ajout de l’annexe, corrections mineures (reformulations, mises en cohérences) | Matthieu GRALL | Document de travail |
| 30/04/2025 (v0.3) | Transformation du document en _markdown_ | Cécile LAMARQUE | Document de travail |
| 07/05/2025 (v0.4) | Harmonisation du document avec les autres | Matthieu GRALL | Document de travail |
| 07/05/2025 (v1.0) | Finalisation d'une première version complète, cohérente, et en _markdown_ | Matthieu GRALL | Amélioration continue |

## Document de référence
Les références suivantes sont utilisées entre crochets dans le corps du document :
| <center>Libellé court</center> | <center>Libellé long</center> |
| --- | --- |
| [EN 301 549] | Exigences d’accessibilité pour les produits et services ICT, _European Telecommunications Standards Institute_ (ETSI, 2018)<br/>[Lien](https://accessibilite.numerique.gouv.fr/doc/fr_301549v020102p.pdf) |
| [Guide d'hygiène de l'ANSSI] | Guide d’hygiène informatique, Agence nationale de la sécurité des systèmes d’information (ANSSI, 2017)<br/>[Lien](https://cyber.gouv.fr/sites/default/files/2017/01/guide_hygiene_informatique_anssi.pdf) |
| [Guide sécurité de la CNIL] | Sécurité des données personnelles, Commission nationale de l’informatique et des libertés (CNIL, 2024)<br/>[Lien](https://www.cnil.fr/sites/cnil/files/2024-03/cnil_guide_securite_personnelle_2024.pdf) |
| [ISO/IEC 27002] | Sécurité de l'information, cybersécurité et protection de la vie privée — Mesures de sécurité de l'information, _International Organization for Standardization_ (ISO, 2022)<br/>[Lien](https://www.iso.org/fr/standard/75652.html) |
| [ISO/IEC 42001] | Technologies de l’information – Intelligence artificielle – Système de management, _International Organization for Standardization_ (ISO, 2023)<br/>[Lien](https://www.iso.org/fr/standard/81230.html) |
| [Lignes directrices IA de l'UE] | Communication de la Commission au Parlement européen, au Conseil, au Comité économique et social européen et au Comité des régions – Renforcer la confiance dans l'intelligence artificielle axée sur le facteur humain COM(2019) 168 final (2019)<br/>[Lien](https://eur-lex.europa.eu/legal-content/FR/TXT/PDF/?uri=CELEX:52019DC0168) |
| [Loi I&L] | Loi n°78-17 du 6 janvier 1978 relative à l’informatique, aux fichiers et libertés, modifiée<br/>[Lien](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000886460/) |
| [Recommandations IA de l'ANSSI - 2024] | Recommandations de sécurité pour un système d’IA générative, Agence nationale de la sécurité des systèmes d’information (ANSSI, 2024)<br/>[Lien](https://cyber.gouv.fr/sites/default/files/document/Recommandations_de_s%C3%A9curit%C3%A9_pour_un_syst%C3%A8me_d_IA_g%C3%A9n%C3%A9rative.pdf) |
| [Recommandations IA de l'ANSSI - 2025] | Développer la confiance dans l’IA par une approche par les risques cyber (ANSSI, 2025)<br/>[Lien](https://cyber.gouv.fr/sites/default/files/document/analyse_commune_haut_niveau_des_risques_cyber_ia.pdf) |
| [Recommandations IA de la CNIL] | Recommandations sur le développement des systèmes d’intelligence artificielle, Commission nationale de l’informatique et des libertés (CNIL, 2024)<br/>[Lien](https://www.cnil.fr/fr/les-fiches-pratiques-ia) |
| [Règlement IA] | Règlement (UE) 2024/1689 du Parlement européen et du Conseil du 13 juin 2024 établissant des règles harmonisées concernant l’intelligence artificielle […] (règlement sur l’intelligence artificielle, 2024)<br/>[Lien](https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX:32024R1689) |
| [RGAA] | Référentiel général d’amélioration de l’accessibilité (RGAA), Direction interministérielle du numérique (DINUM, 2023)<br/>[Lien](https://accessibilite.numerique.gouv.fr/doc/RGAA-v4.1.2.pdf) |
| [RGESN] | Référentiel général d’écoconception de services numériques (RGESN), Autorité de régulation de la communication audiovisuelle et numérique (ARCOM, 2024)<br/>[Lien](https://ecoresponsable.numerique.gouv.fr/docs/2024/rgesn-mai2024/referentiel_general_ecoconception_des_services_numeriques_version_2024.pdf) |
| [RGI] | Référentiel général d’interopérabilité (RGI), Direction interministérielle du numérique (DINUM, 2020)<br/>[Lien](https://cellar-c2.services.clever-cloud.com/storage-demo/numerique-gouv-website/documents/Referentiel_General_Interoperabilite_V2.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=ZWM9OJBMLHVWM86C0Y2S%2F20250430%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20250430T125123Z&X-Amz-Expires=3600&X-Amz-SignedHeaders=host&X-Amz-Signature=9b72dabec2c535c569bfc6a1e30b1c55cb1b0d002e98f68b88e1814b61e9d3ff) |
| [RGIAF] | Référentiel général pour l’IA frugale (RGIAF), ministère de la transition écologique et de la cohésion des territoires (2024)<br/>[Lien](https://greentechinnovation.fr/storage/2024/06/Referentiel-general-pour-lIA-frugale.pdf) |
| [RGPD] | Règlement (UE) 2016/679 du Parlement européen et du Conseil du 27 avril 2016, relatif à la protection des personnes physiques à l’égard du traitement des données à caractère personnel et à la libre circulation de ces données<br/>[Lien](https://eur-lex.europa.eu/eli/reg/2016/679/oj?locale=fr) |
| [US EO 13960] | _Promoting the Use of Trustworthy Artificial Intelligence in the Federal Government_, _Executive Order 13960_ (2020)<br/>[Lien](https://trumpwhitehouse.archives.gov/presidential-actions/executive-order-promoting-use-trustworthy-artificial-intelligence-federal-government/) |
| [WCAG] | Règles pour l’accessibilité des contenus Web (_Web Content Accessibility Guidelines_ - WCAG), _World Wide Web Consortium_ (W3C, 2023)<br/>[Lien](https://www.w3.org/WAI/standards-guidelines/wcag/fr) |

## 1. Objet du document
**Ce document propose une liste de bonnes pratiques qui permettent de respecter les critères de confiance que tout système d’intelligence artificielle (IA) devrait respecter**.

Il s’inscrit dans un ensemble de documents méthodologiques en amélioration continue, destinés à aider les organismes à gérer les risques liés à l’IA, et qui peuvent être utiles ensemble ou séparément :
1. [Exemples de micro-cas d'usages de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Micro-cas%20d'usages%20-%20Exemples.md) ;
2. [Critères de confiance de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Crit%C3%A8res%20de%20confiance.md) ;
3. [Bonnes pratiques de l'IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Bonnes%20pratiques.md) ;
4. [Méthode de gestion des risques de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20M%C3%A9thode.md).

Il peut être directement utilisé dans le cadre des projets de nouveaux services qui reposent sur l’IA pour comparer ce qui est prévu ou mis en œuvre aux bonnes pratiques, et peut également être intégré à une démarche de gestion des risques.

## 2. Introduction
La multiplicité des documents de référence, spécifiques à l’IA<sup><a href="#note1" id="ref1">[1]</a></sup>  ou applicables à tous les systèmes<sup><a href="#note2" id="ref2">[2]</a></sup>, apporte de la confusion chez ceux qui doivent ou souhaitent les appliquer.

Ils peuvent en effet sembler :
-	**chacun incomplet**, car leurs périmètres diffèrent (par domaines comme la sécurité de l’information ou la protection des droits et libertés, par techniques d’IA comme les LLM<sup><a href="#note3" id="ref3">[3]</a></sup> , par phases comme le développement, etc.). Ceci est notamment dû au fait que les problématiques liées à l’IA imposent une vision globale, alors que les périmètres de compétences et spécialités des organismes émetteurs sont restreints ;

-	**tous incohérents**, car leurs structures, bonnes pratiques et terminologies diffèrent, mêmes si elles ont des similarités, et que les normes internationales<sup><a href="#note4" id="ref4">[4]</a></sup>  ne sont pas encore matures.

Or, quand on veut mettre en œuvre un système basé sur l’IA, on doit ou on souhaite **respecter l’ensemble des références applicables, et ce, de manière cohérente !**

Ainsi, ce document **propose des bonnes pratiques harmonisées**, organisées selon les [Critères de confiance de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Crit%C3%A8res%20de%20confiance.md), qui considèrent les différents [Exemples de micro-cas d'usages de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20Micro-cas%20d'usages%20-%20Exemples.md), et qui peuvent être utilisées dans le cadre de la [Méthode de gestion des risques de l’IA](https://github.com/matthieu-grall/ai/blob/main/IA%20-%20Gestion%20des%20risques%20-%20M%C3%A9thode.md).

L'[Annexe : « Déclaration d'applicabilité »](#annexe---déclaration-dapplicabilité-) peut être utilisé pour présenter les pratiques mises en œuvre en comparaison aux bonnes pratiques.

Note : un renvoi vers les documents de référence est privilégié quand cela est opportun.

## 3. Bonnes pratiques pour l'IA
### 3.1. Gouvernance responsable
<ins>Objectif</ins> : instaurer un cadre de gouvernance qui permet de partager et contrôler l’éthique des processus mis en œuvre dans les projets qui reposent sur l’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE], [ISO/IEC 42001].

**BP01.	Formaliser les responsabilités des parties intéressées**

Identifier les parties intéressées (usagers, organisations, développeurs d'IA, fournisseurs d'IA, fournisseurs de données, formateurs, institutions, etc.) et formaliser leurs responsabilités dans le cadre de l’ensemble du cycle de vie des systèmes d’IA.

**BP02.	Partager les valeurs éthiques**
Impliquer, voire former, les parties intéressées pour assurer que les technologies liées à l'IA sont produites et utilisées conformément à des valeurs éthiques, en surveillant les préjugés, la confidentialité et les abus, tout en promouvant l'innovation et la confiance.

**BP03.	Déterminer des mécanismes de contrôle**
Trouver et mettre en œuvre le(s) moyen(s) le(s) plus efficace(s), c’est-à-dire cohérent(s) avec la taille, la maturité et les processus existants de l’organisme, pour vérifier régulièrement que l’éthique est effectivement considérée dans les projets qui reposent sur de l’IA (ex : reporting, revue annuelle, indicateurs basés sur des objectifs prédéfinis, audits, rapports de gouvernance, comité d’éthique).

### 3.2. Fiabilité et sûreté
<ins>Objectif</ins> : assurer la robustesse des systèmes qui reposent sur l’IA afin d’améliorer leur fiabilité et la sécurité des biens et des personnes.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE].

**BP04.	Vérifier les données d’entrée possibles**

Vérifier les particularités des données futures, par exemple à l’aide de modules spécifiques dans la chaine de traitements de données.

**BP05.	Vérifier la robustesse du modèle**

Vérifier que le modèle ne peut pas être attaqué pour produire un résultat indésirable, par exemple dans le cadre d’une chaine de modèles.

**BP06.	Éprouver les limites du système dans sa globalité**

Mettre en place des mesures pour éprouver et consolider le système d’IA (ex : tests de charge et de stress, simulations d’attaques, redondances techniques, procédures de réponse aux incidents) en considérant l’amont et l’aval du système d’IA.

**BP07.	Évaluer les performances du système**

Faire des mesures quantitatives pour évaluer les performances du modèle dans diverses conditions de stress, notamment les attaques contradictoires, le bruit et les changements de distribution des données (ex : taux de faux positifs/négatifs, étude de l’erreur quadratique moyenne – MSE, distance de Wasserstein, score de Brier).

**BP08.	Mettre en place les mesures de sûreté nécessaires**

Tester et valider le système d’IA pour répondre aux normes de sûreté et aux exigences réglementaires dans les applications où la sûreté est primordiale (ex : véhicules autonomes, soins de santé), intégrer plusieurs mesures redondantes pour gérer les pannes sans causer de dommages ni de perturbations significatives, laisser la main à l’humain, en particulier dans le cadre de prises de décisions critiques, pour intervenir, outrepasser ou guider les actions de l'IA si nécessaire.

### 3.3. Équité
<ins>Objectif</ins> : détecter et corriger les biais par des mécanismes de vérification et d’audit des algorithmes.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Recommandations IA de la CNIL].

#### 3.3.1. Réduction des biais liés à la formulation du cas d'usage

**BP09.	Définir clairement le(s) cas d’usage(s)**

Décrire précisément le cas d’usage, les limitations et les exceptions, et s’assurer que les personnes en charge de la conception et du développement des outils en ont connaissance et les comprennent.

#### 3.3.2. Réduction des biais liés aux données d'entrée

**BP10.	Diversifier les données d’entrée**

Utiliser des sources de données diverses et représentatives.

**BP11.	Rendre les données exploitables**

Limiter les données qu’à celles qui seront traitées, les transformer / intégrer de façon cohérente (ex : via une ontologie qui sert de pivot), et les nettoyer de manière approfondie, afin de faciliter leur traitement, de ne pas traiter de données inutilisables, inutiles, sujettes à des règles internes ou externes, ou qu’on ne souhaite pas traiter.

#### 3.3.3. Réduction des biais liés aux données d'entrainement

**BP12.	S’assurer de la qualité des données d’entrainement**

Vérifier la pertinence des données par rapport au problème à résoudre, leur fiabilité (crédibles et/ou de sources objectives), et la légalité de leur collecte et de leur traitement.

**BP13.	Faire des échantillonnages équilibrés des données d’entrainement**

Respecter les bonnes pratiques d’échantillonnage pour que les échantillons soient équilibrés.

**BP14.	Corriger les corrélations indésirables**

Identifier les corrélations entre les caractéristiques ou les variables, évaluer leur impact et gérer ceux qui ne sont pas acceptables.

**BP15.	Collecter de nouvelles données dès que cela est nécessaire**

Recourir à de nouvelles données d’entrée jusqu’à avoir l’assurance que les biais sont suffisamment réduits.

#### 3.3.4. Réduction des biais liés à l'agorithme d'entrainement / Architecture du modèle

**BP16.	Évaluer la qualité du modèle**

Mesurer l'équité à l’aide de modèles mathématiques, comme l'indépendance statistique, les intervalles de confiance, l'étude de séparation et l'étude de suffisance.

**BP17.	Évaluer les performances du modèle**

Évaluer les performances de l'algorithme de manière régulière.

**BP18.	Faire auditer le modèle**

Réaliser un audit pour identifier et corriger les biais.

#### 3.3.5. Réduction des biais liés aux données de sortie

**BP19.	Valider les données de sorties**

Valider les résultats produits, si possible de manière continue, voire consulter des experts en éthique et inclusion.

**BP20.	Obtenir les retours des usagers**

Collecter régulièrement les commentaires et retours d'expérience des usagers, pour détecter et corriger les biais dans les résultats.

### 3.4. Transparence

<ins> Objectif </ins> : rendre explicites les algorithmes et les processus de décision via une documentation accessible, des interfaces interactives et des explications techniques adaptées aux différents publics.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [Lignes directrices IA de l'UE].

**BP21.	Formaliser les éléments utiles à la transparence**

Élaborer les explications<sup><a href="#note5" id="ref5">[5]</a></sup>,  nécessaires à la transparence<sup><a href="#note6" id="ref6">[6]</a></sup>, notamment pour expliquer d’où les données proviennent les données, la forme qu’elles prennent et leur utilisation par l’organisme, et les faire connaître<sup><a href="#note7" id="ref7">[7]</a></sup>  aux personnes chargées de créer et de maintenir les modèles et les flux de données, aux usagers, et aux autorités compétentes.

### 3.5. Sécurité des informations
<ins>Objectif</ins> : appliquer les bonnes pratiques de sécurité de l’information au système d’IA, pour réduire les risques sur l’organisme en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données, tout le long du cycle de vie du système.

<ins>Principale(s) référence(s)</ins> : [Recommandations IA de l'ANSSI - 2024], [Recommandations IA de l'ANSSI - 2025].

**BP22.	Respecter les recommandations de l’ANSSI**

Appliquer les [Recommandations IA de l'ANSSI - 2024] (chapitre 5) applicables dans le cas d’un système d’IA générative et les [Recommandations IA de l'ANSSI - 2025] (annexe I).

**BP23.	Adopter des bonnes pratiques de sécurité de l’information**

Appliquer la politique de sécurité des systèmes d’information, ou les bonnes pratiques de sécurité de l’information applicables selon la maturité de l’organisme en la matière (ex : [Guide sécurité de la CNIL], [Guide d'hygiène de l'ANSSI], [ISO/IEC 27002]).

### 3.6. Protection des droits et libertés
<ins>Objectif</ins> : appliquer les grands principes de la protection de la vie privée au traitement de données par IA, pour réduire les risques sur les personnes concernées en cas de disparition de données, de modification non désirée de données ou d’accès non autorisé à des données.

<ins>Principale(s) référence(s)</ins> : [Recommandations IA de la CNIL], [Loi I&L], [RGPD].

**BP24.	Respecter les recommandations de la CNIL**

Appliquer les [Recommandations IA de la CNIL] applicables dans le cas d’une phase de développement.

**BP25.	Mettre le traitement en conformité avec la réglementation**

Formaliser les éléments nécessaires<sup><a href="#note8" id="ref8">[8]</a></sup>  à la personne / au service en charge de la protection de la vie privée pour bâtir la conformité du traitement de données à caractère personnel à la [Loi I&L] / au [RGPD].

### 3.7. Maintenabilité et évolutivité
<ins>Objectif</ins> : assurer performances, maintien en conditions opérationnelle et de sécurité, intégration de nouvelles fonctionnalités, et comptabilité ascendante, tout le long du cycle de vie du système d’IA.

<ins>Principale(s) référence(s)</ins> : [Règlement IA], [ISO/IEC 42001].

**BP26.	Adopter un principe de modularité et de réutilisabilité**

Mettre en œuvre une conception modulaire du système d'IA, pour réutiliser/remplacer les composants de la chaîne sans affecter l'ensemble du système.

**BP27.	Documenter le système**

Élaborer une documentation complète, qui comprend des commentaires sur le code, des manuels d'utilisation et une documentation sur le prétraitement des données, la formation des modèles et les processus de déploiement.

**BP28.	Contrôler la qualité du code**

Appliquer les bonnes pratiques de développement pour produire un code de haute qualité, notamment des conventions de nommage appropriées, un style cohérent et des algorithmes efficaces.

**BP29.	Permettre l’évolutivité**

Concevoir le système pour gérer des charges accrues et évoluer selon les besoins. Ceci implique également le maintien des performances et la gestion des ressources.

**BP30.	Maîtriser les évolutions**

Mettre en œuvre un processus de gestion des évolutions, qui intègre la veille technologique, les tests de comptabilité ascendante, l’automatisation des correctifs et mises à jour, le contrôle des versions<sup><a href="#note9" id="ref9">[9]</a></sup> , et la surveillance des performances.

### 3.8. Interopérabilité
<ins>Objectif</ins> : assurer l’interopérabilité fluide des données et des technologies sur lesquelles elles reposent.

<ins>Principale(s) référence(s)</ins> : [RGI].

**BP31.	Assurer la comptabilité des données**

Identifier les sources de données, les données consommées, les traitements de données effectués et les données produites, vérifier que ces données sont référencées (ex : dans une ontologie pivot) pour faciliter leur interopérabilité et leur réutilisation.

**BP32.	Adopter des bonnes pratiques d’interopérabilité**

Appliquer les bonnes pratiques applicables du [RGI] et, le cas échéant, vérifier la conformité aux outils autorisés en interne pour favoriser l’interopérabilité des technologies<sup><a href="#note10" id="ref10">[10]</a></sup>.

### 3.9. Respect de l’environnement
<ins>Objectif</ins> : réduire globalement les besoins en ressources matérielles et énergétiques et les impacts environnementaux associés.

<ins>Principale(s) référence(s)</ins> : [RGESN], [RGIAF].

**BP33.	Adopter des bonnes pratiques d’écoconception**

Identifier la consommation d'énergie des centres de données (_data centers_) lors de l’entrainement des modèles, l'économie circulaire du matériel, l'empreinte carbone, l'obsolescence et les déchets électroniques, et appliquer les bonnes pratiques applicables du [RGESN] ou du [RGIAF].

### 3.10. Accessibilité
<ins>Objectif</ins> : intégrer les principes d’accessibilité numérique dès la conception et tester régulièrement l’interface pour garantir une utilisation inclusive.

<ins>Principale(s) référence(s)</ins> : [RGAA], [EN 301 549], [WCAG].

**BP34.	Adopter des bonnes pratiques d’accessibilité**

Se conformer au [RGAA] en appliquant les bonnes pratiques applicables de l’[EN 301 549] ou des [WCAG]<sup><a href="#note11" id="ref11">[11]</a></sup>, en visant l'accessibilité et l'autonomisation des usagers, pour favoriser une expérience d'IA positive et inclusive pour tous les usagers.

## Annexe : « Déclaration d'applicabilité »
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

### Sécurité des informations
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
<a name="note1" id="note1">[1]</a> Notamment [ISO/IEC 42001], [Recommandation IA de l'OCDE], [Recommandations IA de l'ANSSI - 2024], [Recommandations IA de l'ANSSI - 2025], [Recommandations IA de la CNIL], [Règlement IA] et [RGIAF]. [↩](#ref1)
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
