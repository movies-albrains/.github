# .github
Web application allowing you to borrow a book

# Spécifications fonctionnelles
- Présentation d'un catalogue de film, en fonction des recommandations relatives aux meilleurs notes et aux genres préférés
- rechercher un film dans le catalogue
- possibilité de noter un film et de faire des commentaires
- emprunter et retourner un film
- Gestion des utilisateurs: l'emprunteur, l'admin
- Anaylyses de données: analyse du comportement des utilisateurs, la popularité des films
- l'emprunt d'un livre est payant, et cela dépend de la durée de l'emprunt
- possibilité de donner une remise ou code promo à un utilisateur, ou associé à un film
- au dela de la période d'emprunt, l'emprunteur peut recevoir des pénalités si cela arrive souvent
- l'utilisateur recoit des notifications par mail lorsque l'emprunt est effectif; il est prévénu quand la date limite d'emprunt arrive
- un utilisateur ne peut emprunter qu'un seul exemplaire du même film
- quand l'utilisateur met le film dans son papier, il est verrouiller pendant un certain temps
- l'utilisateur a la possiblité de liker ou mettre des films dans une liste de souhaits

## pour plus tard
- l'utilisateur doit fournir l'adresse à laquelle on envoit le film version disque, ou le mail auquel envoyer la version en ligne
- pour un film en ligne, le lien du film est disponible pendant une durée déterminée

# Spécifications non fonctionnelles
- Les films vont êtres initialisées en utilisant le script disponible sur la page [Movielens](https://grouplens.org/datasets/movielens/)
- Les utilisateurs font régulièrement des recherches, ce qui demande du cpu
- On a beaucoup de données de films, ratings, commentaires...
- 
