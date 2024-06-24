# APP - Microservices

[![My Skills](https://skillicons.dev/icons?i=prisma,git,nestjs,ts,sqlite,postgres,yarn)](https://skillicons.dev)

En este folder se encuentran un:

1. `docker-compose.yml`
2. `.env`

Los cuales sirven para levantar una aplicacion de microservices, estos son:

1. `auth-ms`
2. `orders-ms`
3. `products-ms`
4. `gateway-ms`
5. `payments-ms`

El `docker-compose.yml` no construye las imagenes de los microservice sino que usa imagenes ya construidas.

## Opciones para adquirir las imagenes

### Opcion 1:

    1. Clonar cada repositorio del microservice correspondiente, por ejemplo:
        git clone https://github.com/Nest-Microservices-Shop/auth-ms.git

    2. Paso seguido debes moverte al directorio de los microservice para crear un .env segun el template

    3. Luego debes construir la imagen de cada microservice con el comando `docker compose -f docker-compose.yml build` o el ``docker compose -f docker-compose.prod.yml build`` segun sea el caso

        NOTA: importante, debes modificar el nombre de la imagen dentro del docker-compose.yml que se encuentra en la raiz de este proyecto con el nombre que le asignaste al crearla segun el docker-compose.prod.yml dentro de cada microservice

    4. Finalmente debes levantar un contenedor con las imagenes respectivas `docker compose up -d`

### Opcion 2:

    1. Clonar este repositorio

    2. Crear un .env segun el .env.template

    3. Iniciar docker desktop

    4. Finalmente debes ejecutar `docker compose up -d`

    -   Importante: Las imagenes que se usan en este docker-compose.yml ya se encuentran en el mi docker hub

### Fuente:

El codigo fuente de todo la aplicacion de microservice de estas imagenes de docker se pueden encontrar en la siguiente organization:

```
https://github.com/Nest-Microservices-Shop
```

NOTA:
Existe una tercera opcion para levantar esta aplicacion, pero la misma se indica en el README.md del codigo fuente de la organization mencionada anteriormente. Especificamente en el `products-launcher`
