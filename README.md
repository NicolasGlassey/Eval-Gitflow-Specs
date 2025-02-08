# GRP1 - Evaluation pratique 2024 - Gitflow

## Enoncé

Lors de cette épreuve, nous allons valider les compétences suivantes:

* utilisation des commandes git de base
* application correcte du git-flow (nvie)
* lecture et analyse d'un arbre (tree) produit par git-flow

## Moyens à disposition

| Critère    | Valeur |
| -------- | ------- |
| Accès internet | oui |
| Travail collaboratif | non |
| Temps à disposition | 45 min |

## Pondération et barême

Cette évaluation vaut pour 50% de la deuxième note du module.

Le barême est l'habituel [nbPtsObtenus/nbPtsMaximum]/5*1

---

## Préparation de votre environnement

* créer un fork du dépôt transmis par teams

```
via l'interface graphique de Github
```

!!! Forkez toutes les branches (main et develop)

* "cloner" votre dépôt

```
git clone <votreUrl>
```

* initialiser git-flow

```
git flow init
```

* mettez à jour la branche develop avec le dépôt distant (en étant sur la branche develop)

```
git pull
```

* copier le fichier "reponse.md" hors de votre dépôt local

## Etat de l'arbre

* Schéma Draw IO

![ProjectTree](./img/project-tree.svg)

* Les "commits" rouges sont ceux déjà présents. Les autres sont à produire par vos soins.

#### Critères d'évaluation

| Critère    | Valeur | Pondération |
| -------- | ------- | --- |
| Hotfix | Toutes les étapes sont présentes | 5pts |
| Feature F2 | Toutes les étapes sont présentes | 4pts |
| Release | Toutes les étapes sont présentes | 6pts |
| Chronologie des branches | Selon le schéma draw io   | 6pts |
| Bonnes pratiques de commits (préfixes) | Selon le schéma draw io   | 3pts |
| Bonus | Combien de branches doivent être présentes sur le dépôt à la fin ???   | 1pt |

---

## Arbre à obtenir à la fin du travail

```git
git log --graph --oneline --decorate --all
```

```
λ git log --graph --oneline --decorate --all
*   37334d3 (HEAD -> develop) Merge tag '1.1.0' into develop
|\
| *   fad3245 (tag: 1.1.0, main) Merge branch 'release/1.1.0'
| |\
| | * 914cdd8 refactor:
| | * 6ac15a7 test:
| |/
|/|
* |   3f22803 Merge branch 'feature/f2' into develop
|\ \
| * | 6147660 refactor:
| * | 63401fb fix:
| * | 2d58ecb feat:
| * | 2c9a2f9 test:
|/ /
* | cd409fe Merge tag '1.0.1' into develop
|\|
| *   5899bd8 (tag: 1.0.1) Merge branch 'hotfix/1.0.1'
| |\
| | * ee319ec refactor:
| | * 259fff5 fix:
| | * 259fff6 chore:
| | * f03107f test:
| |/

---------------------------------------------------- //point de départ

* |   c20b028 Merge branch 'feature/f1' into develop
|\ \
| |/
|/|
| * b839c2e refactor:
| * ffe54cd feat:
| * 6d0d436 test:
|/
* 9975104 chore:
```

## Modalités de livraison

* Une fois l'exercice terminé, synchroniser correctement votre dépôt local avec votre distant.
* Vous notifiez votre livraison à l'aide d'une issue (en "tag" l'enseignant), en intégrant le fichier "response.md" qui contiendra les commandes nécessaires pour recréer l'arbre demandé.
