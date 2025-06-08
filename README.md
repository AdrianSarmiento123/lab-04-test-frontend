# Mi proyecto: Historia de Usuario 1:  Crear publicación
# Happy Path
Cliente abre la página de crear publicación.

Escribe texto válido en la caja de texto.

Hace clic en el botón "Enviar".

La publicación se envía correctamente.

El campo de texto se limpia.

Se muestra confirmación o la nueva publicación aparece listada.

# Unhappy Paths

El Cliente hace clic en "Enviar" sin escribir nada → debe mostrar mensaje de error y no enviar.

El Cliente escribe solo espacios " " → debe mostrar mensaje de error y no enviar.

El Cliente escribe un texto muy largo que supera el límite permitido → debe mostrar mensaje de error o truncar el texto.

Error de red al intentar enviar la publicación → debe mostrar mensaje de error.

# Historia de Usuario 2: Cliente envía mensaje a Freelancer

# Happy Path
Cliente abre la pestaña de mensajes de su dashboard.

Escribe mensaje válido en la caja de texto.

Hace clic en "Enviar mensaje".

El mensaje se envía correctamente.

El input de mensaje se limpia.

El mensaje aparece en la conversación.

# Unhappy Paths
Cliente intenta enviar mensaje vacío → se muestra error.

Cliente envía solo espacios → se muestra error.

Cliente intenta enviar mensaje muy largo → error o truncamiento.

Cliente hace clic en "Enviar" y hay error de red → se muestra error.

# Historia de Usuario 3: Freelancer responde a Cliente

# Happy Path
Freelancer abre su dashboard de publicaciones aceptadas.

Selecciona una publicación con un mensaje recibido.

Escribe respuesta en la caja de texto.

Hace clic en "Enviar".

La respuesta se envía correctamente y se muestra.

# Unhappy Paths
Freelancer intenta responder sin texto → error.

Freelancer envía espacios → error.

Freelancer envía texto largo → error o truncamiento.

Error de red al responder → se muestra error.




















# Laboratorio 04: Pruebas Unitarias con Jest en React

Este laboratorio tiene como objetivo proporcionar una introducción práctica a las pruebas unitarias en aplicaciones React utilizando Jest y React Testing Library.

## Aplicación Todo List

La aplicación desarrollada es una lista de tareas (Todo List) con las siguientes funcionalidades:

- Añadir nuevas tareas
- Marcar tareas como completadas
- Eliminar tareas
- Filtrar tareas por estado (todas, activas, completadas)
- Ver estadísticas de tareas
- Borrar todas las tareas completadas

## Estructura del Proyecto

```
app/
├── components/
│   ├── Todo.tsx               # Componente principal que integra todos los demás
│   ├── TodoForm.tsx           # Formulario para añadir nuevas tareas
│   ├── TodoItem.tsx           # Componente individual para cada tarea
│   ├── TodoList.tsx           # Lista de tareas
│   ├── TodoFilter.tsx         # Filtros para las tareas
│   ├── TodoStats.tsx          # Estadísticas de tareas
│   └── __tests__/             # Directorio de pruebas
│       ├── TodoItem.test.tsx  # Pruebas para TodoItem
│       ├── TodoForm.test.tsx  # Pruebas para TodoForm
│       └── TodoList.test.tsx  # Pruebas para TodoList
├── page.tsx                   # Página principal
└── layout.tsx                 # Layout de la aplicación
```

## Instrucciones del Laboratorio

En este laboratorio, exploraremos cómo escribir pruebas unitarias efectivas siguiendo el patrón **Prepare, Execute and Validate**:

1. **Prepare**: Configurar el entorno de prueba y los datos necesarios
2. **Execute**: Realizar la acción que queremos probar
3. **Validate**: Verificar que el resultado es el esperado

### Ejercicios

#### Ejercicio 1: Completar prueba de TodoItem

Completa el test para verificar que el componente `TodoItem` muestra correctamente el texto de una tarea con caracteres especiales.

Archivo: `app/components/__tests__/TodoItem.test.tsx`

#### Ejercicio 2: Completar prueba de TodoForm

Completa el test para verificar que el componente `TodoForm` maneja correctamente la entrada de texto con espacios al inicio o final.

Archivo: `app/components/__tests__/TodoForm.test.tsx`

#### Ejercicio 3: Completar prueba de TodoList

Completa el test para verificar que el componente `TodoList` pasa correctamente las funciones onToggle y onDelete a cada TodoItem.

Archivo: `app/components/__tests__/TodoList.test.tsx`

## Casos de Prueba

En las pruebas existentes, podrás encontrar ejemplos de:

- **Happy Path**: Pruebas que verifican el comportamiento correcto cuando todo funciona como se espera
- **Unhappy Path**: Pruebas que verifican el comportamiento cuando hay situaciones inesperadas o errores

## Ejecución de Pruebas

Para ejecutar las pruebas, utiliza el siguiente comando:

```bash
npm test
```

Para ejecutar las pruebas en modo observador (útil durante el desarrollo):

```bash
npm run test:watch
```

## Recursos Adicionales

- [Jest Documentation](https://jestjs.io/docs/getting-started)
- [React Testing Library Documentation](https://testing-library.com/docs/react-testing-library/intro/)
- [Jest DOM Testing Library](https://github.com/testing-library/jest-dom)
