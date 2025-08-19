# Personal Portfolio

This repository contains a simple static site served by Caddy inside Docker.

## Development setup

1. **Install Docker** and the Docker Compose plugin.
2. **Start the dev server**:
   ```sh
   docker compose -f deploy/docker-compose.dev.yml up --build
   ```
   - Builds the Caddy image defined in `docker/Dockerfile`.
   - Serves the files in `app/` on [http://localhost:3000](http://localhost:3000).
   - Automatically reloads when you edit files under `app/`.
3. **Stop the server** with `Ctrl+C` and clean up containers:
   ```sh
   docker compose -f deploy/docker-compose.dev.yml down
   ```

