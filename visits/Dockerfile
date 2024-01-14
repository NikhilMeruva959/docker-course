FROM node:alpine

WORKDIR '/app'

COPY package.json .
RUN npm install
#copy rest of src code now
COPY . .

#Default command
CMD ["npm", "start"]