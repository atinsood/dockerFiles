FROM ubuntu:latest
MAINTAINER Atin Sood <atinsood@gmail.com>

#House keeping
RUN apt-get update
RUN apt-get -y install python-software-properties

#Installing maven
RUN add-apt-repository http://ppa.launchpad.net/natecarlson/maven3/ubuntu

#Install sun java
RUN add-apt-repository -y ppa:webupd8team/java
# automatically accept oracle license
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections

#Now install everything
RUN apt-get update
RUN apt-get install -y git curl oracle-java7-installer maven3

#And now the ssh stuff
RUN apt-get install -y openssh-server
RUN mkdir /var/run/sshd
RUN echo "root:root" | chpasswd
EXPOSE 22
