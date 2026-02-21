FROM node:24-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY ["package.json", "package-lock.json*", "./"]

# Install production dependencies only
RUN npm install --omit=dev

# Copy the rest of the application source code to the container
COPY . .

# Expose the port the app runs on (e.g., 3000, 8080)
EXPOSE 3001

# Command to run the application when the container starts
CMD ["node", "src/index.js"]
