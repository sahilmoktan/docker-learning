# Learning docker

Running other Img by pulling

docker pull ubuntu
 docker run -it ubuntu
    ls for listing
    mkdir hello // creating folder
    cd hello //root change

    touch hello-ubuntu.txt //making file

    ============================

CREATION OF OUR OWN DOCKER IMG

create folder hello-docker
hello.js with command console.log('helloDocker')

Dockerfile
    from node:20-alpine  /using node in docker img
    WORKDIR  /app  //
    copy . .  // 1st dot current dir to 2nd dot : docker's dir coping code/command
    CMD node hello.js  // command that runs docker's node enging

cd hello-docker //change root

docker build -t hello-docker . //creation of docker img
 then docker run hello-docker  // run docker img

 so, docker run -it hello-docker sh  // opens in shell
 it enters shell
 node hello.js

