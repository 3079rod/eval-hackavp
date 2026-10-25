# HackAVP — Justifications de la notation de Christophe Roger

**Version du 26 octobre 2026 — 11 projets, 22 critères par projet, notation sur 100.**

Ce document accompagne `christophe-roger_grille_hackavp_notation.csv`. Il présente l’évaluation conduite par Christophe Roger avec une assistance IA. Chaque projet comporte une appréciation d’ensemble, les notes par critère et les références qui permettent de les relire. Les commentaires et les notes globales correspondent au CSV.

J’ai utilisé une assistance IA pour maintenir la cohérence des critères et des choix de notation, ainsi que pour générer et contrôler les livrables. Les choix de notation et les arbitrages sont les miens.

## Comment les notes ont été établies

J’ai lu directement tous les articles et regardé toutes les vidéos. Les retranscriptions ont servi d’appui au travail préparatoire avec l’IA. Les pièces remises examinées complètent cette lecture. Aucun test indépendant des services ni nouveau complément demandé aux équipes ne vient s’ajouter au rendu.

Chaque projet est apprécié pour ce qu’il apporte lui-même. Un contrat ou une architecture bien expliqué peut justifier des points sans exiger une démonstration de toute la chaîne collective. Les résultats d’une autre équipe ne lui sont pas attribués. La restitution et l’effet sur la décision peuvent concerner le candidat, le recruteur ou le pilotage RH, selon le projet.

Les 22 critères sont tous notés. Lorsque le rendu ne donne aucun élément permettant des points, la note est zéro ; une note partielle reconnaît les éléments effectivement décrits ou montrés. Le bonus d’interaction est compris dans le barème sur 100, sans renormalisation. Les profils JSON Resume et Europass de CV FORGE sont reconnus comme des documents structurés.

Les tracks déclarées sont conservées. Une localisation non établie n’est pas assimilée à une exécution hors Nouvelle-Calédonie. Les dates de modification signalées ci-dessous sont celles relevées lors de la revue des sources : elles ne constituent pas une archive du contenu présent à la clôture du 21 octobre.

Cadre : [présentation du hackathon](https://dev.to/adriens/hackavp-premier-hackathon-dedie-a-lemploi-dans-la-fonction-publique-en-ncl-3oj0), [guide du jury et liste des soumissions](https://dev.to/adriens/hackavp-guide-devaluation-pour-les-membres-du-jury-12i0), [dépôt d’évaluation](https://github.com/adriens/eval-hackavp).

## Notes finales

L’ordre suit celui de la grille ; ce tableau n’est pas un classement.

| N° | Projet | Socle /40 | Technicité /25 | Valeur RH /25 | Track /10 | Total /100 |
| ---: | --- | ---: | ---: | ---: | ---: | ---: |
| 1 | CV Generator | 32,5 | 18 | 12 | 4,5 | **67** |
| 2 | Insight Squad | 29 | 14 | 8 | 3,5 | **54,5** |
| 3 | JOBMATCH NC | 31 | 16,5 | 4 | 3,5 | **55** |
| 4 | AVPRO | 35,5 | 18,5 | 13,5 | 8 | **75,5** |
| 5 | Adopte un Job | 36,5 | 18,5 | 15 | 9 | **79** |
| 6 | CV FORGE | 29,5 | 18,5 | 7 | 4 | **59** |
| 7 | CV-Matching | 34 | 20 | 14,5 | 10 | **78,5** |
| 8 | OPT + | 11 | 4 | 1 | 2,5 | **18,5** |
| 9 | Veille CDO (RSS + Claude) | 26 | 13 | 21 | 6,5 | **66,5** |
| 10 | Mapping AVP–ESCO | 32 | 19 | 7 | 8,5 | **66,5** |
| 11 | HACKAVPI | 30,5 | 19 | 4,5 | 4 | **58** |

## 1. CV Generator — 67/100

**Soumission :** CV Generator. **Auteur indiqué dans la grille :** Quoc-Kim BUI. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** Génération documentaire, composant MS4 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) · [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE) · [Pièces remises](https://drive.google.com/drive/folders/1X-YqC9b_xPNxvZQBHAPo7j6FlnyzJaEn).

### Appréciation d’ensemble

La solution permet de produire un CV à partir d’un profil et d’une offre, avec un traitement local et une API bien documentée. C’est un résultat utile et facile à réutiliser. Les documents examinés contiennent toutefois des ajouts non étayés par le profil fourni : le CV mentionne du suivi de projets et la lettre une capacité à animer des groupes de travail. Le guide considère aussi que le candidat n’a pas le permis B, alors que cette information est simplement absente du profil. Ces erreurs expliquent la réserve sur la fiabilité des documents et limitent la note globale.

### Socle commun — 32,5/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **2,5/4** | L’aperçu des documents est lisible et l’interface va à l’essentiel. La présentation reste assez classique pour un générateur de CV. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=208s) — 3:28–3:35 |
| UX & utilisabilité | **3,5/5** | Le dépôt, le choix de l’offre, la génération et l’aperçu s’enchaînent simplement. Le profil JSON Resume et la clé API demandent davantage d’aisance technique. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=157s) — 2:37–3:58 |
| Accessibilité | **1/4** | Les exports bureautiques sont pratiques à lire. Le rendu donne peu d’informations sur l’usage au clavier, les lecteurs d’écran et les contrastes de l’interface. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Parcours utilisateur |
| Adéquation moyens / résultats | **4,5/5** | Le traitement local sert bien l’objectif de confidentialité. Les composants existants, l’API et les exports suffisent à fournir le parcours montré ; le temps de traitement et les besoins matériels sont moins précisément mesurés. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Souveraineté ; Qualité, tests et déploiement |
| Standards & Open Data | **6/6** | JSON Resume et les échanges structurés donnent une base solide aux entrées et aux sorties. Les exports facilitent leur réutilisation. Les erreurs de contenu sont examinées dans la qualité des documents. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Données ouvertes ; Architecture |
| Storytelling | **3,5/4** | Le besoin, l’architecture et le parcours se comprennent facilement. La démonstration produit le CV, mais ne montre pas la génération de la lettre et du guide également annoncés. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=41s) — 0:41–1:18 ; 2:37–3:48 |
| Réutilisabilité & essaimage | **4/4** | L’API documentée, la séparation des services et les conteneurs donnent de bons moyens de reprendre la solution dans un autre contexte. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Qualité, tests et déploiement ; dépôt lié |
| Plaisir de lecture | **4/4** | Le parcours de Camille et l’analogie de la quête rendent l’article agréable. Les explications de code, de prompts et d’architecture enrichissent la lecture pour un développeur. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Un lagon d'offres ; parcours de Camille ; Architecture |
| Plaisir de visionnage | **3,5/4** | Le propos suit quatre étapes claires et mène à la génération puis à l’aperçu du CV. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=17s) — 0:17–0:40 ; 2:37–3:48 |

### Technicité — 18/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **6/8** | Le profil et l’offre alimentent les prompts de manière cohérente. Le CV reprend les principaux faits du JSON, mais ajoute du suivi de projets que la source n’établit pas. | [Pièces remises](https://drive.google.com/drive/folders/1X-YqC9b_xPNxvZQBHAPo7j6FlnyzJaEn) — JSON source et CV PDF, une page ; contrôle du 24 octobre |
| Intégrabilité | **8/8** | L’API REST et l’entrée JSON Resume sont bien documentées. Les formats de sortie et la séparation du service offrent des points de raccordement clairs. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=138s) — 2:18–2:35 |
| Maintenabilité | **4/5** | Les tests pytest, Ruff, la CI, les versions et le worker séparé témoignent d’une démarche de maintenance structurée. Le rendu décrit ces moyens ; leur exécution n’a pas été contrôlée. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Qualité, tests et déploiement |
| Interaction inédite (bonus) | **0/4** | Le parcours utilise une interface web et des documents classiques. Aucun usage de voix, d’IoT ou d’un autre média ne justifie le bonus. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE) — Vidéo complète |

