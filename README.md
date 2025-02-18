# TP2_Microservices
## Description
Cette API RESTful permet de gérer un registre de personnes. Elle prend en charge les opérations CRUD (Créer, Lire, Mettre à jour, Supprimer) en stockant les données dans une base SQLite3.  

L’API est développée avec **Node.js** et utilise **Express.js** pour la gestion des routes.

## Technologies utilisées
- **Node.js** : Environnement d'exécution JavaScript côté serveur.
- **Express.js** : Framework minimaliste pour Node.js facilitant la gestion des requêtes HTTP.
- **SQLite3** : Base de données relationnelle légère, adaptée aux applications de petite et moyenne envergure.

## Prérequis
- **Node.js** installé sur votre machine.
- **Postman** (ou tout autre outil de test API) pour envoyer des requêtes HTTP.

## Installation

1. **Cloner le dépôt :**
   ```sh
   git clone https://github.com/TON-UTILISATEUR/NOM-DU-REPO.git
   cd NOM-DU-REPO
Initialiser le projet Node.js :

sh
Copier
Modifier
npm init -y
Installer les dépendances :

sh
Copier
Modifier
npm install express sqlite3
Démarrer le serveur :

sh
Copier
Modifier
node index.js
Le serveur s'exécutera sur http://localhost:3000.

Structure du projet
bash
Copier
Modifier
/mon-projet-api
│── database.js      # Configuration de la base SQLite3
│── index.js         # Serveur Express.js et routes API
│── package.json     # Dépendances et scripts du projet
│── README.md        # Documentation
Routes de l'API
1. Récupérer toutes les personnes
GET /personnes
Réponse :

json
Copier
Modifier
{
  "message": "success",
  "data": [
    { "id": 1, "nom": "Bob", "adresse": "123 Rue A" },
    { "id": 2, "nom": "Alice", "adresse": "456 Rue B" }
  ]
}
2. Récupérer une personne par ID
GET /personnes/:id
Exemple : /personnes/1
Réponse :

json
Copier
Modifier
{
  "message": "success",
  "data": { "id": 1, "nom": "Bob", "adresse": "123 Rue A" }
}
3. Ajouter une nouvelle personne
POST /personnes
Corps de la requête :

json
Copier
Modifier
{
  "nom": "David",
  "adresse": "789 Rue C"
}
Réponse :

json
Copier
Modifier
{
  "message": "success",
  "data": { "id": 3 }
}
4. Mettre à jour une personne
PUT /personnes/:id
Exemple : /personnes/1
Corps de la requête :

json
Copier
Modifier
{
  "nom": "Robert",
  "adresse": "999 Boulevard D"
}
Réponse :

json
Copier
Modifier
{
  "message": "success"
}
5. Supprimer une personne
DELETE /personnes/:id
Exemple : /personnes/2
Réponse :

json
Copier
Modifier
{
  "message": "success"
}
Tests avec Postman
Ouvrir Postman.
Créer une nouvelle collection.
Configurer les requêtes GET, POST, PUT, DELETE en respectant les formats décrits ci-dessus.
Exécuter les requêtes et vérifier les réponses JSON.
Améliorations possibles
Ajout d’une gestion avancée des erreurs.
Validation des données avec Joi ou express-validator.
Implémentation de tests unitaires avec Jest.
Ajout d’une interface web pour la gestion des personnes.
Déploiement sur un serveur cloud.
Licence
Ce projet est sous licence MIT.

yaml
Copier
Modifier

---

Cette version est claire, bien structurée et professionnelle. Elle ne contient ni emojis ni tableaux et respecte les standards de documentation des APIs. 

Tu peux l'ajouter à ton dépôt GitHub avec ces commandes :  

```sh
git add README.md
git commit -m "Ajout du README"
git push origin main
