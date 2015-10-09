FROM ubuntu
MAINTAINER Kacey Cole <kcole@izeni.com>

# Fetch system deps
RUN apt-get update && apt-get upgrade -y -o DPkg::Options::=--force-confold

RUN apt-get install -y python-software-properties software-properties-common
RUN add-apt-repository ppa:saltstack/salt -y
RUN apt-get update
RUN apt-get install -y salt-master salt-minion salt-ssh salt-syndic
# Remove problematic optional dep.
RUN apt-get remove -y dmidecode

EXPOSE 4505 4506
CMD /usr/bin/salt-master --log-level=error
