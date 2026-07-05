# Projet FTML

Projet du cours FTML (Fundamentals of Machine Learning). Le dépôt regroupe les
exercices de simulation, les exercices de régression et de classification sur les
jeux de données fournis, et l'application au jeu de données CIFAR-10.

## Contenu

- `exercices_*` : Dossier contenant les notebooks (la partie mathématique est
dans le rapport)
- `misc` : Éléments éparses de code et de rapport avant mise en forme du
repository
- `report.pdf` : Rapport associé au projet
- `report.tex` : Code source du rapport
- `requirements.txt` : Dépendances Python épinglées.

## Prérequis

Python 3.11 ou plus récent. Installation des dépendances dans un environnement
virtuel :

```bash
python -m venv .venv
source .venv/bin/activate        
pip install -r requirements.txt
```

L'utilisation du flag `--recursive` lors du git clone est nécessaire pour
récupérer les données du projet.

## Données

Les jeux de données ne sont pas versionnés (taille et fichiers fournis par le cours).
Il faut les placer manuellement avant d'exécuter les notebooks.

### CIFAR-10 (notebook `cifar_ex6_7.ipynb`)

Télécharger la version « CIFAR-10 python » depuis
<https://www.cs.toronto.edu/~kriz/cifar.html>, puis extraire l'archive de sorte à
obtenir l'arborescence suivante à la racine du projet :

```
data_cifar/cifar-10-batches-py/
    data_batch_1 ... data_batch_5
    test_batch
    batches.meta
```

### Données du projet (Exercices 4 et 5)

Les données de régression et de classification fournies avec le sujet sont attendues
sous `FTML/project/data/regression/` et `FTML/project/data/classification/`
(fichiers `X_train.npy`, `y_train.npy`, `X_test.npy`, `y_test.npy`). Le notebook
cherche ce dossier dans les répertoires parents ; adapter le chemin si besoin.

## Exécution

Ouvrir les notebooks avec Jupyter et exécuter les cellules dans l'ordre :

```bash
jupyter lab
```

## Rapport

Rapport commun concatenant la partie mathématique des exercices 1 à 3 et la
partie explication et analyse des exercices 6 et 7.
