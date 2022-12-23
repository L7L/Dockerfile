FROM openjdk:8 AS Build_Image
RUN  apt update && apt install maven -y
COPY C:\Users\rsjat\Downloads\Devops_project\vprofile  vprofile
RUN  cd vprofile && mvn install 

FROM tomcat
RUN  rm -rf /usr/local/tomcat/webapps/*
COPY --from=Build_Image vprofile/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war 
EXPOSE 8080
CMD ["catalina.sh","run"]
