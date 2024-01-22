FROM node:alpine

WORKDIR /usr/src/app

# copy the package.json files from local machine to the workdir in container
COPY package*.json ./

# run npm install in our local machine
RUN npm install

# copy the generated modules and all other files to the container
COPY . .

#Ativando as linhas abaixo, o retorno é sempre 502. O contêiner não fica rodando o "node index.js".
#ENV DOCKERIZE_VERSION v0.7.0

#RUN apk add --no-cache wget
#RUN wget -O - https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz | tar xzf - -C /usr/local/bin
#RUN apk del wget

EXPOSE 5000

CMD [ "node", "index.js" ]