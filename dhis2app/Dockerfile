FROM tomcat:8.5.30-jre8

RUN apt-get update
RUN apt-get -y install curl
RUN rm -rf /usr/local/tomcat/webapps/*
RUN mkdir -p /opt/dhis2/config/apps/

COPY wait-for-it.sh wait-for-it.sh
COPY setenv.sh /usr/local/tomcat/bin/setenv.sh
COPY hibernate.properties /opt/dhis2/config/hibernate.properties
COPY dhis.conf /opt/dhis2/config/dhis.conf
COPY static /opt/dhis2/config/static
COPY dhis.war /usr/local/tomcat/webapps/ROOT.war
COPY server.xml /usr/local/tomcat/conf/
