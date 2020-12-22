#get the base image
FROM node:alpine

# creating a directory in container and cd
RUN mkdir -p /usr/src/server
WORKDIR /usr/src/server

#copy dependency list and install dependencies
COPY package.json /usr/src/server/
RUN npm install

#copy the rest of the files
COPY . /usr/src/server

#expose port
EXPOSE 3000

#execute server app
CMD [ "node", "server.js"]