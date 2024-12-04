# Utilisation de l'image officielle Node.js
FROM node:18-alpine

# Installation de wget pour le healthcheck
RUN apk add --no-cache wget

# Création et définition du répertoire de travail
WORKDIR /usr/src/app

# Copie des fichiers package.json et package-lock.json
COPY package*.json ./

# Installation des dépendances
RUN npm install

# Copie du code source
COPY . .

# Exposition du port 3000
EXPOSE 3000

# Commande pour démarrer l'application
CMD ["npm", "start"]
