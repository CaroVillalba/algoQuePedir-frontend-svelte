# Algoritmos III - Trabajo Práctico 2025 - Frontend (Svelte)

## Descripción del proyecto

Este proyecto es el frontend del TP **"Algo Que Pedir"** de la materia Algoritmos III (2025) pensado para el **punto de vista del local**, desarrollado en **SvelteKit**. Consume la API REST del backend desarrollado en Spring Boot con Kotlin, el mismo que utiliza la app mobile en React donde los usuarios realizan sus pedidos.

Comenzó como un **maquetado estático** con HTML y CSS, enfocado en aplicar buenas prácticas de diseño web, estructura semántica y estilos responsivos. Luego fue **migrado a Svelte** para incorporar componentes reutilizables, mejorar la performance y convertirlo en una aplicación dinámica conectada al backend.

La aplicación se centra en los casos de uso de quien administra el restaurante:

* Registro e inicio de sesión
* Gestión de la información del local
* Gestión de ingredientes
* Gestión de platos
* Seguimiento de los pedidos realizados por los usuarios desde la app en React

## Objetivos del proyecto

* Practicar maquetado web con HTML semántico y CSS
* Implementar un diseño responsive con enfoque Mobile First
* Migrar la UI hacia componentes Svelte
* Conectar la interfaz con servicios backend reales
* Mejorar la estructura del código, la modularidad y la escalabilidad

## Tecnologías utilizadas

**Maquetado**

* HTML5
* CSS3
* Flexbox / CSS Grid

**Framework**

* Svelte
* SvelteKit (routing y estructura de la aplicación)
* TypeScript
* Vite (bundler)
* Node.js (entorno)

Backend: Spring Boot + Kotlin (API REST). Repositorio: `<https://github.com/CaroVillalba/algoQuePedir-backend>`

## Estructura del proyecto

* `src/lib` → Componentes y utilidades reutilizables
* `src/routes` → Rutas y pantallas de la aplicación (SvelteKit)
  * `auth` → Pantallas de autenticación
  * `main` → Pantallas principales de gestión del local
  * `+layout.svelte` → Layout general de la aplicación
  * `+page.svelte` → Página de inicio
  * `+error.svelte` → Página de manejo de errores
* `src/stores` → Stores para el estado compartido
* `src/types` → Modelos y tipos de las respuestas de la API
* `src/mocks` → Datos simulados para desarrollo y pruebas
* `src/app.html` → Plantilla HTML base
* `src/app.css` → Estilos globales
* `src/app.d.ts` → Declaraciones de tipos globales

## Requisitos

* Node.js 20 o superior
* npm
* Backend del TP corriendo localmente (ver su README)

## Endpoints consumidos

**Autenticación**

* `POST /v1/auth/register` → Crear un usuario
* `GET /v1/auth/login` → Loguear usuario

**Local**

* `GET /v1/local/{id}` → Obtener info del local
* `PUT /v1/local/{id}` → Actualizar info del local

**Ingredientes**

* `GET /v1/ingredients` → Listar todos los ingredientes
* `GET /v1/ingredients/{id}` → Obtener un ingrediente
* `POST /v1/ingredients` → Crear ingrediente
* `PUT /v1/ingredients/{id}` → Actualizar ingrediente
* `DELETE /v1/ingredients/{id}` → Borrar ingrediente

**Platos**

* `GET /v1/dishes` → Listar todos los platos
* `GET /v1/dishes/{id}` → Obtener un plato
* `POST /v1/dishes` → Crear plato
* `PUT /v1/dishes/{id}` → Actualizar plato
* `DELETE /v1/dishes/{id}` → Borrar plato

**Pedidos (Orders)**

* `GET /v1/order` → Listar pedidos por estado o todos
* `GET /v1/order/orderDetail/{orderId}` → Obtener detalle de un pedido

## Diseño y responsividad

El maquetado fue diseñado priorizando:

* Estructura clara y semántica
* Layout adaptable con **Flexbox** y **CSS Grid**
* Enfoque **Mobile First**
* Variables CSS para escalabilidad
* Componentes reutilizables al migrar a **Svelte**

## Capturas

<p align="center">
  <img width="700" alt="Vista general de la aplicación" src="https://github.com/user-attachments/assets/795839f4-ff97-46e5-8883-1afb6a664522" />
</p>

## Cómo correr el proyecto

1. Clonar el repositorio
2. Instalar dependencias:

```
npm install
```

3. Levantar el backend (ver README del backend)
4. Ejecutar en modo desarrollo:

```
npm run dev
```

5. Para generar el build de producción:

```
npm run build
```


## Aprendizajes

Este proyecto permitió:

* Aplicar buenas prácticas de maquetado HTML/CSS
* Migrar una UI estática hacia un framework moderno
* Trabajar con componentes, props y reactividad en Svelte
* Usar SvelteKit para el routing y la organización de la aplicación
* Conectar un frontend con servicios backend reales
* Comprender el flujo completo desde prototipo hasta desarrollo

## Equipo de trabajo

* Lucía Arrieta
* Valentino Salguero
* Elias Serantes
* Carolina Villalba
* Ulises Zagare
