FROM ubuntu:14.04
MAINTAINER Adnan Issadeen <adnan.issadeen@live.com>

RUN apt-get update && apt-get install wget curl sqlite3 -y --force-yes 
RUN apt-get update && apt-get -y --force-yes build-dep python3.4
RUN mkdir /usr/src/python 
WORKDIR /usr/src/python
RUN wget https://www.python.org/ftp/python/3.4.1/Python-3.4.1.tgz \
    && tar -xvf Python-3.4.1.tgz 
WORKDIR /usr/src/python/Python-3.4.1 
RUN ./configure \
    && make -j$(nproc) \
    && make -j$(nproc) EXTRATESTOPTS='--exclude test_shutil test_socket' test \
    && make altinstall
RUN pip3.4 install bcrypt && pip3.4 install Flask && pip3.4 install MonthDelta
RUN curl -sL https://deb.nodesource.com/setup | bash - \
    && apt-get install -y --force-yes nodejs
