# Install Wordpress with Docker

## Usage

### Start the WordPress server

```bash
docker compose up
```

### Get IP address of the WordPress server

```bash
docker inspect \
  -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' \
  $(docker compose ps -q nginx)
```

### Access the WordPress server

Open a web browser and go to the IP address of the WordPress server on port 8080.

You can also use the following command to open the WordPress server in a web browser.

```bash
container=$(docker compose ps -q nginx)
ip=$(docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $container)
xdg-open http://$ip:8080
```

## Documentation

* https://gitlab.com/geoffrey-grebert/wordpress-simple-linux
