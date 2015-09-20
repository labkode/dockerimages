#
# ClawIO Docker file 
#
# Version 0.1

FROM debian:7
MAINTAINER Hugo Gonzalez Labrador, clawio@hugo.labkode.com

RUN apt-get update
RUN apt-get -y install wget
RUN apt-get -y install apt-transport-https
RUN apt-get -y install vim
 
RUN wget -qO - https://deb.packager.io/key | apt-key add - 
RUN 	echo "deb https://deb.packager.io/gh/clawio/clawiod wheezy develop" | tee /etc/apt/sources.list.d/clawiod.list && \
	apt-get update
RUN  apt-get -y --force-yes install clawiod

CMD /bin/bash
