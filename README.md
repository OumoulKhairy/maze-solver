# 🧩 Résolution de Labyrinthe — ESP Dakar, Master 1

## 👥 Répartition du travail

| Étudiant | Responsabilité | Fichiers |
|---|---|---|
| **Étudiant 1** | Structures de données & Chargement | `Cell.java`, `Maze.java`, `MazeLoader.java`, `MazeGenerator.java` |
| **Étudiant 2** | Algorithmes DFS & BFS | `MazeSolver.java`, `SolverResult.java`, `DFSSolver.java`, `BFSSolver.java` |
| **Étudiant 3** | Affichage, comparaison & GUI | `MazeDisplay.java`, `PerformanceComparator.java`, `MazeGUI.java`, `Main.java` |

---

## 📁 Structure du projet

```
labyrinthe/
├── src/
│   ├── Cell.java               # Représentation d'une case
│   ├── Maze.java               # Structure du labyrinthe (matrice 2D)
│   ├── MazeLoader.java         # Chargement/Sauvegarde fichier
│   ├── MazeGenerator.java      # Génération aléatoire (Recursive Backtracker)
│   ├── MazeSolver.java         # Interface commune des algorithmes
│   ├── SolverResult.java       # Résultat d'un algorithme
│   ├── DFSSolver.java          # Depth First Search
│   ├── BFSSolver.java          # Breadth First Search
│   ├── MazeDisplay.java        # Affichage console coloré
│   ├── PerformanceComparator.java  # Comparaison DFS vs BFS
│   ├── MazeGUI.java            # Interface graphique Swing
│   └── Main.java               # Point d'entrée
├── labyrinthes/
│   └── exemple1.txt            # Labyrinthe exemple
├── compile_and_run.sh          # Script de compilation
└── README.md
```

---

## 🚀 Compilation et exécution

### Prérequis
- Java JDK 8 ou supérieur

### Compiler
```bash
mkdir out
javac -d out src/*.java
```

### Lancer en mode console
```bash
java -cp out Main
```

### Lancer en mode GUI (interface graphique)
```bash
java -cp out Main --gui
```

### Ou utiliser le script
```bash
chmod +x compile_and_run.sh
./compile_and_run.sh          # mode console
./compile_and_run.sh --gui    # mode graphique
```

---

## 📐 Format du fichier labyrinthe

```
#######
#S===E#
#=###=#
#=====#
#######
```

| Caractère | Signification |
|---|---|
| `#` | Mur |
| `=` | Passage libre |
| `S` | Point de départ |
| `E` | Point d'arrivée |
| `+` | Chemin solution (affiché après résolution) |
| `.` | Case visitée |

---

## 🧠 Algorithmes implémentés

### DFS (Depth First Search)
- Utilise une **pile** (`Stack`)
- Explore en profondeur avant de revenir en arrière
- **Ne garantit pas** le chemin le plus court
- Avantage : faible consommation mémoire

### BFS (Breadth First Search)
- Utilise une **file** (`Queue`)
- Explore niveau par niveau
- **Garantit** le chemin le plus court
- Avantage : optimal pour trouver la solution minimale

---

## 📊 Comparaison des algorithmes

| Critère | DFS | BFS |
|---|---|---|
| Structure | Pile (Stack) | File (Queue) |
| Chemin optimal | ❌ Non garanti | ✅ Garanti |
| Mémoire | Faible | Plus élevée |
| Vitesse | Variable | Systématique |

---

## 🎨 Interface graphique

L'interface Swing permet de :
- 🎲 Générer un labyrinthe aléatoire de taille variable
- 📂 Charger un labyrinthe depuis un fichier `.txt`
- 🔍 Résoudre avec DFS (affichage coloré)
- 🌊 Résoudre avec BFS (affichage coloré)
- 📊 Comparer les deux algorithmes côte à côte

---

## 📧 Livraison

- **Mail** : envoitp@gmail.com
- **Objet** : `Projet_Labyrinthe_Gx` (x = numéro du groupe)
- **Contenu** : Lien GitHub + Lien vidéo YouTube (max 10 min)
- **Date limite** : 12/04/2026
