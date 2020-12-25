FROM centos:7

RUN \
    yum -y install \
        httpd \
        php \
        php-cli \
        php-common \
        mod_ssl \
        opnessl

RUN echo "<?php phpinfo(); ?>" > /var/www/html/hola.php

COPY public_html /var/www/html

COPY ssl.conf /etc/httpd/conf.d/default.conf

COPY docker.crt /docker.crt
COPY docker.key /docker.key

EXPOSE 443

CMD apachectl -DFOREGROUND