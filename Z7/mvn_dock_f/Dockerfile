FROM maven:3.5.2-jdk-8
RUN apt update
RUN apt-get install -y 
WORKDIR /tmp
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /tmp/boxfuse-sample-java-war-hello
RUN mvn package -f /tmp/boxfuse-sample-java-war-hello
RUN mkdir /tmp/webapps
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war /tmp/webapps