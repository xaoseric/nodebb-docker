# Pull base image.
FROM ubuntu:latest

# Install Node.js
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install nodejs -y
RUN apt-get install npm -y
RUN cd /opt ; git clone https://github.com/NodeBB/NodeBB nodebb
RUN cd /opt/nodebb ; npm install
RUN apt-get install imagemagick -y

# Create a mountable volume
VOLUME /opt/nodebb

# Define working directory.
WORKDIR /opt/nodebb

# Expose ports
EXPOSE 4567

# Define default command.
CMD ["node", "app.js"]
