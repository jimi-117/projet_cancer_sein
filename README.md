Contexte du projet
Le Breast Cancer Wisconsin (diagnostic) Dataset est un jeu de données classique du Machine Learning. Il est composé de 569 exemples, chaque exemple étant défini par 30 caractéristiques ; ces caractéristiques correspondent principalement aux propriétés géométriques mesurées sur les cellules issues de la biopsie. Chaque exemple est classé dans la catégorie "Benign" (n=357) si la tumeur est bénigne et dans la catégorie "Malignant" (n=212) si la tumeur est maline. Le nombre de catégories de la classification est de 2, on parle alors de classification binaire. La finalité de ce travail est ainsi d'entrainer un modèle de Machine Learning à identifier le type de tumeur (bénigne ou maline) en fonction des propriétés géométriques mesurées sur les cellules issues de la biopsie.

Dans le but de tenir nos objectifs, nous allons tout d'abord construire une présentation de type Powerpoint qui décrit les concepts de base de la classification binaire selon le plan suivant :

En quoi consiste la classification binaire ?
Qu'est-ce qu'une matrice de confusion ?
Qu'est-ce qu'un faux négatif ? un vrai négatif ? un faux positif ? un vrai positif ?
Qu'est-ce que le taux de classification (accuracy) ?
Qu'est-ce que le rappel (recall) ?
Qu'est-ce que la précision (precision) ?
Qu'est-ce que le F1-score ?
Qu'est-ce qu'une courbe ROC ?
Qu'est-ce que l'Area Under the Curve (AUC) ?
Dans une seconde présentation de type Powerpoint, décrire :

Qu'est-ce qu'une régression logistique ?
Qu'est-ce que le Feature Scaling ?
A quoi sert-il et quels sont ses avantages ?
Qu'est-ce que la normalisation des données ?
Qu'est-ce que la standardisation des données ?
Comment l'utilise-t-on lorsque l'on a un jeu de train et un jeu de test ?
Nous sommes maintenant armé.e.s pour implémenter en langage Python l'entrainement d'un modèle de type régression logistique à diagnostiquer l'absence ou la présence d'un cancer du sein. Pour cela, nous allons construire un Jupyter Notebook selon le plan suivant :

Importation des librairies Python nécessaires à la résolution du problème
Chargement des données du Breast Cancer Wisconsin (diagnostic) Dataset
Mise au format Numpy des données
NB Par défaut, ce jeu de données représente les patients malades par la valeur 0 et les patients sains par la valeur 1, ce qui est l'inverse de ce qui se fait traditionnellement en santé. Nous devons donc relabelliser les patients sains par la valeur 0 et les patients malades par la valeur 1.
Echantillonnage des données
NB test_size = 113
Afficher sous forme d'histogrammes la distribution du jeu de données initial, du jeu de train et du jeu de test en fonction de chaque catégorie (bénigne et maline)
Effectuer le Feature Scaling
Entrainer le modèle de régression logistique
NB model = LogisticRegression(C = 0.1, max_iter = 10000)
Calculer et afficher les performances obtenues sur le jeu d'apprentissage
Matrice de confusion
Taux de classification, Rappel, Précision et F1-Score
Courbe ROC, AUC
Calculer et afficher les performances obtenues sur le jeu de test
Matrice de confusion
Taux de classification, Rappel, Précision et F1-Score
Courbe ROC, AUC
Bravo, nous sommes maintenant à même de proposer un outil d'aide à la prise de décision clinique au corps médical !
