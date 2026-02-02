# Use Java 17
FROM eclipse-temurin:17-jdk-alpine

# Set working directory
WORKDIR /app

# Copy pom and source
COPY . .

# Build the application
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Run the jar
CMD ["java", "-jar", "target/*.jar"]
