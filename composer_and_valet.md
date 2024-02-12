# **Instalando Composer y Valet**

Desde la terminal ejecutar

`brew install composer`

Instalando Valet desde composer

`composer global require laravel/valet`

Puedes cerciorar que la instalacion de Composer ha funcionado ejecutando unicamente `composer` en la terminal

Lo siguiente que se instalará por lo general se realiza en la instalación cuando haces `valet install` pero si deseas realizarlo acá de forma individual, te dejo estos comandos:

## Instalando dnsmasq

`brew install dnsmasq`

Ejecutar el path

`echo "address=/.test/127.0.0.1" > $(brew --prefix)/etc/dnsmasq.conf`

Reiniciar dnsmasq

`sudo brew services restart dnsmasq`

## Instalando nginx

`brew install nginx`

## Instalando Valet

`valet install`

## Iniciando Valet

`valet start`

Ahora crea un directorio en **HOME** llamado ***Sites**,* en este directorio guardarás los repositorios de PHP, cuando hayas creado la carpeta y agregado los repositorios que necesites, dentro de ***Sites*** ejecuta el siguiente comando:

`valet park`

## Ahora instala redis

`brew install redis`

y luego ejecutas

`redis-server`

Ahora puedes hacer un `valet restart` para resetear valet

Puedes verificar el status de tu valet con:

`valet status`

Y listo, ya puedes ir al navegador y ejecutar `tuproyecto.test` para verificar que está funcionando

# Ojo si te da problemas el valet, un error tipo: ***Laravel Valet 502 Bad Gateway*** haz esto.

Acceder a la ruta desde tu carpeta raíz:

`nano /usr/local/etc/nginx/nginx.conf` y agrega las siguientes líneas:

`
fastcgi_buffers 16 16k;
`


`
fastcgi_buffer_size 32k;
`

Luego guardas con Cltr + O (letra O) y presionas enter, y luego Ctrl + X para salir 

Luego copia el archivo `laravel-echo-server.json` en el repositorio sgu, este archivo se encuentra en las carpetas compartidas en la nube, en la carpeta `recursos` específicamente

Luego haz un `composer global update`

Luego `valet install`

## Consideraciones a tener en cuenta

1. Checa tu versión de PHP en la consola, que sea la correcta: `php -v`
2. Detén redis y vuelvelo a correr
3. Ejecuta dentro del repo: `laravel-echo-server start`
4. Ejecuta `npm run hot`
