FROM node:21

# create the /app directory, cd into /app
WORKDIR /app

# How to build the application
# inside /app
# copy files from local into the container
COPY main.js .
COPY package-lock.json .
COPY package.json .

COPY public public
COPY views views

# Install dependencies, uses the lock instead of json file
RUN npm ci

# How to run the application

# Environment variables
ENV APP_PORT=3000

# Tell the container what port the application need
EXPOSE ${APP_PORT}

# Use shell to run
ENTRYPOINT node main.js

# Alternative, you are not starting process thru shell
# ENTRYPOINT [ "/usr/bin/node","/app/main.js" ]