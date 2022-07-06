FROM centos:7
RUN yum update -y
RUN yum install nginx
RUN rm -rf  /usr/share/nginx/html/*
ADD https://github.com/roboshop-devops-project/frontend.git /tmp/
RUN mv /tmp/frontend/static/* /usr/share/nginx/html/
CMD ["start","nginx"]