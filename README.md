# PCEM-486-SB16-TGUI9400

## Introduccion
Este repositorio contiene una maquina virtual para PCem v17.
El fichero 486-SB16-TGUI9400.zip contiene la maquina virtual
La carpeta Software contiene imagenes de todo el software instalado en la maquina virtual

## Instalacion
Para instalar la maquina virtual hay que seguir los siguientes pasos
 1. Descomprimir el fichero 486-SB16-TGUI9400.zip, en el que se encuentran tres ficheros:
    - 486-SB16-TGUI9400.cfg
    - 486-SB16-TGUI9400.win486.nvr
    - 486-SB16-TGUI9400.img
 2. Copiar 486-SB16-TGUI9400.cfg en la carpeta configs que se encuentra en la carpeta de instalacion de PCem
 3. Copiar 486-SB16-TGUI9400.win486.nvr dentro de la carpeta nvr que se encuentra en la carpeta de instalacißin de PCem
 4. Guardar 486-SB16-TGUI9400.img
 5. Ejecutar PCem: Ahora la nueva maquina virtual 486-SB16-TGUI9400 estará disponible. Abrir su configuración y seleccionar 486-SB16-TGUI9400.img como la imagen del disco duro. El disco duro debe configurarse como un disco duro tipo 46. Es necesario asegurarse de que la configuración del disco es la correcta. Si es necesario, ajustar los datos deldisco de forma que:
    - El numero de sectores debe ser 17
    - El numero de caras debe ser 15
    - El numero de cilindros debe ser 1224
    - El tamaño calculado por la aplicacion debe ser 152Mb
 6. Ahora la maquina virtual deberia estar lista para ser ejecutada

## Hardware

Equipo basado en 486
 - Bios: AMI WinBios 486
 - CPU: Intel i486 DX2 66Mhz 16 Mb RAM
 - Tarjeta grafica: Trident TGUI9400CXi 2Mb
 - Tarjeta de sonido: Sound Blaster 16
 - Disco duro: HDD tipo 46 (160 Mb)
 - Disquetera 3,5 pulgadas, 1,44Mb
 - CDROM 24x

## Software instalado
 - MS-DOS 6.22
 - Sound Blaster 16/AWE for DOS/Windows 3.1 (c:\sb16)
 - MICROSOFT MOUSE, Software version 9.01 (c:\mouse)
 - SciTech Display Doctor 5.3a (c:\ss53a)
 - OAK CDROM driver
 - Host DPMI (c:\cswdpmi)

## autoexec.bat
@ECHO OFF  
SET SOUND=C:\SB16  
SET BLASTER=A220 I5 D1 H5 P330 T6  
SET MIDI=SYNTH:1 MAP:E  
C:\SB16\DIAGNOSE /S  
C:\SB16\MIXERSET /P /Q  
C:\DOS\SMARTDRV.EXE /X  
PROMPT $p$g  
set mouse=C:\MOUSE  
C:\MOUSE\mouse.exe /Q  
PATH C:\DOS  
SET TEMP=C:\DOS  
LOADHIGH=C:\DOS\MSCDEX.EXE /D:MSCD001  
C:\SDD53A\UNIVBE  

## config.sys
DEVICE=C:\DOS\SETVER.EXE  
DEVICE=C:\DOS\HIMEM.SYS  
DOS=HIGH  
DEVICEHIGH=C:\DOS\OAKCDROM.SYS /D:MSCD001  
FILES=40  