### Valeur RH — 12/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0/5** | Le service reçoit la référence d’une offre et délègue le rapprochement à CV-Matching. Il ne fournit donc pas ici de résultat de matching qui lui soit propre. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Données ouvertes ; CV-Matching |
| Documents générés | **2/5** | Le CV est bien généré dans la vidéo et a été comparé au JSON. Il conserve les faits principaux, mais ajoute du suivi de projets et supprime les mois. La lettre et le guide remis ont aussi été lus : ils comportent des réserves de fidélité et leur génération n’est pas montrée, comme le demande le guide pour les compter comme productions démontrées. | [Pièces remises](https://drive.google.com/drive/folders/1X-YqC9b_xPNxvZQBHAPo7j6FlnyzJaEn) — JSON et CV PDF ; vidéo 3:05–3:37 |
| Qualité de la restitution | **3,5/5** | Le guide organise bien les forces, les écarts et la préparation à l’entretien. Il considère toutefois le permis B comme manquant alors que le profil ne le renseigne pas, et son appréciation du suivi de projets ne concorde pas avec le CV. | [Pièces remises](https://drive.google.com/drive/folders/1X-YqC9b_xPNxvZQBHAPo7j6FlnyzJaEn) — Guide de préparation à l'entretien, pages 1 à 3 ; JSON et CV PDF |
| Facilité de création | **3,5/5** | Un profil et une référence d’offre suffisent à produire le CV. Le rendu explique moins bien la création et l’enchaînement des autres pièces. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=168s) — 2:48–3:37 |
| Effet sur la décision | **3/5** | Le CV et la lettre relient le parcours au poste et peuvent aider à examiner la candidature. Le suivi de projets ajouté dans le CV et l’animation de groupes affirmée dans la lettre fragilisent cependant la confiance dans le dossier. | [Pièces remises](https://drive.google.com/drive/folders/1X-YqC9b_xPNxvZQBHAPo7j6FlnyzJaEn) — CV PDF et lettre PDF, une page chacun ; JSON source |

### Track déclarée — 4,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **0/4** | Le traitement local montré concerne la génération de documents. Le rapprochement avec les offres est assuré par une autre brique. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Données ouvertes ; Architecture |
| Frameworks Open Source | **2/2** | llama.cpp, Qwen et les services conteneurisés sont identifiés et donnent une base locale réutilisable. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Le LLM et le prompt ; Qualité, tests et déploiement |
| Cohérence des licences | **1/2** | Les composants sont nommés, mais leurs licences et les obligations de redistribution ne sont pas suffisamment détaillées pour apprécier complètement ce point. | [Article](https://dev.to/spewq/hackavp-cv-generator-la-solution-de-preparation-de-candidature-1p30) — Le LLM et le prompt ; dépôt lié |
| Matériel et installation | **1,5/2** | Docker Compose et Tailscale sont expliqués. La démonstration utilise une RTX 5080 ; le matériel minimal nécessaire est moins précisément établi. | [Vidéo](https://www.youtube.com/watch?v=sNb1rM0gVDE&t=89s) — 1:29–2:16 |

### Points à garder en tête

- Les trois PDF remis ont été lus et comparés au JSON. Le suivi de projets ajouté au CV, l’animation de groupes dans la lettre et le permis B dans le guide sont les réserves concrètes de fidélité.
- Le JSON était affiché comme modifié le 17 octobre et le CV le 14 octobre. Sans historique, leur correspondance exacte à la génération ne peut pas être reconstituée.

## 2. Insight Squad — 54,5/100

**Soumission :** Et si les données du recrutement répondaient à nos questions ?. **Auteur indiqué dans la grille :** Elodie Tran. **Track déclarée :** SaaS no limit.

**Ce qui est évalué :** Pilotage Power BI, composant MS7 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) · [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA).

### Appréciation d’ensemble

Le tableau de bord donne une lecture utile des recrutements et aide à repérer les offres qui méritent davantage d’attention. La distinction entre données réelles et données de test est appréciable. Le résultat convainc surtout comme outil de pilotage ; certains indicateurs demandent encore à être précisés et la manière de reproduire la diffusion est peu expliquée. Les assistants et les alertes restent des pistes pour la suite.

### Socle commun — 29/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **2,5/4** | L’angle des offres qui restent sans candidature est pertinent. La présentation est claire, dans une forme de tableau de bord assez habituelle. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — L'angle mort ; tableau de bord |
| UX & utilisabilité | **3,5/5** | Les vues sur l’activité, les offres et les délais parlent aux utilisateurs RH. Le rendu illustre moins leur utilisation autonome au quotidien. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=80s) — 1:20–2:05 ; 3:56–4:07 |
| Accessibilité | **1/4** | Les indicateurs rendent l’activité plus lisible. Les possibilités d’usage au clavier, avec un lecteur d’écran ou sur mobile sont peu expliquées. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Tableau de bord en action |
| Adéquation moyens / résultats | **4,5/5** | Power BI et l’API permettent d’obtenir un cockpit utile avec un assemblage raisonnable. Les coûts récurrents et les conditions de publication sont moins détaillés. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=192s) — 3:12–3:42 ; 3:56–4:07 |
| Standards & Open Data | **4,5/6** | Les échanges REST et JSON ainsi que les référentiels métiers sont bien identifiés. La manière de récupérer et de réutiliser les sorties du rapport est moins expliquée. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Quels indicateurs ; Deux API |
| Storytelling | **3,5/4** | La progression des mesures vers les actions est claire. L’article distingue honnêtement ce qui existe de ce qui reste envisagé. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=127s) — 2:07–3:10 ; 4:11–4:23 |
| Réutilisabilité & essaimage | **2,5/4** | Une autre source de données pourrait remplacer l’API. La reprise dépend toutefois du modèle retenu et des conditions de publication dans l’environnement Microsoft. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Interopérabilité ; suite logique |
| Plaisir de lecture | **3,5/4** | Le problème, les indicateurs et les actions possibles s’enchaînent bien. La place donnée à l’assistant futur est un peu importante par rapport au cockpit livré. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — L'angle mort ; Quels indicateurs ; La suite logique |
| Plaisir de visionnage | **3,5/4** | Le propos explique clairement la boucle mesure-action et les indicateurs. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=21s) — 0:21–0:54 ; 1:20–2:43 ; 3:56–4:23 |

### Technicité — 14/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **4,5/8** | Les offres, les candidatures et les référentiels servent des indicateurs utiles. Le choix d’écarter un score de matching jugé peu fiable est expliqué. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — D'où viennent les données |
| Intégrabilité | **7/8** | L’API REST, le JSON et l’accès par jeton rendent la source remplaçable. Les paramètres nécessaires pour reprendre le connecteur mériteraient davantage d’explications. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Un cas d'école d'interopérabilité ; Deux API à ne pas confondre |
| Maintenabilité | **2,5/5** | Les corrections des métriques et des dates sont présentées, ce qui aide à comprendre le rapport. Les tests automatisés et la procédure de déploiement restent peu détaillés. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=166s) — 2:46–3:10 |
| Interaction inédite (bonus) | **0/4** | L’assistant conversationnel est encore une perspective. Le tableau de bord ne montre pas, à lui seul, une interaction justifiant ce bonus. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — La suite logique : un assistant |

### Valeur RH — 8/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0/5** | Le score candidat-poste a été écarté faute de données fiables. Les indicateurs de recrutement ne réalisent pas ce rapprochement. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Deux API à ne pas confondre |
| Documents générés | **0/5** | Le cockpit ne produit ni CV, ni lettre, ni préparation à l’entretien. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Notre part : savoir si ça marche |
| Qualité de la restitution | **4/5** | Les vues d’ensemble, les statuts, les comparaisons territoriales et les neuf offres sans candidature rendent le diagnostic utile. L’indicateur « Offres encore ouvertes » apparaît toutefois sans valeur. Les taux demandent aussi une lecture attentive de leurs dénominateurs. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Le tableau de bord en action ; captures et actions |
| Facilité de création | **0/5** | Le rapport ne comporte pas de parcours de création des pièces de candidature. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA) — Vidéo complète |
| Effet sur la décision | **4/5** | Les listes et les comparaisons aident à choisir les offres à relancer et les délais à examiner. Elles décrivent une situation sans en expliquer toutes les causes ; les actions proposées restent donc à apprécier, sans créditer les alertes futures. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Le tableau de bord en action ; captures et actions |

### Track déclarée — 3,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching | **0/4** | Cette soumission ne met pas en œuvre de chaîne de matching. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Deux API à ne pas confondre |
| Qualité de l’architecture | **1,5/2** | Le partage des rôles entre l’API et Power BI est clair. L’architecture de l’assistant relève encore des évolutions envisagées. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Un cas d'école d'interopérabilité |
| Déployabilité IaC | **0,5/2** | L’actualisation quotidienne est annoncée. Le rendu ne montre ni IaC ni procédure permettant de reproduire la diffusion du rapport. | [Vidéo](https://www.youtube.com/watch?v=a3MfiMyH_nA&t=236s) — 3:56–4:23 |
| Pertinence des intégrations | **1,5/2** | L’import des données de l’API dans Power BI est adapté au besoin. Les alertes et l’assistant sont encore futurs et n’ajoutent pas de points. | [Article](https://dev.to/elodie_tran_data/et-si-les-donnees-du-recrutement-repondaient-a-nos-questions--1d5o) — Mesure à l'action ; assistant |

### Points à garder en tête

- L’indicateur « Offres encore ouvertes » apparaît sans valeur dans la capture examinée. Les taux doivent être lus avec leurs périmètres et leurs dénominateurs ; des pourcentages différents ne constituent pas à eux seuls une contradiction.
- Les candidatures et certaines données d’activité sont synthétiques. L’assistant et les alertes sont présentés comme des évolutions.

## 3. JOBMATCH NC — 55/100

**Soumission :** JOBMATCH NC. **Auteur indiqué dans la grille :** Maud Granger. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** Coordination et architecture de l'ensemble collectif.

**Sources :** [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) · [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY).

### Appréciation d’ensemble

Le travail d’organisation est sérieux : les rôles sont clairs et les échanges entre composants sont bien expliqués. On comprend comment l’ensemble doit fonctionner. Le rendu reste cependant plus convaincant sur la coordination que sur l’exécution : le raccordement du générateur est encore présenté comme une étape à venir dans la vidéo. La note récompense ce travail d’organisation, sans lui attribuer les réalisations des autres équipes.

### Socle commun — 31/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **3/4** | Les sept micro-startups, les illustrations et les schémas donnent une identité au travail de coordination. L’ensemble est cohérent, même si la forme reste assez classique. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Sept micro-startups ; Flux ; Coordonner l'ensemble |
| UX & utilisabilité | **3,5/5** | Le résumé, le tableau des rôles et la progression du document aident à comprendre l’organisation. Les supports opérationnels, notamment le Kanban et les décisions, sont moins détaillés pour une reprise immédiate. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — En bref ; Sept micro-startups ; Coordonner l'ensemble |
| Accessibilité | **2,5/4** | Les titres, les listes et le tableau des rôles apportent une lecture textuelle utile. Certaines relations présentées dans les schémas n’ont pas d’équivalent textuel complet clairement établi. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Structure de l'article ; tableau des rôles ; descriptions des schémas |
| Adéquation moyens / résultats | **4,5/5** | Les rôles, les formats communs et le suivi sont organisés avec des moyens cohérents. L’effort est peu chiffré, mais le rendu ne laisse pas apparaître de disproportion. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=164s) — 2:44–3:16 |
| Standards & Open Data | **4,5/6** | JSON Resume, les API et les AVP servent de contrats communs. Les schémas précis et la manière de les versionner sont moins détaillés. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — L'interopérabilité commence par les données |
| Storytelling | **3,5/4** | Les dépendances et les difficultés de coordination sont bien racontées. L’annonce d’un flux complet est toutefois à rapprocher d’une vidéo où le raccordement du générateur reste à venir. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — La logique du MVP |
| Réutilisabilité & essaimage | **3/4** | La répartition des responsabilités et les enseignements sont transférables. Les procédures et les adaptations à prévoir dans un autre contexte restent assez générales. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Sept micro-startups ; au-delà du hackathon |
| Plaisir de lecture | **3,5/4** | L’article aide à comprendre les équipes et leurs difficultés. Les rappels sur la nécessité de faire communiquer les briques deviennent parfois répétitifs. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Sept micro-startups ; Coordonner l'ensemble ; Ce que ce projet m'a appris |
| Plaisir de visionnage | **3/4** | Le récit explique la naissance du collectif et les flux entre modules. Certains passages restent abstraits et répètent le message de coordination. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=42s) — 0:42–1:56 ; 1:58–3:16 ; 3:19–4:45 |

