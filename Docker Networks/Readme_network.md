Tipos de networks por defecto:
- `bridge` Network por defecto.
- `host` 
- `overlay`
- `macvlan`
- `none`

Listar todas las redes existentes:
```
docker network ls
```

Crear una red con el nombre que queramos asignar:
```
docker network create <network_name>
```

Crear una red con subred y puerta de enlace:
- `--subnet <subnet_ip>/<range>` Asignar rangos de IP de la subred.
- `--gateway <gateway_ip>` Asignar puerta de enlace.
```
docker network create --subnet 172.124.10.0/24 --gateway 172.124.10.1 <network_name>
```


:
```

```

:
```

```

:
```

```