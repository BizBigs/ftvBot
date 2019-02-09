# Use an official node runtime as a parent image
FROM node:10

# Set the working directory to /home/app
WORKDIR /var/www/app

# Bundle app source
COPY src/ /var/www/app
COPY /docker/node/package.json /var/www/app

# If you are building your code for production
# RUN npm install --only=production
RUN npm install

# Make port 8000 available to the world outside this container
EXPOSE 8080

RUN chmod 777 -R /var/www/app

CMD npm start