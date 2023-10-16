# Compose file source

- https://github.com/Graylog2/docker-compose
    - open_core/docker-compose.yml
        - modified volume definition in compose file 
    - open_core/.env.example
        - copy .env.example to .env and modify it


# .env

```bash
# GRAYLOG_PASSWORD_SECRET
pwgen -N 1 -s 96

# GRAYLOG_ROOT_PASSWORD_SHA2
echo -n "Enter Password: " && head -1 </dev/stdin | tr -d '\n' | sha256sum | cut -d" " -f1
```

# Startup

```bash
docker-compose up -d
```
