FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update
RUN apt install -y maven git
WORKDIR /tmp
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /tmp/boxfuse-sample-java-war-hello/
RUN mvn package
RUN mkdir /tmp/webapps/
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war /tmp/webapps/
cmd ["mvn"]
