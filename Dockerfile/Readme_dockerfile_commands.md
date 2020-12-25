
# Docker build Image

## Docker build

Montar imagen de Docker:
- `--tag <tag:version>` Nombre que se le da a la imagen.
- `.` Ruta en la que se encuentra el fichero Dockerfile.
```
docker build --tag <tag:version> .
```

## Docker run

Montar contenedor de una imagen:
- `-d`
- `-p <local_port>:<container_port>`
- `image`
```
docker run -d -p <local_port>:<container_port> <image>
```

# Comandos para la ejecución constante de la imagen

Eliminar contenedor creado anteriormente:
```
docker rm <container> -f
```
Eliminar imagen construida anteriormente:
```
docker rmi <image>
```
Construir imagen:
```
docker build -t <image> .
```
Levantar contenedor partiendo de la imagen:
```
docker run -d -p 80:80 --name <container> <image>
```

Ejecución in-line:
```
docker rm <container> -f; docker rmi <image>; docker build -t <image> .; docker run -d -p 80:80 --name <container> <image>;
```