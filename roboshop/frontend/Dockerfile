FROM centos:7
RUN yum update -y
RUN yum install unzip -y
RUN yum install yum-utils -y
RUN yum install epel-release -y
RUN yum install nginx -y
RUN rm -rf  /usr/share/nginx/html/*
ADD https://github.com/roboshop-devops-project/frontend/archive/refs/heads/main.zip /tmp

RUN unzip /tmp/main.zip -d /tmp/

WORKDIR /tmp/frontend-main/
RUN cp -r  static/* /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]