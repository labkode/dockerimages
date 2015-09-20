#
# ClawIO Docker file 
#
# Version 0.1

FROM centos:7
MAINTAINER Hugo Gonzalez Labrador, clawio@hugo.labkode.com

RUN yum install -y wget curl vim
RUN rpm --import https://rpm.packager.io/key
RUN echo $'[clawiod]\n\
name=Repository for clawio/clawiod application.\n\
baseurl=https://rpm.packager.io/gh/clawio/clawiod/centos7/develop\n\
enabled=1'\
 | tee /etc/yum.repos.d/clawiod.repo

RUN rm -f /lib/systemd/system/multi-user.target.wants/*;\
rm -f /etc/systemd/system/*.wants/*;\
rm -f /lib/systemd/system/local-fs.target.wants/*; \
rm -f /lib/systemd/system/sockets.target.wants/*udev*; \
rm -f /lib/systemd/system/sockets.target.wants/*initctl*; \
rm -f /lib/systemd/system/basic.target.wants/*;\
rm -f /lib/systemd/system/anaconda.target.wants/*;
RUN yum install -y clawiod 
CMD /bin/bash
