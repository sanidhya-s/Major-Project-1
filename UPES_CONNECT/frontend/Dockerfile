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
WORKDIR /app
COPY package.json .
COPY package-lock.json .
EXPOSE 3000
COPY . .
RUN npm install react-scripts --legacy-peer-deps
CMD ["npm", "run", "start"]
