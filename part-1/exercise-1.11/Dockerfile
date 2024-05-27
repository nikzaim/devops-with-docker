FROM openjdk:8

WORKDIR /usr/src

COPY . .

# The issue was that locally the mvnw script had Windows line endings (\r\n called CRLF).
RUN apt-get update && apt-get install -y dos2unix && find . -type f -print0 | xargs -0 dos2unix 

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]

EXPOSE 8080