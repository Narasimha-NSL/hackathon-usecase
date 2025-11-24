FROM node:18

WORKDIR /app

# Copy application source code
COPY application-service/. .

# Expose the port your app runs on
EXPOSE 3000

# Start the app
CMD ["node", "src/index.js"]
