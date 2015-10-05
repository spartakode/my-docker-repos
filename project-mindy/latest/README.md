#Project Mindy Docker Container#

A simple docker container to get up and running with mindy. In order to test if
it is working, pull the container, and do the following.

run the command

`sudo docker run -it spartakode/mindy:latest /bin/bash`

then run

`mkdir /mindy-hello && cd /mindy-hello`

Follow the instructions at [the mindy docs](http://project-mindy.github.io/mindy/mindy.html#hello-world) to test if mindy has been installed correctly.

**Note**: You don't need to use $INSTALL/bin/mindy(comp). Using mindycomp and
mindy alone will suffice
