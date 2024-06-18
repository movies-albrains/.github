# Architecture document

## Table of contents
1. [Summary](#summary)
2. [Requirements](#requirements)
3. [Domain design](#domain-design)

## Summary
- This document describes the MovieBrains application's architecture
- MovieBrains application help people to borrow blogbuster movie
- The application give informations about the movie's rate, comments, the most watched movie and so on
- A visitor can watch the movie catalog
- if a visitor is interested by a movie, he has to sign up before ordering the movie

## Requirements
### Users
- Platform administrator
- connected user
- visitor
### Functional requirements
- Display all movies using pagination
- Display catalog base on recommendations (favourites genders, rates ...)
- Search in the movie catalog
- Each user can suggest the addition of new movies
- Each user can rate a movie after returning, and add some comments
- borrowing and return a movie
- Admin user can add a new movie
- Build analytics base on movie and users
- The borrowing price depends on borrowing duration
- Discount code base on movie or specific users
- Penalties for users who fail to return a movie on time
- Notify user when borrowing deadline is being reached
- Only one copy of the movie may be borrowed by the same user
- rgpd

### Non functional requirements
- Initialize catalog database using [Movielens](https://grouplens.org/datasets/movielens/)
- Expecting 300.000 movies
- Promotional trailier: 50Mb per movie => 15GB
- 1M comments and rating on movies
- 10.000 active users

## Domain design
### Domains and sub domains
- **Business domain:** Borrowing movies
- **Core subdomains:** movie's catalog, inventory, order, exclusivity contract, movie analytics, recommendation engine, web application
- **Generic subdomains:** shipping, payment, authentication/authorisation
- **Support subdomains:** ad campaigns, discount, notification, security/confidentialité, social networks integration, movie streaming services integration, reporting, wishlist, profile, accounting, shopping cart, review (notes, commentaires, réactions)

### Context Map
![Context Map](../src-gen/movies-albrains_ContextMap.png)
![Precise Context Map ](../out/src-gen/movies-albrains_ContextMap/movies-albrains_ContextMap.png)
