# Comandos Básicos de Git

## git init

Inicializa Git en una carpeta y la convierte en un repositorio.

```bash
git init
```

Resultado:

```text
Initialized empty Git repository
```

### ¿Cuándo se usa?

Cuando quieres comenzar a controlar versiones en un proyecto nuevo.

### PDT

Este comando crea una carpeta oculta llamada:

```text
.git
```

Aquí Git almacena toda la información del repositorio.

---

## git status

Muestra el estado actual del repositorio.

```bash
git status
```

Permite ver:

- Archivos modificados.
- Archivos nuevos.
- Archivos preparados para commit.
- Rama actual.

Ejemplo:

```text
On branch main

Changes not staged for commit:
  modified: README.md
```

### PDT

Es uno de los comandos más utilizados en Git.

Si tienes dudas sobre el estado del proyecto:

```bash
git status
```

---

## git add

Agrega archivos al área de preparación (staging area).

### Agregar un archivo

```bash
git add README.md
```

### Agregar todos los archivos

```bash
git add .
```

### ¿Qué hace?

Le dice a Git:

> "Quiero incluir estos cambios en el próximo commit."

---

### Flujo

```text
Archivo modificado
↓
git add
↓
Staging Area
↓
git commit
```

---

## git commit

Guarda una nueva versión del proyecto.

```bash
git commit -m "Agrega documentación de Git"
```

### ¿Qué registra?

- Cambios realizados.
- Autor.
- Fecha.
- Mensaje descriptivo.

### Ejemplo

```bash
git commit -m "Corrige errores en README"
```

---

### Buenas prácticas

Usar mensajes claros:

```bash
git commit -m "Agrega sección de comandos básicos"
```

Evitar:

```bash
git commit -m "cambios"
```

---

### PDT

Un commit es como guardar una partida de un videojuego.

---

## git log

Muestra el historial de commits.

```bash
git log
```

Ejemplo:

```text
commit a1b2c3d4
Author: Emily
Date: ...

    Agrega README inicial
```

---

### Versión resumida

```bash
git log --oneline
```

Resultado:

```text
a1b2c3d Agrega README inicial
f8e7d6c Corrige errores
```

### PDT

`git log --oneline` es más cómodo para revisar rápidamente el historial.

---

## git diff

Muestra las diferencias entre versiones.

```bash
git diff
```

Permite ver exactamente qué líneas fueron modificadas.

Ejemplo:

Antes:

```js
const nombre = "Juan";
```

Después:

```js
const nombre = "Emily";
```

Git mostrará la diferencia entre ambos cambios.

---

### ¿Cuándo usarlo?

Antes de hacer:

```bash
git add .
```

o

```bash
git commit
```

para revisar los cambios realizados.

---

## Flujo básico de trabajo

```text
Crear o modificar archivos
↓
git status
↓
git add .
↓
git status
↓
git commit -m "mensaje"
↓
git log --oneline
```

---

## Resumen

### Inicializar repositorio

```bash
git init
```

---

### Ver estado

```bash
git status
```

---

### Preparar archivos

```bash
git add .
```

---

### Crear commit

```bash
git commit -m "mensaje"
```

---

### Ver historial

```bash
git log
```

o

```bash
git log --oneline
```

---

### Ver diferencias

```bash
git diff
```

---

## PDT Personal

Cuando trabajes en un proyecto, este suele ser el flujo más común:

```bash
git status

git add .

git commit -m "describe lo que hiciste"

git push origin main
```

Si haces esto de forma constante, tendrás un historial limpio y fácil de entender.
