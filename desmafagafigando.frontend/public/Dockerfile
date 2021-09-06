FROM node:13.12.0-alpine

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json ./
COPY package-lock.json ./

RUN npm install --silent

COPY . ./

CMD ["npm", "start"]

# RUN THE COMMAND DOWN BELOW TO START THE CONTAINER
# docker run -it --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true desmafagafigando:dev
# later on you can access the site locally by browsing the address: http://localhost:3001