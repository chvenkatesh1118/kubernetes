FROM centos:7
RUN yum update -y
RUN yum install git -y
FROM nginx
RUN rm -rf  /usr/share/nginx/html/*
WORKDIR /tmp/
RUN git clone https://github.com/roboshop-devops-project/frontend.git
RUN mv /tmp/frontend/static/* /usr/share/nginx/html/
CMD ["start","nginx"]