### Technicité — 16,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **6,5/8** | Le rôle des données OPT, du profil structuré et des interfaces est bien posé. Le rendu explique moins les alternatives étudiées et les raisons de les écarter. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=118s) — 1:58–3:04 |
| Intégrabilité | **7/8** | Les responsabilités, les formats et les interfaces facilitent la compréhension des raccordements. Le détail et le versionnement des contrats pourraient être davantage développés. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=164s) — 2:44–3:16 |
| Maintenabilité | **3/5** | Le suivi des dépendances, le Kanban et la documentation donnent des moyens de conserver les décisions. La gestion des changements de contrats est moins expliquée. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Coordonner l'ensemble |
| Interaction inédite (bonus) | **0/4** | La présentation ne montre pas d’interaction média particulière au service du parcours. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY) — Vidéo complète |

### Valeur RH — 4/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **1/5** | Le document décrit les entrées, les sorties et le rôle du matching. Le point récompense cette conception, sans lui attribuer les résultats du moteur d’une autre équipe. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=157s) — 2:37–2:44 |
| Documents générés | **0/5** | Aucun CV, lettre ou guide n’est produit dans les éléments de cette soumission. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=164s) — 2:44–2:54 |
| Qualité de la restitution | **1/5** | La place de la restitution dans le parcours est décrite. Aucun diagnostic individuel propre au projet n’est présenté pour en apprécier davantage la qualité. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Composants ; flux |
| Facilité de création | **1/5** | La circulation des données pour préparer les pièces est expliquée. Le point reconnaît cette préparation, mais le rendu ne montre pas de création de documents par ce livrable. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=133s) — 2:13–3:16 |
| Effet sur la décision | **1/5** | Le rôle du recruteur et la circulation du dossier sont pris en compte. L’aide à examiner une candidature reste indirecte et peu illustrée. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=142s) — 2:22–3:04 |

### Track déclarée — 3,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **1/4** | Le schéma décrit les étapes du rapprochement. Il s’agit d’un travail de conception ; aucune exécution de matching propre à ce livrable n’est montrée. | [Vidéo](https://www.youtube.com/watch?v=snGr9dbooWY&t=118s) — 1:58–3:16 |
| Frameworks Open Source | **1,5/2** | Les technologies réutilisables et leurs rôles sont identifiés. L’inventaire des frameworks propres au travail de coordination reste moins précis. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Sept micro-startups |
| Cohérence des licences | **0/2** | Les licences applicables au livrable ne sont pas documentées de façon à attribuer des points. Ce zéro ne signifie pas qu’une incompatibilité a été démontrée. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Architecture collective |
| Matériel et installation | **1/2** | Les principes de répartition des ressources sont expliqués. Les consignes propres de prise en main et d’installation restent succinctes. | [Article](https://dev.to/maud_granger_nc/jobmatch-nc-quand-linteroperabilite-devient-plus-quun-defi-technique-1ma) — Flux ; logique du MVP |

### Points à garder en tête

- L’article annonce un flux complet alors que la vidéo envisage encore le raccordement du générateur. Cette différence reste signalée, sans attribuer au livrable de coordination les défauts ou les résultats des autres projets.
- Le document est évalué pour ses rôles, ses contrats et ses supports de suivi. Les quelques points RH reconnaissent la conception décrite, pas une exécution empruntée aux autres soumissions.

## 4. AVPRO — 75,5/100

**Soumission :** AVPRO. **Auteur indiqué dans la grille :** Luca BEROULE. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** Interface recruteur MS6 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) · [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM).

### Appréciation d’ensemble

Une démonstration convaincante, avec un parcours recruteur clair et des explications qui aident à comprendre les scores et à examiner les candidatures. L’article est agréable à lire, y compris dans ses détails techniques. Les données fictives permettent de comprendre le fonctionnement, mais donnent moins de recul sur la pertinence des rapprochements. L’ensemble mérite une bonne note pour la qualité de l’expérience proposée.

### Socle commun — 35,5/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **3/4** | La symétrie entre candidat et recruteur et le panneau de preuves donnent une présentation cohérente. Le swipe reprend un usage déjà familier. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM&t=64s) — 1:04–1:17 |
| UX & utilisabilité | **5/5** | Les filtres avec compteurs, les preuves, la confirmation, l’annulation temporaire et le suivi d’entretien rendent le parcours clair et maîtrisable. Le panier intermédiaire évoqué pendant la revue reste une préférence personnelle. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM&t=81s) — 1:21–2:07 |
| Accessibilité | **2/4** | L’adaptation aux écrans et les boutons alternatifs au swipe sont expliqués. Le clavier et les lecteurs d’écran font l’objet de moins de précisions. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Responsive ; parcours recruteur |
| Adéquation moyens / résultats | **4,5/5** | Le front statique et l’adaptateur API suffisent aux fonctions montrées et évitent des composants supplémentaires. Les gains en temps et en ressources sont moins quantifiés. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Sous le capot ; Et ensuite |
| Standards & Open Data | **6/6** | JSON Resume, les échanges API et les référentiels donnent des formats clairs aux données. Les offres fictives de la démonstration ne remettent pas en cause ce travail sur les standards. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Formats de CV ; routes ; adaptation API |
| Storytelling | **4/4** | Le problème recruteur, les étapes et les arbitrages sont exposés avec des exemples précis. Le récit permet de comprendre les choix. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Nos arbitrages ; parcours |
| Réutilisabilité & essaimage | **3,5/4** | Le front statique et l’adaptateur centralisé facilitent la reprise. La procédure d’adaptation à un autre contexte est un peu moins développée. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Un seul fichier ; Et ensuite |
| Plaisir de lecture | **4/4** | Le parcours, les arbitrages et les extraits de code rendent l’article concret et agréable. Les détails techniques participent ici au plaisir de lecture. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Parcours recruteur ; Sous le capot ; Nos arbitrages |
| Plaisir de visionnage | **3,5/4** | La présentation suit un ordre clair : connexion, compréhension du score, décision puis entretien. La fin est assez dense techniquement. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM&t=55s) — 0:55–2:22 ; 2:26–3:25 |

### Technicité — 18,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **7/8** | Les données de candidature, le service de matching et la minimisation des informations transmises ont un rôle clair. L’adaptateur centralisé convient bien au besoin de l’interface. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — La démo ; notre place |
| Intégrabilité | **8/8** | Les routes, les types et l’adaptation des formats de CV sont expliqués. L’isolation des appels API donne des contrats de raccordement clairs. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Routes ; CORS et clé d'API |
| Maintenabilité | **3,5/5** | TypeScript, l’adaptateur et le cache limité facilitent l’évolution de l’interface. Les tests automatisés et la gestion des changements sont moins décrits. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Sous le capot |
| Interaction inédite (bonus) | **0/4** | Le swipe et l’interface web ne montrent pas une interaction média suffisamment distincte pour ce bonus. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM) — Vidéo complète |

