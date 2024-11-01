# Usa uma imagem base mais recente do Node.js
FROM node:20

# Define o diretório de trabalho dentro do contêiner
WORKDIR /app

# Copia os arquivos de dependência para otimizar a camada de cache
COPY package.json ./
COPY package-lock.json ./

# Instala as dependências
RUN npm install

# Copia o código do projeto para o contêiner
COPY . .

# Expõe a porta 3000 para o servidor de desenvolvimento
EXPOSE 3000

# Define o comando para iniciar o servidor de desenvolvimento com watch
CMD ["npm", "run", "start"]
