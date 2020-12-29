Tipos de networks por defecto:
- `bridge` Red por defecto.
- `host` Red local.
- `overlay`
- `macvlan`
- `none` Sin red.

Listar todas las redes existentes:
```
docker network ls
```

Crear una red:
```
docker network create <network_name>
```

Eliminar una red:
```
docker network rm <network_name>
```

Crear una red con subred y puerta de enlace:
- `--subnet <subnet_ip>/<range>` Asignar rangos de IP de la subred.
- `--gateway <gateway_ip>` Asignar puerta de enlace.
```
docker network create --subnet <subnet_ip>/<range> --gateway <gateway_ip> <network_name>
```

Levantar un contenedor en una red específica:
- `--network <network>` Asignar la red al contenedor.
```
docker run -d --network <network> <image>
```

Conectar contenedores entre distintas redes:
```
docker network connect <network> <container>
```

Desconectar contenedores entre distintas redes:
```
docker network disconnect <network> <container>
```

Asginar IP a un contenedor:
```
docker run -d --network <network> --ip <ip> <image>
```