# Use Node.js 18
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json if they exist
COPY package*.json ./

# Install dependencies only if package.json exists
RUN if [ -f package.json ]; then npm install; fi

# Copy the rest of the application code
COPY . .

# Expose port (adjust to your app)
EXPOSE 3000

# Run the application
CMD ["node", "index.js"]

