FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update
RUN apt install -y maven git
WORKDIR /tmp
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
RUN git clone https://github.com/eug3n33/DZ.git
RUN cp /tmp/DZ/Z12/Config.properties /tmp/App42PaaS-Java-MySQL-Sample/WebContent/Config.properties
WORKDIR /tmp/App42PaaS-Java-MySQL-Sample
RUN mvn clean
RUN mvn install
RUN mkdir /tmp/webapps
RUN cp /tmp/App42PaaS-Java-MySQL-Sample/target/App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT.war /tmp/webapps
RUN cp /tmp/DZ/Z12/Config.properties /tmp/webapps