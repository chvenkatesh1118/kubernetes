
FROM centos:7
RUN yum -y install epel-release
RUN apt-get -y install sudo

RUN yum -y install nginx
RUN curl -s -L -o /tmp/Dockerfile.zip "https://github.com/roboshop-devops-project/frontend/archive/main.zip"
RUN  unzip /tmp/Dockerfile.zip
RUN  cd /usr/share/nginx/html
RUN  rm -rf *
RUN  mv Dockerfile-main/* .
RUN  mv static/* .
RUN  rm -rf Dockerfile-master static README.md
RUN  mv localhost.conf /etc/nginx/default.d/log.conf
EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

#$(docker ps | grep nginx | awk '{print $1}')