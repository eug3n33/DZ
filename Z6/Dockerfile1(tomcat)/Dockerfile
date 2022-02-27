FROM tomcat:9.0
RUN apt-get update
RUN apt-get install -y maven git
WORKDIR /tmp/
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /tmp/boxfuse-sample-java-war-hello/
RUN mvn package
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war