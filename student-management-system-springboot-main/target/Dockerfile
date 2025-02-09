# Use an official JDK runtime as a parent image
FROM adoptopenjdk/openjdk10-openj9


# Set the working directory inside the container
WORKDIR /app

# Copy the build jar file into the container
COPY student-management-system-0.0.1-SNAPSHOT.jar app.jar

# Expose the application port (change if necessary)
EXPOSE 8080

# Command to run the application
CMD ["java", "-jar", "app.jar"]
