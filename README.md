# Virtual-Box-Maquina-virtual

En este espacio dejo mis apuntes sobre maquinas virtuales y sus usos

## Requerimientos

- Programa [Virtual Box](https://www.virtualbox.org/)
- Sistema operativo para la maquina virtual <b>Windows Server 2008</b>
- Conocimientos básicos sobre el internet (IPv4, DNS, ROUTER, HTTP, HTTPS )

## Instalación

### Creación de maquina virtual

1. Abrir el programa Virtual Box
2. Hacer click en la opción <b>Nuevo</b> o <b>Crear</b>
3. Seleccionar la opción <b>Windows</b> y <b>Windows Server 2008</b> y ponle un nombre a la maquina
4. Seleccionar la opción <b>Next</b> o <b>siguiente</b>
5. Elegir el espacio de memoria (en este caso 32Gb)
6. Seleccionar la opción <b>Next</b> o <b>siguiente</b> hasta crear la maquina virtual
7. Encender o abrir nueva maquina virtual

### Instalación de Windows Server 2008

1. Encender o abrir maquina virtual recién creada y seleccionar el archivo de instalación de Windows Server 2008
2. Sigue el paso de la instalación y selecciona si deseas partir el disco o no, el windows necesitara al menos 10Gb para su correcta instalación.
3. Una vez instalado el sistema operativo, se puede cerrar la maquina virtual y volver a abrirla para usarla

### Creación de una red

1. Navegar a <b>Centro de redes y Recursos compartidos > Administrar Conexiones de red > Conexión de area local > Propiedades > Protocolo de internet version 4 (TCP/IPv4) </b>
2. Seleccionar la opción <b>Usar la siguiente dirección IP</b> O similar para cambiar la dirección IP de manera manual para colocar la nueva IP (1.0.0.1 Para el ejemplo). La mascara de pondrá automática.
3. Comprobar la configuración a traves de la terminal de comandos CMD Usando el comando <b>ipconfig</b>

### Creación de Directorio Activo

#### Definición:

Es un conjunto de servidores que se comunican entre sí para proporcionar servicios de directorio a los clientes de director.
Los clientes de directorio son los usuarios y los programas que acceden a los recursos de red.
Los servidores de directorio son los servidores que proporcionan servicios de directorio a los clientes de directorio.
Cuando instalamos el directorio activo podemos decir que nuestro servidor es un controlador de dominio. A la vez que estos se conforman de uno o más dominios.
<i>Es decir que podemos controlar quienes tienen acceso a la información(archivos) a traves de usuarios</i>

#### Instalación

1. Abrir la ventana ejecutar o con el comando teclas Windows+R, y escribir <b>dcpromo</b>
2. Cuando cargue, seguiremos el paso a paso de la instalación para <b>Crear dominio nuevo en bosque nuevo</b>
3. Lo llamaremos midominio.com y seleccionamos siguiente
4. Seleccionaremos Windows server 2003 continuaremos con la el paso a paso de instalación.
5. Al reiniciar la maquina virtual podemos ver el dominio al inicio de la sesión.

#### Verificación del DNS

1. Ir a <b>Inicio > Herramientas Administrativas > Usuarios y equipos de Active Directory</b> para poder comprobar el dominio que hemos creado
2. Ahora vamos a nuestro dominio creado 'midominio.com' y accedemos a la carpeta <b>Users</b> donde crearemos un usuario.
3. Proveemos la información que nos solicita y aceptamos para crear el nuevo usuario. (contraseña ejemplo: 12345678\*a)

### Activación de usuarios

1. Generar otras maquinas virtuales con Windows, siempre y cuando no sea Windows Server.
2. Ir a <b>Explorador de Archivos</b> y dar click derecho sobre <b>equipo</b>, luego click en <b>Propiedades > Nombre de equipo</b>.
3. Cambiar el nombre del equipo por el nombre de usuario creado en Windows Server y establecer el dominio como el que hemos creado (midominio.com).
4. Una vez hecho esto, ingresar la contraseña solicitada para que se reinicie Windows y quede exitosamente conectado al directorio activo.
