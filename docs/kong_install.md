# Kong Installation

If you want to set up Kong locally, you can easily use Docker Compose for local development.

Follow the Docker Compose configuration provided here:
[docker-compose.yaml](../docker-compose.yaml)

Make sure you have the following installed before starting:
- Docker
- Docker Compose

<br />

Then run:
```bash
docker compose up -d
```

This will start Kong and its required services in detached mode.

<br />

To verify that Kong is running:

```bash
docker ps
```