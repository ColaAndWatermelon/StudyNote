FROM openjdk:8
VOLUME /tmp
ADD implementstest-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 9999
ENTRYPOINT ["java","-jar","/app.jar"]
