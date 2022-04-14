0. docker version:
touch Dockerfile
aquire image from docker hub
https://hub.docker.com/
FROM node:alpine // an image containing minimal linux and node
touch app.js
echo "console.log('hello')" > app.js
echo "WORKDIR /app" >> Dockerfile
echo "CMD node /app.js" >> Dockerfile

0. docker build -t docker-start . // -t flag names, . specifies current location:
docker images / docker image ls

0. docker run docker-start

0. publish a container:
login to docker
play with docker
docker pull <repo>
docker run (:

0. win- you can switch windows and linux using the docker icon in tray

0. docker run ubuntu // it pulls from the hub if not present
docker ps // list processes
docker ps -a // list all including stopped ones

0. docker run -it ubuntu // it run in interactive shell:
docker run kalilinux/kali-rolling
root@a7ade54b2ab9:/#
<user>@<machine>:<location>#-admin, $- user

0. usefull linux commands:
whoami
echo $0 //in what shell are we
history
!2 // runs the second command from the history

0. apt and apt-get:
apt // advanced package tool
apt list //displays the installed db
apt update // updates the package databaseexit
apt install nano / python3
apt remove <package> -y

0. linux file system:
/ //root
bin // binaries/ programs
boot // boot related files
dev // devices files that are needed to access devices
etc // editable text configuration
home // home directories for users
root // home dir of the root user
lib // keeping library files such as software libs
var // variables frequantly updated files such as log app data...
proc // files for running processes

0. navigatin:
pwd
ls  | ls 1 | ll | ls -l
drwxr-xr-x   1 root root 4096 Apr  5 05:02 var/
<d f permissions> <user> size date 
cd path // relative
cd /bin // absolute
cd .. // up
cd ../.. // two levels up
ls /bin // shows the content of a directory without navigation
cd ~ // goto home directory


0. 