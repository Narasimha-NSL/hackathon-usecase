# Use Node.js 18 LTS
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install --production

# Copy source code
COPY . .

# Expose the port (optional, for clarity)
EXPOSE 3003

# Start the application
CMD ["node", "index.js"]
