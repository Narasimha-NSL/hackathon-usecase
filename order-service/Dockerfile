# Use Maven + Java 17 for building Java microservice
FROM maven:3.9.4-eclipse-temurin-17 AS build

# Set working directory
WORKDIR /app

# Copy pom.xml and source files
COPY pom.xml .
COPY src ./src

# Build the application
RUN mvn clean install -DskipTests

# Use a lightweight JDK for running
FROM eclipse-temurin:17-jre

WORKDIR /app

# Copy built jar from build stage
COPY --from=build /app/target/*.jar app.jar

# Expose port (adjust to your app)
EXPOSE 8080

# Run the application
CMD ["java", "-jar", "app.jar"]

