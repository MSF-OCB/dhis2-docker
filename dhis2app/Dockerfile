#FROM tomcat:8.5.29-jre8
FROM tomcat:8.5.30-jre8-alpine

RUN apk update && apk add curl && rm -rf /usr/local/tomcat/webapps/*
COPY setenv.sh /usr/local/tomcat/bin/setenv.sh
COPY dhis.war /usr/local/tomcat/webapps/ROOT.war
COPY hibernate.properties /opt/dhis2/config/hibernate.properties
COPY dhis.conf /opt/dhis2/config/dhis.conf
COPY wait-for-it.sh wait-for-it.sh
#COPY dhis2-export-app /opt/dhis2/config/apps/dhis2-export-app/
COPY static /opt/dhis2/config/static
#COPY static/logo_banner.png /usr/local/tomcat/webapps/ROOT/images/
#COPY static/logo_front.png /usr/local/tomcat/webapps/ROOT/images/
