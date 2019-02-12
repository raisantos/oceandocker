FROM node:lts-alpine

# Instala um server http simples em node para servir o conteudo
RUN npm install -g http-server

# Faz com que a pasta app seja o diretorio de trabalho
WORKDIR /app

# Copia os arquivos de controle de dependencia do node
COPY package*.json ./

# Instala as dependencias do projeto
RUN npm install

# Copia o codigo fonte do projeto para o diretorio de trabalho
COPY . .

# Faz o build do projeto
RUN npm run build

# Expoe a porta 8080
EXPOSE 8080

# Inicia o servidor,servindo o resultado do build
CMD [ "http-server", "dist" ]