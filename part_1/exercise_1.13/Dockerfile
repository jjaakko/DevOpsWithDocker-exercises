FROM openjdk:8
EXPOSE 8080
RUN git clone https://github.com/docker-hy/spring-example-project.git
WORKDIR /spring-example-project/
RUN ./mvnw package
CMD java -jar ./target/docker-example-1.1.3.jar