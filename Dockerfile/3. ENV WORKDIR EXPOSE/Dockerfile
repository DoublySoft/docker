FROM centos:8

RUN yum install httpd -y

WORKDIR /var/www/html

COPY beryllium .

ENV contenido prueba

RUN echo "$contenido" > prueba.html

EXPOSE 8080

CMD apachectl -DFOREGROUND
