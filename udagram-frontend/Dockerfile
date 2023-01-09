# Use Ionic 
FROM beevelop/ionic AS ionic

# Create  directory
WORKDIR /usr/src/app


# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy app source
COPY . .

# Build project
RUN ionic build

# Use Nginx 
FROM nginx:alpine

# Copy www /usr/share/nginx/html
COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html
