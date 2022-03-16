FROM centos
ADD https://nginx.org/download/nginx-1.19.0.tar.gz /tmp
RUN yum install epel-release
RUN yum install ngnix -y
CMD ["nginx", "-g", "daemon off;"]