FROM maven:3.5.2-jdk-8
RUN apt update
RUN apt-get install -y git
WORKDIR /tmp
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR /tmp/App42PaaS-Java-MySQL-Sample
RUN echo "app42.paas.db.username = "test1"" > /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
RUN echo "app42.paas.db.port = "8514"" >> /etc/sysctl.conf
RUN echo "app42.paas.db.password = "QQww1122"" >> /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
RUN echo "app42.paas.db.ip = "192.168.2.175"" >> /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
RUN echo "app42.paas.db.name = "test1"" >> /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
RUN mvn clean
RUN mvn install
RUN mkdir /tmp/webapps
RUN cp /tmp/App42PaaS-Java-MySQL-Sample/target/App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT.war /tmp/webapps