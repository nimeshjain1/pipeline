FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y iputils-ping telnet apache2 
EXPOSE 80
CMD ["apache2ctl", "-D","FOREGROUND"]
