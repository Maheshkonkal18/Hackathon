# STEP 1: Build React app
FROM node:18-alpine AS build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# STEP 2: Serve using Nginx
FROM nginx:alpine

# Copy build output to Nginx default folder
COPY --from=build /app/dist /usr/share/nginx/html

# Expose port 80 for HTTP
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
