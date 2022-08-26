FROM mongodb
RUN  sed -i -e 's/127.0.0.1/0.0.0.0/' /etc/mongod.conf
RUN mongo < data/users.js
RUN mongo < catalogue.js

