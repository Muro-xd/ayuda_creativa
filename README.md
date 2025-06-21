# 📘 Manual de Usuario – Ayuda Creativa (Astro + Tailwind)

Este proyecto es una documentación interactiva tipo **manual de usuario**, construida con [Astro](https://astro.build) y [Tailwind CSS](https://tailwindcss.com). Permite navegar entre distintas categorías y artículos de ayuda para facilitar el uso de un sistema de gestión.

## 🚀 Tecnologías utilizadas

- 🧑‍🚀 Astro  
- 🎨 Tailwind CSS  
- 📁 Rutas estáticas basadas en archivos (`/src/pages`)  
- 🧩 Componentes reutilizables (`Sidebar`, `Layout`, `ManualArticle`)  

## 📁 Estructura del proyecto
````
/
├── public/                      → Archivos públicos (favicon, imágenes, etc.)
├── src/
│   ├── components/              → Sidebar, Header, Footer, ManualArticle, etc.
│   ├── layouts/                 → Layout base con Header y Footer
│   └── pages/                   → Categorías y artículos (rutas)
│       ├── articulos/
│       │   ├── index.astro
│       │   └── como-anadir-varios-precios-a-un-articulo.astro
│       ├── ventas/
│       │   ├── index.astro
│       │   └── como-hacer-una-venta.astro
│       └── ...
├── tailwind.config.mjs
├── astro.config.mjs
└── package.json
````
## 🧑‍💻 Instalación local

1. Clona el repositorio:

   git clone https://github.com/tu-usuario/ayuda-creativa.git  
   cd ayuda-creativa

2. Instala dependencias:

   npm install

3. Ejecuta el proyecto:

   npm run dev

Abre tu navegador en [http://localhost:4321](http://localhost:4321)

## 🎨 Tailwind CSS

Este proyecto ya viene con **Tailwind CSS totalmente configurado** mediante `@astrojs/tailwind`.

Archivos clave:

- `tailwind.config.mjs`: configuración principal  
- `src/styles/global.css`: estilos globales (si aplica)  
- `@tailwindcss/typography`: mejora la apariencia del texto con clases `prose`  

✅ No necesitas instalar Tailwind por separado. Ya está listo para usar.

## 🧪 Comandos disponibles

| Comando            | Acción                                        |
|--------------------|-----------------------------------------------|
| `npm run dev`      | Inicia el servidor local                      |
| `npm run build`    | Genera los archivos de producción en `/dist`  |
| `npm run preview`  | Previsualiza el sitio generado                |
| `npm run astro`    | Ejecuta comandos del CLI de Astro             |

## 🌐 Navegación por categorías

Cada categoría del manual tiene su propia ruta:

- `/articulos`  
- `/ventas`  
- `/documentos-electronicos`  
- `/configuracion`  
- `/kardex`  
- `/clinicas`  

Cada artículo es accesible con rutas como:

/articulos/como-anadir-varios-precios-a-un-articulo  
/ventas/como-hacer-una-venta

## 📱 Diseño Responsive

- 🖥️ En escritorio: sidebar fijo con índice completo del manual.  
- 📱 En móviles: el sidebar se oculta para mejorar la lectura del artículo.  
  *(Opcional: implementar menú desplegable o modal para navegación)*

## 📝 Agregar un nuevo artículo

1. Agrega el título en el array correspondiente de `Sidebar.astro` y/o `index.astro` dentro de su categoría.  
2. Crea un archivo `.astro` dentro de `/src/pages/{categoria}/` con el nombre adecuado (slug).  
3. Usa el componente `<ManualArticle />` pasando `title` y `content`.

## ✅ Pendientes / Ideas de mejora

- [ ] Menú colapsable en mobile (☰ Índice)  
- [ ] Centralizar categorías/artículos en un archivo `.json` o `.ts`  
- [ ] Implementar buscador de artículos  
- [ ] Internacionalización (i18n)

## 🧑‍🚀 Autor

Proyecto desarrollado por [Tu Nombre o Empresa].  
Licencia: MIT
