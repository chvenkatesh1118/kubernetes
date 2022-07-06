FROM centos:7
RUN yum update -y
RUN yum install unzip -y
RUN yum install yum-utils
RUN yum install epel-release
RUN yum install nginx -y
ADD https://github.com/roboshop-devops-project/frontend/archive/refs/heads/main.zip /tmp

RUN unzip /tmp/main.zip
RUN rm -rf  /usr/share/nginx/html/*
WORKDIR /tmp/
RUN mv frontend-main /static/* /usr/share/nginx/html/
CMD ["start","nginx"]