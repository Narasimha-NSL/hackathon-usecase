# Use Node.js 18 LTS
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY COPY src/package*.json ./

RUN npm install --production

# Copy source code
COPY src/ ./src

# Expose the port
EXPOSE 3001

# Start the application
CMD ["node", "src/index.js"]

