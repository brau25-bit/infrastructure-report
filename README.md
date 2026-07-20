# Sistema de reportes infrastructura

Configuracion de docker compose para levantar los servicios necesarios para el poryecto "Sistema de gestion de reportes"

Actualmente inlcuye:

- Frontend
- Nginx
- API nodejs

## Requisitos

- Docker 29.6.1
- Docker compose v5.2.0

## Variables de entorno

Crear un archivo '.env'.

ejemplo:

- POSTGRES_USER=mangaAdmin
- POSTGRES_PASSWORD=password
- POSTGRES_DB=manga

## Ejecucion

Constuir e iniciar contenedores:

```bash
docker compose up -d 
```

Ver servicios activos:

```bash
docker compose ps
```

Ver logs:
```bash
docker compose logs -f 
```

## Puertos

Docker tomara los puertos por defecto de cada servicio, si es necesario usar un puerto se pueden agregar mediante la opcion:

```docker
ports:
  - "host_port:cont_port"
```