### Valeur RH — 13,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **3,5/5** | Les compétences et les prérequis rendent les correspondances compréhensibles. Les offres et scores fictifs donnent toutefois moins de recul sur la justesse des rapprochements avec des AVP réels. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM&t=64s) — 1:04–1:17 |
| Documents générés | **0/5** | L’interface ne produit pas de CV ni de lettre de candidature. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM) — Vidéo complète |
| Qualité de la restitution | **5/5** | Les points forts, les éléments à vérifier et les souhaits sont bien séparés. Les preuves par compétence et les prérequis aident à comprendre le score. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Je comprends le score |
| Facilité de création | **0/5** | Le parcours traite les candidatures reçues ; il ne crée pas les pièces du candidat. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Parcours recruteur |
| Effet sur la décision | **5/5** | Les filtres, les preuves et les prérequis aident à comparer les candidatures. La confirmation, l’annulation et le suivi d’entretien rendent ensuite les décisions plus faciles à organiser. | [Vidéo](https://www.youtube.com/watch?v=tjHP83BT0JM&t=94s) — 1:34–2:07 |

### Track déclarée — 8/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **4/4** | L’interface envoie les données utiles au matching et présente les correspondances et leurs preuves. Cette articulation est bien expliquée ; la localisation onPrem reste un point de conformité non établi sur les pièces. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — CORS et clé d'API |
| Frameworks Open Source | **2/2** | React, TypeScript et Vite sont clairement identifiés et le code est référencé. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — La stack |
| Cohérence des licences | **0,5/2** | Les frameworks sont nommés, mais les licences du code et des dépendances sont peu expliquées. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — La stack ; track choisie |
| Matériel et installation | **1,5/2** | Le front statique, Vite et le parcours fonctionnel donnent des éléments de prise en main utiles. La configuration du serveur de production est moins détaillée. | [Article](https://dev.to/sh0ck3r/hackavp-avpro-lespace-recruteur-qui-remplace-la-boite-mail-par-un-swipe-et-explique-chaque-10ph) — Track choisie ; Et ensuite |

### Points à garder en tête

- Les offres et les scores sont fictifs : ils expliquent le fonctionnement de l’interface, mais ne permettent pas de conclure à la justesse des rapprochements réels.
- La track onPrem est conservée. La localisation complète des couches utilisées n’est pas établie par les pièces ; cela ne démontre pas une exécution hors Nouvelle-Calédonie.
- L’article affichait une modification le 22 octobre, après la clôture du 21 octobre. Le contenu exact modifié n’a pas été reconstitué.

## 5. Adopte un Job — 79/100

**Soumission :** Adopte un Job. **Auteur indiqué dans la grille :** Bastian. **Track déclarée :** SaaS no limit.

**Ce qui est évalué :** Interface candidat MS3 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) · [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4).

### Appréciation d’ensemble

Le parcours candidat est particulièrement réussi : on crée son profil, on consulte de vraies offres et on comprend pourquoi elles sont proposées. La conservation du profil et le suivi des candidatures rendent l’ensemble pratique. Quelques réserves demeurent, notamment sur le support Word annoncé différemment selon les sources. La présentation est agréable, mais les mouvements permanents des diapositives finissent par gêner. La génération de documents assurée par une autre brique n’entre pas dans cette note.

### Socle commun — 36,5/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **3,5/4** | Les cartes, le profil et le suivi donnent une identité visuelle cohérente. Le swipe transpose un usage familier au recrutement public. | [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4&t=111s) — 1:51–2:07 |
| UX & utilisabilité | **5/5** | Le formulaire, les questions guidées et le dépôt de CV offrent trois façons de commencer. La relecture, la conservation des saisies et les commandes alternatives au swipe rendent le parcours pratique. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Le parcours, étapes 1 à 5 ; Accessibilité |
| Accessibilité | **3/4** | Les commandes clavier, les libellés pour lecteurs d’écran, les thèmes et la réduction des animations sont décrits. L’auteur précise que l’audit RGAA reste à faire. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Accessibilité ; Et ensuite |
| Adéquation moyens / résultats | **4,5/5** | Le front léger et le relais sans état répondent au besoin sans ajouter de complexité inutile. Le relais corrige une limite CORS précisément identifiée. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot |
| Standards & Open Data | **6/6** | JobPosting, JSON Resume, les métiers OPT-NC et ROME ont des usages explicites. L’export et la réimportation du profil lui donnent une vraie portabilité. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Standards ouverts ; Je crée mon profil ; Sous le capot |
| Storytelling | **3,5/4** | Le parcours et les choix sont expliqués précisément. Une divergence demeure : Word est annoncé dans la vidéo et encore présenté comme une évolution dans l’article. | [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4&t=64s) — 1:04–1:09 |
| Réutilisabilité & essaimage | **4/4** | L’article précise les points à adapter : serveur d’offres, adaptateur API, référentiel et libellés. Le code et une démonstration autonome donnent de bons moyens de reprise. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Réutiliser Adopte un Job ailleurs |
| Plaisir de lecture | **4/4** | Le ton direct, les étapes et les exemples de scores rendent la lecture agréable. Les explications techniques aident à comprendre les choix. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Le parcours ; Sous le capot ; Accessibilité |
| Plaisir de visionnage | **3/4** | La présentation est agréable, mais les mouvements permanents des diapositives donnent l’effet « blob » relevé par le juré et réduisent le confort de visionnage. | [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4&t=40s) — 0:40–1:49 ; 1:51–2:27 |

### Technicité — 18,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **7/8** | Les offres réelles, le référentiel métiers et le service de matching ont chacun une fonction claire dans le parcours. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Contexte ; parcours ; sous le capot |
| Intégrabilité | **8/8** | Le profil exportable, l’adaptateur API et le relais définissent clairement les échanges. Les formats permettent de reprendre le profil ailleurs. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot ; parcours étape 4 |
| Maintenabilité | **3,5/5** | TypeScript strict et l’adaptateur unique évitent de coupler les écrans aux formats des serveurs. Les tests automatisés et la gestion des changements restent moins détaillés. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot |
| Interaction inédite (bonus) | **0/4** | Le swipe ne suffit pas à ouvrir ce bonus. Aucun autre usage de média inédit n’est montré. | [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4) — Vidéo complète |

### Valeur RH — 15/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **4/5** | L’exemple du profil sans compétences radio face à une offre radio donne un résultat faible et cohérent. Les preuves et prérequis aident à l’examiner ; le pourcentage reste une indication, pas une probabilité d’embauche. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Je vois pourquoi une offre me correspond |
| Documents générés | **0/5** | La préparation du profil est montrée, mais aucun CV ciblé, lettre ou guide n’est produit par cette interface. Les documents d’un autre service ne lui sont pas attribués. | [Vidéo](https://www.youtube.com/watch?v=ZGLNDIPJ9z4&t=90s) — 1:30–1:49 |
| Qualité de la restitution | **5/5** | La jauge, les compétences, les preuves et les écarts permettent de comprendre les propositions. Les souhaits ne deviennent pas des exclusions automatiques. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Je vois pourquoi une offre me correspond |
| Facilité de création | **1/5** | Le profil préparé et exportable facilite la constitution d’une candidature. Le rendu ne montre pas la création des pièces documentaires depuis l’interface. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Je prépare ma candidature |
| Effet sur la décision | **5/5** | Les correspondances et les prérequis aident le candidat à choisir une offre. Le contact, l’objet de courriel préparé et les statuts lui permettent ensuite de passer à l’action. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Je prépare ma candidature ; Je candidate, et je suis la réponse |

### Track déclarée — 9/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching | **4/4** | Le profil est associé aux offres réelles, transmis au scoring et accompagné de correspondances lisibles. L’interface remplit bien son rôle dans ce rapprochement. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot ; Je vois pourquoi une offre me correspond |
| Qualité de l’architecture | **2/2** | Le front, le relais sans état et l’adaptateur ont des responsabilités distinctes. Les écrans restent séparés des formats du serveur. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot |
| Déployabilité IaC | **1/2** | L’hébergement PHP et la compilation Vite sont expliqués. Le rendu ne montre pas de déploiement IaC complet. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Sous le capot ; réutiliser ailleurs |
| Pertinence des intégrations | **2/2** | Les échanges avec les offres, l’analyse de profil et le matching s’organisent autour du profil portable et du relais. Ces intégrations servent directement le parcours. | [Article](https://dev.to/c2b/adopte-un-job-on-swipe-les-vrais-postes-de-lopt-nc-et-on-voit-pourquoi-ils-nous-correspondent-48pc) — Projet commun ; parcours étape 4 |

### Points à garder en tête

- Le support Word est annoncé dans la vidéo, alors que l’article le présente encore comme une évolution.
- Les mouvements permanents des diapositives ont été pris en compte dans le plaisir de visionnage, selon l’appréciation directe du juré.

## 6. CV FORGE — 59/100

**Soumission :** CV FORGE. **Auteur indiqué dans la grille :** Florian DOUDOUTE. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** Extraction et structuration de CV MS1 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) · [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw).

### Appréciation d’ensemble

La démonstration montre un résultat concret : transformer un CV en profils JSON Resume et Europass réutilisables, avec une chaîne locale bien expliquée. Ces sorties constituent bien des documents et la vidéo donne des éléments rassurants sur le cas présenté. Les omissions et les hallucinations reconnues appellent toutefois à la prudence. La présentation, assez simple et marquée par des fautes de français, est moins soignée. Le projet reste centré sur l’extraction du profil.

### Socle commun — 29,5/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **2/4** | La transformation du CV en profil portable est utile. La présentation privilégie toutefois le workflow technique plutôt qu’une expérience candidat particulièrement originale. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=54s) — 0:54–2:15 |
| UX & utilisabilité | **3,5/5** | Swagger et le workflow expliquent le dépôt, le traitement et le retour du profil. Ces supports conviennent aux intégrateurs ; une prise en main plus guidée aiderait encore. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=54s) — 0:54–2:15 |
| Accessibilité | **1/4** | Le dépôt réduit la ressaisie. Le rendu apporte peu de précisions sur la navigation au clavier et les lecteurs d’écran. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Le défi ; fonctionnement |
| Adéquation moyens / résultats | **4,5/5** | Le matériel personnel et un modèle léger permettent un traitement local sans API d’IA payante. L’essai de 24 secondes donne un repère concret, sans représenter une moyenne générale. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Pourquoi Qwen ; qualité des données |
| Standards & Open Data | **6/6** | JSON Resume donne un format ouvert au profil, Pydantic en contrôle la structure et Europass offre une autre sortie réutilisable. La conformité de structure ne garantit pas la fidélité des faits. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — JSON Resume ; Europass |
| Storytelling | **3,5/4** | Le récit explique clairement les erreurs rencontrées et les compromis matériels. La démonstration permet de suivre le traitement. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=54s) — 0:54–3:29 |
| Réutilisabilité & essaimage | **3,5/4** | Le contrat JSON Resume et les composants remplaçables facilitent la reprise. Les étapes d’installation et de configuration sont moins détaillées. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Architecture qui peut évoluer |
| Plaisir de lecture | **3,5/4** | Le nom disparu et les compromis matériels rendent le retour d’expérience intéressant. Certains messages, notamment la distinction entre JSON valide et contenu fidèle, reviennent plusieurs fois. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Retour d'expérience ; Qualité des données ; RTX 4060 ou RTX 5080 |
| Plaisir de visionnage | **2/4** | Les fautes de français et la présentation assez simple diminuent le plaisir de visionnage, selon l’appréciation directe du juré. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=54s) — 0:54–3:29 ; 3:36–4:37 |

