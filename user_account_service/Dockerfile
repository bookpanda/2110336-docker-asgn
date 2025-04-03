# Use Node v4 as the base image.
FROM node:4

WORKDIR /app

# Add everything in the current directory to our image, in the 'app' folder.
COPY package.json /app/

# Install dependencies
RUN npm cache clean --force && npm install

COPY . /app

# Expose our server port.
EXPOSE 80

# Run our app.
CMD ["node", "/app/index.js"]
