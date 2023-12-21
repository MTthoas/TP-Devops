# Utiliser l'image officielle de Node.js comme base
FROM node:16

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers package.json et package-lock.json (ou yarn.lock si vous utilisez Yarn)
COPY package*.json ./

# Installer les dépendances du projet
RUN npm install

# Copier le reste des fichiers du projet dans le conteneur
COPY . .

# Exposer le port que Vite utilise (par défaut 3000, mais peut être différent selon votre configuration Vite)
EXPOSE 3000

# Commande pour exécuter le serveur de développement Vite
CMD ["npm", "run", "dev"]
