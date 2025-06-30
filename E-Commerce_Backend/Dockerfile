# Use a lightweight Java 17 runtime
FROM eclipse-temurin:17-jdk-alpine

# Create app directory in the container
WORKDIR /app

# Copy the built jar file from target/ to the container
COPY target/*.jar app.jar

# Expose the Spring Boot port
EXPOSE 8080

# Command to run the app
ENTRYPOINT ["java", "-jar", "app.jar"]

