# Docker Compose

Levantar contenedores:
```
docker-compose up -d
```

Levantar contenedores mediante un fichero `yml` nombrado distinto de `docker-compose`:
- `-f <file_name>` Asignamos el nombre del fichero.
```
docker-compose -f <file_name> up -d
```

Parar y eliminar contenedores:
```
docker-compose down
```

Construir image
```
docker-compose build
```


## Docker compose file examples:

- [Port](docker-compose-port.yml)
- [Env](docker-compose-env.yml)
- [Volume](docker-compose-volume.yml)
- [Network](docker-compose-network.yml)
- [Build](docker-compose-build.yml)
- [Cmd](docker-compose-cmd.yml)
- [Memory](docker-compose-memory.yml)
- [Restart](docker-compose-restart.yml)