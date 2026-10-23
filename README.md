# eval-hackavp

Évaluation des 11 soumissions du **HackAVP 2026**, le hackathon de l'OPT-NC, de la Station N et de la commission Data & IA d'OPEN NC, dédié à l'emploi dans la fonction publique en Nouvelle-Calédonie.

Le dépôt contient une grille de notation commune et une copie de cette grille par évaluateur (humain ou modèle). Toutes les copies ont le même format, ce qui permet de comparer les évaluations avec DuckDB.

## Sources

- **Guide du jury** (source de vérité pour la liste des soumissions et les pistes) : <https://dev.to/adriens/hackavp-guide-devaluation-pour-les-membres-du-jury-12i0>
- **Lancement du hackathon** (défi, fonctions attendues, grille sur 100) : <https://dev.to/adriens/hackavp-premier-hackathon-dedie-a-lemploi-dans-la-fonction-publique-en-ncl-3oj0>

## Fichiers

| Fichier | Rôle |
|---|---|
| `grille_hackavp_notation.csv` | Modèle : les 11 candidats avec les notes vides. **Ne pas noter dedans.** |
| `adriens_grille_hackavp_notation.csv` | Copie vierge destinée à l'évaluation d'Adrien SALES |
| `opus-5_5_grille_hackavp_notation.csv` | Évaluation par Claude Opus 5.5 |
| `sonnet-5_5_grille_hackavp_notation.csv` | Évaluation par Claude Sonnet 5.5 |
| `haiku-5_5_grille_hackavp_notation.csv` | Évaluation par Claude Haiku 5.5 |
| `detection_ia_articles.csv` | Part de texte généré par IA dans chaque article, selon ZeroGPT (article entier) et Pangram (extrait), mesurée le 23/10/2026 |
| `methode_detection_ia.md` | Méthode, contrôles et limites de cette mesure |
| `jury.csv` | Composition du jury : identifiant (préfixe du fichier de grille), nom, type, profil LinkedIn |
| `rapport_hackavp.qmd` | Rapport Quarto (R, DuckDB, ggplot2) : classements, accord entre évaluateurs, détection IA |
| `Taskfile.yml` | Build du rapport PDF avec Task et xelatex |

Les fichiers s'appellent `<evaluateur>_grille_hackavp_notation.csv`. Dans `<evaluateur>`, les points de version sont remplacés par des `_` : `opus-5_5`, `sonnet-5_5`, `adriens`. Cette convention permet aux requêtes ci-dessous de lire toutes les évaluations d'un coup.

## Format du CSV

- Encodage UTF-8 **avec BOM**, fins de ligne CRLF, séparateur virgule, décimales avec un point (`0.5`).
- Une ligne d'en-tête, puis une ligne par soumission (11 lignes), 19 colonnes.
- `N°` : numéro de la soumission dans le guide du jury (1 à 11).

