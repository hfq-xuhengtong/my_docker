FROM ubuntu:14.04

MAINTAINER xuht 

RUN apt-get update \
    && apt-get install openssh-server -y \
    && mkdir -p /var/run/sshd \ 
    && mkdir /root/.ssh

ADD authorized_keys /root/.ssh/authorized_keys
ADD run.sh /run.sh
RUN chmod 755 /run.sh

EXPOSE 22

CMD ["/run.sh"]
