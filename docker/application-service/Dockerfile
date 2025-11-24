FROM node:18

WORKDIR /app

# Copy package.json and package-lock.json from application-service folder
COPY application-service/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY application-service/. .

# Expose the port your app runs on
EXPOSE 3000

# Start the app
CMD ["node", "src/index.js"]

