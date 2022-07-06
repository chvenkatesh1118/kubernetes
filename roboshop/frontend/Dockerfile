FROM centos:7
RUN yum update -y
FROM nginx
ADD https://github.com/roboshop-devops-project/frontend/archive/refs/heads/main.zip /tmp
RUN unzip /tmp/main.zip
RUN rm -rf  /usr/share/nginx/html/*
WORKDIR /tmp/
RUN mv /tmp/frontend-main /static/* /usr/share/nginx/html/
CMD ["start","nginx"]