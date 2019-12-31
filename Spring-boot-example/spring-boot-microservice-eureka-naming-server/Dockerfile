# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

# Add Maintainer Info
LABEL maintainer="bharath.giri@me.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 9091 available to the world outside this container
EXPOSE 9091

# The application's jar file
ARG JAR_FILE=target/spring-boot-microservice-eureka-naming-server-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} spring-boot-microservice-eureka-naming-server.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/spring-boot-microservice-eureka-naming-server.jar"]