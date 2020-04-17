FROM centos:7.7.1908
LABEL maintainer="massimo.groppelli@zucchetti.it"

ENV JAVA_MAJOR_VERSION=8

# /dev/urandom is used as random source, which is prefectly safe
# according to http://www.2uo.de/myths-about-urandom/
RUN yum install -y \
       java-1.8.0-openjdk-1.8.0.242.b08-0.el7_7 \ 
       java-1.8.0-openjdk-devel-1.8.0.242.b08-0.el7_7 \ 
    && echo "securerandom.source=file:/dev/urandom" >> /usr/lib/jvm/jre/lib/security/java.security \
    && yum clean all

ENV JAVA_HOME /etc/alternatives/jre