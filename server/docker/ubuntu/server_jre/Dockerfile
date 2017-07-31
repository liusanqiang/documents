FROM ubuntu:16.04
MAINTAINER tianshuo <tslearn@163.com>

RUN apt-get update -y && \
    apt-get install -y curl tar && \
    mkdir -p /opt/java && \
    cd /opt/java && \
    curl -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k http://download.oracle.com/otn-pub/java/jdk/8u144-b01/090f390dda5b47b9b721c7dfaa008135/server-jre-8u144-linux-x64.tar.gz && \
    tar xf server-jre-8u144-linux-x64.tar.gz -C /opt/java && \
    rm -f server-jre-8u144-linux-x64.tar.gz && \
    ln -s /opt/java/jdk* /opt/java/jdk && \
    ln -s /opt/java/jdk /opt/java/jvm

ENV JAVA_HOME=/opt/java/jdk \
    PATH=${PATH}:/opt/java/jdk/bin
