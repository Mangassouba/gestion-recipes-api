## Gestion de Recettes - Application Node.js

## Description

Cette application est un gestionnaire de recettes de cuisine développé avec Node.js et Express pour le backend, ainsi que MySQL pour la gestion des données. Elle permet de créer, récupérer, mettre à jour et supprimer des recettes. L'application utilise Jasmine pour les tests unitaires afin de valider les différentes fonctionnalitésUD (Create, Read, Update, Delete). en utilisant expressjs et mysql pour la gestion de la base de données.

## prérequis

Avant de démarrer, assurez-vous d'avoir installé les logiciels suivants :

- Node.js (version 14+)
- MySQL (version 5.7+)
- npm (le gestionnaire de paquets Node.js)

## Technologies Utilisées

- **Node.js** : Plateforme JavaScript côté serveur.
- **Express** : Framework web pour Node.js.
- **MySQL** : Système de gestion de base de données relationnelle.
- **Jasmine** : Framework de tests pour JavaScript.
- **Postman** : Utilisé pour tester l'API.

## Installation

1. Clonez le dépôt sur votre machine locale :

```
git clone https://github.com/Mangassouba/gestion-recipes-api.git
```

2. Accédez au répertoire du projet :

```
cd gestion-recipes-api
```

3. Installez les dépendances du projet :

```
npm install
```

## Utilisation

Pour démarrer l'application, exécutez la commande suivante :

```
 npm start
```

## Configuration de la base de donnée

dans le projet le fichier .env.example faut le renommé en .env et ajouter vos identifiant pour pouvoir se conncter à la base de donnée

pour se connecter sur la machine local et faire de test  dans le fichier .env mettez :

    DB_HOST=localhost

pour se connecter sur docker et faire de test  dans le fichier .env mettez 

    DB_HOST=db

## Endpoints de l'API

## GET /recipes

- Description : Récupère toutes les recettes.

- Réponse

        [
                {
                    "id": 2,
                    "titre": "Crêpes classiques",
                    "type": "Dessert",
                    "ingredient": "250g de farine, 3 ?ufs"
                },
                {
                    "id": 3,
                    "titre": "Soupe de légumes",
                    "type": "Entrée",
                    "ingredient": "3 carottes, 2 pommes de terre"
                }
            ]

## POST /recipes

- Description : Crée une nouvelle recette.

- Corps de la requête :

```
{

"titre": "Salades Césars",
"type": "Entrée",
"ingredient": "Laitue, Poulet, Parmesan, Croutons"

    }
```

- Reponse:

```
{
  "message": "Recette ajouter avec succès"
}
```

## PUT /recipes/id

- Description : Met à jour une recette existante.

- Corps de la requête :

          {
          "titre": "Salade Césars",
          "type": "Entrée",
          "ingredient": "Laitue, Poulet, Parmesan, Croutons"
          }

- Réponse :

```

{
  "message": "Recette mise à jour avec succès"
}
```

## DELETE /recipes/id

- Description : Supprime une recette par ID.
- Réponse :

```
{
  "message": "Recette supprimée avec succès"
}
```

## les tests unitaires

L'application utilise Jasmine pour les tests unitaires. Pour exécuter les tests, utilisez la commande suivante :

```
npm test
```

Exemple:

![](/src/assets/images/img%20test.JPG)

Les tests incluent la vérification des fonctionnalités principales telles que la création, la récupération, la mise à jour, et la suppression des recettes.

## Recherche des erreurs et formatage de code

- Analyse du code: recherche des erreurs dans le code

      npm run lint

- Formatage de code

      npm run format

## Containerisation avec Docker

- Construction de l'image

      docker build -t api-gestion-recipes .

 - Lien vers l'image DockerHub : [Image Docker](https://hub.docker.com/r/mangassouba15/api-gestion-recipes)

- Telecharger l'image:

       docker pull mangassouba15/api-gestion-recipes

- Lancer les contenaires

      docker-compose up --build

- Lancer les conteneurs Docker

      docker-compose up -d

## Auteur

[Hama Houllah Mangassouba](https://github.com/Mangassouba)
