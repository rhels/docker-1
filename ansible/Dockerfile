FROM ubuntu:15.04
MAINTAINER Thomas Steinbach <thomas.steinbach@aikq.de>

# prerequisites
RUN \
 apt-get update && \
 DEBIAN_FRONTEND=noninteractive apt-get -y install \
   sudo \
   git \
   # for use in playbook2dockerimage
   supervisor \
   python-pip \
   python-dev && \
 mkdir -p /etc/ansible && \
 echo "localhost ansible_connection=local" > /etc/ansible/hosts && \
 pip install markupsafe ansible docker-py && \
 apt-get clean && \
 apt-get autoclean
