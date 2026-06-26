# Projet FTML

Projet du cours FTML (Fundamentals of Machine Learning). Le dépôt regroupe les
exercices de simulation, les exercices de régression et de classification sur les
jeux de données fournis, et l'application au jeu de données CIFAR-10.

## Contenu

- `exercices_1_3.ipynb` : vérifications numériques des exercices 1 à 3 (prédicteur
  de Bayes, prédicteur optimal selon la perte, estimateur sans biais de la variance).
- `exercices_4_5.ipynb` : exercice 4 (régression : OLS, Ridge, Lasso) et exercice 5
  (classification : régression logistique, k-NN, SVC), avec analyse des données,
  validation croisée et discussion des résultats.
- `cifar_ex6_7.ipynb` : exercices 6 et 7 sur CIFAR-10. Exercice 6 (classification
  supervisée : baselines, SVM, passage à l'échelle par Nyström) et exercice 7
  (apprentissage de représentations non supervisé : PCA, dictionnaire K-means).
- `rapport_cifar.tex` / `rapport_cifar.pdf` : rapport accompagnant les exercices 6 et 7.
- `requirements.txt` : dépendances Python épinglées.

## Prérequis

Python 3.11 ou plus récent. Installation des dépendances dans un environnement
virtuel :

```bash
python -m venv .venv
source .venv/bin/activate        # sous Windows : .venv\Scripts\activate
pip install -r requirements.txt
```

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

### Données du projet (notebook `exercices_4_5.ipynb`)

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

Le rapport des exercices 6 et 7 se compile depuis les sources LaTeX :

```bash
pdflatex rapport_cifar.tex
```

Le PDF compilé (`rapport_cifar.pdf`) est également présent dans le dépôt.
