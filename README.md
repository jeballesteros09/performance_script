# SCRIPT DE INFORMACIÓN DE RENDIMIENTO

El propósito del siguiente script es obtener y mostrar información del sistema, tales como el rendimiento de la CPU, memoria, discos, y red. El script es de código abierto y se distribuye bajo la Licencia Pública General de GNU (GNU GPL). El script está incompleto, específicamente falta la última función para mostrar toda la información del sistema en pantalla (me dio pereza continuar escribiendo código).

## Descripción

El script ofrece un menú interactivo con varias opciones que permiten al usuario visualizar información detallada del sistema:

1. **Información de CPUs**: Muestra los detalles de la CPU utilizando el comando `lscpu`.
2. **Información de memoria**: Muestra el uso de la memoria con el comando `free -mh`.
3. **Información de discos**: Muestra información sobre los discos y dispositivos USB conectados usando `df -h` y `lsusb`.
4. **Información de red**: Muestra la configuración y detalles de la red con el comando `ip a`.
5. **Toda la información de diagnóstico**: Esta función está en desarrollo y permitirá presentar un diagnóstico completo del sistema.
6. **Salir**: Cierra el script.

## Cómo usar

Para ejecutar el script, primero asegúrate de darle permisos de ejecución:

```bash
chmod +x script.sh
```

Luego, ejecútalo con:

```bash
./script.sh
```

Al ejecutar el script, se mostrará un menú principal con las opciones disponibles. Selecciona una opción para ver la información deseada. Después de elegir una opción, tendrás subopciones que te permiten:

- Presentar la información en pantalla.
- Capturar la información en un archivo de texto.
- Mostrar la información en pantalla y guardarla en un archivo.
- Volver al menú principal.

## Requisitos

- Sistema operativo basado en Linux.
- Permisos de ejecución de scripts de bash.

## Notas

- La opción 5 (Toda la información de diagnóstico) está pendiente de implementación.
- La información capturada se guarda con un nombre que incluye el tipo de información, el nombre del host y la fecha y hora actuales.

## Licencia

Este proyecto se distribuye bajo la Licencia Pública General de GNU (GNU GPL). Puedes redistribuirlo y/o modificarlo bajo los términos de la GPL. Para más información, consulta [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html).

## Autor

Creado por J.
