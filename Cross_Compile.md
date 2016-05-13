# Compilacion Cruzada

## Introduccion

La compilacion de codigo fuente realizado bajo una determinada arquitectura que genera codigo ejecutable para una arquitectura diferente se llama __compilacion cruzada__ .

En la compilacion cruzada hay dos tipos de sistemas

__*huesped*__
:donde nos brinda la oportunidad de aprovechar los recursos que disponemos  

__*objetivo*__ :
donde se ejecuta el codigo.

para realizar este tipo de compilacion nos apoyamos de __Builroot__.

## Builroot

Esta es una herramienta que simplifica y automatiza el proceso de construccion de un sistema embebido linux completo, usando compilacion cruzada.

### Requerimientos de sistemas

Builroot esta diseñado para correr en sistema linux.

Esta es una lista general de los paquetes obligatorios para ejecutar *builroot*:

+ which
+ sed
+ make (version 3.81 or any later)
+ binutils
+ build-essential (only for Debian based systems)
+ gcc (version 2.95 or any later)
+ g++ (version 2.95 or any later)
+ bash
+ patch
+ gzip
+ bzip2
+ perl (version 5.8.7 or any later)
+ tar
+ cpio
+ python (version 2.6 or any later)
+ unzip
+ rsync
+ wget
+git


## Compilacion para la Raspberry Pi 2

### Sistema huesped

A continuacion se muestra una descripcion del CPU que sera utilizado como *huesped*

+ Architecture:          x86_64
+ CPU op-mode(s):        32-bit, 64-bit
+ Byte Order:            Little Endian
+ CPU(s):                12
+ On-line CPU(s) list:   0-11
+ Thread(s) per core:    2
+ Core(s) per socket:    6
+ Socket(s):             1
+ NUMA node(s):          1
+ Vendor ID:             GenuineIntel
+ CPU family:            6
+ Model:                 45
+ Model name:            Intel(R) Xeon(R) CPU E5-2620 0 @ + 2.00GHz
+ Stepping:              7
+ CPU MHz:               1814.062
+ BogoMIPS:              4000.22
+ Virtualization:        VT-x
+ L1d cache:             32K
+ L1i cache:             32K
+ L2 cache:              256K
+ L3 cache:              15360K
+ NUMA node0 CPU(s):     0-11

### Obtencion de buildroot

Primero tenemos que obtener directamente de la pagina de buildroot

	$ wget https://buildroot.org/downloads/buildroot-2016.02.tar.gz

### Descomprimir el archivo

Una vez que tenemos el archivo bastara con descomprimirlo

	 $ tar xvzf buildroot-2016.02.tar.gz

### Configuracion para Raspberry Pi 2

Nuestro sistema objetivo esta descrito a continuacion.

bla bla bla

accedemos al directorio descomprimido y como la Raspberry Pi 2 es una tarjeta popular ya existe un archivo de configuracion paa esta tarjeta ( como tambien lo existe para la version 1 y recientemente para la version 3)

Ahora simplemente hay que ejecutar el siguiente comando:

	$ make raspberrypi2_defconfig

Ahora para agregar paquetes a nuestra compilacion simplemnte ejecutamos:

	$ make menuconfig

Donde nos muesta ventanas donde podemos elegir paquetes o opciones a compilar que previamente no incluia el archivo *"raspberrypi2_defconfig"*

![uno](Imagenes/01.png "Pantalla inicial")
