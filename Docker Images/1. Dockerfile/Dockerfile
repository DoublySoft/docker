FROM centos

LABEL version="1.0"
LABEL description="This is an apache image"
LABEL vendor="yo"

RUN yum install httpd -y

WORKDIR /var/www/html

COPY public_html .
# ADD public_html .

RUN echo "$(whoami)" > user1.html
RUN useradd daniel
USER daniel
RUN echo "$(whoami)" > /tmp/user2.html
USER root
RUN cp /tmp/user2.html .

ENV contenido Prueba 2
RUN echo "$contenido" > prueba.html

# VOLUME .

# EXPOSE 8080

COPY run.sh /run.sh

CMD sh /run.sh