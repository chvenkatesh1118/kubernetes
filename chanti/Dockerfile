FROM centos:7
RUN yum install epel-release -y
RUN yum install nginx -y
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

