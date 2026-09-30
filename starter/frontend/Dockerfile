FROM node:18-alpine

ARG REACT_APP_MOVIE_API_URL
ENV REACT_APP_MOVIE_API_URL=${REACT_APP_MOVIE_API_URL}

WORKDIR /app

# Copy dependency files
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy application code
COPY . .

# Build the React application
RUN npm run build

# Expose frontend port
EXPOSE 3000

# Start the application
CMD ["npm", "run", "serve"]
