# Ramas (Branches)

Las ramas permiten trabajar en nuevas funcionalidades o realizar cambios sin afectar la versión principal del proyecto.

Por defecto, la mayoría de los repositorios utilizan una rama principal llamada:

```text
main
```

---

## ¿Por qué usar ramas?

Imagina que estás trabajando en una aplicación de tareas.

```text
main
↓
Versión estable
```

Quieres crear una nueva funcionalidad:

```text
Login de usuarios
```

En lugar de modificar directamente `main`, puedes crear una rama independiente.

```text
main
│
└── login
```

Así puedes trabajar de forma segura y luego unir los cambios cuando todo funcione correctamente.

---

## git branch

Permite crear y visualizar ramas.

### Ver ramas existentes

```bash
git branch
```

Resultado:

```text
* main
```

El asterisco (\*) indica la rama actual.

---

### Crear una nueva rama

```bash
git branch login
```

Resultado:

```text
main
login
```

La rama se crea, pero sigues trabajando en `main`.

---

### PDT

`git branch` crea la rama, pero no cambia a ella.

---

## git switch

Permite cambiar de una rama a otra.

### Cambiar de rama

```bash
git switch login
```

Resultado:

```text
Switched to branch 'login'
```

Ahora estás trabajando en la rama:

```text
login
```

---

### Crear y cambiar al mismo tiempo

```bash
git switch -c dashboard
```

Equivale a:

```bash
git branch dashboard

git switch dashboard
```

---

### PDT

Actualmente `git switch` es la forma recomendada para cambiar ramas.

---

## git checkout

Durante muchos años fue el comando tradicional para cambiar ramas.

### Cambiar de rama

```bash
git checkout login
```

---

### Crear y cambiar

```bash
git checkout -b login
```

---

### ¿Por qué existe git switch?

Porque `git checkout` hacía demasiadas cosas:

- Cambiar ramas.
- Recuperar archivos.
- Restaurar versiones.

Git creó comandos más específicos:

```bash
git switch
```

y

```bash
git restore
```

---

### PDT

En proyectos modernos es preferible usar:

```bash
git switch
```

---

## git merge

Permite unir cambios de una rama a otra.

---

### Ejemplo

Tenemos:

```text
main
│
└── login
```

Trabajamos en:

```text
login
```

Hacemos commits y terminamos la funcionalidad.

Ahora queremos llevar esos cambios a:

```text
main
```

---

### Paso 1

Volver a main.

```bash
git switch main
```

---

### Paso 2

Fusionar la rama.

```bash
git merge login
```

Resultado:

```text
main
↓
Incluye los cambios de login
```

---

### Flujo visual

Antes:

```text
main
│
└── login
```

Después del merge:

```text
main
↓
Contiene login
```

---

### PDT

El merge siempre se ejecuta desde la rama que recibirá los cambios.

Ejemplo:

```bash
git switch main

git merge login
```

Significa:

```text
Trae todo lo que existe en login
↓
y agrégalo a main
```

---

## Flujo típico de trabajo

### Crear una rama

```bash
git branch nueva-funcionalidad
```

---

### Cambiar a la rama

```bash
git switch nueva-funcionalidad
```

---

### Trabajar normalmente

```bash
git add .

git commit -m "Agrega funcionalidad"
```

---

### Volver a main

```bash
git switch main
```

---

### Fusionar cambios

```bash
git merge nueva-funcionalidad
```

---

## Resumen

### Ver ramas

```bash
git branch
```

---

### Crear rama

```bash
git branch nombre-rama
```

---

### Cambiar de rama

```bash
git switch nombre-rama
```

---

### Crear y cambiar

```bash
git switch -c nombre-rama
```

---

### Método antiguo

```bash
git checkout nombre-rama
```

---

### Fusionar ramas

```bash
git merge nombre-rama
```

---

## PDT Personal

Piensa en las ramas como líneas de trabajo independientes.

```text
main
↓
Versión estable

feature-login
↓
Nueva funcionalidad

feature-dashboard
↓
Otra funcionalidad
```

Cuando una funcionalidad está lista:

```text
feature-login
↓
git merge
↓
main
```

Así puedes desarrollar nuevas características sin poner en riesgo la versión principal del proyecto.
