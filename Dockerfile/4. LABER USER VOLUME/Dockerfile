FROM centos:8

LABEL version="1.0"
LABEL description="This is an apache image"
LABEL vendor="yo"

RUN yum install httpd -y

WORKDIR /var/www/html

COPY beryllium .

RUN echo "$(whoami)" > ./user1.html

RUN useradd Daniel

USER Daniel

RUN echo "$(whoami)" > /tmp/user2.html

VOLUME .

USER root

RUN cp /tmp/user2.html ./user2.html

CMD apachectl -DFOREGROUND
