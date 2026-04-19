# Use official Node.js LTS image
FROM node:18-alpine

# Set working directory inside the container
WORKDIR /usr/src/app

# Copy package files first (layer caching optimization)
COPY package*.json ./

# Install dependencies
RUN npm install --only=production

# Copy application source code
COPY app.js .

# Expose the port the app runs on
EXPOSE 3000

# Define the command to run the app
CMD ["node", "app.js"]
