# Use official Node.js runtime as a base image
FROM node:18-alpine

# Set working directory inside container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for better caching)
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy the rest of the application code
COPY . .

# Expose the port your app runs on (default Express: 3000)
EXPOSE 3000

# Start the application
CMD ["node", "server.js"]
