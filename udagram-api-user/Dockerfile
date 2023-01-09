# Use NodeJS 
FROM node:13

# Create  directory
WORKDIR /usr/src/app


# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy app source
COPY . .

# port image
EXPOSE 8080

# Docker image
CMD [ "npm", "run", "prod" ]
