# Use the latest Ubuntu as the base image
FROM ubuntu:latest

LABEL DEVOPSENGG="D"

RUN apt update 
RUN apt install unzip nginx -y
RUN rm -rf /usr/share/nginx/html/index.html

WORKDIR /usr/share/nginx/html/

COPY neogym-html /usr/share/nginx/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]