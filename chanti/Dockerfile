FROM centos:7
RUN yum install epel-release -y
RUN yum install nginx -y
EXPOSE 81/TCP
RUN systemctl start nginx
RUN systemctl restart nginx
