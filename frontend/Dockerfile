FROM node:alpine as builder 
#as builder, from commander and below is known as buider phase

WORKDIR '/app'

COPY package.json .
RUN npm install
#copy rest of src code now
COPY . .

RUN npm run build

#second phase
FROM nginx
#copy something from the other phase that we were just working on
COPY --from=builder /app/build /usr/share/nginx/html
#dont need start nginx cmd