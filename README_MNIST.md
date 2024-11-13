# Classification d'Images Bruitées de Chiffres - MNIST
## Description
Ce projet utilise des réseaux de neurones pour classifier des images de chiffres bruitées issues du jeu de données MNIST. Les modèles implémentés incluent des réseaux de neurones profonds (DNN) et des réseaux de neurones convolutifs (CNN), optimisés pour améliorer la précision de la classification.

## Auteur
Takwa Ben Radhia

## Structure du Notebook
### 1. Import des Bibliothèques
Les bibliothèques essentielles pour la manipulation des données, la création et l’entraînement des modèles de réseaux de neurones, et la visualisation des résultats (matplotlib, seaborn, numpy, keras, sklearn) sont importées.

### 2. Chargement et Prétraitement des Données
Les données de formation et de test sont chargées depuis des fichiers .npy et normalisées :

Affichage des Images : Visualisation de quelques exemples d'images de chiffres bruitées pour mieux comprendre le jeu de données.
Prétraitement : Les images sont aplaties (pour le DNN), normalisées, et les étiquettes sont encodées en one-hot.
### 3. Modèle Deep Neural Network (DNN)
Un modèle de réseau de neurones profond est construit en utilisant des couches denses avec des unités de Dropout pour réduire le sur-apprentissage :

Architecture : Plusieurs couches denses avec des fonctions d’activation ReLU et une sortie Softmax.
Entraînement : Le modèle est entraîné sur les données, et les courbes d’accuracy et de loss sont tracées pour analyser les performances.
Matrice de Confusion : Affiche la matrice de confusion sur l’ensemble de test pour visualiser les erreurs de classification.
### 4. Modèle DNN Amélioré
Le modèle DNN initial est ajusté avec des couches supplémentaires de normalisation par batch et d’autres hyperparamètres, comme le nombre d'epochs et le taux d'apprentissage. Malgré les modifications, les performances n’évoluent pas de manière significative.

### 5. Modèle Convolutional Neural Network (CNN)
Une architecture CNN est implémentée pour une meilleure extraction de caractéristiques à partir des images brutes :

Architecture : Inclut des couches de convolution et de pooling pour capturer les caractéristiques spatiales, avec une couche finale dense pour la classification.
Entraînement et Évaluation : Le modèle est entraîné et évalué, et les courbes d’accuracy et de loss sont visualisées.
Matrice de Confusion : Montre la performance en classification sur les données de test.
### 6. Modèle CNN Amélioré
Une architecture CNN plus complexe est construite avec des couches convolutives supplémentaires et une régularisation par Dropout, pour améliorer encore la précision du modèle.

### 7. Validation Croisée K-Fold
Pour évaluer la robustesse du modèle CNN, une validation croisée à 5 plis est effectuée. Les courbes d’accuracy et de loss pour chaque pli sont affichées pour évaluer la variance des performances sur des échantillons différents.

### Conclusion
Le modèle CNN présente de meilleures performances et une meilleure robustesse par rapport au DNN pour la classification des images bruitées du jeu de données MNIST.

## Installation et Exécution
Importer les bibliothèques : Assurez-vous que les bibliothèques nécessaires (keras, matplotlib, seaborn, sklearn) sont installées.
Charger les données : Assurez-vous d'avoir les fichiers train_images.npy, train_labels.npy, test_images.npy, et test_labels.npy.
Exécuter le notebook : Suivez chaque cellule pour charger les données, définir les modèles et visualiser les résultats.
## Résultats
Les performances du modèle CNN surpassent celles du DNN, et la validation croisée montre que le modèle n'est pas fortement dépendant des échantillons d'entraînement.
