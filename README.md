# Strapi application

## API que va consommer l'appilication restaurant_app_ionic

### Les collections :

* Users : contient les utilisateurs, les champs oblogatoires au moment de la création sont :
  * username
  * email
  * password
  * nom
  * prenom
  * adresse
  * telephone
* Plats : contient les différents plats, les champs oblogatoires au moment de la création sont :
  * nom
  * prix
  * description
* Commandes : contient les commandes effectuées par les utilisateurs, voici ses champs :
  * Users
  * Plats
  
