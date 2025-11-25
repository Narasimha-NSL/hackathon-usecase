# Use Node.js 18 LTS
FROM node:18

# Set working directory
WORKDIR /app
COPY src/package*.json ./
RUN npm install --production

# Copy the rest of the source code
COPY src/. .

# Expose the port (optional, for clarity)
EXPOSE 3003

# Start the application
CMD ["node", "index.js"]
