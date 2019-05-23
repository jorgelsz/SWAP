# Práctica 6

## ¿Qué hemos hecho?

En esta práctica se ha intentado trabajar con NFS, haciendo que un servidor se encargase de exportar una carpeta mediante NFS a todos sus clientes.

### Configurar servidor

Para comenzar debemos de instalar las herramientas que vamos a utilizar:

![Instalar herramientas](./assets/install.png)

Tras esto creamos la carpeta que deseamos compartir y le damos los permisos necesarios:

![Crear carpeta y dar permisos](./assets/permisos.png)

Tras esto debemos de editar el fichero `/etc/exports` para dar permisos de lectura y escritura a los clientes.

`/dat/compartida/ 192.168.56.11(rw) 192.168.56.12(rw)`

Una vez realizado esto, tan solo quedará reiniciar el servicio en el servidor:
`sudo service nfs-kernel-server restart`


### Configurar cliente

Debemos de instalar los paquetes que vamos a usar y crear el punto de monaje:

![Crear carpeta](./assets/cliente.png)
![Crear punto de montaje](./assets/mount.png)

Tras esto ya tenemos el sistema funcionando.
Tan solo quedaría modificar el archivo fstab para que no se desconfigure cada vez que el sistema se reinicia.
Para ello hemos de escribir lo siguiente en el archivo `/etc/fstab`:

![Archivo fstab](./assets/fstab.png)



