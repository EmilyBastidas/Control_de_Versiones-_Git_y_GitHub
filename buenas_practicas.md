# Buenas Prácticas

Las buenas prácticas ayudan a mantener proyectos organizados, facilitar el trabajo en equipo y comprender el historial de cambios de manera clara.

---

## Mensajes de Commit

Un commit debe describir claramente qué cambio se realizó.

### Buenos ejemplos

```bash
git commit -m "Agrega validación de formulario"
```

```bash
git commit -m "Corrige error en login"
```

```bash
git commit -m "Actualiza documentación de Git"
```

---

### Malos ejemplos

```bash
git commit -m "cambios"
```

```bash
git commit -m "arreglo"
```

```bash
git commit -m "asd"
```

---

### Recomendaciones

Describe:

```text
Qué hiciste
```

No:

```text
Cómo te sentías cuando lo hiciste
```

---

### PDT

Si dentro de tres meses lees el commit, deberías entender inmediatamente qué cambió.

---

## Organización de Ramas

Evita trabajar directamente sobre:

```text
main
```

Utiliza ramas para nuevas funcionalidades o correcciones.

---

### Ejemplo

```text
main
│
├── feature-login
│
├── feature-dashboard
│
└── fix-navbar
```

---

### Convenciones comunes

#### Nuevas funcionalidades

```text
feature/nombre-funcionalidad
```

Ejemplo:

```text
feature/login
```

---

#### Corrección de errores

```text
fix/nombre-error
```

Ejemplo:

```text
fix/navbar-responsive
```

---

#### Documentación

```text
docs/nombre-documento
```

Ejemplo:

```text
docs/readme
```

---

### PDT

Una rama debería tener un objetivo específico.

---

## Flujo de Trabajo

Un flujo simple y efectivo:

### 1. Actualizar repositorio

```bash
git pull origin main
```

---

### 2. Crear rama

```bash
git switch -c feature/login
```

---

### 3. Realizar cambios

```bash
git add .
```

---

### 4. Crear commit

```bash
git commit -m "Agrega formulario de login"
```

---

### 5. Subir rama

```bash
git push origin feature/login
```

---

### 6. Crear Pull Request

```text
GitHub
↓
Pull Request
↓
Revisión
```

---

### 7. Fusionar cambios

```text
Merge
↓
main
```

---

### Flujo visual

```text
main
↓
Nueva rama
↓
Desarrollo
↓
Commit
↓
Push
↓
Pull Request
↓
Merge
↓
main
```

---

## Resolución de Conflictos

Un conflicto ocurre cuando Git no puede decidir automáticamente qué cambios conservar.

---

### Ejemplo

Dos personas modifican la misma línea:

Versión A:

```js
const nombre = "Emily";
```

Versión B:

```js
const nombre = "Ana";
```

Git no sabe cuál debe mantenerse.

---

### Resultado

Git mostrará algo parecido a:

```text
<<<<<<< HEAD
const nombre = "Emily";
=======
const nombre = "Ana";
>>>>>>> feature/login
```

---

### Resolver conflicto

Elegir la versión correcta:

```js
const nombre = "Emily";
```

o

```js
const nombre = "Ana";
```

o incluso combinar ambas si corresponde.

---

### Después de resolver

```bash
git add .

git commit -m "Resuelve conflicto de merge"
```

---

### Cómo evitar conflictos

#### Hacer pull frecuentemente

```bash
git pull
```

---

#### Trabajar en ramas separadas

```text
feature/login
feature/dashboard
feature/tasks
```

---

#### Mantener commits pequeños

Es más fácil resolver conflictos en cambios pequeños que en cambios enormes.

---

### PDT

Los conflictos son normales.

No significan que algo esté roto.

Simplemente Git necesita que un humano decida qué versión conservar.

---

## Resumen

### Commits

```text
Mensajes claros y descriptivos
```

---

### Ramas

```text
Una rama = una tarea
```

---

### Flujo de trabajo

```text
Pull
↓
Branch
↓
Commit
↓
Push
↓
Pull Request
↓
Merge
```

---

### Conflictos

```text
Ocurren cuando Git encuentra cambios incompatibles.
```

Se resuelven manualmente.

---

## PDT Personal

Antes de hacer un commit pregúntate:

```text
¿Este mensaje explica claramente lo que hice?
```

Antes de crear una rama pregúntate:

```text
¿Esta rama tiene un único propósito?
```

Y antes de hacer merge pregúntate:

```text
¿Probé mis cambios?
```

Estas tres preguntas evitan gran parte de los problemas habituales al trabajar con Git y GitHub.
