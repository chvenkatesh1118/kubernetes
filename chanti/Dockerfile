
FROM centos:7
RUN yum -y install epel-release
RUN yum -y update
RUN yum -y install nginx
RUN curl -s -L -o /tmp/frontend.zip "https://github.com/roboshop-devops-project/frontend/archive/main.zip"
RUN cd /usr/share/nginx/html
RUN rm -rf *
RUN unzip /tmp/frontend.zip
RUN mv frontend-main/* .
RUN mv static/* .
RUN rm -rf frontend-master static README.md
RUN mv localhost.conf /etc/nginx/default.d/roboshop.conf
EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

#$(docker ps | grep nginx | awk '{print $1}')