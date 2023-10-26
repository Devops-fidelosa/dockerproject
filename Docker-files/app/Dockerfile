FROM openjdk:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/Devops-fidelosa/dockerproject.git
RUN cd dockerproject && mvn install
# the above stage is to build the artifact

FROM tomcat:9-jre11
LABEL "Project"="fidevcontainerization"
LABEL "Author"="Fidelosa"
RUN rm -rf /usr/local/tomcat/webapps/* 
# to remove the default tomcat application
COPY --from=BUILD_IMAGE dockerproject/target/fidev-v1.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
