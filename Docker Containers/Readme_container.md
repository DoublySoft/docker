Listar todas la imagenes:
```
docker images
```

Listar imagenes por filtrado:
```
docker images | grep <name>
```

Listar contenedores levantados;
```
docker ps
```

Listar todos los contenedores:
```
docker ps -a
```

Levantar contenedor desde una imagen:
- `-d --detach` Lanzar contenedor en segundo plano.
- `-p --port <lacal_port:container_port>`  Mapear puertos para interactuar con ellos en local.
```
docker run -d -p <lacal_port:container_port> <image>
```

Renombrar contenedor:
```
docker rename <old_name> <new_name>
```

Iniciar contenedor:
```
docker start <container>
```

Reiniciar contenedor:
```
docker restart <container>
```

Detener contenedor:
```
docker stop <container>
```

Acceder al contenedor:
- `-i --interactive` Ver iteractividad del contenedor.
- `-t --tty` Acceder al terminal del contenedor.
- `-u --user` Usuario dentro del contenedor.
```
docker exec -i -t <container> bash
```

Ver consumo de recursos de un contenedor:
```
docker stats <container>
```

Limitar consumo de RAM de un contenedor:
```
docker run -d -m <bytes> <image>
```

Limitar consumo de CPU de un contenedor:
```
docker run -d -c <cpus> <image>
```

Copiar archivos de local a un contendor
```
docker cp <local_file> <container:path>
```

Copiar archivos de un contenedor a local
```
docker cp <container:path> <local_file>
```

Convertir un contenedor en una imagen:
```
docker commit <container> <image>
```