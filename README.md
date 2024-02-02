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
- l'admnistrateur peut ajouter de nouveau film
- certaines données de l'utilisateur sont conservées pendant une durée déterminée (rgpd)

## pour plus tard
- l'utilisateur doit fournir l'adresse à laquelle on envoit le film version disque, ou le mail auquel envoyer la version en ligne
- pour un film en ligne, le lien du film est disponible pendant une durée déterminée

# Spécifications non fonctionnelles
- Les films vont êtres initialisées en utilisant le script disponible sur la page [Movielens](https://grouplens.org/datasets/movielens/)
- Les utilisateurs font régulièrement des recherches, ce qui demande du cpu
- On a beaucoup de données de films, ratings, commentaires...
- près de 1000 utilisateurs connectés simultanément
- tolérence de perte de messages ??
- configurer la retention des données (avec aws config ?)
- **Performance:** l'application vidéothèque offre une navigation fluide et une réponse rapide, même avec un grand nombre de vidéos répertoriées
- **Sécurité:** Implémentez des mesures de sécurité robustes pour protéger les données des utilisateurs, y compris les informations de compte et les préférences de visionnage.
- **Compatibilité:** Garantissez la compatibilité de l'application avec divers dispositifs (smartphones, tablettes, ordinateurs) et systèmes d'exploitation (iOS, Android, Windows, etc.).
- **Accessibilité:** Assurez-vous que l'application est accessible à tous les utilisateurs, y compris ceux ayant des besoins spécifiques tels que des limitations visuelles ou auditives.
- **Extensibilité:** Concevez l'application pour permettre facilement l'ajout de nouvelles fonctionnalités et l'expansion de la vidéothèque sans compromettre la stabilité.
- **Interactivité utilisateur:** Fournissez une interface utilisateur conviviale et intuitive, favorisant une expérience utilisateur positive et encourageant l'exploration du contenu.
- **Efficacité du stockage:** Optimisez l'utilisation de l'espace de stockage pour minimiser l'empreinte de l'application tout en conservant une performance optimale.
- **Gestion des erreurs:** Mettez en place des mécanismes efficaces pour gérer les erreurs, fournir des messages d'erreur clairs et guider les utilisateurs en cas de problème.
- **Évolutivité des serveurs:** Si l'application utilise des serveurs, assurez-vous qu'ils sont dimensionnés pour gérer la charge prévue, avec des mécanismes d'évolutivité en place.
- **Politiques de confidentialité:** Respectez les normes de confidentialité des données en mettant en œuvre des politiques de confidentialité claires et en permettant aux utilisateurs de contrôler leurs informations personnelles.
- **Gestion des APIs:** fournir des api claires et compréhensibles, bien documentées, permettant une intégration future avec un api management.

# Workflows
Description de l'ensemble des principaux workflow de l'application.

## Inscription d'un utilisateur
- Sur l'interface principale, l'utilisateur clique sur le bouton d'inscription
- Il remplit un formulaire avec son nom, prénom, e-mail, mot de passe. L'email est unique pour un utilisateur
- L'utilisateur a aussi la possibilité de se connecter avec Gmail et Facebook
- Après validation, l'utilisateur recoit un mail avec un lien de confirmation
- Une fois qu'il a cliqué sur le lien, il arrive sur une page qui lui demande de choisir la langue et les genres de film préférés
- Enfin il arrive sur la page principale avec des suggestions de films lui correspondant

## Connexion de l'utilisateur
- Sur l'écran principal, l'utilisateur clique sur connexion
- il saisit son login et mot de passe, puis valide
- il peut aussi se connecter avec Gmail ou Facebook
- une fois validé, il est renvoyé vers l'écran d'accueil

## Écran principal
- l'écran principal affiche la liste des films recommandés pour l'utilisateur s'il est  connecté, ou les films du moment si on n'a pas d'utilisateur connecté
