# # FROM nginx:alpine
# # COPY build /usr/share/nginx/html
# # EXPOSE 80
# # CMD ["nginx", "-g", "daemon off;"]


# FROM node:alpine
# WORKDIR /app
# COPY package.json ./
# COPY package-lock.json ./
# EXPOSE 3000
# COPY . .
# CMD ["npm", "run", "start"]

FROM node:20

# Install yarn
RUN npm install yarn

WORKDIR /app

# Copy package.json and package-lock.json files
COPY package.json .
COPY package-lock.json .

# Expose port 3000
EXPOSE 3000

# Copy the rest of the application files
COPY . .

RUN npm install react-scripts --legacy-peer-deps

# Command to start the application
CMD ["npm", "run", "start"]
