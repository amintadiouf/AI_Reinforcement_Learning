# TD1- Exercice 4 : Programmation de BFS et DFS

Ce dossier contient mon travail réalisé pour l'exercice 4 du TD1 du
cours de AI and Reinforcement Learning.

## Objectif

L'objectif de cet exercice est d'implémenter en Python deux algorithmes
de recherche dans le fichier `search.py`:

-   la recherche en largeur (**BFS:Breadth-First Search**) ;
-   la recherche en profondeur (**DFS:Depth-First Search**).

L'exercice 4 utilise un environnement Pokémon dans lequel un personnage
doit trouver un chemin entre une position initiale et un Centre Pokémon.

## Structure du projet

``` text
exo4/
├── main.py
├── search.py
├── pokemon_game.py
├── requirements.txt
├── pokemon-sprites/
└── .gitignore
```

## Environnement de travail

Le projet est exécuté avec Python 3.12 et un environnement virtuel
Python.

### Création de l'environnement virtuel

``` bash
python3 -m venv .venv
```

### Activation de l'environnement virtuel

``` bash
source .venv/bin/activate
```

### Installation des dépendances

Une fois l'environnement virtuel activé :

``` bash
python -m pip install -r requirements.txt
```

### Exécution du programme

Depuis le dossier `Exo4` :

``` bash
python main.py
```

## Résultats obtenus

Lors de l'exécution avec la carte utilisée dans le td, les résultats
obtenus sont les suivants :

### BFS

BFS trouve le chemin :

``` text
(1, 9) → (2, 9) → (3, 9) → (4, 9) → (5, 9)
```

avec les actions :

``` text
down → down → down → down
```

Le coût du chemin est de **4**.

### DFS

DFS trouve le chemin :

``` text
(1, 9) → (2, 9) → (2, 10) → (2, 11) → (2, 12)
→ (3, 12) → (4, 12) → (5, 12)
→ (5, 11) → (5, 10) → (5, 9)
```

avec les actions :

``` text
down → right → right → right → down → down → down
→ left → left → left
```

Le coût du chemin est de **10**.

Ces résultats montrent que BFS trouve ici le chemin le plus court,
tandis que DFS trouve un chemin valide mais plus long.
