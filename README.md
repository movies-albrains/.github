# .github
Web application allowing you to borrow a book

# Functional requirements
- Display all movies paginated
- Display catalog base on recommendations (favourites genders, rates ...)
- Search in the movie catalog
- Each user can suggest the addition of new movie
- Each user can rate a film after borrowing, and add some comments
- borrowing and return a movie
- pré-commande de film qui arrive bientôt sur la plateforme, ou qui va bientôt être retourné
- Type of users: visitor, borrower,admin
- Build analytics base on movie and users
- The borrowing price depends on borrowing duration
- Discount code base on movie or specific users
- Penalties for users who fail to return a movie on time
- l'utilisateur recoit des notifications par mail lorsque l'emprunt est effectif; il est prévénu quand la date limite d'emprunt arrive
- Only one copy of the movie may be borrowed by the same user
- quand l'utilisateur met le film dans son papier, il est verrouiller pendant un certain temps
- l'utilisateur a la possiblité de liker ou mettre des films dans une liste de souhaits
- l'admnistrateur peut ajouter de nouveau film
- certaines données de l'utilisateur sont conservées pendant une durée déterminée (rgpd)

## pour plus tard
- l'utilisateur doit fournir l'adresse à laquelle on envoit le film version disque, ou le mail auquel envoyer la version en ligne
- pour un film en ligne, le lien du film est disponible pendant une durée déterminée

# Non functional requirements
- Initialize catalog database using [Movielens](https://grouplens.org/datasets/movielens/)
- Expecting 300.000 movies
- Promotional trailier: 50Mb per movie => 15GB
- 1M comments and rating on movies
- 10.000 active users
- **Sécurité:** Implémentez des mesures de sécurité robustes pour protéger les données des utilisateurs, y compris les informations de compte et les préférences de visionnage.
- **Extensibilité:** Concevez l'application pour permettre facilement l'ajout de nouvelles fonctionnalités et l'expansion de la vidéothèque sans compromettre la stabilité.
- **Politiques de confidentialité:** Respectez les normes de confidentialité des données en mettant en œuvre des politiques de confidentialité claires et en permettant aux utilisateurs de contrôler leurs informations personnelles.

# Workflows

## [User registration](./workflows/signup.md)
## [Authenticate user](./workflows/signin.md)
## [Add a movie](./workflows/add-movie.md)
## Add a movie to whitelist
## Add a movie to the cart
## [Borrowing movie](./workflows/borrow.md)
## [Return a movie](./workflows/return.md)
## [Delete a movie](./workflows/remove-movie.md)
## Discount code
## Ad campaign
## Suggest a movie
## Delete account
## Report a movie
