# Pull base image.
FROM debian:latest
MAINTAINER NodeBB Docker Team <docker-devs@nodebb.org>

# Install base packages
RUN apt-get update && apt-get upgrade -y
RUN apt-get install redis-server -y

# Create a mountable volume
VOLUME ["/data"]

# Define working directory.
WORKDIR /data

# Expose ports
EXPOSE 6379

# Define default command.
CMD ["redis-server"]
