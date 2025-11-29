# Backend (Node + Express + MongoDB)
FROM node:18-alpine

# Work directory inside container
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the code
COPY . .

# Environment variables (values you will pass at runtime)
ENV PORT=5000

# Container will listen on this port
EXPOSE 5000

# Start command
CMD ["npm", "start"]
