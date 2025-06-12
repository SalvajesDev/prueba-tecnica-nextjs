# Prueba técnica NextJS

## 🎯 Objetivo

Crear una pequeña aplicación con el stack:
* Next.js (App Router)
* Prisma ORM con PostgreSQL
* ShadCN UI

El objetivo es crear un formulario para registrar clases y una vista que las muestre con filtros, usando rutas API personalizas y componentes UI.

## 📝Funcionalidades requeridas

1. Crear clases mediante un formulario

Debe de haber una vista en la ruta /create que contenga un formulario con los siguientes campos:

* title (string, requerido)
* description (string, opcional)
* date (fecha futura, requerida)
* category (select: "programación", "diseño", "marketing")


2. Usar API personalizada para guardar y consultar clases

La aplicación debe de tener rutas API tipo REST bajo /api/classes

🔷 POST /api/classes -> Crear una nueva clase

**Respuesta esperada**:
* 201 Created con objeto de clase creada
* 400 Bad Request si falta algún campo requerido o la fecha es inválida.


🔷 GET /api/classes -> Obtener listado de clases. Soporta filtros por query params

**Query params opcionales**:
* category: "programación" | "diseño" | "marketing"
* futureOnly: true (para mostrar solo clases en el futuro)

**Ejemplo:**

GET /api/classes?category=programacion&futureOnly=true

3. Mostrar clases creadas en una lista (ruta /)
* Ver todas las clases en distintas cards
* Filtrar por:
    * Categoría (select)
    * Fecha (solo clases futuras a la fecha actual)

4. Test unitario con JEST

Realiza el test que consideres más importante para las integraciones realizadas.

## 🧩Requisitos técnicos

* Usar App Router
* Base de datos con Prisma (postgreSQL)
* Formulario con ShadCN UI
* Filtrado desde el cliente (opcional: también desdee el servidor)
* El proyecto debe de compilar correctamente
* El test tiene que pasar

## 🧠 Bonus (opcional)

* Validación con zod
* Mensajes de éxito/error visuales
* Mostrar total de clases encontradas tras filtrar
* Búsqueda por texto (title contiene...)

## 🚀 Cómo entregar

* Ve subiendo los cambios como consideres oportunos al repositorio de Git


