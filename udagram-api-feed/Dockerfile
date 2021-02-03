# Use NodeJS base image
FROM node:12.20.0

# Create app directory
WORKDIR /usr/src/api-feed

# Install app dependencies by copying
# package.json and package-lock.json
COPY *.json ./

# Install dependencies
RUN npm install

# Copy app source
COPY . ./

# NOT SECURE SET ENV
ENV PORT=8080
# Bind the port that the image will run on
EXPOSE 8080

# Define the Docker image's behavior at runtime
CMD ["npm", "run", "dev"]
