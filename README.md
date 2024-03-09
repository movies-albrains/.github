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
- Gestion des utilisateurs: l'emprunteur, l'admin
- Anaylyses de données: analyse du comportement des utilisateurs, la popularité des films
- l'emprunt d'un livre est payant, et cela dépend de la durée de l'emprunt
- possibilité de donner une remise ou code promo à un utilisateur, ou associé à un film
- au dela de la période d'emprunt, l'emprunteur peut recevoir des pénalités si cela arrive souvent
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
- 1M comments and rating on movies
- 10.000 active users
- **Sécurité:** Implémentez des mesures de sécurité robustes pour protéger les données des utilisateurs, y compris les informations de compte et les préférences de visionnage.
- **Extensibilité:** Concevez l'application pour permettre facilement l'ajout de nouvelles fonctionnalités et l'expansion de la vidéothèque sans compromettre la stabilité.
- **Interactivité utilisateur:** Fournissez une interface utilisateur conviviale et intuitive, favorisant une expérience utilisateur positive et encourageant l'exploration du contenu.
- **Efficacité du stockage:** Optimisez l'utilisation de l'espace de stockage pour minimiser l'empreinte de l'application tout en conservant une performance optimale.
- **Gestion des erreurs:** Mettez en place des mécanismes efficaces pour gérer les erreurs, fournir des messages d'erreur clairs et guider les utilisateurs en cas de problème.
- **Politiques de confidentialité:** Respectez les normes de confidentialité des données en mettant en œuvre des politiques de confidentialité claires et en permettant aux utilisateurs de contrôler leurs informations personnelles.

# Workflows
Description de l'ensemble des principaux workflow de l'application.

## [User registration](./workflows/signup.md)
## [Authenticate user](./workflows/signin.md)
## [Add a movie](./workflows/add-movie.md)
## Ajouter un film dans les favories
## Ajouter un film dans le panier
## [Emprunt de film](./workflows/borrow.md)
## [Retour de film](./workflows/return.md)
## Code promotionnel
## [Supprimer un film](./workflows/remove-movie.md)

## Code promotionnel

## Campagne de communication

## Suggérer un film

## Supprimer son compte

## Signaler un film
