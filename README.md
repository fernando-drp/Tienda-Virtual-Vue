Tienda Virtual Vue

Aplicación de comercio electrónico desarrollada con Vue 3, que permite visualizar productos, gestionar un carrito de compras y administrar productos, cupones y ventas mediante Firebase.

Tecnologías utilizadas

Vue 3— construcción de interfaces con componentes.
Vite — entorno de desarrollo y compilación.
Pinia — gestión del estado de la aplicación.
Vue Router — navegación entre vistas.
Firebase / Firestore — almacenamiento y gestión de datos.
Tailwind CSS — diseño y estilos de la interfaz.
FormKit — construcción y validación de formularios.
JavaScript — lógica de la aplicación.

Funcionalidades

- Visualización del catálogo de productos.
- Carrito de compras.
- Gestión del estado del carrito.
- Administración de productos.
- Gestión de cupones de descuento.
- Registro y consulta de ventas.
- Integración con Firebase y Firestore.
- Navegación mediante Vue Router.

Instalación y ejecución

1. Clonar el repositorio
   git clone https://github.com/fernando-drp/Tienda-Virtual-Vue.git

2. Entrar en la carpeta
   cd Tienda-Virtual-Vue

3. Instalar dependencias
   npm install

4. Configurar las variables de entorno

Crea un archivo `.env.local` en la raíz del proyecto y configura las variables que utiliza la aplicación:

.env

VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=

Completa los valores con la configuración de tu proyecto Firebase.

5. Iniciar el servidor de desarrollo

npm run dev
Compilar para producción
npm run build

👨‍💻 Autor

Desarrollado por el Ing.Fernando De La Rosa Palma como proyecto de aprendizaje y práctica de desarrollo web con Vue 3 y Firebase.
