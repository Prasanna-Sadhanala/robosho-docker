FROM node:20
WORKDIR /app
Copy package.json .
COPY *.js .
Run npm install
Env MONGO=true
    MONGO_URL="mongodb://mongodb:27017/catalogue" \
    
CMD ["node","server.js"]