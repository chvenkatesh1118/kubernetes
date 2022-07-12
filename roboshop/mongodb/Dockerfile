FROM mongodb
RUN  sed -i -e 's/127.0.0.1/0.0.0.0/' /etc/mongod.conf
ADD https://github.com/roboshop-devops-project/mongodb/archive/main.zip /tmp/
RUN unzip /tmp/mongodb.zip -d /tmp/
