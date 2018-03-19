# Curso Git desde CERO

Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos

## Zonas de Git
1. Directorio de trabajo
2. Area de preparacion
3. Directorio Git


## Flujo de trabajo basico de Git.
1. Modificas una serie de archivos en tu directoriode trabajo.
2. Preparas los archivos, añadiendolos a tu area de preparacion.
3. Confirmas los cambios, lo que toma los archivos tal y como estan en el area de preparacion y almacena esa copia instantanea de manera permanente en tu directorio Git.

## Configurando Git por primera vez
```
git config --global user.name "name"
git config --global user.email "email"
git config --global core.editor nano
git config list
```

### Configuracion SSH en windows
Usando Gitbash seguimos los siguientes pasos:

1. Creamos una carpeta llamada `llaves-ssh` en alguna ubucacion de nuestra eleccion. Se recomienda crearla en el disco local `c` para evitar problemas de rutas.

2. Ejecutamos el comando `ssh-keygen -t rsa -C "mi-correo-ejemplo@ejemplo.com"`
El correo debe ser el mismo con el que nos registramos en Github para evitar posibles problemas.
Dejamos el passphrase vacio y damos enter.
Cuando nos pida la ruta escribimos `/c/Users/Elodia/llaves-ssh/github_rsa`

3. Iniciamos ssh-agent en background ejecutando el comando `eval $(ssh-agent -s)`.

4. Agregamos la llave ssh generada a ssh-agent ejecutando el comando `ssh add /c/Users/Elodia/llaves-ssh/github_rsa`.

5. Usar el comando `cat /c/Users/Elodia/llaves-ssh/github_rsa.pub`.
Con este comando vemos todo el contenido del archivo, copiamos todo el texto que nos muestra.

6. Ir a las configuraciones de nuestro Github y agregar una nueva llave SSH con el contenido que hemos copiado de `github_rsa.pub`.

Desde ahora podemos hacer pull y push sin que Github nos este pidiendo los datos de acceso.

