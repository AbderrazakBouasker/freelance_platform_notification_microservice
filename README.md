# freelance_platform_notification_microservice

## Docker build instructions

### Create a docker network if it doesn't exist
```bash
docker network create freelance-platform
```

### Build the docker image
```bash
docker build -t notification-service .
```

### Run the docker image
```bash
docker run -p 9093:8080 --name notification-service --network freelance-platform notification-service
```

### Test the service
```bash
curl http://localhost:9093/hello
```

