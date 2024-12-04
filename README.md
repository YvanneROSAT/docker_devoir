# Docker Exercise avec Healthcheck

Ce projet est une application Node.js simple conteneurisée avec Docker et incluant un healthcheck.

## Structure du Projet

```
docker-exercise/
├── app/
│   ├── server.js
│   ├── package.json
│   └── Dockerfile
└── docker-compose.yml
```

## Fonctionnalités

- Serveur HTTP Node.js simple
- Endpoint principal retournant "Hello, Docker World!"
- Healthcheck sur l'endpoint `/health`
- Configuration Docker avec docker-compose

## Instructions d'Installation et d'Exécution

1. Cloner le projet
2. Se placer dans le répertoire du projet
3. Lancer l'application avec Docker Compose :
   ```bash
   docker-compose up --build
   ```

## Accès à l'Application

- Application principale : http://localhost:3000
- Endpoint de healthcheck : http://localhost:3000/health

## Vérification du Healthcheck

Pour vérifier l'état du healthcheck :
```bash
docker-compose ps
```
ou
```bash
docker inspect <container_id> | grep "Health"
```

## Arrêt de l'Application

Pour arrêter l'application :
```bash
ctrl + C