| Colonne | Contenu |
|---|---|
| `N°`, `Projet`, `Auteur`, `Profil auteur`, `Piste`, `Article dev.to`, `Vidéo YouTube` | Identification de la soumission |
| `Problème et solution : clarté et impact (/4)` | Note |
| `Solution et pertinence (/4)` | Note |
| `Interop : schéma d'architecture (/1)` | Note |
| `Interop : solutions externes (/1)` | Note |
| `Interop : autres MicroStartups (/2)` | Note |
| `Usage des données / de l'IA (/3)` | Note |
| `Structure et slides (/2)` | Note |
| `Qualité de l'oral (/2)` | Note |
| `Respect du temps (/1)` | Note |
| `TOTAL /20` | Somme des notes renseignées |
| `Commentaires` | Justification de l'évaluateur |
| `Conflit d'intérêt` | Rempli pour les n° 9 et 10 (soumissions de l'organisateur) |

Une cellule de note **vide** veut dire « non évalué ». Ce n'est pas un zéro. Le `TOTAL /20` ne fait alors la somme que des critères notés, et le commentaire doit le dire.

La grille est celle des MicroStartups du Master MIAGE, sur 20 points. Elle n'est pas la grille sur 100 points publiée dans le guide du jury.

## Pistes

| Piste | Soumissions |
|---|---|
| onPrem souverain | 1, 3, 4, 6, 7, 11 |
| SaaS no limit | 2, 5, 8, 9, 10 |

La n° 5 (*Adopte un Job*) est en **SaaS no limit**, comme le déclare son article. Le guide du jury avait été corrigé en « onPrem » le 22/10/2026, puis la piste SaaS a été confirmée : le guide doit être aligné.

## Points connus

- **Conflit d'intérêt** : les n° 9 et 10 sont des soumissions d'Adrien SALES, l'organisateur. Ils restent en compétition : seul l'organisateur ne les note pas (et ne vote pas sur ces deux projets). Tous les autres évaluateurs, modèles compris, les notent normalement.
- **Vidéos 1 et 6** : les sous-titres de *CV Generator* et *CV FORGE* n'ont pas pu être récupérés avec `yt-dlp`, alors que les vidéos existent. Dans les évaluations des modèles, l'oral et le respect du temps sont donc laissés vides pour ces deux projets, qui sont notés sur 17.
- **Ce que les modèles n'ont pas vu** : ils ont lu les articles (API dev.to) et les transcriptions automatiques des vidéos. Ils n'ont vu ni les images, ni les vidéos elles-mêmes.

## Requêtes DuckDB

### Classements d'un évaluateur

```sql
CREATE VIEW n AS
SELECT "N°" AS num, Projet, Piste, "TOTAL /20" AS total
FROM read_csv('opus-5_5_grille_hackavp_notation.csv');

-- Gagnant par piste
SELECT Piste, num, Projet, total FROM n
QUALIFY rank() OVER (PARTITION BY Piste ORDER BY total DESC) = 1;

-- Classement par piste
SELECT Piste, rank() OVER (PARTITION BY Piste ORDER BY total DESC) AS rang, num, Projet, total
FROM n ORDER BY Piste, rang;

-- Classement global
SELECT rank() OVER (ORDER BY total DESC) AS rang, num, Projet, Piste, total
FROM n ORDER BY rang;
```

### Bench de toutes les évaluations

```sql
CREATE VIEW evals AS
SELECT regexp_extract(filename, '([^/]+)_grille_hackavp_notation\.csv$', 1) AS evaluateur,
       "N°" AS num, Projet, Piste, "TOTAL /20" AS total
FROM read_csv('*_grille_hackavp_notation.csv', filename = true, union_by_name = true)
WHERE "TOTAL /20" IS NOT NULL;   -- écarte les copies encore vierges

-- Notes côte à côte, une colonne par évaluateur
PIVOT (SELECT evaluateur, num, Projet, Piste, total FROM evals)
ON evaluateur USING first(total) ORDER BY num;

-- Moyenne et dispersion par soumission
SELECT num, any_value(Projet) AS Projet, round(avg(total), 2) AS moyenne,
       round(stddev_samp(total), 2) AS ecart_type, count(*) AS n
FROM evals GROUP BY num ORDER BY moyenne DESC;
```

Le motif `*_grille_hackavp_notation.csv` ne prend pas le modèle `grille_hackavp_notation.csv`, qui n'a pas de préfixe. Les copies vierges sont écartées par le filtre sur `TOTAL /20`.

Avec le CLI, lancer `duckdb -no-agent -box < requete.sql`. Si la variable `AI_AGENT` est définie, `-no-agent` est nécessaire pour que les commandes `.print` fonctionnent.

## Détection de contenu généré par IA

La part de texte généré par IA dans chaque article a été mesurée avec deux détecteurs. Le détail est dans `methode_detection_ia.md`, les chiffres dans `detection_ia_articles.csv`.

1. **Préparation** : texte de l'article récupéré par l'API dev.to, puis nettoyé (sans code, intégrations, images, URL ni balises).
2. **ZeroGPT** (gratuit, sans compte) : articles entiers, envoyés en fichier `.txt`. Presque tout sort à 0 % : résultat jugé peu fiable.
3. **Pangram** (compte gratuit, 20 crédits par jour, 1 crédit pour 100 mots) : un extrait de 50 à 100 mots par article, choisi avec une règle fixe (premiers paragraphes de prose, sans titres, listes, emojis ni citations). Quatre articles ressortent entre 46 et 73 % d'IA.
4. **Contrôles** : deux textes témoins écrits par IA (brut et retravaillé) sont reconnus à 100 % par Pangram. Le contrôle sur un texte humain reste à faire.

Ces scores donnent une indication, pas une preuve. Ils ne doivent pas servir, seuls, à pénaliser une équipe.

## Rapport PDF

```sh
task          # vérifie les outils, puis rend rapport_hackavp.pdf
task open     # ouvre le PDF
task clean    # supprime les fichiers générés
```

Il faut Quarto, R (paquets DBI, duckdb, dplyr, tidyr, ggplot2, forcats, stringr, knitr, rmarkdown, scales), xelatex et la police Inter. Le rapport relit à chaque rendu toutes les grilles `*_grille_hackavp_notation.csv` présentes : pour ajouter un membre du jury, il suffit de déposer sa grille et de relancer `task`. Le prix du jury (coup de cœur) s'affiche dès qu'un fichier `prix_du_jury.csv` (colonnes `N°`, `Motivation`) est présent. Le rapport prend le nom et le type de chaque évaluateur dans `jury.csv`, et y affiche la grille comme « Reçue » ou « En attente ». Pour une grille absente de `jury.csv`, les noms de fichiers commençant par un nom de modèle (`opus`, `sonnet`, `haiku`, `gpt`, etc.) sont classés « Modèle IA », les autres « Membre du jury ».
