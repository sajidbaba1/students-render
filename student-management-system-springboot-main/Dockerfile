# Stage 1: Build the application using Maven
FROM maven:3.8.6-openjdk-17-slim AS builder
WORKDIR /app

# Copy the Maven project file and download dependencies (cached unless pom.xml changes)
COPY pom.xml .
RUN mvn dependency:go-offline

# Copy the source code and build the JAR (skip tests if desired)
COPY src ./src
RUN mvn clean package -DskipTests

# Stage 2: Create the final runtime image
FROM openjdk:17-slim
WORKDIR /app

# Copy the built JAR from the builder stage
COPY --from=builder /app/target/student-management-system-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
