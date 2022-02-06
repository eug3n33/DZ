FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update
RUN apt install -y wget
RUN apt-get install -y default-jdk
WORKDIR /tmp/
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.58/bin/apache-tomcat-9.0.58.tar.gz
RUN mkdir /opt/tomcat
RUN tar zxvf apache-tomcat-*.tar.gz -C /opt/tomcat --strip-components 1
RUN /opt/tomcat/bin/startup.sh
EXPOSE 8080
CMD ["catalina.sh", "run"]
