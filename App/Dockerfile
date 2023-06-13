FROM tomcat:9-jdk8-corretto-al2
LABEL "project" = "Interior"
LABEL " Author" = "ckc1"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY  target/web.war /usr/local/tomcat/webapps/ROOT.war
############### old change ################
EXPOSE 8080
CMD ["catalina.sh","run"]
WORKDIR /USR/local/tomcat/
VOLUME /usr/local/tomcat/webapps
