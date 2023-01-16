FROM node:8.16.0-alpine

WORKDIR /app 

COPY . . 

RUN --network=my-bridge-network npm install  && \ 
    npm audit fix 
    
EXPOSE 4000

CMD npm start 
