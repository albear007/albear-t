# Build stage
FROM node:20-alpine AS build
WORKDIR /app
COPY package.json ./
RUN npm install
COPY app ./app
COPY vite.config.js ./
RUN npm run build

# Serve stage
FROM caddy:alpine
COPY docker/Caddyfile.prod /etc/caddy/Caddyfile
COPY --from=build /app/dist /srv
