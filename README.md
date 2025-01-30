# Búsqueda de Universidades

Este proyecto es una aplicación web desarrollada utilizando HTML, CSS y Perl, y se encuentra completamente montada en Docker. Permite realizar búsquedas de universidades según varios criterios como el nombre de la universidad, periodo de licenciamiento, departamento, localidad y carrera, todo basado en un archivo CSV que contiene la información de las universidades.

## Características

- **Interfaz web**: La aplicación tiene una interfaz gráfica sencilla desarrollada con HTML y CSS.
- **Búsqueda avanzada**: Los usuarios pueden buscar universidades filtrando por:
  - Nombre de la universidad
  - Periodo de licenciamiento
  - Departamento
  - Localidad
  - Carrera
- **Backend en Perl**: El servidor backend está desarrollado en Perl, utilizando CGI para manejar las peticiones.
- **Datos en CSV**: La información de las universidades está almacenada en un archivo CSV que es procesado por el script Perl para realizar las búsquedas.
- **Dockerizado**: El proyecto está montado en un contenedor Docker para facilitar su despliegue y ejecución en diferentes entornos.

## Instalación

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/RominaCamargo/B-squeda-de-Universidades.git
   cd B-squeda-de-Universidades
   ```

2. **Construir la imagen de Docker**:

   Asegúrate de tener Docker instalado. Luego, construye la imagen con el siguiente comando:

   ```bash
   docker build -t busqueda-universidades .
   ```

3. **Ejecutar el contenedor Docker**:

   Una vez que la imagen se haya creado, ejecuta el contenedor:

   ```bash
   docker run -p 80:80 busqueda-universidades
   ```

   Esto hará que la aplicación esté disponible en tu navegador en `http://localhost`.

## Uso

1. Accede a la página en tu navegador.
2. Utiliza el formulario de búsqueda para filtrar universidades por el nombre, periodo de licenciamiento, departamento, localidad o carrera.
3. Los resultados se mostrarán en la misma página.

## Estructura de Archivos

- **Dockerfile**: Contiene las instrucciones para construir la imagen de Docker.
- **cgi-bin/consult.pl**: Script Perl que maneja las peticiones y realiza las búsquedas sobre el archivo CSV.
- **css/styles.css**: Archivo de estilos CSS para la presentación de la página web.
- **index.html**: Página principal que contiene el formulario de búsqueda.
- **csv/universidades.csv**: Archivo CSV con los datos de las universidades.

## Tecnologías Utilizadas

- **HTML**: Estructura de la página web.
- **CSS**: Estilos visuales de la página.
- **Perl (CGI)**: Backend para manejar las solicitudes y procesar el archivo CSV.
- **Docker**: Contenedor para facilitar la instalación y ejecución del proyecto.
