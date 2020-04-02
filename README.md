# Strapi application

## Auteur : Alioune Harouna Kanoute. Classe : Master 2 GLSI

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
* Menu : correspond au menu du jour défini par l'administrateur, contient un composant qui est constitué d'une collection de plats.

### Les roles

* Admin(<h3>à ajouter au niveau de "Roles & Permissions" dans strapi </h3>) : qui correspond au role de l'administrateur, y ajouté les comptes utlisateurs correspondants. Autoriser ces actions :
  * create, delete, find, findone et update sur les collections Menus et Plats
  * find et delete sur la collection Commandes
  * upload sur la collection Upload
  * Dans users-permissions :
    * callback, connect sur la collection Auth
    * findone, me et update sur la collectin User
    
* Authenticated : qui correspond aux utilisateurs simples, tout compte créé y ajouté par défaut. Autoriser ces actions :
  * find sur la collection Menus
  * create, delete, find, findone et update sur les collections Commandes
  * upload sur la collection Upload
  * Dans users-permissions :
    * callback, connect et register sur la collection Auth
    * findone, me et update sur la collectin User
    
* Public : qui correspond aux accès public.  Autoriser ces actions :
  * find sur les collections Menus et Plats
  * Dans users-permissions :
    * connect et register sur la collection Auth
