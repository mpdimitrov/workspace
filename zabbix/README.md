# Tuto Zabbix

Zabbix installation

![](https://github.com/akmalovaa/zabbix-docker/raw/main/.images/scheme.excalidraw.png)

## Usage

### Installation

1. Start all the services

    ```bash
    docker compose up -d
    ```

2. Open the url <http://localhost:8080> (retry many times if the login page is not yet ready)

3. Connect to Zabbix with the following user:
   
   * username: `admin`
   * password: `zabbix`

4. Edit the **Host configuration** of the `Zabbix server` host:
   1. Set the *DNS name* to `zabbix-agent`
   2. Set the *Connect to* to `DNS`

### Uninstall

```
docker compose down --volumes
```

### Start and Stop

#### Stop

```bash
docker compose stop
```

#### Start

```
docker compose start
```

## External doc

* https://github.com/akmalovaa/zabbix-docker
* Docker images:
  * [MariaDB](https://hub.docker.com/_/mariadb)
  * Zabbix:
    * [Server Mysql](https://hub.docker.com/r/zabbix/zabbix-server-mysql)
    * [Web Nginx](https://hub.docker.com/r/zabbix/zabbix-web-nginx-mysql)
    * [Agent](https://hub.docker.com/r/zabbix/zabbix-agent)