### Technicité — 18,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **7/8** | L’OCR, Qwen, Pydantic et JSON Resume ont des rôles distincts et cohérents. Le choix du modèle tient compte de la mémoire disponible. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Fonctionnement ; interopérabilité |
| Intégrabilité | **8/8** | Le retour du profil avec le même identifiant, JSON Resume et l’export vers un éditeur rendent les échanges faciles à comprendre et à reprendre. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=40s) — 0:40–0:50 ; 2:12–3:29 |
| Maintenabilité | **3,5/5** | Les étapes séparées et les sorties intermédiaires aident à localiser une perte d’information. Pydantic apporte des contrôles utiles ; les tests de régression et les versions sont moins expliqués. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Qualité des données |
| Interaction inédite (bonus) | **0/4** | Le dépôt et l’OCR constituent une entrée documentaire classique. Aucun usage média particulier ne justifie le bonus. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw) — Vidéo complète |

### Valeur RH — 7/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0/5** | Le service extrait le profil, mais ne le compare pas aux offres. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Chaque application à son niveau |
| Documents générés | **3,5/5** | JSON Resume et Europass sont bien des documents structurés réutilisables. La vidéo étaye la fidélité sur l’exemple présenté, mais les omissions et inventions reconnues limitent la confiance générale. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=144s) — 2:24–3:29 |
| Qualité de la restitution | **0/5** | Le service ne fournit pas d’analyse des forces et des écarts face à un poste. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Fonctionnement |
| Facilité de création | **2/5** | Le profil obtenu peut être relu, corrigé et réutilisé. Les erreurs reconnues et l’absence de pièces ciblées limitent toutefois l’automatisation montrée. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=144s) — 2:24–3:29 |
| Effet sur la décision | **1,5/5** | La remise en forme peut aider à lire le CV. Elle apporte moins d’aide pour apprécier un poste précis, et les erreurs d’extraction appellent une relecture. | [Vidéo](https://www.youtube.com/watch?v=hP2PnFdzvSw&t=185s) — 3:05–3:29 |

### Track déclarée — 4/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **0/4** | Le pipeline local extrait des informations ; il n’effectue pas le matching visé par ce critère. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Fonctionnement |
| Frameworks Open Source | **2/2** | FastAPI, Pydantic et Ollama sont identifiés. L’usage de FastAPI établit bien le recours à un framework Open Source. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Configuration utilisée |
| Cohérence des licences | **0,5/2** | La stack est connue, mais les conditions de licence et de redistribution, notamment celles de n8n, restent peu analysées. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Configuration utilisée |
| Matériel et installation | **1,5/2** | La RTX 4060 de 8 Go et le modèle choisi sont adaptés au traitement présenté. Les consignes de mise en service pourraient être plus détaillées. | [Article](https://dev.to/florian_doudoute/hackavp-cv-forge-lusine-a-cv-boostee-par-ia-locale-4a64) — Configuration utilisée |

### Points à garder en tête

- Un JSON conforme au schéma peut encore contenir une omission ou une invention. La vidéo apporte des éléments sur le cas montré, sans établir un taux de fidélité général.
- Le traitement de 24 secondes correspond à un essai, pas à une moyenne. Les conditions de licence, notamment de n8n, restent peu expliquées.
- L’article affichait une modification le 23 octobre, après la clôture du 21 octobre. Le détail des changements n’est pas reconstitué.

## 7. CV-Matching — 78,5/100

**Soumission :** CV-Matching. **Auteur indiqué dans la grille :** Jo Biden. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** Moteur de matching MS5 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) · [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A).

### Appréciation d’ensemble

Les explications par compétence sont un vrai point fort : elles permettent de comprendre les rapprochements au lieu de se fier uniquement à un score. Le choix des modèles, l’intégration et les possibilités d’exécution locale sont bien expliqués. Les résultats annoncés sont encourageants, mais les petits jeux fictifs et les limites relevées dans les preuves invitent à garder du recul sur leur fiabilité générale. Une proposition solide et bien argumentée.

### Socle commun — 34/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **3/4** | Les preuves par compétence apportent une différence utile. La présentation reste celle d’un service spécialisé de scoring. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — La règle : pas de chiffre sans preuve |
| UX & utilisabilité | **3,5/5** | Le classement et les preuves sont obtenus à partir d’un CV ou d’une offre. JSON Resume et les notions techniques demandent toutefois une certaine aisance. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A&t=106s) — 1:46–2:10 |
| Accessibilité | **1,5/4** | Les preuves textuelles rendent le résultat plus compréhensible. Le rendu explique moins les possibilités d’usage sur mobile et avec des outils d’assistance. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — La règle : pas de chiffre sans preuve |
| Adéquation moyens / résultats | **4,5/5** | Deux modèles spécialisés, un GPU de 4 Go et une possibilité d’exécution sur CPU constituent des moyens adaptés au besoin. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Petit PC, grandes ambitions |
| Standards & Open Data | **6/6** | JSON Resume, JobPosting et ROME sont utilisés de manière explicite. REST, OpenAPI et MCP donnent des formats clairs aux échanges. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Une brique dans JobMatch NC |
| Storytelling | **4/4** | L’analogie des deux enquêteurs et le récit des essais expliquent bien la méthode. L’article distingue le PC, l’installation locale et la vitrine Hugging Face. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Le jour où ; Petit PC |
| Réutilisabilité & essaimage | **4/4** | L’image Docker, les modèles embarqués, l’API et les outils MCP facilitent la reprise. Plusieurs modes d’exécution sont décrits. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Une brique ; Petit PC |
| Plaisir de lecture | **4/4** | L’analogie rend la méthode accessible. Les exemples et les résultats moins favorables rendent le récit concret et crédible. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Le jour où j'ai arrêté de croire mes intuitions ; Petit PC |
| Plaisir de visionnage | **3,5/4** | Le besoin, les deux sens du classement et les limites sont expliqués clairement malgré la densité. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A&t=13s) — 0:13–1:41 ; 1:46–3:03 |

### Technicité — 20/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **8/8** | Embeddings, reranker, rareté des compétences et ROME remplissent des rôles précis. Les données ouvertes sont particulièrement bien exploitées. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Une brique |
| Intégrabilité | **8/8** | OpenAPI, les routes et les outils MCP documentent les entrées et les sorties dans les deux sens du matching. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Table des échanges ; routes principales |
| Maintenabilité | **4/5** | Les versions figées et la séparation des jeux de tests donnent de bons repères pour suivre l’évolution du moteur. Les résultats restent ceux rapportés dans le rendu. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Le jour où ; Petit PC |
| Interaction inédite (bonus) | **0/4** | Le service utilise des API et une interface web classiques. Aucun média inédit ne justifie le bonus. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A) — Vidéo complète |

