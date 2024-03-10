# .github
Web application allowing you to borrow a book

# Functional requirements
- Display all movies paginated
- Display catalog base on recommendations (favourites genders, rates ...)
- Search in the movie catalog
- Each user can suggest the addition of new movie
- Each user can rate a film after borrowing, and add some comments
- borrowing and return a movie
- Type of users: visitor, borrower,admin
- Admin user can add a new movie
- Build analytics base on movie and users
- The borrowing price depends on borrowing duration
- Discount code base on movie or specific users
- Penalties for users who fail to return a movie on time
- Notify user when borrowing deadline is being reached
- Only one copy of the movie may be borrowed by the same user
- quand l'utilisateur met le film dans son papier, il est verrouiller pendant un certain temps
- User can add a movie to whitelist, rate and comment a movie
- rgpd

# Non functional requirements
- Initialize catalog database using [Movielens](https://grouplens.org/datasets/movielens/)
- Expecting 300.000 movies
- Promotional trailier: 50Mb per movie => 15GB
- 1M comments and rating on movies
- 10.000 active users

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
