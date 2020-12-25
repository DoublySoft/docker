FROM nginx

RUN useradd daniel

COPY public_html /usr/share/nginx/html

ENV archivo Environment

WORKDIR /usr/share/nginx/html

RUN echo "${archivo}" > /usr/share/nginx/html/env.html

EXPOSE 90

LABEL version=1

USER daniel

RUN echo "Yo soy $(whoami)" > /tmp/me.html

USER root

RUN cp /tmp/me.html /usr/share/nginx/html/docker.html

VOLUME /var/log/nginx

# Con este comando no se queda levantado el contendor
# CMD ["nginx", "-g", "daemon off;"]