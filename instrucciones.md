# Buscador Inteligente de Documentos - Guía de Instalación

Este documento describe los pasos para configurar y ejecutar el proyecto del chatbot buscador de documentos en un nuevo computador.

## Prerrequisitos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

1.  **Python:** (Versión 3.10 o superior recomendada). Para verificar si lo tienes, abre una terminal y escribe `python --version`. Si no está instalado, descárgalo desde [python.org](https://www.python.org/downloads/).
2.  **Git:** Para verificar, abre una terminal y escribe `git --version`. Si no está instalado, descárgalo desde [git-scm.com](https://git-scm.com/downloads/).

## Pasos de Instalación y Ejecución

Sigue estos pasos en orden desde una terminal o línea de comandos.

### 1. Clonar el Repositorio
Primero, descarga el código fuente desde GitHub. Reemplaza `tu-usuario` y `tu-repositorio` con los tuyos.

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
Use code with caution.
Markdown
2. Navegar a la Carpeta del Proyecto
Una vez clonado, entra en la carpeta del proyecto.
cd tu-repositorio
Use code with caution.
Bash
3. Crear y Activar un Entorno Virtual
Es una buena práctica aislar las dependencias del proyecto. Crearemos un entorno virtual llamado .venv.
# Crear el entorno
python -m venv .venv

# Activar el entorno (depende de tu sistema operativo)
# En Windows:
.venv\Scripts\activate
# En macOS o Linux:
source .venv/bin/activate
Use code with caution.
Bash
Sabrás que está activado porque tu prompt de la terminal comenzará con (.venv).
4. Instalar las Dependencias
Con el entorno activado, instala todas las librerías necesarias usando el archivo requirements.txt. Este paso puede tardar unos minutos.
pip install -r requirements.txt
Use code with caution.
Bash
5. Configurar las Claves de API
El proyecto necesita claves de API para funcionar. Estas se guardan en un archivo .env que no está en el repositorio por seguridad.
Crea un nuevo archivo llamado .env en la raíz del proyecto.
Abre el archivo .env y pega el siguiente contenido, reemplazando los valores de ejemplo con tus claves reales:
OPENROUTER_API_KEY="TU_CLAVE_DE_OPENROUTER_AQUI"
HF_TOKEN="TU_TOKEN_DE_HUGGINGFACE_AQUI"
Use code with caution.
6. Ejecutar el Chatbot en Visual Studio Code
¡Ya está todo listo para ejecutar el proyecto!
Abre la carpeta del proyecto en Visual Studio Code.
Abre el archivo del notebook (ej. document_search_chatbot.ipynb).
Selecciona el Kernel correcto: En la esquina superior derecha de la ventana del notebook, haz clic en "Select Kernel". Escoge el entorno de Python que corresponda a tu entorno virtual (.venv). Debería aparecer como 'Python 3.x.x ('.venv')'.
Ejecuta las celdas: Haz clic en "Run All" en la parte superior del notebook, o ejecuta cada celda en orden. La última celda lanzará la interfaz de Gradio.
7. Detener la Aplicación
Para detener el servidor de Gradio, busca la celda que se está ejecutando (tendrá un temporizador) y haz clic en el icono de "Stop" (■) que aparece a su izquierda.

