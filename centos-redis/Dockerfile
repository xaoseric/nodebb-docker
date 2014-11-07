ROM centos:centos7
MAINTAINER NodeBB Docker Team <docker-devs@nodebb.org>

# install packages
RUN yum -y update ; yum clean all
RUN yum -y install epel-release ; yum clean all
RUN yum -y install redis ; yum clean all

# Define mountable directories
VOLUME ["/data"]

# Define working directory
WORKDIR /data

# Expose ports
EXPOSE 6379

CMD [ "redis-server" ]
