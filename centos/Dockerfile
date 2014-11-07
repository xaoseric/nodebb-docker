FROM centos:centos7
MAINTAINER NodeBB Docker Team <docker-devs@nodebb.org>

# install main packages:
RUN yum -y update ; yum clean all
RUN yum -y install epel-release tar ; yum clean all
RUN yum -y install wget ; yum clean all
RUN yum -y groupinstall "Development Tools"
RUN yum -y install nodejs git ImageMagick npm
RUN yum -y install openssl openssl-devel;

# clone nodebb and install it
RUN cd /opt ; git clone https://github.com/NodeBB/NodeBB nodebb
RUN cd /opt/nodebb ; npm install

# Create a nodebb volume
VOLUME /opt/nodebb

# Define a working directory
WORKDIR /opt/nodebb

# Expose ports
EXPOSE 80
EXPOSE 443
EXPOSE 4567

CMD [ "node", "app.js" ]

