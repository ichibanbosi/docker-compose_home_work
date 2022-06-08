FROM alpine:latest
RUN apk update && \
apk add maven openjdk11
RUN mkdir /opt/boxfuse && \
mkdir /mnt/build
RUN touch /mnt/build/test.txt
ADD ./boxfuse-sample-java-war-hello-master /opt/boxfuse
#RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && cd boxfuse-sample-java-war-hello
WORKDIR /opt/boxfuse
RUN mvn package
RUN cp /opt/boxfuse/target/hello-1.0.war /mnt
