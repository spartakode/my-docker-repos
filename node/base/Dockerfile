FROM ubuntu:14.04.2
MAINTAINER Adnan Issadeen <spartakode@outlook.com>

RUN apt-get update && apt-get install wget curl sqlite3 vim software-properties-common python-software-properties -y --force-yes
RUN apt-add-repository ppa:git-core/ppa -y && apt-get update -y && apt-get install git -y
RUN mkdir /usr/src/node
WORKDIR /usr/src/node
RUN wget http://nodejs.org/dist/v0.12.3/node-v0.12.3-linux-x64.tar.gz -O node.tar.gz \
    && tar -xvf node.tar.gz \
    && cp -rp node-v0.12.3-linux-x64 /usr/local \
    && ln -s /usr/local/node-v0.12.3-linux-x64 /usr/local/node
RUN echo 'export PATH=$PATH:/usr/local/node/bin' >> ~/.bashrc
RUN /bin/bash -c 'source ~/.bashrc'
