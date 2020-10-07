FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y nodejs
RUN apt-get install -y npm
# RUN npm install -g yarn

# COPY . /app

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json ./

RUN npm install

# bundle app’s source code inside the Docker image
COPY . .
# WORKDIR /bin

# EXPOSE 3000

# ENTRYPOINT ["node"]
CMD ["npm", "start"]
