# Use Node.js 18 as the base image
FROM node:18

# Set working directory inside the container
WORKDIR /app

# Copy only package.json and package-lock.json to leverage Docker cache
COPY application-service/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY application-service/. .

# Expose the port your app runs on
EXPOSE 3000

# Start the application
CMD ["node", "src/index.js"]
