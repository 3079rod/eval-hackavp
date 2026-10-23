# Mesure du contenu généré par IA dans les articles

Ce document explique comment a été mesurée, le 23/10/2026, la part de texte généré par IA dans les 11 articles du HackAVP. Les résultats sont dans `detection_ia_articles.csv`.

> **À lire avant d'utiliser les chiffres.** Un détecteur d'IA donne une indication, pas une preuve. Sur les mêmes textes, deux détecteurs ont donné des résultats opposés (voir plus bas). Ces scores ne doivent pas servir, seuls, à pénaliser une équipe.

## 1. Préparation des textes

Pour chaque article :

1. Le texte source a été récupéré en Markdown par l'API publique de dev.to (`https://dev.to/api/articles/<auteur>/<slug>`, champ `body_markdown`).
2. Il a été nettoyé pour ne garder que la prose écrite par l'équipe. Ont été retirés :
   - les blocs de code ;
   - les intégrations dev.to (`{% embed %}`, `{% youtube %}`…) ;
   - les images ;
   - les URL (le texte des liens est conservé) ;
   - les balises HTML, les séparateurs de tableaux et la mise en forme Markdown (`**`, `#`, `>`, `` ` ``).

   Les titres, les listes et les emojis sont restés dans le texte.
3. Chaque texte nettoyé a été enregistré dans un fichier `.txt` (de 178 à 2 263 mots).

## 2. Premier essai : Humalingo (abandonné)

L'article 1 a d'abord été soumis à <https://humalingo.com/ai-detector>, via le navigateur et sans compte.

- Résultat : 95 % d'IA, 97 % de « plagiat ».
- **L'essai s'est arrêté là**, car la version gratuite est limitée à 3 analyses et le compteur affichait déjà « 0 / 3 Free uses left ».
- **Ce résultat a été jugé peu fiable** :
  - pendant l'analyse, l'outil affiche « I reviewed your text on cognitive load », alors que l'article ne parle pas de charge cognitive ;
  - le score de plagiat est forcément élevé, puisque l'article est déjà publié sur dev.to ;
  - le site vend un service de réécriture (« AI Humanizer ») : il a intérêt à trouver beaucoup d'IA.

## 3. Première mesure : ZeroGPT (articles entiers)

Les 11 articles ont été soumis à <https://www.zerogpt.com/>, via le navigateur Chrome, sans compte.

- **Limite** : 15 000 caractères par analyse. Le plus long article nettoyé en fait 14 408, donc chaque article a été analysé en une seule fois, sans découpage.
- **Procédure** : envoi du fichier `.txt` par le bouton « Upload File », qui lance l'analyse. On relève ensuite le verdict (« Your File Content is … ») et le pourcentage « AI GPT* ».
- Une fenêtre demandait de désactiver le bloqueur de publicité. Elle a été fermée par « Continue without supporting us », sans modifier les réglages du navigateur.

### Contrôles

Ils servent à vérifier que l'outil détecte bien quelque chose et que le mode d'envoi ne fausse pas le résultat.

| Test | Résultat ZeroGPT |
|---|---|
| Texte témoin écrit par une IA (un paragraphe générique, en français, sur la transformation numérique), collé dans la zone de texte | 100 % IA |
| Même texte témoin, envoyé sous forme de fichier | 100 % IA |
| Article 2 réduit à sa prose (23 paragraphes, sans titres, listes ni emojis) | 0 % IA |

L'outil fonctionne et les deux modes d'envoi donnent le même résultat. Retirer la mise en forme de l'article 2 ne change rien.

## 4. Deuxième mesure : Pangram, sur des extraits

Le résultat de ZeroGPT a été jugé douteux (voir section 6). Les articles ont donc été soumis à <https://www.pangram.com/>, un détecteur qui annonce une détection multilingue, dont le français, et qui figure en bonne place dans des comparatifs indépendants.

- **Compte** : gratuit, créé par l'organisateur. Il donne 20 crédits par jour, à raison de 1 crédit pour 100 mots.
- **Conséquence** : les articles entiers (environ 15 000 mots) ne tenaient pas dans le quota. Chaque article a donc été mesuré sur un **extrait de 50 à 100 mots**, soit 1 crédit par article.
- **Règle de choix de l'extrait**, la même pour tous : les premiers paragraphes de prose rédigée de l'article (au moins 150 caractères), coupés à une fin de phrase. Sont exclus les titres, les listes à puces, les emojis, les citations (blocs `>`) et les lignes « Track : … ».
- **Limites** : les articles 9 et 10 ont très peu de prose, et leurs extraits contiennent des fragments de listes numérotées. Pangram indique pour chaque extrait « Less accurate on short text » : sur moins de 100 mots, le résultat est moins sûr. Enfin, un extrait ne représente pas forcément tout l'article.
- **Procédure** : texte collé dans l'onglet « Text » du tableau de bord, puis bouton « Check for AI ». On relève le verdict, la part d'IA et le détail (« AI-generated content appears in the later part », etc.).

### Contrôles Pangram

| Test | Résultat |
|---|---|
| Témoin IA brut (style caricatural, 89 mots) | 100 % IA, « Possibly AI » |
| Témoin IA retravaillé (écrit par une IA dans un style familier et concret, 89 mots) | 100 % IA, « Possibly AI » |
| Texte écrit par un humain | Pas encore fait : un texte de l'organisateur est attendu |

Pangram reconnaît donc aussi un texte d'IA écrit pour paraître humain, ce que ZeroGPT ne garantissait pas. Le contrôle humain reste à faire : sans lui, on ne connaît pas le taux de faux positifs sur ce type de texte.

## 5. Résultats

| N° | Projet | Mots (article) | ZeroGPT : % IA (article entier) | Pangram : % IA (extrait) | Détail Pangram |
|---|---|---|---|---|---|
| 1 | CV Generator | 1 064 | 0 | 0 | Humalingo : 95 % |
| 2 | Insight Squad | 1 671 | 0 | 0 | |
| 3 | JOBMATCH NC | 1 589 | 12,16 | 0 | |
| 4 | AVPRO | 2 263 | 0 | 2 | |
| 5 | Adopte un Job | 2 094 | 0 | **73** | Surtout IA, début écrit par un humain |
| 6 | CV FORGE | 2 158 | 0 | **65** | IA dans la deuxième partie |
| 7 | CV-Matching | 1 508 | 0 | **46** | IA dans la deuxième partie |
| 8 | OPT + | 337 | 0 | **57** | IA dans la première partie |
| 9 | RSS + Claude CoWork | 178 | 0 | 0 | Extrait avec fragments de listes |
| 10 | Mapping ESCO | 454 | 0 | 0 | Extrait avec fragments de listes |
| 11 | HACKAVPI | 1 759 | 11,1 | 0 | |

## 6. Interprétation

- **ZeroGPT ne distingue presque pas les articles** : 9 sur 11 sont à 0 %, et les deux autres à environ 11-12 %. Il ne repère que le style d'IA le plus caricatural, comme celui du texte témoin.
- **Pangram distingue deux groupes** : 4 articles avec une part d'IA importante (Adopte un Job, CV FORGE, OPT +, CV-Matching, de 46 à 73 %) et 7 articles jugés humains (de 0 à 2 %).
- **Les deux outils ne sont pas d'accord** : aucun des 4 articles signalés par Pangram n'est signalé par ZeroGPT. Pangram contredit aussi la lecture de l'article 2, jugé « très généré » par un lecteur, et le score de Humalingo sur l'article 1.
- **Le résultat de Pangram est le plus crédible des trois**, car il a passé les deux contrôles IA. Mais il porte sur des extraits de 100 mots au plus, et le contrôle humain manque. Il donne une piste à vérifier par la lecture, pas une preuve.
- **Conclusion : aucune de ces mesures ne permet de dire de façon certaine quels articles ont été écrits avec l'aide d'une IA.** Pour aller plus loin, il faudrait mesurer les articles entiers, par exemple avec l'essai gratuit de 7 jours de Pangram.

### Lien entre qualité de l'article et taux d'IA

Corrélations calculées avec DuckDB entre la note totale (/20) et deux indicateurs de l'article :

| Évaluateur | Projets | Note / taux d'IA ZeroGPT | Note / taux d'IA Pangram | Note / nombre de mots |
|---|---|---|---|---|
| Adrien SALES | 9 | 0,15 | -0,31 | 0,75 |
| Opus 5.5 | 11 | 0,08 | 0,13 | 0,83 |
| Sonnet 5.5 | 11 | -0,03 | 0,13 | 0,76 |

- **Pas de lien net entre la note et le taux d'IA mesuré.** Avec ZeroGPT, c'est attendu : le taux vaut presque toujours 0, donc il ne peut rien expliquer. Avec Pangram, la tendance est faible et change de signe selon l'évaluateur : légèrement négative pour l'évaluation humaine (-0,31), légèrement positive pour les modèles (0,13). Sur 9 à 11 projets, ces valeurs ne sont pas significatives.
- **Lien net entre la note et la longueur de l'article**, chez les trois évaluateurs. Les articles les plus courts (OPT +, et les n° 9 et 10) sont les moins bien notés. La longueur mesure en partie le travail de rédaction, mais elle peut aussi récompenser un texte long produit sans effort. Elle n'est pas un critère de qualité à elle seule.

## 7. Reproduire la mesure

1. Récupérer chaque article avec l'API dev.to et le nettoyer comme décrit en section 1.
2. Sur <https://www.zerogpt.com/>, envoyer chaque fichier par « Upload File » et relever le pourcentage. Sur Pangram (compte requis), coller chaque extrait dans l'onglet « Text » et relever la part d'IA ; avec un quota suffisant, analyser plutôt les articles entiers.
3. Refaire d'abord le contrôle avec un texte témoin : s'il ne sort pas à 100 %, l'outil a changé et les nouveaux résultats ne sont pas comparables.
4. Utiliser un seul détecteur pour tous les articles, car les scores de deux détecteurs différents ne sont pas comparables.
