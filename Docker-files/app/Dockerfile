FROM openjdk:11 AS BUILD_IMAGE
#apt bcz openjdk image is debian based
RUN apt update && apt install maven -y
RUN git clone https://github.com/devopshydclub/vprofile-project.git
RUN cd vprofile-project && git checkout docker &&  mvn install 

FROM tomcat:9-jre11
LABEL "Project"="Vprofileapp"
LABEL "Author"="Abdul Qadir"
RUN rm -rf /usr/local/tomcat/webapps/*
#copying the artifact from build image to this image
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]