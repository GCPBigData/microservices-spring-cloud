FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD target/processor-1.0-SNAPSHOT.jar app.jar
ENTRYPOINT [ "sh", "-c", "java -Djava.security.egd=order:/dev/./urandom -Dspring.profiles.active=docker -Dspring.cloud.config.uri=http://config-server:8888 -jar /app.jar" ]