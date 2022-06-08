FROM alpine:latest
RUN apk update && \
apk add maven openjdk11
COPY ../boxfuse-sample-java-war-hello-master /opt
#RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && cd boxfuse-sample-java-war-hello
WORKDIR /opt
RUN mvn package
RUN cp /opt/target/hello-1.0.war /mnt