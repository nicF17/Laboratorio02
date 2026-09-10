# Laboratorio 02 - Solución

## Comandos a ejecutar para configuración

1. Bajar la imagen
```bash
docker pull nmatsui/hello-world-api
```
### Primera copia
2. Correr imagen
```bash
docker run -d --rm -p 3000:3000 nmatsui/hello-world-api
```

3. Verificar que el estatus sea Up
```bash
docker ps
```
nombre: crazy_curie

ID: 32e8ac3acdb6

4. Visualizar logs
```bash
docker logs crazy_curie
```

### Segunda copia
5. Correr imagen
```bash
docker run -d --rm -p 3001:3000 nmatsui/hello-world-api
```
6. Verificar que el estatus sea de la segunda instancia
```bash
docker ps
```
nombre: busy_sanderson

ID: fbd65561c77c

### Tercera copia
7. Correr imagen
```bash
docker run -d --rm -p 3002:3000 nmatsui/hello-world-api
```
8. Verificar que el estatus sea de la tercera instancia
```bash
docker ps
```
nombre: crazy_jackson

ID: d648658ce40c

## Configuración de BD
1. Bajar BD
```bash
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

2. Verificar el estatus de la BD
```bash
docker ps
```

# Comandos para despliegue
1. Crear el archivo .env y colocar lo siguiente:
```bash
MESSAGE1="Nicolas Romero Castillo 1"
MESSAGE2="Nicolas Romero Castillo 2"
MESSAGE3="Nicolas Romero Castillo 3"
PASSWORD="password"
USER="user"
```

2. Comando para levantar el contenedor:
```bash
docker compose up -d
```


## Responder los tipos de redes y los tipos de volumen que existen en Docker

### Tipos de redes en Docker
Existen 6 tipos de redes en Docker: bridge, que es una red privada del host y es la que viene predeterminadamente; host, en donde el host y contenedor comparten la misma red; none, donde ningún contenedor comparte red; overlay, redes Swarm Overlay que permiten que los contenedores se conecten entre sí; upvlan, en donde se conectan contenedores a VLAN externas y macvlan en donde los contenedores se conectan como dispositivos de la red del host.

### Tipos de volúmenes en Docker
Existen tres tipos de volúmenes de datos en Docker: montaje de enlace, se le asigna del host a un archivo dentro del contenedor; volúmenes con nombre, que conserva datos después de eliminar o reiniciar un contenedor y volúmenes anónimos, se crea automáticamente si no colocas un nombre de volumen o enlace de montaje.

## Comentario
Profesor, me di cuenta que me di cuenta que en dos commits no usé Conventional Commits (olvidé "feat"), las disculpas del caso.

## Capturas de despliegue
![image alt](https://github.com/nicF17/Laboratorio02/blob/a87114a5315dff65941cc22bdf005f4411b6736c/IaC1.png)
![image alt](https://github.com/nicF17/Laboratorio02/blob/a87114a5315dff65941cc22bdf005f4411b6736c/Iac2.png)
![image alt](https://github.com/nicF17/Laboratorio02/blob/a87114a5315dff65941cc22bdf005f4411b6736c/IaC3.png)
![image alt](https://github.com/nicF17/Laboratorio02/blob/a87114a5315dff65941cc22bdf005f4411b6736c/IaC4.png)
![image alt](https://github.com/nicF17/Laboratorio02/blob/a87114a5315dff65941cc22bdf005f4411b6736c/IaC5.png)
