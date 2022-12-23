FROM openjdk:8 AS Build_Image
RUN  apt update && apt install maven -y
RUN git clone -b vp-docker https://github.com/devopshydclub/vprofile-project.git
RUN  cd vprofile-project && mvn install 

FROM tomcat
RUN  rm -rf /usr/local/tomcat/webapps/*
COPY --from=Build-Image vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war 
EXPOSE 8080
CMD ["catalina.sh","run"]
