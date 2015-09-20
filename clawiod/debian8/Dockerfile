#
# ClawIO Docker file 
#
# Version 0.1

FROM debian:8
MAINTAINER Hugo Gonzalez Labrador, clawio@hugo.labkode.com

RUN apt-get update
RUN apt-get -y install wget curl apt-transport-https vim
 
RUN wget -qO - https://deb.packager.io/key | apt-key add - 
RUN 	echo "deb https://deb.packager.io/gh/clawio/clawiod jessie develop" | tee /etc/apt/sources.list.d/clawiod.list && \
	apt-get update && \
	apt-get -y --force-yes install clawiod

CMD /bin/bash
