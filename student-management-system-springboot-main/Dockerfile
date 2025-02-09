FROM openjdk:17-jdk-slim

# Set the working directory
WORKDIR /app

# Copy the build jar file into the container
COPY target/student-management-system-0.0.1-SNAPSHOT.jar

# Expose the application port (change if necessary)
EXPOSE 8080

# Command to run the application
ENTRYPOINT ["java", "-jar", "app.jar"]

