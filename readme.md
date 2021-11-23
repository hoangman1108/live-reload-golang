# How to run

Hide **mysql** in docker-compose if not use

```bash
version: "3.8"
services:
  web:
    build:
      context: .
      dockerfile: dev.Dockerfile
    container_name: menekel_api
    ports:
      - 3000:9090
    # depends_on:
    #   - mysql
    volumes:
      - ./:/app
  # mysql:
  #   image: mysql:5.7 
  #   container_name: menekel_mysql
  #   command: mysqld --user=root
  #   ports:
  #     - 3306:3306
  #   environment:
  #     - MYSQL_DATABASE=article
  #     - MYSQL_USER=user
  #     - MYSQL_PASSWORD=password
  #     - MYSQL_ROOT_PASSWORD=root
  #   healthcheck:
  #     test: ["CMD", "mysqladmin" ,"ping", "-h", "localhost"]
  #     timeout: 5s
  #     retries: 10
```

Copy **config.toml.example** to **config.toml**

```bash
cp config.toml.example config.toml
```

## Live code relead

Use docker compose

Run code

```bash
docker-compose up -d
```

Check logs

```bash
docker-compose logs -f
```
## License
[Hoang Man](https://github.com/hoangman1108/live-reload-golang)