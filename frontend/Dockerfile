# Use official Node.js image as base
FROM node:18

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Build the React app
RUN npm run build

# Install a static file server to serve the built React app
RUN npm install -g serve

# Expose the port the app runs on
EXPOSE 3000

# Command to start the application
CMD ["serve", "-s", "build", "-l", "3000"]
