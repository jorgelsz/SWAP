# Práctica 1

## ¿Qué hemos hecho?
La primera práctica ha consistido en la puesta a punto de las máquinas virtuales en nuestros ordenadores.
Las máquinas instaladas han sido un par de **Ubuntu Server 16.04**.

El software que hemos utilizado para virtualizar ha sido **VirtualBox**.

En cada máquina se ha instalado la pila LAMP para que puedan servir como servidores web.

### A tener en cuenta
Para la correcta realización de la práctica era necesario que ambas máquinas se pudieran comunicar entre sí, y además, con la máquina host.
Para ello hemos debido de añadir un nuevo adaptador de red a cada máquina virtual, teniendo uno de ellos de tipo **Red NAT** y otro de tipo **Host-Only**. De esta forma sendas máquinas se comunican entre sí, y tienen conexión con el exterior.

