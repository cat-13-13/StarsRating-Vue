## StarsRating-Vue

Componente de calificación con estrellas utilizando Vue.js.
Consta de lo siguiente:

1. Cinco estrellas vacías inicialmente.
2. Al pasar el cursor sobre una estrella, se resalta esa estrella y todas las estrellas anteriores.
3. Al hacer clic en una estrella, se mantienen fijas las estrellas resaltadas hasta ese punto y se guarda el número de estrellas seleccionadas.
4. Al hacer clic en la última estrella fija, se restablece el estado y se vuelven a mostrar las estrellas vacías.
5. Al hacer clic en una estrella fija que no sea la última, se actualiza la valoración y esa pasa a ser la última estrella fija.

## Requisitos Previos

Asegúrate de tener instalado lo siguiente antes de comenzar:

- Node.js (v18.16.0)
- Vue CLI (@vue/cli 5.0.8)

## Configuración del Proyecto

Sigue los siguientes pasos para configurar el proyecto en tu entorno local:

1. Clona este repositorio: `git clone https://github.com/cat-13-13/StarsRating-Vue.git`
2. Navega hasta el directorio del proyecto: `cd StarsRating-Vue`
3. Instala las dependencias: `npm install`

## Uso

Para iniciar el proyecto ejecuta el comando `npm run serve`

## Directorios

- `src/`: Directorio raíz del código fuente

  - `assets/`: Recursos estáticos como imágenes y fuentes
  - `components/`: Componentes reutilizables
  - `App.vue`: Componente principal de la aplicación
  - `main.js`: Punto de entrada de la aplicación

- `public/`: Directorio de archivos estáticos públicos

  - `favicon.ico`: Archivo de ícono de la página
  - `index.html`: Archivo HTML principal

- `.gitignore`: Archivo de configuración de Git para ignorar archivos/directorios
