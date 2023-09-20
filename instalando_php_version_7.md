# Instalacion de PHP 7.4 en MacOS

---

## Instalar Homebrew

El primer paso seria descargar Homebrew, descárgalo desde la página oficial o bien desde el siguiente enlace:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Para asegurarte que has instalado homebrew puedes hacer desde la terminal el comando

`brew --version`

## Instalar la fórmula de PHP

Instalar la formula con este primer comando

`brew tap shivammathur/php`

y luego

`brew install shivammathur/php/php@7.4`

## Colocar el path en el archivo .zshrc (Recuerda tener instalado zsh y ohmyzsh en tu terminal)

Agregar el path en el archivo que generalmente se encuentra en el directorio de HOME de tu Mac, eso lo haras ejecutando estos comandos desde la terminal:

1.

`echo 'export PATH="/usr/local/opt/php@7.4/bin:$PATH"' >> ~/.zshrc`

2.

`echo 'export PATH="/usr/local/opt/php@7.4/sbin:$PATH"' >> ~/.zshrc`

También agregas los siguientes:

1.

`export LDFLAGS="-L/usr/local/opt/php@7.4/lib"`

2.

`export CPPFLAGS="-I/usr/local/opt/php@7.4/include”`

## Reiniciar la terminal

Si estas con .zshrc hacer lo siguiente:

`source ~/.zshrc`

Reiniciamos el servicio

`brew services restart shivammathur/php/php@7.4`

## Seleccionar la versión de PHP instalada

Siempre desde la terminal haces:

`brew link php@7.4`

Ahora haces un `php-v` para verificar que efectivamente la versión de PHP está instalada y en uso, tendrías que ver una salida como esto:

```
PHP 7.4.33 (cli) (built: Sep  1 2023 04:12:20) ( NTS )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
    with Zend OPcache v7.4.33, Copyright (c), by Zend Technologies
```
