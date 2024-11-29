### Pasos para instalar las imágenes de Docker en MacOS

Con estos pasos tendrás Postgres y el SGU Legacy con Docker

### Descargar e Instalar Docker Desktop, e inicia sesión

---

https://www.docker.com/products/docker-desktop/

- Luego haz un `docker-compose` en tu terminal y debería de aparecerte la version de Docker instalada en tu computadora

- Descargar las imágenes de Docker (Postgres y sgu) desde OneDrive en SGU/docker, descarga todo eso en .zip
- Luego ve a tu directorio local y en tu home crea una carpeta llamada *Docker*, descomprimelas y guardálas ahí

### Instalar Volúmenes y Networks

---

Una vez instalado Docker haz lo siguiente en tu terminal lanzando estos comandos:

![Captura de pantalla 2024-11-29 a la(s) 10.32.01 a. m..png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b1890256-bccc-4f30-a93c-9acf2e78b882/13beb8a9-b9b2-4653-8835-1cf8fb321856/Captura_de_pantalla_2024-11-29_a_la(s)_10.32.01_a._m..png)

### Instalando Postgresql

---

- Entra a la carpeta de *Postgres* y verificar en tu archivo `docker-compose.yml` que las siguientes lineas existan:

```jsx
 build:
      args:
        user: sammy
        uid: 1000
      context: ./
      dockerfile: Dockerfile  
```

> Si no las tienes agrégalas antes de la palabra image, asegúrate de la tabulación en el archivo y guarda los cambios
> 

- Ahora dentro de la carpeta de *Postgres* lanza desde consola el comando siguiente:

```jsx
docker-compose build
```

- Luego lanza:

```jsx
docker-compose up -d
```

Y listo.

### Instalando sgu

---

- Entra a la carpeta de *sgu y* lanza desde consola el comando siguiente:

```jsx
docker-compose build
```

- Luego lanza:

```jsx
docker-compose up -d
```

y listo.
