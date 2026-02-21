FROM openjdk:17-jre-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the application's JAR file from your local target/build directory to the container's /app directory
# Ensure you build your application locally first (e.g., 'mvn clean package')
COPY target/*.jar app.jar

# Expose the port your application listens on (optional, if it's a web app)
EXPOSE 8080

# Define the entry point command to run the JAR file
ENTRYPOINT ["java", "-jar", "app.jar"]