### Valeur RH — 14,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **4,5/5** | Les preuves, les cas hors sujet et les reformulations donnent des éléments sérieux. Les petits jeux fictifs et les limites du vérificateur empêchent de généraliser les résultats annoncés. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Le jour où j'ai arrêté de croire mes intuitions |
| Documents générés | **0/5** | Le moteur produit des scores et des preuves, sans générer de CV ciblé, de lettre ni de guide d’entretien. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A) — Vidéo complète |
| Qualité de la restitution | **5/5** | Les phrases sources, la couverture des compétences et la séparation des savoir-être permettent d’examiner les correspondances au lieu de s’en tenir à un score. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Et ensuite |
| Facilité de création | **0/5** | Le clic lance une analyse ; il ne produit pas les pièces de candidature visées par ce critère. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A&t=106s) — 1:46–2:10 |
| Effet sur la décision | **5/5** | Les classements dans les deux sens et les preuves aident le candidat à choisir des offres et le recruteur à comparer les profils. | [Vidéo](https://www.youtube.com/watch?v=KbRVm8iZH5A&t=120s) — 2:00–2:10 |

### Track déclarée — 10/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **4/4** | L’exécution locale sur le PC est expliquée, avec Docker et une option CPU. La vitrine Hugging Face ne suffit pas à contredire cette exécution ; la localisation des appels publics reste à distinguer. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Petit PC |
| Frameworks Open Source | **2/2** | Les deux modèles spécialisés sont identifiés et leur exécution sans API d’IA externe est expliquée. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs ; Petit PC |
| Cohérence des licences | **2/2** | Les licences MIT pour bge-m3 et Apache-2.0 pour le reranker sont explicitées. La cohérence des modèles est bien documentée. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Deux enquêteurs |
| Matériel et installation | **2/2** | Le GPU de 4 Go, le mode CPU et l’image Docker donnent plusieurs possibilités d’installation clairement décrites. | [Article](https://dev.to/jocc0/cv-matching-le-bon-profil-preuves-a-lappui-hackavp-4oh8) — Petit PC, grandes ambitions |

### Points à garder en tête

- Les résultats annoncés, notamment 84 % contre 71 %, portent sur de petits jeux fictifs. Le test de reformulation de sept cas ne doit pas être lu comme une mesure générale d’exactitude.
- Le vérificateur peut rejeter des preuves partielles. La vidéo locale et la vitrine Hugging Face peuvent coexister ; la localisation des appels publics est une question distincte.
- L’article affichait une modification le 22 octobre, après la clôture du 21 octobre. Aucun contenu précis n’est attribué au travail postérieur sur cette seule base.

## 8. OPT + — 18,5/100

**Soumission :** OPT +. **Auteur indiqué dans la grille :** Japheth ROKO. **Track déclarée :** SaaS no limit.

**Ce qui est évalué :** Copilote candidat/RH présenté autour de Gemini et Vertex AI.

**Sources :** [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) · [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI).

### Appréciation d’ensemble

L’intention est compréhensible, mais le rendu donne trop peu de matière pour apprécier le résultat. L’article est très court et la vidéo ressemble davantage à une présentation promotionnelle qu’à une démonstration. On voit une interface et des scores, sans voir comment ils sont obtenus ni comment les documents annoncés sont produits. La note reste donc basse : elle reconnaît les quelques éléments présentés, mais les promesses ne suffisent pas à établir le fonctionnement.

### Socle commun — 11/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **1/4** | Le double parcours répond à un besoin compréhensible. Les écrans présentés apportent peu d’éléments pour apprécier une identité visuelle propre et aboutie. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Un copilote RH, deux parcours |
| UX & utilisabilité | **1/5** | Le dépôt et la saisie sont annoncés, mais aucune suite d’interactions ne permet de suivre un parcours réellement utilisé. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=20s) — 0:20–0:50 |
| Accessibilité | **0/4** | Les écrans ne suffisent pas à apprécier l’usage au clavier ou avec un lecteur d’écran. Aucun élément précis du rendu ne permet d’attribuer des points sur ce critère. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Article complet |
| Adéquation moyens / résultats | **1/5** | Le SaaS peut simplifier un prototype. Le peu de résultats montrés et l’absence de repères sur le temps, les coûts ou les ressources limitent l’appréciation. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Architecture SaaS |
| Standards & Open Data | **1/6** | Les AVP et les métiers OPT sont cités. Les formats et la façon dont les données sont effectivement utilisées restent peu expliqués. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini accompagne les candidats |
| Storytelling | **2/4** | Le problème et les deux publics se comprennent. Le récit reste cependant général et montre peu de réalisations concrètes. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=1s) — 0:01–1:36 |
| Réutilisabilité & essaimage | **1/4** | L’idée pourrait être reprise, mais l’article ne fournit ni code, ni configuration, ni mode d’emploi pour le faire. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Article complet |
| Plaisir de lecture | **2/4** | Le texte court permet de distinguer les deux publics. Le manque d’exemples et d’explications limite l’intérêt de la lecture. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini accompagne les candidats ; Vertex AI aide les équipes RH |
| Plaisir de visionnage | **2/4** | Le propos est bref, mais répète surtout les bénéfices attendus sans dérouler de scénario. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=20s) — 0:20–1:36 |

### Technicité — 4/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **2/8** | Gemini et Vertex AI sont des choix plausibles pour un copilote. Le rôle effectif des services et le cheminement des données sont peu développés. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini ; Vertex AI |
| Intégrabilité | **1/8** | Les deux parcours sont annoncés sans contrat d’interface, format de sortie ni exemple d’échange suffisamment détaillé. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Article complet |
| Maintenabilité | **1/5** | La rétention et l’hébergement sont évoqués. Les tests, l’architecture détaillée et la manière de faire évoluer le service restent peu expliqués. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Données protégées |
| Interaction inédite (bonus) | **0/4** | Aucune interaction média particulière n’est montrée. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI) — Vidéo complète |

### Valeur RH — 1/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0,5/5** | Des scores apparaissent à l’écran, mais leur calcul et les éléments qui les justifient ne sont pas montrés. Le demi-point reconnaît la présentation du principe de rapprochement. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=25s) — 0:25–0:41 |
| Documents générés | **0/5** | CV, lettre et préparation sont annoncés, sans production visible permettant de les compter comme documents générés. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=41s) — 0:41–0:50 |
| Qualité de la restitution | **0,5/5** | Les forces et les écarts sont évoqués, mais aucun exemple détaillé ne permet de juger la qualité d’un diagnostic individuel. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=35s) — 0:35–0:41 |
| Facilité de création | **0/5** | Le rendu ne montre ni génération ni téléchargement des pièces de candidature. | [Vidéo](https://www.youtube.com/watch?v=K3clM7j3QQI&t=41s) — 0:41–0:50 |
| Effet sur la décision | **0/5** | Aucune analyse effectivement utilisée pour éclairer un choix de candidature ou une action RH n’est montrée. Les bénéfices annoncés ne suffisent pas à apprécier cet effet. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Article complet |

### Track déclarée — 2,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching | **1/4** | Les services d’IA sont nommés. Les entrées, l’enchaînement et les contrôles du matching restent trop peu expliqués pour aller au-delà d’une appréciation du principe. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini ; Vertex AI |
| Qualité de l’architecture | **1/2** | La séparation candidat/RH et les services Google donnent une idée de l’architecture. L’implémentation est peu détaillée. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini ; Vertex AI |
| Déployabilité IaC | **0/2** | Aucune configuration IaC, aucun script et aucune procédure de reproduction ne sont fournis pour attribuer des points. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Article complet |
| Pertinence des intégrations | **0,5/2** | L’usage conjoint de deux accès à Gemini est décrit. Leur intégration opérationnelle n’est pas montrée. | [Article](https://dev.to/japheth_roko_98b65d73fb64/opt--2abd) — Gemini ; Vertex AI |

### Points à garder en tête

- L’interface et les scores affichés sont reconnus comme tels. Ils ne montrent pas le calcul, une analyse détaillée ou la génération des documents annoncés.
- L’article consulté affichait une publication le 21 octobre, sans date de modification visible. Cela ne prouve pas qu’il n’a jamais été modifié.

## 9. Veille CDO (RSS + Claude) — 66,5/100

**Soumission :** Pendant un hackathon data… je trouve une opportunité de CDO dans ma propre entreprise. **Auteur indiqué dans la grille :** Adrien SALES. **Track déclarée :** SaaS no limit.

**Ce qui est évalué :** Veille personnalisée et préparation de candidature sans code.

**Sources :** [Article](https://dev.to/adriens/pendant-un-hackathon-data-je-trouve-une-opportunite-de-cdo-dans-ma-propre-entreprise-4bp9) · [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A) · [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs).

### Appréciation d’ensemble

L’idée est simple et utile : partir des offres pour préparer une candidature avec Claude. La vidéo montre bien les trois documents produits et leur personnalisation. Le résultat est intéressant, même si l’originalité de la proposition reste modeste. La première offre retenue nécessite une correction humaine, et plusieurs aspects restent peu expliqués, notamment la reproduction de la configuration et l’enregistrement sur Drive.

### Socle commun — 26/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **2/4** | Le scénario est utile, mais repose sur l’interface standard de Claude et un usage conversationnel courant. L’originalité et le travail esthétique propres à la proposition restent modestes. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=8s) — 0:08–1:28 ; 4:02–4:43 |
| UX & utilisabilité | **4/5** | La conversation et la planification sont faciles à déclencher. Le parcours conserve quelques interventions, notamment les autorisations et la correction de l’offre proposée. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=19s) — 0:19–3:21 |
| Accessibilité | **1,5/4** | Le langage naturel réduit la barrière technique. Le rendu explique moins les possibilités d’usage avec des outils d’assistance et par un public peu à l’aise avec le numérique. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=19s) — 0:19–1:31 |
| Adéquation moyens / résultats | **4,5/5** | Le RSS et un assistant existant permettent d’obtenir rapidement un résultat. Le coût de l’abonnement et les dépenses récurrentes sont moins détaillés. | [Article](https://dev.to/adriens/pendant-un-hackathon-data-je-trouve-une-opportunite-de-cdo-dans-ma-propre-entreprise-4bp9) — Contexte ; Conclusion |
| Standards & Open Data | **4/6** | Le flux RSS officiel et le profil existant sont réutilisés. Aucun format standard de profil ni contrat d’export précis n’est montré. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=0s) — 0:00–0:51 ; 3:38–3:59 |
| Storytelling | **3/4** | Le cas concret et la revue des trois documents rendent la démarche compréhensible. L’article est bref et l’enregistrement Drive annoncé reste à distinguer de ce qui est visible. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=526s) — 8:46–11:50 |
| Réutilisabilité & essaimage | **2,5/4** | La démarche et la source RSS sont accessibles. Les paramètres du profil et des connecteurs sont moins formalisés ; un mode d’emploi complet aiderait à les reprendre. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=19s) — 0:19–1:28 |
| Plaisir de lecture | **2/4** | L’article donne vite le contexte, mais laisse l’essentiel des explications aux vidéos. Sa lecture seule apporte assez peu de détails sur la démarche. | [Article](https://dev.to/adriens/pendant-un-hackathon-data-je-trouve-une-opportunite-de-cdo-dans-ma-propre-entreprise-4bp9) — Contexte ; Ce qui est démontré ; Conclusion |
| Plaisir de visionnage | **2,5/4** | La conversation et la revue des documents sont intéressantes. La vidéo longue consacre toutefois plusieurs minutes au RSS avant d’aborder le scénario principal. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=69s) — 1:09–4:26 ; 4:29–8:42 ; 8:46–11:50 |

