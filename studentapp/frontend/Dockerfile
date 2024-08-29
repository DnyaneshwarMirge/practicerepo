FROM ubuntu:latest
LABEL frontend="D"
LABEL DevopsEngg="D"


RUN apt-get update && \
    apt-get install apache2 -y
COPY index.html /var/www/html/index.html

EXPOSE 80
CMD httpd -DFOREGROUND