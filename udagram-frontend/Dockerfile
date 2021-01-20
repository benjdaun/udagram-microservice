# Use NodeJS base image
FROM node:12.20.0

# Create app directory
WORKDIR /usr/src/frontend

# Install app dependencies by copying
# package.json and package-lock.json
COPY *.json ./

# Install ionic
RUN npm install -g ionic
# Install dependencies
RUN npm install

# Copy app source
COPY . ./

# build ionic build

RUN ionic build

# NOT SECURE SET ENV
ENV PORT=8100
# Bind the port that the image will run on
EXPOSE 8100

# Define the Docker image's behavior at runtime
CMD ["ionic", "serve"]
