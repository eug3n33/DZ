FROM maven
RUN apt-get update
RUN apt-get install -y git
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git /tmp/
WORKDIR /tmp/boxfuse-sample-java-war-hello/
RUN mvn package
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war /tmp/webapps