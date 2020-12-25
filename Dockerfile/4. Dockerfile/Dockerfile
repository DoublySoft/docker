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

CMD apachectl -DFOREGROUND