FROM node:alpine3.14
RUN addgroup app && adduser -S -g app app
USER app
WORKDIR /app
COPY . .
CMD node app.js
RUN npm i
EXPOSE 3000



# docker build -t react-app .
