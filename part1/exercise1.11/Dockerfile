FROM amazoncorretto:8

#copy the source code to the container
COPY . .

# Build the project with ./mvnw package
RUN ./mvnw package

RUN java -jar ./target/docker-example-1.1.3.jar

# Expose the application port
EXPOSE 8080