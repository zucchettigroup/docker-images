FROM openjdk:8u292-jre

MAINTAINER Stefano Ortiz

ENV PDI_RELEASE=9.1 \
    PDI_VERSION=9.1.0.0-324 \
    PDI_HOME=/opt/pentaho-di \
    KETTLE_HOME=/pentaho-di

RUN curl -L -o /tmp/pdi-ce-${PDI_VERSION}.zip \
    https://downloads.sourceforge.net/project/pentaho/Pentaho%20${PDI_RELEASE}/client-tools/pdi-ce-${PDI_VERSION}.zip && \
    unzip -q /tmp/pdi-ce-${PDI_VERSION}.zip -d $PDI_HOME && \
    rm /tmp/pdi-ce-${PDI_VERSION}.zip