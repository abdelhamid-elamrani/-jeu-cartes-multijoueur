# Jeu de cartes multijoueur

Application web permettant à plusieurs joueurs de créer et rejoindre des parties de cartes en ligne, avec synchronisation des actions en temps réel.

## Fonctionnalités

- Création et gestion de parties multijoueur
- Authentification des utilisateurs
- Gestion des joueurs et du classement
- Synchronisation des actions de jeu en temps réel avec WebSocket
- Chat entre les joueurs
- Persistance des données avec MySQL

## Technologies utilisées

### Backend
- Java 17
- Spring Boot
- Spring Data JPA
- REST API
- WebSocket
- Maven

### Frontend
- React

### Base de données
- MySQL

## Structure du projet

Le projet est composé de deux parties principales :

- `backend` : API Spring Boot et logique métier
- `frontend` : interface utilisateur React

## Lancement du projet

### Backend

```bash
cd backend
./mvnw spring-boot:run
```

### Frontend

```bash
cd frontend
npm install
npm start
```

Assurez-vous également d'avoir une instance MySQL configurée avant de lancer le backend.

## Auteur

Projet développé dans le cadre de ma formation en ingénierie.