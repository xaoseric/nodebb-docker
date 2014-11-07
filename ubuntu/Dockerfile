# Pull base image.
FROM ubuntu:latest
MAINTAINER NodeBB Docker Team <docker-devs@nodebb.org>

# Install base packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install nodejs npm imagemagick git -y

# Install nodebb
RUN cd /opt ; git clone https://github.com/NodeBB/NodeBB nodebb
RUN cd /opt/nodebb ; npm install

# Create a mountable volume
VOLUME /opt/nodebb

# Define working directory.
WORKDIR /opt/nodebb

# Expose ports
EXPOSE 80
EXPOSE 443
EXPOSE 4567

# Define default command.
CMD ["node", "app.js"]
