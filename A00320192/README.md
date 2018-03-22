# so-exam1
### Examen 1
**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Tema:** Comandos de Linux, Virtualización
**Estudiante:** Juan Camilo Villada G.  
**Código:** A00320192  
**Correo:** jncvg17@hotmail.com

### Actividades

**Validación ISO Debian 9**
1. Primero se descarga la imagen adecuada de Debian 9 de la web oficial. (https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/)
2. En la misma pagina, acceder a MD5SUMS para obtener los valores MD5 del archivo ISO de Debian.
3. Una vez finalizada la descarga, realizar la validación (MD5, SHA-1, SHA-256 o SHA-512) y comparar sus resultados

Nota: Para esta validación se uso el siguiente comando en el sistema operativo macOS High Sierra

``` sh
md5 archivo.iso | grep valorMD5
```

![alt text](https://raw.githubusercontent.com/JnCV17/so-exam1/master/A00320192/screenshots/ScreenshotValidacion.png)

**Instalación Debian 9**

1. Primero, se inicia VirtualBox

2. Una vez iniciado VirtualBox, nos dirigimos a la pestaña "New" y hacemos clic alli.

3. Despues de hacer clic en "New" se desplegara una ventana donde se solicita el nombre de la maquina virtual que se desea crear, el sistema operativo de la maquina virtual y la version del sistema operativo. En este caso, al nombrar Debian a la maquina, se ajustaran automaticamente los otros campos a "Linux" y "Debian (64-bit)". Una vez hecho esto, hacemos clic en "Continue"

4. En la siguiente ventana se desplegara una ventana donde se solicita el tamaño de memoria RAM que se le desea asignar a la maquina virtual. Por defecto se encuentra en 1024 MB (1 GB). Una vez hecho esto, hacemos clic en "Continue"

5. Una vez asignada la RAM, se nos despliega una nueva ventana con información acerca del disco duro. En esta ventana nos permiten: No agregar un disco duro virtual, crear un nuevo disco virtual y seleccionar un disco duro virtual existente. Seleccionamos la opción para crear un nuevo disco virtual. Por defecto asignara 8.00 GB de disco duro.

6. Si se selecciona la opcion para crear un nuevo disco duro virtual, se desplegara un dialogo donde se solicita elegir el tipo de formato para el disco duro virtual, para el cual hay tres (3) tipos: VDI (VirtualBox Disk Image), VHD (Virtual Hard Disk) y VMDK (Virtual Machine Disk). Por defecto se encuentra seleccionada la opción VDI, por lo tanto continuaremos con esta.

7. Una vez seleccionado el tipo de formato para el disco duro virtual, se despliega un nuevo dialogo con dos opciones acerca del tamaño de almacenamiento para el disco duro. Estas dos opciones son "Dynamically Allocated" y "Fixed Size". Debido a que no sera necesario usar mas de 8 GB de memoria, seleccionamos la opción "Fixed Size".

8. Al continuar, se despliega una ventana para asignar el nombre al disco duro, su ubicacion y para re asignar el tamaño del disco duro. Dado que no necesitamos ninguna configuracion especial para este disco duro virtual continuaremos sin modificar nada y hacemos clic en la opcion "Create".

9. Una vez finalizado el proceso de creación, la ventana se cerrara y aparecera una nueva maquina virtual Debian con el nombre asignado anteriormente. Iniciamos esta maquina virtual.

10. Al iniciar la maquina virtual aparecera un dialogo el cual solicita la imagen de instalacion de Debian. Seleccionamos la imagen y hacemos clic en "Start".

11. Al hacer clic en "Start" la maquina se reiniciara y ejecutara la imagen de instalación de Debian. En ella seleccionamos la opcion "Install", luego seleccionamos el idioma deseado, el pais o region deseado y finalmente el mapeo de teclado deseado.
12. Una vez seleccionadas estas opciones, el instalador cargara componentes adicionales y al finalizar, solicitara la configuracion de la red. Podemos ignorar estas opciones por el momento y seleccionar continuar hasta la pantalla de creacion de usuarios y contraseñas

13. En la pantalla de creacion de usuarios y contraseñas, se solicita ingresar una contraseña de usuario root. Al ingresarla, seleccionamos continuar y nos solicitara que re ingresemos la contraseña root. Una vez hecho esto presionamos continuar.
14. Se desplegara una nueva pantalla solicitando ingresar el nombre completo del usuario. Al introducirlo y continuar, el instalador asignara un nombre de usuario a partir del nombre introducido anteriormente. Si se desea, se puede modificar, de lo contrario presionamos continuar.

15. Al continuar, se solicita una contraseña para el usuario anterior. Una vez se asigna la contraseña presionamos continuar.

16. Al continuar, el instalador realizara algunos ajustes automaticamente y solicitara que se seleccione la zona horaria en la que nos encontramos. Al seleccionar, presionamos continuar y el instalador continuara realizando ajustes automaticos hasta que despliegue una ventana con opciones de particionamiento de discos.

17. En la ventana de particionamiento de discos, se nos despliegan varias opciones: Instalacion guiada - uso completo del disco, Instalacion guiada - uso completo del disco y configuracion de un administrador de volumenes, Instalacion guiada - uso completo del disco y configuracion de un administrador de volumenes encriptado y Manual. Seleccionamos la opcion por defecto y presionamos continuar.

18. Al continuar, el instalador despliega una lista de discos duros disponibles. Se elige el disco duro en el que se desea realizar la instalacion y se presiona continuar.

19. Al continuar, se nos pide seleccionar un esquema de particionamiento para el cual hay tres (3) opciones: Todos los archivos en una sola particion, una particion /home independiente y particiones /home, /var y /tmp independientes. Seleccionamos la opcion por defecto y presionamos continuar.

20. Al continuar, el instalador realizara unas configuraciones automaticas y finalmente solicitara confirmar las opciones seleccionadas anteriormente o deshacerlos. Seleccionamos finalizar para continuar con el proceso.

21. Al seleccionar finalizar, se despliega una nueva ventana para confirmar estas selecciones, seleccionamos "Si" para continuar.

22. Al seleccionar "Si" el instalador inicia automaticamente la instalacion del sistema base.

23. Una vez finalizada la instalacion del sistema base, el instalador nos informara de la configuración del manejador de paquetes usando una imagen adicional, asi como de que podemos saltar este paso. En este caso, saltaremos este paso seleccionando la opcion "No"

24. Al seleccionar no, se despliega una nueva ventana de configuracion del manejador de paquetes donde se pide seleccionar el pais mas cercano a la red en la que nos encontramos, esto con el objetivo de encontrar un mirror adecuado para la configuracion del manejador de paquetes. Seleccionamos el pais y presionamos enter.

25. Al seleccionar el pais, se despliega un listado de mirrors para realizar la configuración. Seleccionamos el que deseamos y presionamos enter.

26. Al seleccionar el mirror, se nos solicita ingresar un Proxy si lo hay. En caso de no haber un proxy, como en este caso, simplemente presionamos continuar.

27. Al continuar, el instalador iniciara automaticamente el escaneo del mirror e iniciara la descarga de los archivos que necesite. Durante la instalación de estos archivos, saltaran dialogos a los que se puede marcar si o no y un dialogo donde listan una serie de paquetes que se pueden instalar en Debian para que se seleccione y se instale en este momento. (Este proceso podria tardar un poco)

28. Una vez finalizado este proceso, el instalador solicitara instalar GRUB boot debido a que es el unico sistema operativo en el disco duro. Aceptamos la instalación presionando "Si".

29. Una vez aceptada la instalación, el instalador desplegara una lista de discos duros que detecto, seleccionamos el disco duro en el que realizamos la instalacion y presionamos enter.

30. Una vez finalizada la instalacion, el sistema desplegara un mensaje indicando que el procedimiento fue exitoso. Presionamos continuar (si no lo hace automaticamente) y el instalador finalizara, reiniciando la maquina virtual

31. Una vez reinicie la maquina virtual, el sistema iniciara mostrando el usuario que creo anteriormente indicando que el sistema esta listo para ser usado y ha finalizado la instalacion correctamente.

Nota: Para consultar informacion del sistema operativo se usaron los siguientes comandos:

``` sh
cat /etc/debian_version
```

``` sh
lsb_release -a
```

``` sh
uname -a
```

``` sh
uname -r
```

![alt text](https://raw.githubusercontent.com/JnCV17/so-exam1/master/A00320192/screenshots/ScreenshotInfoDebian.png)

**Configuración de adaptador puente y conexión SSH**

1. Con la maquina virtual apagada, en "Ajustes", nos dirigimos a la pestaña "Red"
2. En la pestaña "Red", seleccionamos "Adaptador 1" que es la interfaz de red que se encuentra activa por defecto.
3. Cambiamos la opción de "NAT" a "Adaptador Puente" y seleccionamos a que puerto se conectara, Ethernet o WiFi. En este caso sera WiFi (AirPort).

![alt text](https://raw.githubusercontent.com/JnCV17/so-exam1/master/A00320192/screenshots/ScreenshotDebianNetConfig.png)


4. Iniciamos la maquina virtual.
5. Iniciamos Terminal en la maquina Debian
6. Haciendo uso del comando "ip a" obtenemos la información de las interfaces de red disponibles. Para el caso la interfaz enp0s3
7. Con la información obtenida de las interfaces de red, podemos intentar hacer una conexion por SSH a la maquina Debian. Al intentar una conexion, si no esta instalado el modulo de SSH en Debian, la conexion sera rechazada. Por lo tanto, instalaremos SSH en la maquina virtual.

``` sh
apt-get install openssh-server --no-install-recommends
```

8. Una vez instalado openssh, modificamos su configuracion para poder acceder a modo root desde SSH y reiniciamos el servicio una vez modificado el archivo.

``` sh
vim /etc/ssh/sshd_config
```

``` sh
# Authentication:
 
LoginGraceTime 2m
#PermitRootLogin prohibit-password
PermitRootLogin yes
StrictModes yes
#MaxAuthTries 6
#MaxSessions 10
```

9. Debido a que el sistema operativo Host es macOS, nos dirigimos a la aplicacion Terminal para realizar la conexion por SSH usando el usuario creado y la contraseña. Finalmente, se establece una conexion SSH entre el Host y la maquina virtual usando una interfaz de red en modo puente.

![alt text](https://raw.githubusercontent.com/JnCV17/so-exam1/master/A00320192/screenshots/ScreenshotSSH.png)





