# docker/Dockerfile
FROM caddy:alpine

# Copy the Caddy config into the standard path
COPY docker/Caddyfile.prod /etc/caddy/Caddyfile

# Copy your static site into the container
COPY app /srv