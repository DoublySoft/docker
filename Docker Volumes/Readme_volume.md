Crear volumen desde la línea de comandos:
- `-v <local_path:container_path>` Establecemos la ruta local y la del contenedor dónde quedarán guardados los archivos.
```
docker run -d -v <local_path:container_path> <image>
```

Crear volumen anónimo desde la línea de comandos:
- `-v <container_path>` Establecemos la ruta del contenedor de dónde se extraerán los datos y docker se encargará de guardarlos.
```
docker run -d -v <container_path> <image>
```

Crear volumen mediante nombre:
```
docker volume create <volume_name>
```

Levantar contenedor mediante volumen creado:
```
docker run -d -v <volume_name:container_path> <image>
```

Listar volúmenes sin usar:
```
docker volume ls -f dangling=true
```

Eliminar volúmenes sin usar:
```
docker volume rm (docker volume ls -f dangling=true -q)
```