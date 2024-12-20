# CryptCleaner

CryptCleaner es un proyecto de ransomware simulado desarrollado en Python. El objetivo del proyecto es encriptar los archivos dentro de un directorio utilizando la biblioteca `cryptography`, mientras que al usuario se le presenta un señuelo que simula ser una herramienta de limpieza de archivos innecesarios.

## Tabla de Contenidos
- [Descripción](#descripción)
- [Instalación](#instalación)
- [Uso](#uso)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Dependencias](#dependencias)
- [Funcionalidades](#funcionalidades)
- [Advertencias](#advertencias)
- [Contribución](#contribución)
- [Licencia](#licencia)

## Descripción

CryptCleaner actúa como una aplicación maliciosa que encripta archivos en segundo plano mientras engaña al usuario al presentarse como un software de optimización del sistema. 

El ransomware encripta todos los archivos dentro de un directorio seleccionado por el usuario y genera un archivo de texto al final del proceso informando que los archivos han sido encriptados.

> **Nota importante**: Este proyecto es solo con fines educativos. No debe ser utilizado para actividades maliciosas.

## Instalación

Sigue los siguientes pasos para configurar y ejecutar el proyecto en tu entorno local.

### Prerrequisitos

- **Python 3.8 o superior** instalado en tu máquina.
- **PyCharm** (u otro IDE de tu preferencia).

### Clonar el Repositorio

```bash
git clone https://github.com/tu_usuario/cryptcleaner.git
cd cryptcleaner
```
### Crear un Entorno Virtual
```bash
python -m venv venv
```

### Activar el Entorno Virtual
- En Windows:
```bash
venv\Scripts\activate
```
- En macOS/Linux:
```bash
source venv/bin/activate
```
### Instalar Dependencias
Dentro del entorno virtual, instala las dependencias necesarias:

```bash
pip install -r requirements.txt
```
### Uso
1. Coloca los archivos que deseas encriptar en la carpeta data/ o especifica otro directorio.
2. Ejecuta el proyecto desde el archivo main.py:
```bash
python src/main.py
```
3. La aplicación presentará una interfaz de consola simulando la limpieza de archivos innecesarios, mientras en segundo plano los archivos en el directorio serán encriptados.

4. Al finalizar el proceso, verás un mensaje informándote que los archivos han sido encriptados.

### Desencriptar archivos
Para desencriptar los archivos, necesitarías la clave privada generada durante el proceso de encriptación (no implementada en este proyecto por ser un ransomware simulado).

## Estructura del Proyecto
```bash
CryptCleaner/         # Carpeta raíz del proyecto
│
├── venv/             # Entorno virtual (creado automáticamente)
│
├── src/              # Carpeta principal del código fuente
│   ├── __init__.py   # Archivo para inicialización del módulo
│   ├── main.py       # Archivo principal que ejecuta el proyecto
│   ├── encryptor.py  # Contiene las funciones para cifrado
│   ├── decoy.py      # Simula la app de señuelo
│   ├── utils.py      # Utilidades generales como manejo de archivos
│
├── data/             # Carpeta para los archivos a encriptar
│   └── ...           # Archivos de ejemplo
│
├── requirements.txt  # Archivo de dependencias
│
└── README.md         # Documentación del proyecto
```
## Dependencias
- cryptography: Biblioteca utilizada para el cifrado de archivos.
- tras dependencias pueden agregarse en el futuro para funcionalidades adicionales.
### Instalación de Dependencias
Puedes instalar las dependencias ejecutando:

```bash
pip install -r requirements.txt
```
## Funcionalidades
- Cifrado de directorios: Utiliza AES para encriptar archivos dentro de un directorio.
- Señuelo de limpieza de archivos: Presenta una interfaz de consola que simula la optimización de archivos basura mientras se ejecuta el cifrado en segundo plano.
- Generación de nota de rescate: Informa al usuario que sus archivos han sido encriptados.

## Advertencias
Este proyecto está diseñado con fines educativos únicamente. No debe ser utilizado para propósitos maliciosos ni para crear software malicioso. El uso indebido de este proyecto puede llevar a consecuencias legales.

## Contribución
Si deseas contribuir al proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama nueva (git checkout -b feature/nueva-funcionalidad).
3. Realiza tus cambios y haz un commit (git commit -m 'Agrega nueva funcionalidad').
4. Haz un push a tu rama (git push origin feature/nueva-funcionalidad).
5. Abre un Pull Request.

## Licencia
Este proyecto está bajo la licencia MIT - mira el archivo **LICENSE** para más detalles.