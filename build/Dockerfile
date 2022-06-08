FROM alpine:latest
RUN apk update && \
apk add maven openjdk11
RUN touch /mnt/test.txt
#ADD ./boxfuse-sample-java-war-hello-master /opt/boxfuse-sample-java-war-hello-master
#RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && cd boxfuse-sample-java-war-hello
WORKDIR /opt
RUN mvn package
RUN cp /opt/target/hello-1.0.war /mnt