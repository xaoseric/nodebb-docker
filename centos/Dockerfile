FROM centos:centos7
MAINTAINER NodeBB <sales@nodebb.org>

RUN yum -y update ; yum clean all
RUN yum -y install epel-release tar ; yum clean all
RUN yum -y install wget ; yum clean all
RUN yum -y groupinstall "Development Tools"
RUN yum -y install nodejs git redis ImageMagick npm
RUN cd /opt ; git clone https://github.com/NodeBB/NodeBB nodebb 
RUN mkdir /opt/run
ADD start.sh /opt/run/start.sh
RUN chmod -v +x /opt/run/start.sh

EXPOSE 80
EXPOSE 443
EXPOSE 6379

CMD [ "/opt/run/start.sh" ]
