# Specify a base image
FROM node:14-alpine

#instead of just putting it in contianer ls, it will store specifically in a folder 
WORKDIR /usr/app

#Install dependencies
# COPY ./ ./ 

#look in the current wrkdir and find package.json -> put int wkdir of container
COPY ./package.json ./ 
RUN npm install
COPY ./ ./

#Default command
CMD ["npm", "start"]