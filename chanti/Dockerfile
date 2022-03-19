FROM centos:7
RUN yum install epel-release -y
RUN yum install nginx -y
RUN systemctl start nginx
EXPOSE 81/TCP
RUN systemctl restart nginx
