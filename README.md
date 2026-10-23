# Les offres d'Oriane

Site statique qui liste les offres d'emploi d'Oriane (événementiel, communication, graphisme dans le sport et l'automobile), hébergé sur GitHub Pages.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | La page : design « pass d'accréditation », recherche, tri, filtres, suivi de candidature |
| `offres.json` | Les données : date de mise à jour, offres retenues (`offers`), offres écartées (`seen`) |
| `manifest.webmanifest` + `icons/` | Icône quand le site est ajouté à l'écran d'accueil du téléphone |
| `robots.txt` | Demande aux moteurs de recherche de ne pas indexer le site |

## Mise à jour

La veille quotidienne modifie uniquement `offres.json`, puis publie le changement (`git commit` + `git push`). GitHub Pages met le site à jour en une à deux minutes.

Pour corriger une offre à la main : modifier `offres.json`, vérifier que le JSON reste valide, puis `git commit` et `git push`.

## Champs d'une offre

`id`, `score` (1 à 5), `family` (`sport`, `auto` ou `event`), `city` (Le Mans, Nantes, Angers, Bordeaux, Vendée), `zone` (département), `title`, `employer`, `sector`, `about`, `location`, `contract`, `kind` (`CDI`, `CDD` ou `NA`), `dates`, `salary`, `salaryMonthly` (nombre ou `null`), `summary`, `posted` (AAAA-MM-JJ), `postedApprox`, `offerUrl`, `applyUrl`, `applyEmail` et `applySubject` (facultatifs), `missions`, `profile`, `pros`, `cons`, `extra` (facultatif), `added` (AAAA-MM-JJ, date d'ajout par la veille).

## Confidentialité

Le dépôt et le site sont publics : n'y mettre aucune coordonnée personnelle (email, téléphone, CV). Le suivi de candidature reste dans le navigateur du téléphone.
