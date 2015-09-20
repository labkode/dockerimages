#
# ClawIO Docker file 
#
# Version 0.1

FROM ubuntu:12.04
MAINTAINER Hugo Gonzalez Labrador, clawio@hugo.labkode.com

RUN apt-get update
RUN apt-get -y install wget apt-transport-https vim curl
 
RUN wget -qO - https://deb.packager.io/key | apt-key add - 
RUN 	echo "deb https://deb.packager.io/gh/clawio/clawiod precise develop" | tee /etc/apt/sources.list.d/clawiod.list && \
	apt-get update && \
	apt-get -y --force-yes install clawiod

CMD /bin/bash
