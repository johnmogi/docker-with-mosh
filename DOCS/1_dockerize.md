0. touch Dockerfile:
FROM
WORKDIR
COPY
ADD
RUN // run linux and win commands
ENV // enviroment variables
EXPOSE // expose a specific port
USER // usually a user with limited privileges
CMD
ENTRYPOINT


0. docker samples:
https://docs.docker.com/samples/
in docker hub filter by tag a specific version
for example- node 14 alpine etc.

0. build :
docker build -t react-app .
<run><build><tag><name-of-image>
docker images
docker image ls

0. docker run -it react-app sh
<run> interactive app shell
COPY package*.json README.md /app/
[---]
WORKDIR /app //this ensures current workdir
COPY . . // I no longer nee to specify location
COPY ["hello world", "."]
ADD http://.../file.json .
ADD file.zip . //this auto uncompress this into the directory
echo node_modules > .dockerignore


0. RUN npm i:
RUN apk install python // alpine doesn't have apt

0. enviroment variables:
ENV API_URL=http://api.myapp.com
shell-> printenv
printenv API_URL
echo $API_URL

0. expose port inside container:
EXPOSE 3000 // this more documents then run the actual port

0. play around with some linux commans inside a container:
alpine doesn't have useradd-
addgroup app //create the group prior to user
adduser -S -G app app //best practice same username as group
<cmd><sys><group><name><username>
groups app // show the users of the group
addgroup john && adduser -S -g john john

0. docker run react-app npm start
reshape users in dockerifile:
FROM node:alpine3.14
RUN addgroup app && adduser -S -g app app
USER app
WORKDIR /app
COPY . .
CMD node app.js
RUN npm i
EXPOSE 3000

0. CMD npm start // can run only one so use an array
RUN // builtime runs at build
CMD ["npm", "start"] // avoid running a seperate shell - exec form



0. ENTRYPOINT ["npm", "start"]

0. 

