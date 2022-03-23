
FROM centos:7
RUN yum -y install epel-release
RUN yum -y update
RUN yum -y install nginx
RUN curl -s -L -o /tmp/frontend.zip "https://github.com/roboshop-devops-project/frontend/archive/main.zip"
RUN sudo cd /usr/share/nginx/html
RUN sudo rm -rf *
RUN sudo unzip /tmp/frontend.zip
RUN sudo mv frontend-main/* .
RUN sudo mv static/* .
RUN sudo rm -rf frontend-master static README.md
RUN sudo mv localhost.conf /etc/nginx/default.d/roboshop.conf
EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

#$(docker ps | grep nginx | awk '{print $1}')