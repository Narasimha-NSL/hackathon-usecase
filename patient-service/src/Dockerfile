# application-service/Dockerfile
FROM node:18

WORKDIR /app

# Copy only package files if they exist
COPY package*.json ./ 2>/dev/null || echo "No package.json, skipping npm install"

# Install dependencies if package.json exists
RUN if [ -f package.json ]; then npm install; fi

# Copy the rest of the source code
COPY . .

# Expose port
EXPOSE 3000

# Start the app
CMD ["node", "src/index.js"]
