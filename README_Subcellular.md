# README pour TP_subcellular.ipynb
Ce notebook est une implémentation d'un modèle de classification pour la localisation subcellulaire des protéines, utilisant le jeu de données MultiLoc. L'objectif est de prédire la localisation subcellulaire des protéines à partir de leurs caractéristiques, en s'appuyant sur des réseaux de neurones convolutionnels et résiduels.

Auteur: Takwa Ben Radhia

## Description du Projet
Ce projet utilise le jeu de données MultiLoc pour entraîner et évaluer des modèles de deep learning capables de classifier la localisation subcellulaire des protéines. MultiLoc est une ressource populaire dans le domaine de la bioinformatique, fournissant des informations sur les caractéristiques protéiques et leurs localisations dans différentes compartiments cellulaires.

## Objectifs
1. Entraînement d'un modèle de réseau de neurones convolutionnel (CNN) pour la classification subcellulaire.
2. Implémentation d'un réseau de neurones résiduel (ResNet) pour une meilleure performance.
3. Validation croisée par K-fold pour évaluer la robustesse des modèles.
## Structure du Notebook
### 1. Importation des Bibliothèques
Les bibliothèques principales utilisées incluent numpy, pandas, tensorflow.keras pour la création et l'entraînement des modèles, ainsi que matplotlib et seaborn pour la visualisation des performances.

### 2. Chargement et Préparation des Données
- Les données sont téléchargées directement depuis des liens externes et extraites dans un dossier local dataset/.
- Le notebook charge les données d'entraînement et de validation à partir de fichiers .npz.
- Les classes sont encodées en one-hot, et une analyse de la distribution des classes est effectuée pour visualiser le déséquilibre des classes.
### 3. Modèle CNN (Convolutional Neural Network)
Un modèle CNN est défini avec les étapes suivantes :

- Convolutions 1D suivies de max-pooling et de dropout pour éviter le surapprentissage.
- Aplatissement des données et couche fully-connected pour la classification.
- Compilation avec l'optimiseur Adam et une fonction de perte categorical_crossentropy adaptée à la classification multi-classes.
### 4. Validation Croisée avec K-fold
Pour évaluer la performance du modèle de manière plus robuste, une validation croisée K-fold est implémentée. Les résultats de chaque fold sont enregistrés et visualisés.

### 5. Modèle ResNet (Residual Network)
Le notebook implémente également un modèle ResNet pour tirer parti de la profondeur du réseau sans risque de dégradations dues à des gradients instables.

- Des modules résiduels sont empilés pour renforcer la capacité d'apprentissage du modèle tout en facilitant la propagation du gradient.
- Le modèle est entraîné et évalué de manière similaire au CNN de base.
### 6. Visualisation des Performances
Des courbes d'accuracy et de loss sont tracées pour les ensembles d'entraînement et de validation afin de mieux comprendre la convergence des modèles et la stabilité de l'apprentissage. Une matrice de confusion est également générée pour évaluer la performance en termes de classification des différentes classes.

## Exécution du Notebook
1- Télécharger les données : Le notebook inclut un script pour télécharger et extraire automatiquement les fichiers du jeu de données MultiLoc.
2- Exécuter chaque cellule : Suivez les étapes du notebook pour importer les données, entraîner les modèles et visualiser les résultats.
3- Analyse des résultats : Observez les résultats de la validation croisée, les courbes d'entraînement et les matrices de confusion pour évaluer les performances des modèles.
## Conclusions et Améliorations Futures
Ce notebook fournit une solution initiale pour la classification subcellulaire à l'aide de modèles CNN et ResNet. Quelques pistes d'améliorations futures incluent :

- L'exploration de modèles plus profonds ou plus complexes pour améliorer la précision.
- L'ajout de techniques de régularisation et de gestion du déséquilibre des classes (par exemple, rééchantillonnage).
- Une analyse plus approfondie des erreurs de classification pour ajuster le modèle aux classes difficiles à prédire.




