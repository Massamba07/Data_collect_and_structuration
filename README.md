# Data_collect_and_structuration
Acquisition et structureation de données

Le but de cet exercice est de construire un conteneur de données qui contiendra des data sets concernant les 1000 films les mieux notés selon IMDB de 2000 à maintentant.

Question 1 
Extraction de données
Commencez par extraire les données dont vous aurez besoin pour répondre à la question posée. Vous pourrez combiner différentes méthodes pour extraires toutes les sources dont vous aurez besoin, comme par exemple:

télécharger des data sets accessibles en Open Data à partir de kaggle
scraper la page des 250 films les mieux notés d'IMDB
utiliser des API(s) existantes pour récupérer des informations manquantes
Réponse 1
Affichez dans les cellules ci-dessous les structures de données dans lesquelles vous avez récupéré les informations pertinentes et donnez quelques caractéristiques de chacun de ce(s) data set(s) (par exemple taille, valeurs uniques, min , max ...)

[ ]

Question 2 
Filtrage et structuration des données
Vous allez maintenant filtrer vos données pour vous assurer qu'elles correspondent aux critères fixés dans les consignes et les structures en 3 dataframes distincts décrits ci dessous.

Vous présenterez les variables que vous avez retenues et donnerez un aperçu de leur quantité de valeurs manquantes

Dataframe contenant des informations spécifiques au film :
Ce dataframe doit contenir à minima une colonne renseignant:

le titre du film
l'année de sa sortie en salle
la durée du film (runtime)
son genre
le nom de son réalisateur (director)
la liste des acteurs principaux
Et en bonus d'autres informations comme:

une description du film
une photo de l'affiche du film
Dataframe contenant des informations concernant la popularité du film :
Ce dataframe doit contenir à minima une colonne renseignant:

le nombre de votes d'utilisateurs pour ce film (échelle de 1 à 10)
la note moyenne des votes reçus (échelle de 1 à 10)
les recettes du film (en millions de $)
Et en bonus d'autres informations comme:

la note mediane des votes reçus (échelle de 1 à 10)
l'écart type des votes reçus
Dataframe contenant des informations concernant chaque acteur et réalisateur présents dans ces films :
Ce dataframe doit contenir à minima une colonne renseignant:

leur nom
leur pays de naissance
leur age
s'il est toujours vivant
son/ses métier(s) (a choisir parmi la liste: acteur, realisateur, producteur)
Et en bonus d'autres informations comme:

une photo

Afficher dans les cellules ci dessous les informations concernant les dataframes

Question 3 
Nettoyage des données
Realisez des opérations de nettoyage des données afin de rendre vos data sets le plus facilement exploitables. Vous réaliserez a minima les traitements suivants:

convertir les différents types de données rencontrées dans un format adapté pour faciliter les traitements futurs et gagner en RAM
vérification et/ou traitement des valeurs manquantes, des doublons (par exemple des noms identiques, ou écrits avec des orthographes différentes)
vérification et traitement des outliers

Question 4 
Agrégation et structuration des données
Vos données étant nettoyées, vous allez maintenant les structurez et les stocker dans un conteneur de données au format HDF5. Vous êtes libre d'architecturer votre conteneur comme vous le souhaitez créerez a minima deux groupes:

un groupe contenant les images que vous allez acquérir
un groupe pour chaque dataset
Affichez à minima, des informations concernant chaque groupe ainsi que les data sets qu'ils contient

Question 5 
Exploitation de vos données
A partir de votre conteneur de données HDF5 vous allez extraire, filtrer et agréger vos données pour répondre aux questions suivantes:

Quelle est la durée médiane des films ? 
Quels sont les notes moyennes des films par genre ?
Faites un graphique pour représenter la répartition des durées des films 
Quels sont les caractéristiques des films (genre, durée, ...) et acteurs (vivant ou décédé, age, métier, ...), classés dans les 5% des films les mieux notés ? 