### Technicité — 13/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **6/8** | Le RSS, le profil et Claude servent directement le besoin. Le choix des informations conservées du profil et les réglages de l’analyse sont moins expliqués. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=0s) — 0:00–3:59 |
| Intégrabilité | **5/8** | RSS, notifications et tâche conversationnelle sont assemblés de manière utile. Les permissions, les formats de sortie et les paramètres des connecteurs sont moins détaillés. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=63s) — 1:03–1:28 |
| Maintenabilité | **2/5** | Le service demande peu de composants propres. La conservation des consignes, leur versionnement et les contrôles après modification restent toutefois peu expliqués. | [Article](https://dev.to/adriens/pendant-un-hackathon-data-je-trouve-une-opportunite-de-cdo-dans-ma-propre-entreprise-4bp9) — Contexte ; Conclusion |
| Interaction inédite (bonus) | **0/4** | La conversation et les notifications sont des usages courants de l’assistant. Aucun média particulier ne justifie le bonus. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A) — Vidéo complète |

### Valeur RH — 21/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **3/5** | Le lien avec le poste de données est expliqué. Une première offre réseau doit cependant être écartée par l’auteur, ce qui montre une limite concrète de la sélection. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=127s) — 2:07–3:00 ; 3:38–3:59 |
| Documents générés | **4/5** | Le CV, la lettre et la préparation sont ouverts en DOCX et ciblent le poste de responsable des données. Les pièces sont bien présentes, mais la fidélité de tous les faits biographiques ne peut pas être établie par la comparaison disponible. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=526s) — 8:46–11:50 |
| Qualité de la restitution | **5/5** | La restitution relie le parcours au poste, distingue la technique de la gouvernance et propose des questions d’entretien avec des pistes de réponse contextualisées. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=681s) — 11:21–11:50 |
| Facilité de création | **5/5** | La demande conversationnelle aboutit aux trois DOCX, ouverts dans la vidéo. Le parcours de création est donc montré ; l’enregistrement Drive est examiné séparément. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=570s) — 9:30–11:21 |
| Effet sur la décision | **4/5** | Les documents et la préparation apportent une aide concrète. Le rendu convainc davantage sur la préparation de candidature que sur l’aide à trancher l’adéquation au poste. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=570s) — 9:30–11:21 |

