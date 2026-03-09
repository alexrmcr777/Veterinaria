# ProyVet

Este es un proyecto de gestión veterinaria desarrollado con **Angular 21**, que permite administrar mascotas y citas médicas. Incluye renderizado del lado del servidor (SSR) mediante Express y usa Bootstrap 5 para la interfaz visual.

---

## Estructura del proyecto

```
Veterinaria-main/
├── src/
│   ├── app/
│   │   ├── features/                   # Módulos funcionales de la aplicación
│   │   │   ├── home/                   # Pantalla de inicio / Dashboard
│   │   │   │   ├── components/
│   │   │   │   │   ├── home-card/      # Tarjetas de resumen (estadísticas)
│   │   │   │   │   └── table/          # Tabla de citas del día
│   │   │   │   └── pages/
│   │   │   │       └── home/           # Página principal del dashboard
│   │   │   ├── mascotas/               # Gestión de mascotas
│   │   │   │   └── pages/
│   │   │   │       ├── mascotas-component/  # Listado de mascotas
│   │   │   │       ├── crear-mascota/       # Formulario de registro
│   │   │   │       ├── editar-mascota/      # Formulario de edición
│   │   │   │       └── ver-historial/       # Historial de la mascota
│   │   │   └── citas/                  # Gestión de citas médicas
│   │   │       └── pages/
│   │   │           ├── citas-component/     # Listado de citas
│   │   │           ├── crear-cita/          # Formulario de nueva cita
│   │   │           └── editar-cita/         # Formulario de edición de cita
│   │   ├── models/                     # Interfaces de datos (TypeScript)
│   │   │   ├── mascotas.model.ts       # Interfaz Mascota
│   │   │   └── citas.model.ts          # Interfaz Cita
│   │   ├── services/                   # Lógica de negocio y datos en memoria
│   │   │   ├── mascotas.ts             # CRUD de mascotas con RxJS
│   │   │   ├── citas.ts                # CRUD de citas con RxJS
│   │   │   └── dashboard.ts            # Servicio de estadísticas del dashboard
│   │   ├── shared/                     # Elementos reutilizables
│   │   │   ├── components/
│   │   │   │   ├── header/             # Encabezado de la aplicación
│   │   │   │   ├── nav-bar/            # Barra de navegación lateral
│   │   │   │   └── footer/             # Pie de página
│   │   │   └── layout/                 # Componente de estructura principal (shell)
│   │   ├── app.routes.ts               # Definición de rutas de la aplicación
│   │   ├── app.config.ts               # Configuración del lado del cliente
│   │   └── app.config.server.ts        # Configuración del lado del servidor (SSR)
│   ├── main.ts                         # Punto de entrada del cliente
│   ├── main.server.ts                  # Punto de entrada del servidor (SSR)
│   └── server.ts                       # Servidor Express para SSR
├── public/                             # Recursos estáticos públicos
├── angular.json                        # Configuración del workspace de Angular CLI
├── package.json                        # Dependencias y scripts del proyecto
└── tsconfig.json                       # Configuración de TypeScript
```

### Resumen de las secciones principales

| Sección | Descripción |
|---|---|
| `features/home` | Dashboard con estadísticas: total de pacientes, citas del día y citas pendientes |
| `features/mascotas` | Permite registrar, editar, eliminar y ver el historial de mascotas |
| `features/citas` | Permite programar, editar y eliminar citas con estados: *Programada*, *Atendida*, *Cancelada*, *No asistió* |
| `models` | Interfaces TypeScript que definen la forma de los datos (`Mascota` y `Cita`) |
| `services` | Servicios con datos en memoria (sin backend real) que simulan un API usando RxJS Observables |
| `shared` | Componentes de layout (header, navbar, footer) compartidos por todas las páginas |

---

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 21.1.4.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
