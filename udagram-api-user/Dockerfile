FROM node:12
# Create app directory
RUN rm -rf /usr/src/app
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
RUN rm -rf node_modules
RUN npm cache clean -f
# RUN rm -rf package-lock.json
COPY package*.json ./
RUN npm i 
# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]