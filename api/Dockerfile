FROM node:20-alpine

COPY package*.json ./

RUN npm install 

COPY . ./

# Port d'écoute de l'API
ENV PORT=3000

# Adresse de la base PostgreSQL : postgres://utilisateur:motdepasse@hôte:port/base
ENV DATABASE_URL=postgres://taskflow:taskflow@localhost:5432/taskflow

# Environnement : local ou production
ENV APP_ENV=local

# Version affichée par /health (en CI, elle est remplacée par le SHA court du commit)
ENV APP_VERSION=dev


CMD ["npm", "run", "dev"]