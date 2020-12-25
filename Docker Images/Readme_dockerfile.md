# Generar fichero Dockerfile

Asignar el sistema operativo o imagen del contendor:
```
FROM <image>
```

Ejecutar instrucciones/comandos del sistema operativo asignado en el fichero con la instrucción `FROM` al montar la imágen:
```
RUN <command>
```

Copiar archivos a la imagen:
- `COPY` Copia archivos locales a la imagen.
- `ADD` Copia archivos desde una URL a la imagen.
```
COPY/ADD <local_path>:<container_path>
```

Variables de entorno:
```
ENV <variable> <content>
```

Directorios de trabajo:
```
WORKDIR <path>
```

Exponer puertos:
```
EXPOSE <port>
```

*Descripción*
```
LABEL <label>=<content>
```

Asignar el usuario que va a ejecutar las tareas:
```
USER <username>
```

Guardar archivos generados en el contenedor de forma persistente en la máquina física, evitando que se pierda el contenido una vez el contenedor muera:
```
VOLUME
```

*Descripción*
```
CMD
```

Fichero para ignorar directorios y archivos:
```
.dockerignore
```