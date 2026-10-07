FROM node:20.20.2-alpine3.22 AS builde
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
 #  MONGO_URL="mongodb://mongodb:27017/catalogue
ENV MONGO=true \
    MONGO_URL="mongodb://mongodb:27017/catalogue" 
    
CMD ["node", "server.js"]