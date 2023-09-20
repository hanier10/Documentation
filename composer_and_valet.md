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

Ahora crea un directorio en **HOME** llamado ***Sites**,* en este directorio guardarás los repositorios de PHP, cuando hayas creado la carpeta y agregado los repositorios que necesites, dentro de ***Sites*** ejecuta el siguiente comando*:*

`valet park`

Ahora puedes hacer un `valet restart` para resetear valet

Puedes verificar el status de tu valet con:

`valet status`

Y listo, ya puedes ir al navegador y ejecutar `tuproyecto.test` para verificar que está funcionando
