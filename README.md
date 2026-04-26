
# MNIST - Réseau de Neurones via Numpy

Ce dépôt contient l'implémentation d'un **réseau de neurones dense à deux couches** entraîné sur le dataset **MNIST**, réalisée **from scratch** avec NumPy uniquement (sans PyTorch, ni TensorFlow).

Le projet a été développé à la suite de la lecture du livre **"Quand la machine apprend"** de [Yann LeCun](https://fr.wikipedia.org/wiki/Yann_LeCun) et s'inspire d'une vidéo pédagogique de [Samson Zhang](https://youtu.be/w8yWXqWQYmU?si=CXMov6Z_KBHAdZH9).

<br/>

## 📌 Objectifs

| Objectif | Description |
|---|---|
| 🧠 **Comprendre le deep learning** | Implémenter un réseau de neurones sans abstraction de haut niveau |
| 📐 **Maîtriser les maths** | Propagation avant, rétropropagation, descente de gradient |
| 📊 **Classifier des images** | Reconnaître les chiffres manuscrits 0–9 avec une haute précision |

<br/>

## 🏗 Architecture du Réseau

```
Entrée (784)  →  Couche cachée (10, ReLU)  →  Couche de sortie (10, Softmax)
```

| Couche | Taille | Activation |
|---|---|---|
| Entrée | 784 (28×28 pixels) | — |
| Couche cachée | 10 neurones | ReLU |
| Couche de sortie | 10 neurones (0–9) | Softmax |

**Optimisation :** Descente de gradient avec rétropropagation (cross-entropie catégorielle)

<br/>

## 🗂 Structure du Projet

| Fichier | Contenu |
|---|---|
| [`mnist.ipynb`](mnist.ipynb) | Notebook principal : chargement, entraînement, évaluation |
| [`MNIST_CSV/mnist_train.csv`](MNIST_CSV/) | Données d'entraînement (60 000 images) |
| [`MNIST_CSV/mnist_test.csv`](MNIST_CSV/) | Données de test (10 000 images) |

<br/>

## 🛠 Installation et Utilisation

### Prérequis

- Python 3.8+
- Jupyter Notebook ou VS Code avec l'extension Python

### Installation

```bash
# Cloner le dépôt
git clone https://github.com/sacha-sz/MNIST-Scratch.git
cd MNIST-Scratch

# Installer les dépendances
pip install numpy pandas matplotlib
```

### Données MNIST

Téléchargez les fichiers CSV depuis [Kaggle – MNIST in CSV](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv) et placez-les dans un dossier `MNIST_CSV/` à la racine du projet.

### Lancement

Ouvrez et exécutez le notebook [`mnist.ipynb`](mnist.ipynb) dans Jupyter ou VS Code.

<br/>

## 🧪 Résultats

Après entraînement (descente de gradient, α = 0.10) :

| Métrique | Valeur |
|---|---|
| Accuracy entraînement | ~85–90 % |
| Accuracy test | ~85–88 % |

*Les résultats peuvent varier légèrement selon l'initialisation aléatoire des poids.*

<br/>

## 🧰 Technologies Utilisées

| Technologie | Rôle |
|---|---|
| **NumPy** | Calcul matriciel (propagation avant/arrière, mise à jour des poids) |
| **Pandas** | Chargement des données CSV |
| **Matplotlib** | Visualisation des images et des résultats |

<br/>

## 📚 Références

- 📖 [*Quand la machine apprend*](https://www.odilejacob.fr/catalogue/sciences/informatique/quand-la-machine-apprend_9782738149312.php) - Yann LeCun (EAN : 9782738149312)
- 🎥 [Building a neural network FROM SCRATCH](https://youtu.be/w8yWXqWQYmU?si=CXMov6Z_KBHAdZH9) - Samson Zhang
- 📦 [Dataset MNIST in CSV](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv) - Kaggle

<br/>

## 📄 Licence

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

<br/>

## 👤 Auteur

- **[@sacha-sz](https://github.com/sacha-sz)**
