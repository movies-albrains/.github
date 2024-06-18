# Architecture document

## Table of contents
1. [Summary](#summary)
2. [Requirements](#requirements)

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
- User can add a movie to whitelist, rate and comment a movie
- rgpd

### Non functional requirements
- Initialize catalog database using [Movielens](https://grouplens.org/datasets/movielens/)
- Expecting 300.000 movies
- Promotional trailier: 50Mb per movie => 15GB
- 1M comments and rating on movies
- 10.000 active users