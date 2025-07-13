# Usa Node 18 LTS, stabile e compatibile con n8n
FROM node:18

# Crea la cartella di lavoro dentro il container
WORKDIR /app

# Copia package.json e package-lock.json per installare dipendenze
COPY package*.json ./

# Installa dipendenze
RUN npm install

# Copia tutto il resto dei file nel container
COPY . .

# Build (se serve, n8n lo richiede)
RUN npm run build

# Espone la porta di default di n8n
EXPOSE 5678

# Comando per avviare n8n
CMD ["npm", "start"]
