# Plano

Maqueta 3D, plano acotado y paseo en primera persona del piso, reconstruidos a partir de dos vídeos. Las medidas son estimadas.

Todo sale de las listas del principio del script de `app/index.html`: al cambiar una medida cambian la maqueta, el plano y las colisiones. Las luces y persianas son una simulación; la función `enviarComando` es el punto donde conectar los aparatos reales.

## Desplegar en Portainer

1. **Stacks › Add stack › Web editor** y pega `docker-compose.yml`.
2. Despliega en Servidor-Oracle. Escucha en el puerto `3082`.
3. Publícalo en `plano.marcogugliandolo.com`.

Al arrancar, el contenedor descarga `main` de este repositorio y lo sirve con nginx. Para publicar cambios: push a GitHub y reinicia el contenedor.

## Archivos

```
app/index.html      la web (una sola página)
nginx.conf          servidor en el puerto 3000
docker-compose.yml  stack para Portainer
```
