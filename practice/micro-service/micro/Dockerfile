FROM ubuntu:latest

LABEL DEVOPSENGG="D"

RUN apt update && apt install unzip apache2 -y && rm -rf /var/www/html/index.html

WORKDIR /var/www/html

# Copy the directory and the specified files into the container
COPY todo season traffic counter puppy /var/www/html/

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
