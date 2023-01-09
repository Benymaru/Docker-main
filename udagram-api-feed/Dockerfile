# Use NodeJS base image
FROM node:13

# Create directory
WORKDIR /usr/src/app


# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy app source
COPY . .

# port image
EXPOSE 8080

# Define the Docker image
CMD [ "npm", "run", "prod" ]
