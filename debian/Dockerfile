# Pull base image.
FROM debian:latest
MAINTAINER NodeBB Docker Team <docker-devs@nodebb.org>

# Install base packages
RUN apt-get update && apt-get upgrade -y
RUN apt-get install nodejs nodejs-legacy npm imagemagick git -y

# Install nodebb
RUN cd /opt && git clone https://github.com/NodeBB/NodeBB nodebb
RUN cd /opt/nodebb && npm install

# Create a mountable volume
VOLUME /opt/nodebb

# Define working directory.
WORKDIR /opt/nodebb

# Expose ports
EXPOSE 4567

# Define default command.
CMD ["node", "app.js"]