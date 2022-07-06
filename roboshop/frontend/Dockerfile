FROM centos:7
RUN yum update -y
RUN yum install unzip -y

ADD https://github.com/roboshop-devops-project/frontend/archive/refs/heads/main.zip /tmp

RUN unzip /tmp/main.zip
FROM nginx
RUN rm -rf  /usr/share/nginx/html/*
WORKDIR /tmp/
RUN mv frontend-main /static/* /usr/share/nginx/html/
CMD ["start","nginx"]