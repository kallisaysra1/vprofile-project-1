FROM maven:3.9.9-eclipse-temurin-21-jammy AS BUILD_IMAGE 
#This build image is going to be the default image for the future artifacts and can be used "BUILD_ON instruction"
RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install



FROM tomcat:10-jdk21
RUN rm -rf /usr/local/tomcat/webapps/* 
#the above line is, usually tomcat image comes with a default application in it, we need to delete all the files and folders in it. so that we can deploy our own application.
# -r = recursively, -f force, *denotes all the files
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh" "run"]

FROM Mysql:latest


