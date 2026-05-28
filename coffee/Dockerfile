FROM ubuntu:24.04
RUN apt-get update
RUN apt-get install -y openjdk-21-jdk maven
WORKDIR /app
COPY . .
RUN mvn clean package -Dmaven.test.skip=true
EXPOSE 8080
CMD ["java", "-jar", "target/coffee-0.0.1-SNAPSHOT.jar"]