### Track déclarée — 6,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching | **3/4** | Le parcours du RSS au profil puis à l’offre retenue est montré. Les règles de sélection et la configuration persistante du rapprochement restent moins précises. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=0s) — 0:00–4:00 |
| Qualité de l’architecture | **1,5/2** | L’assemblage est léger et adapté au besoin. Les permissions et la gestion du contexte sont moins expliquées. | [Vidéo](https://www.youtube.com/watch?v=mqHSh_MxA5A&t=63s) — 1:03–3:06 |
| Déployabilité IaC | **0,5/2** | La tâche est créée manuellement. Aucun export de configuration ni procédure guidée ne permet de la reproduire facilement. | [Article](https://dev.to/adriens/pendant-un-hackathon-data-je-trouve-une-opportunite-de-cdo-dans-ma-propre-entreprise-4bp9) — Article complet |
| Pertinence des intégrations | **1,5/2** | Le RSS et les notifications répondent au besoin. Les deux vidéos ne permettent toutefois pas d’établir l’enregistrement effectif sur Google Drive. | [Vidéo longue](https://www.youtube.com/watch?v=05iDCkPfRCs&t=349s) — 5:49–5:59 ; 14:04–14:08 |

### Points à garder en tête

- Le CV, la lettre et le guide DOCX sont effectivement ouverts dans la vidéo longue, vers 9:30, 10:22 et 11:21. Le bouton Google Drive visible ne prouve pas leur enregistrement sur Drive.
- Une offre réseau est écartée manuellement avant la sélection du poste de données. La création d’une tâche planifiée ne prouve pas, à elle seule, un déclenchement autonome ultérieur.
- L’article affichait une publication le 14 septembre et une modification le 17 septembre, avant la clôture. La fidélité de l’ensemble des faits biographiques n’a pas pu être établie.

## 10. Mapping AVP–ESCO — 66,5/100

**Soumission :** J'ai mappé les offres d'emploi public de l'OPT-NC avec le référentiel ESCO. **Auteur indiqué dans la grille :** Adrien SALES. **Track déclarée :** SaaS no limit.

**Ce qui est évalué :** Enrichissement des AVP par ESCO et exploration dans un notebook.

**Sources :** [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) · [Vidéo](https://www.youtube.com/watch?v=cKV_tJ6qdSo) · [Notebook remis](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook).

### Appréciation d’ensemble

Le travail sur les offres et le référentiel ESCO est intéressant et bien exploité. Les fichiers produits ouvrent des possibilités concrètes d’analyse des besoins en compétences. Certaines correspondances sont toutefois discutables ; leur validation par un LLM ne suffit pas à lever ces réserves. Des explications plus lisibles et une meilleure reproductibilité renforceraient le résultat. La note reconnaît surtout l’apport à l’analyse des offres, sans y assimiler un rapprochement avec des candidats.

### Socle commun — 32/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **3/4** | Le rapprochement entre métiers et compétences apporte un angle intéressant. Les différentes vues donnent de la matière à explorer. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — Les découvertes |
| UX & utilisabilité | **3,5/5** | Le sommaire, les paramètres, les tableaux et les figures organisent bien le notebook pour des analystes. Le nombre de sorties et la technicité demandent toutefois de l’attention. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : sommaire ; tableaux et analyses |
| Accessibilité | **1,5/4** | Les titres, tableaux et libellés donnent des repères. Le code prévoit une palette présentée par l’auteur comme adaptée au daltonisme ; cela ne suffit pas à certifier l’accessibilité des graphiques. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : 5. Analytics, In [18] ; tableaux de résultats |
| Adéquation moyens / résultats | **4,5/5** | Les deux T4 servent au modèle et au traitement des 70 offres. L’exécution Kaggle réussie de 3 h 31 min 44 s fournit un résultat concret ; l’efficience comparative reste moins chiffrée. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : Runtime ; introduction ; données ; sorties |
| Standards & Open Data | **6/6** | Les AVP, ESCO et ISCO structurent l’analyse. Le réemploi des données et des référentiels ouverts est au cœur du projet. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — Expérimentation ; Ressources |
| Storytelling | **3,5/4** | La méthode en trois étapes est claire. Les limites de la validation automatique et l’usage final pourraient être davantage développés. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — Expérimentation ; Perspectives |
| Réutilisabilité & essaimage | **4/4** | Le notebook et les données préparées donnent de bons moyens de reprendre l’analyse sur un autre corpus. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — Ressources |
| Plaisir de lecture | **3/4** | La méthode et les ressources sont faciles à repérer. Plusieurs résultats passent surtout par les figures et sont accompagnés de peu de texte explicatif. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — L'expérimentation ; Les découvertes ; Ressources |
| Plaisir de visionnage | **3/4** | Le commentaire guide l’exploration et donne des exemples. Le parcours reste assez exploratoire et pourrait être davantage synthétisé. | [Vidéo](https://www.youtube.com/watch?v=cKV_tJ6qdSo&t=38s) — 0:38–1:53 ; 2:45–5:02 |

### Technicité — 19/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **8/8** | Les embeddings multilingues, Qwen et les référentiels ont des rôles précis. La possibilité de ne retenir aucun lien évite de forcer toutes les correspondances. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — L'expérimentation |
| Intégrabilité | **8/8** | Les tables et leurs champs sont expliqués, avec des exports DuckDB, Parquet et JSON-LD enrichis d’URI ESCO. Les résultats peuvent être réutilisés sans dépendre du notebook pour leur lecture. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : tables ; JSON-LD enrichi ; Output |
| Maintenabilité | **3/5** | Le code et les étapes sont accessibles. Les tests, le versionnement des sorties et la place des contrôles humains sont moins développés. | [Vidéo](https://www.youtube.com/watch?v=cKV_tJ6qdSo&t=115s) — 1:55–2:15 |
| Interaction inédite (bonus) | **0/4** | Les graphiques servent l’exploration, mais ne constituent pas à eux seuls une interaction média justifiant le bonus. | [Vidéo](https://www.youtube.com/watch?v=cKV_tJ6qdSo) — Vidéo complète |

### Valeur RH — 7/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0/5** | Le rapprochement concerne les offres et ESCO. Aucun candidat n’est comparé à une offre dans ce livrable. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — L'expérimentation |
| Documents générés | **0/5** | Le notebook ne génère ni CV, ni lettre, ni guide d’entretien. | [Vidéo](https://www.youtube.com/watch?v=cKV_tJ6qdSo) — Vidéo complète |
| Qualité de la restitution | **4/5** | Les compétences, les directions et les familles ISCO donnent une lecture utile des besoins. Le tableau relie l’exigence à ESCO, mais les raisonnements en anglais tronqués à 350 caractères restent moins lisibles qu’une synthèse métier. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : 5. Analytics ; comparaisons et explications |
| Facilité de création | **0/5** | Le notebook ne comporte pas de parcours de création des pièces de candidature. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — L'expérimentation |
| Effet sur la décision | **3/5** | La cartographie aide à examiner les compétences communes, la mobilité et la rédaction des offres. Le rendu reste exploratoire et ne déroule pas un arbitrage RH précis ; l’agent de rédaction envisagé n’est pas compté. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : 5. Analytics ; comparaisons et explications |

### Track déclarée — 8,5/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching | **3,5/4** | Le rappel vectoriel puis la sélection par LLM, avec possibilité d’abstention, forment une démarche pertinente. Certaines correspondances restent discutables et la validation demeure surtout automatique. | [Article](https://dev.to/adriens/jai-mappe-les-offres-demploi-public-de-lopt-nc-avec-le-referentiel-esco-a-laide-dembeddings-5765) — L'expérimentation |
| Qualité de l’architecture | **2/2** | Les paramètres, les traitements, les exports et les analyses sont séparés. La répartition sur deux T4 est expliquée et convient au traitement par lot. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : paramètres ; rappel ; validation ; exports |
| Déployabilité IaC | **1/2** | Le code, les paramètres et une exécution réussie sont accessibles. Le chargement depuis main et les dépendances pas entièrement verrouillées rendent une reproduction à l’identique moins sûre. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : installation, paramètres, source AVP main ; Runtime |
| Pertinence des intégrations | **2/2** | ESCO, les AVP, les modèles et Kaggle sont effectivement utilisés ensemble. Le code et les sorties permettent de comprendre leur contribution. | [Notebook](https://www.kaggle.com/code/adriensales/avp-opt-nc-esco-qwen/notebook) — Notebook v8 : Données ; modèles ; exports ; Runtime |

### Points à garder en tête

- Une exigence « Mobiliser des équipes autour d’un projet de changement » est rapprochée d’un concept de coordination de la promotion de destinations touristiques : c’est un exemple concret de correspondance discutable.
- Une absence de lien peut venir d’un manque dans le référentiel, du rappel ou de la sélection ; le rendu ne permet pas toujours de trancher entre ces explications.
- Le notebook examiné est la version 8, datée du 11 octobre 2026. L’article affichait une publication le 18 octobre ; aucune modification postérieure à la clôture n’a été établie par cette lecture.
- La palette dite adaptée au daltonisme est une indication de l’auteur dans le code, pas une certification d’accessibilité attribuée par le jury.

## 11. HACKAVPI — 58/100

**Soumission :** HACKAVPI. **Auteur indiqué dans la grille :** Thimotée. **Track déclarée :** onPrem souverain.

**Ce qui est évalué :** API centrale MS2 de JOBMATCH NC.

**Sources :** [Article](https://dev.to/pastek/hackavpi-dp8) · [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE).

### Appréciation d’ensemble

L’article et la vidéo expliquent très bien le rôle du hub. Les choix concernant l’API, les droits, le stockage et la traçabilité donnent une base sérieuse pour gérer les offres et les profils. L’aide RH montrée reste cependant assez limitée : dépôt, consultation et suivi, sans rapprochement sémantique ni génération de documents propres au projet. L’écart sur le nombre de routes et la localisation indéterminée du VPS restent à relever.

### Socle commun — 30,5/40

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Créativité & esthétique | **1,5/4** | Le hub répond à un besoin concret de centralisation. La solution reste une infrastructure classique, avec peu d’éléments visuels distinctifs. | [Article](https://dev.to/pastek/hackavpi-dp8) — Le projet HackAVP |
| UX & utilisabilité | **3,5/5** | Swagger, les routes et l’authentification facilitent l’usage par les intégrateurs. Des exemples plus guidés aideraient encore à prendre l’API en main. | [Article](https://dev.to/pastek/hackavpi-dp8) — Documentation avec Swagger |
| Accessibilité | **0,5/4** | La documentation interactive et les explications aident les intégrateurs. Le rendu donne peu d’informations sur l’accessibilité de la documentation elle-même. | [Article](https://dev.to/pastek/hackavpi-dp8) — Documentation avec Swagger |
| Adéquation moyens / résultats | **4,5/5** | L’API regroupe stockage, authentification et échanges, avec des conteneurs et un déploiement automatisé. Les moyens sont cohérents ; les coûts et le dimensionnement sont moins chiffrés. | [Article](https://dev.to/pastek/hackavpi-dp8) — Déploiement |
| Standards & Open Data | **6/6** | REST, JSON, Swagger et les AVP officiels sont clairement mobilisés. Les formats et les références d’offres donnent des contrats d’échange utiles. | [Article](https://dev.to/pastek/hackavpi-dp8) — Gestion des données ; Swagger |
| Storytelling | **3/4** | L’article pédagogique et la vidéo technique se complètent bien. Les 27 routes annoncées dans l’un et les 32 dans l’autre laissent toutefois une ambiguïté sur la version présentée. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=247s) — 4:07–4:15 |
| Réutilisabilité & essaimage | **3,5/4** | Les conteneurs, Swagger et le déploiement automatisé facilitent la reprise. Les paramètres et les adaptations à prévoir dans un autre contexte sont moins détaillés. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=39s) — 0:39–1:00 ; 4:18–4:25 |
| Plaisir de lecture | **4/4** | Les analogies et le scénario de Léa rendent l’article concret et très agréable. Les explications techniques participent à la qualité de lecture. | [Article](https://dev.to/pastek/hackavpi-dp8) — Une API, c'est quoi ; Parcours de Léa ; Fonctionnalités |
| Plaisir de visionnage | **4/4** | La présentation est claire, bien structurée et très agréable selon le juré. La densité technique ne gêne pas cette appréciation. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=39s) — 0:39–1:53 ; 1:55–3:45 ; 4:07–4:31 |

### Technicité — 19/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Pertinence des ressources | **7/8** | Les AVP officiels, les profils structurés et les routes sont adaptés au rôle du hub. Le traitement des mises à jour d’offres existantes est moins clairement établi. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=73s) — 1:13–1:27 |
| Intégrabilité | **8/8** | Les routes REST, les droits, le JSON et Swagger définissent des contrats explicites pour les applications qui utilisent le hub. | [Article](https://dev.to/pastek/hackavpi-dp8) — Fonctionnalités ; Swagger |
| Maintenabilité | **4/5** | Flyway, la traçabilité et le déploiement continu organisent l’évolution du service. Les tests de régression, les changements de contrats et la reprise après incident sont moins détaillés. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=39s) — 0:39–1:00 ; 3:10–3:28 ; 4:18–4:25 |
| Interaction inédite (bonus) | **0/4** | L’API ne propose pas d’interaction média particulière. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE) — Vidéo complète |

### Valeur RH — 4,5/25

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Qualité du matching | **0/5** | Le hub fournit les profils et les offres, mais ne calcule pas leur adéquation. | [Article](https://dev.to/pastek/hackavpi-dp8) — Scénario de Léa |
| Documents générés | **0/5** | Le stockage d’un CV ne constitue pas la génération d’un document adapté à une offre. Aucune production de ces pièces n’est montrée. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=140s) — 2:20–2:42 |
| Qualité de la restitution | **1,5/5** | Les statuts et les agrégats donnent une première lecture du suivi RH. Le rendu présente surtout les routes et les indicateurs, sans diagnostic détaillé ni réponse chiffrée complète à examiner. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=210s) — 3:30–3:45 |
| Facilité de création | **1/5** | Le dépôt du CV, le profil JSON et la constitution du dossier préparent une candidature. Le point récompense cette centralisation, sans lui attribuer l’extraction ou la génération d’un autre service. | [Article](https://dev.to/pastek/hackavpi-dp8) — Dépôt CV ; connexion CVForge |
| Effet sur la décision | **2/5** | Les statuts, l’historique et les agrégats aident à repérer les dossiers à traiter. L’apport reste principalement celui du suivi ; aucune analyse propre ne guide aussi précisément un choix RH. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=165s) — 2:45–3:07 |

### Track déclarée — 4/10

| Critère | Note | Justification | Référence |
| --- | ---: | --- | --- |
| Chaîne de matching locale | **0/4** | Le hub met les données à disposition, sans calcul ni consommation de résultat de rapprochement sémantique montré. Les validations bilatérales ne suffisent pas à établir ce matching. | [Article](https://dev.to/pastek/hackavpi-dp8) — Déploiement |
| Frameworks Open Source | **2/2** | Spring Boot, Kotlin, PostgreSQL et Flyway sont identifiés. Le recours aux composants Open Source est bien documenté. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=39s) — 0:39–1:00 |
| Cohérence des licences | **0,5/2** | La stack est connue, mais les licences du code et de ses dépendances sont peu expliquées. | [Vidéo](https://www.youtube.com/watch?v=r8CMPcC_dSE&t=39s) — 0:39–1:00 |
| Matériel et installation | **1,5/2** | Docker et le déploiement continu facilitent la mise en service. Les consignes de configuration et le dimensionnement sont moins détaillés ; la localisation du VPS reste une question de conformité distincte. | [Article](https://dev.to/pastek/hackavpi-dp8) — Déploiement |

### Points à garder en tête

- L’article annonce 27 routes et la vidéo 32. Une différence de version est possible ; le rendu ne permet pas d’en faire une contradiction fonctionnelle certaine.
- L’import des références nouvelles est expliqué. La mise à jour et la clôture des offres déjà connues restent moins établies ; une date d’expiration ne suffit pas à prouver une synchronisation complète.
- La localisation du VPS est indéterminée. La track déclarée est conservée et aucune non-conformité géographique n’est déduite de cette seule absence.
- L’article affichait une publication le 20 octobre et une modification le 22 octobre. Le contenu exact disponible à la clôture du 21 n’est pas reconstitué ; la vidéo référencée dans le guide a été prise en compte.

## Concordance des livrables

Les 242 notes et les onze totaux de ce document sont ceux du CSV et du classeur `evaluation_hackavp_100_points.xlsx`. La formulation des justifications a été clarifiée pour cette version de remise. L’historique de travail reste dans les fichiers de revue ; il n’entre pas dans cette synthèse finale.
