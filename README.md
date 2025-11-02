# Tensorflow_system_recommandation

# Système de Recommandation de Films
 Description du projet

Ce projet met en œuvre un système de recommandation de films à partir du jeu de données MovieLens.
L’objectif est de prédire les notes que les utilisateurs attribueraient à des films qu’ils n’ont pas encore visionnés, puis de leur proposer des recommandations personnalisées.

Le système repose sur une approche de filtrage collaboratif combinée à un modèle de deep learning pour modéliser les relations entre utilisateurs et films à partir de leurs historiques de notation.

# Données utilisées

Le projet exploite deux jeux de données principaux :

Ratings : contient les identifiants des utilisateurs, des films, et les notes attribuées.
Ce jeu de données sert à entraîner le modèle à prédire les évaluations.

Movies : contient les identifiants et les titres des films.
Il est utilisé pour afficher les titres correspondants lors de la génération des recommandations.

# Méthodologie

Prétraitement des données
Les jeux de données sont nettoyés et transformés.
Une matrice utilisateur–film est construite afin de représenter les notes sous forme de tableau.
Les données sont ensuite divisées en ensembles d’entraînement et de test.

# Modélisation
Le modèle repose sur un réseau de neurones séquentiel avec plusieurs couches denses et des couches de régularisation Dropout pour éviter le surapprentissage.
La fonction de perte utilisée est le MSE (Mean Squared Error), adaptée à la prédiction de valeurs continues.
L’optimiseur Adam est utilisé pour ajuster les poids du modèle.

# Entraînement et validation
Le modèle est entraîné sur l’ensemble d’entraînement et validé sur l’ensemble de test.
Les métriques suivies sont principalement l’erreur quadratique moyenne (MSE) et l’erreur absolue moyenne (MAE).

# Prédiction et recommandation
Le modèle prédit les films que chaque utilisateur est susceptible d’apprécier, en estimant les notes qu’il attribuerait aux films qu’il n’a pas encore vus.
Les films avec les notes prédites les plus élevées sont ensuite sélectionnés comme recommandations personnalisées.
Les titres correspondants sont récupérés à partir du jeu de données des films.
