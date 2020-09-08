FROM centos:8

RUN yum install httpd -y

ADD beryllium /var/www/html

CMD apachectl -DFOREGROUND
