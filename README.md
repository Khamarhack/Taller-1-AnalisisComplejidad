 instrucciones y petición de información para el análisis del código

Voy a preparar el informe en PDF que pide: explicar, sin copiar código, el propósito y comportamiento de cada archivo, y responder a las preguntas:

    Cada archivo *.h y *.hxx: ¿qué declara o define?
    Cada archivo *.cxx : ¿qué implementa o ejecuta?
    ¿Qué ejecutables se generan al compilar?
    ¿Qué recibe cada ejecutable por línea de comandos?
    ¿Qué imprime cada ejecutable? Indica la cantidad de columnas y el significado de cada una.

Para poder hacerlo necesito que me facilites lo siguiente (mínimo necesario):

    Repositorio o archivos
        Opción A: URL del repositorio en GitHub (owner/repo) y rama a inspeccionar.
        Opción B: subir/adjuntar el árbol de código fuente (o un .zip) si no está en GitHub.
        Si el repositorio es privado, dame acceso o sube los archivos relevantes.

    Instrucciones de compilación
        Archivo de build (Makefile, CMakeLists.txt, meson, etc.) o los comandos exactos para compilar.
        Indica plataforma/OS para compilar (Linux, macOS, Windows WSL).
        Si hay dependencias externas, dime cómo instalarlas o proporciona instrucciones.

    Objetivos / ejecutables esperados
        Si conoces los nombres de los ejecutables generados, indícalos.
        Si no los conoces, dímelo y buscaré los targets en el build system.

    Ejecuciones de ejemplo
        Para cada ejecutable, dame uno o dos comandos de ejemplo (línea de comandos) y, si es posible, archivos de entrada de muestra o tamaños de muestra.
        Si los programas leen de stdin o de archivos, indícalo.

    Salida esperada
        Si ya sabes cómo luce la salida (por ejemplo, tablas con N columnas, CSV, texto con columnas separadas por espacios), adjunta un ejemplo o describe el formato.
        Si hay opciones CLI para cambiar formato (por ejemplo, --csv, --verbose), indícalas.

    Prioridad o alcance
        ¿Quieres que analice todo el repositorio o sólo una carpeta (por ejemplo, src/, app/, tools/)?
        ¿Debo ejecutar los binarios para observar la salida o solo inspeccionar el código?

    Restricción importante (confirmación)
        Confirmas la regla: "No copies código en el PDF". Yo no incluiré fragmentos de código. En el informe describiré la finalidad de cada archivo, las funciones/clases que expone (conceptualmente), y el comportamiento de los ejecutables con ejemplos de entrada/salida en formato descriptivo (sin mostrar el código fuente).

