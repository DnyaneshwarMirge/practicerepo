FROM mysql:latest
LABEL app="mysql"
LABEL Author="D"

# Arguments and environment variables
ARG MYSQL_DATABASE
ARG MYSQL_USER
ARG MYSQL_PASSWORD
ARG MYSQL_ROOT_PASSWORD

ENV MYSQL_DATABASE=${MYSQL_DATABASE}
ENV MYSQL_USER=${MYSQL_USER}
ENV MYSQL_PASSWORD=${MYSQL_PASSWORD}
ENV MYSQL_ROOT_PASSWORD=${MYSQL_ROOT_PASSWORD}

# Copy the SQL file directly to the MySQL initialization directory
COPY student.sql /docker-entrypoint-initdb.d/student.sql

# Expose MySQL port
EXPOSE 3306

# Default command to start MySQL server
CMD ["mysqld"]


# HOW to Run the container
# docker run -d -p 3306:3306 --name mysql-container \
# -e MYSQL_DATABASE=studentapp \
# -e MYSQL_USER=mayur \
# -e MYSQL_PASSWORD=1234 \
# -e MYSQL_ROOT_PASSWORD=1234 \
# <imageid>