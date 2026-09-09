# Laboratorio 02 - Solución

## Comandos a ejecutar

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
8. Verificar que el estatus sea de la segunda instancia
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

