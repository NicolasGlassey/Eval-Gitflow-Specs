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
*   2bd4e83 (origin/develop, develop) Merge tag '1.1.0' into develop
|\
| *   8db3d80 (HEAD -> main, tag: 1.1.0, origin/main, origin/HEAD) Merge branch 'release/1.1.0'
| |\
| | * f55480c refactor:
| | * 20693de fix:
| |/  
|/|
* |   0bf5395 Merge branch 'feature/f2' into develop
|\ \  
| * | aef0b76 refactor
| * | ffc9f05 fix:
| * | ff5bae9 feat:
| * | 8d7d38f test:
|/ /  
* | 03b8304 Merge tag '1.0.1' into develop
|\|
| *   bb5a0b4 (tag: 1.0.1) Merge branch 'hotfix/1.0.1'
| |\
| | * 96ba25f refactor:
| | * 2bffd96 fix:  
| | * 276e3a8 chore:
| | * 2ffba32 test: 
| |/
---------------------------------------------------- //point de départ
| * 8e4ea90 Update README.md
| * 677fb03 Update README.md
* |   a6020cb Merge branch 'feature/f1' into develop
|\ \
| |/
|/|
| * 8cfee9e refactor:
| * 65c5d31 feat:    
| * 57b4665 test:    
|/
* 108df61 chore:
```

## Modalités de livraison

* Une fois l'exercice terminé, synchroniser correctement votre dépôt local avec votre distant.
* Vous notifiez votre livraison à l'aide d'une issue (en "tag" l'enseignant), en intégrant le fichier "response.md" qui contiendra les commandes nécessaires pour recréer l'arbre demandé.
