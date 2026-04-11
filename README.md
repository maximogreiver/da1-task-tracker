# WorldCupPlanner Tracker

Tracker interactivo para el Obligatorio 1 de Diseño de Aplicaciones 1 — ORT Uruguay.

Permite a los 3 integrantes del equipo llevar el seguimiento de las tareas del obligatorio en tiempo real, con sincronización instantánea via Firebase.

## Features

- 👥 **Asignación por integrante** con un click
- 🔄 **Sincronización en tiempo real** entre los 3 integrantes via Firebase
- 📊 **Barra de progreso** global y por persona
- 🔍 **Filtros** por categoría, persona, estado y búsqueda de texto
- 📌 **Vista Lista** y **Vista Board** (Kanban)
- ➕ **Agregar tareas** personalizadas
- 🌐 **100% offline** (un solo archivo HTML, sin instalar nada)

## Setup (5 minutos)

Cada equipo necesita su propio proyecto de Firebase (gratis). **No compartan las credenciales entre equipos.**

### 1. Crear proyecto en Firebase

1. Ir a [console.firebase.google.com](https://console.firebase.google.com)
2. "Agregar proyecto" → nombre cualquiera (ej: `da1-tracker-equipo42`)
3. Desactivar Google Analytics → Crear

### 2. Crear la Realtime Database

1. Panel lateral → **Compilación → Realtime Database**
2. "Crear base de datos" → elegir ubicación → "Siguiente"
3. Elegir cualquier modo → "Habilitar"
4. Ir a la pestaña **Reglas** y reemplazar todo por:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

5. Click en **Publicar**

### 3. Registrar una app web

1. Ir a **Configuración del proyecto** (engranaje ⚙️) → "General"
2. Scroll abajo → "Agregar app" → ícono Web (`</>`)
3. Nombre cualquiera → **NO** tildar Firebase Hosting → "Registrar app"
4. Copiar los valores de `firebaseConfig` (los van a necesitar)

### 4. Abrir el tracker

1. Descargar `WorldCupPlanner_Tracker_Template.html`
2. Abrir haciendo doble click (se abre en el navegador)
3. Completar los datos de Firebase y los nombres del equipo
4. Click en "Iniciar Tracker"

### 5. Compartir con el equipo

Mandar el mismo archivo HTML a los otros 2 integrantes. Cada uno lo abre, pone los mismos datos de Firebase, y listo: los 3 ven las mismas tareas sincronizadas en tiempo real.

> La config se guarda en el navegador, así que solo hay que ponerla una vez.

## FAQ

**¿Se paga algo?**
No. Firebase Spark (gratis) da 1GB de storage y 10GB de transferencia/mes. Para 3 personas con un tracker es más que suficiente.

**¿Expira?**
No, con las reglas abiertas no tiene vencimiento. El plan Spark no tiene límite de tiempo.

**¿Puedo resetear la config?**
Abrí la consola del navegador (F12) y escribí `resetConfig()`.

**¿Puedo cambiar los nombres de los integrantes?**
Sí, con `resetConfig()` volvés a la pantalla de setup.

## Créditos

Hecho por Máximo Greiver, estudiante de Ingenieria en Sistemas para estudiantes de ORT
