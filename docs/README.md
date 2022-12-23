## Introducción
Software de simulación de Radar OTH (Sobre-horizonte). 
PIDDEF 03-2020.

En este repositorio se encuentran:

   - Core del Simulador de Radar
   - Backend del Simulador de Radar

## Pre-requisitos
Para seguir este documento es necesario tener instalados los siguientes programas:

   - [**Python 3.10**](https://www.python.org/downloads/release/python-3107/)
   
      Para chequear, ejecutar desde una terminal:
      ```
      python --version
      ```
      La respuesta debería ser similar a `Python 3.10.*`
   
   - [**Git**](https://git-scm.com/downloads)

      Para chequear, ejecutar desde una terminal:
      ```
      git --version
      ```
      La respuesta debería ser similar a `git version 2.38.*`

   - [**VS Code**](https://code.visualstudio.com/) o algún IDE para usar los Jupyter Notebooks

## Dependencias
Este repositorio depende de otro: [dependencias_estaticas](https://bitbucket.org/radaresfacet/dependencias_estaticas).

En la sección de [Instalacion](#instalacion) se explica cómo instalarlo.

## Aplicación principal
La aplicación principal se encuentra en: [frontend](https://bitbucket.org/radaresfacet/frontend).

Antes de instalarla, seguir la sección de [Instalacion](#instalacion) de este documento.


## Instalación

Los siguientes pasos sirven para:

   - Instalar el Core del Simulador.
   - Instalar el servidor de Backend.


Al finalizar esta sección, la estructura de carpetas debería quedar así:   
   ```
   |--app-simulador-radar
   | |--simulador_core
   |    |--más contenido
   | |--dependencias_estaticas
   |    |--más contenido
   ```

1. Abrir una terminal en la carpeta que contendrá a `app-simulador-radar`.

2. Con la terminal en la carpeta deseada, ejecutar:
   ```
   mkdir app-simulador-radar && cd app-simulador-radar
   git clone git@bitbucket.org:radaresfacet/simulador_core.git@dev
   git clone git@bitbucket.org:radaresfacet/dependencias_estaticas.git
   ```

3. Usando Python 3.10.*, crear un nuevo ambiente. Se muestran las instrucciones para crear uno usando la herramienta venv. Para Windows:
   ```   
   cd simulador_core
   python -m venv .venv
   .venv\Scripts\activate
   python -m pip install -U pip
   ``` 

4. Instalar requerimientos (desde el ambiente):
   ```
   pip install -r requirements.txt
   ```

## Uso

### Pre-requisitos

1. La terminal debe estar en la carpeta `simulador_core`
2. El ambiente debe estar activado:
   ```
   .venv\Scripts\activate
   ```

3. El servicio de backend debe estar iniciado:   
   ```
   python src/simulador_core/backend_api.py
   ```

### Formas de uso

- Documentación: <http://localhost:5000/documentacion>
- Correr simulación interactiva desde el Backend: <http://localhost:5000/docs> 
- Correr simulación interactiva desde el Jupyter Notebook: [Archivo de Jupyter Notebook](src/simulador_core/guia_de_uso_core.ipynb) (funciona sólo desde un IDE como Visual Studio Code)
- Correr simulación de ejemplo llamando al Core:   
   ```   
   python src\simulador_core\main.py
   ```

- Instalar y usar la aplicación principal: [repo de frontend](https://bitbucket.org/radaresfacet/frontend)

