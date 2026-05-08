FROM node:20.0.0
WORKDIR /app
ENV MONGO="true" \
    MONGODB_URL="mongodb://mongodb:27017/user" \
    REDIS_URL="redis://redis:6379"
EXPOSE 8080
COPY package.json .
COPY *.js .
RUN npm install
CMD [ "node", "server.js" ]