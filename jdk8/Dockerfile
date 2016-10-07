# Version: 1
# Name: jdk8
# Copy from thenewvu/oracle-jdk8
FROM jeckhart/phusion-baseimage

MAINTAINER "boyan.au@gmail.com"

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -qq update && \
    apt-get -qq -y install wget curl unzip htop software-properties-common && \
    apt-get -qq -y autoremove && \
    apt-get -qq -y autoclean 

RUN echo debconf shared/accepted-oracle-license-v1-1 select true | sudo debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | sudo debconf-set-selections

RUN sudo add-apt-repository ppa:webupd8team/java && \
    sudo apt-get update && \
    sudo apt-get install -y --no-install-recommends oracle-java8-installer

RUN sudo apt-get clean && \
    sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

