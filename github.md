# GitHub

GitHub es una plataforma que permite almacenar repositorios Git en la nube, colaborar con otros desarrolladores y gestionar proyectos de software.

---

## Crear repositorios

Un repositorio es el espacio donde se almacena un proyecto.

### Crear un repositorio en GitHub

1. Iniciar sesión en GitHub.
2. Hacer clic en **New Repository**.
3. Elegir un nombre para el proyecto.
4. Agregar una descripción (opcional).
5. Elegir si será público o privado.
6. Crear el repositorio.

---

### Conectar un proyecto local

```bash
git remote add origin https://github.com/usuario/repositorio.git

git push -u origin main
```

---

### PDT

Un repositorio puede contener:

- Código fuente.
- Documentación.
- Imágenes.
- Historial de versiones.
- Configuración del proyecto.

---

## Forks

Un Fork es una copia personal de un repositorio que pertenece a otra persona.

Permite:

- Experimentar sin afectar el proyecto original.
- Realizar contribuciones.
- Proponer mejoras.

---

### Flujo de trabajo

```text
Repositorio Original
↓
Fork
↓
Tu cuenta de GitHub
```

Ahora puedes modificar tu copia libremente.

---

### ¿Cuándo se utiliza?

Cuando deseas contribuir a proyectos de código abierto.

Ejemplo:

```text
Proyecto Original
↓
Fork
↓
Cambios
↓
Pull Request
```

---

### PDT

Un Fork crea una copia completa del repositorio en tu cuenta.

---

## Pull Requests

Un Pull Request (PR) es una solicitud para fusionar cambios de una rama o fork dentro de otro repositorio.

---

### ¿Para qué sirve?

Permite:

- Revisar cambios antes de integrarlos.
- Comentar código.
- Detectar errores.
- Mantener la calidad del proyecto.

---

### Flujo básico

```text
Crear rama
↓
Realizar cambios
↓
Commit
↓
Push
↓
Pull Request
↓
Revisión
↓
Merge
```

---

### Ejemplo

Supongamos que agregas una nueva funcionalidad.

```text
feature-login
↓
Push a GitHub
↓
Pull Request
↓
main
```

El equipo revisa el código antes de aceptarlo.

---

### PDT

Un Pull Request no fusiona automáticamente los cambios.

Primero deben revisarse y aprobarse.

---

## Issues

Los Issues permiten registrar tareas, errores o mejoras dentro de un proyecto.

---

### Ejemplos de Issues

```text
Error al iniciar sesión
```

```text
Agregar modo oscuro
```

```text
Actualizar documentación
```

---

### ¿Para qué sirven?

- Reportar bugs.
- Planificar funcionalidades.
- Organizar tareas.
- Llevar seguimiento del proyecto.

---

### Flujo típico

```text
Issue
↓
Desarrollo
↓
Pull Request
↓
Merge
↓
Issue cerrado
```

---

### PDT

Los Issues funcionan como una lista de tareas para el proyecto.

---

## Flujo completo de colaboración

```text
Issue
↓
Crear rama
↓
Desarrollar solución
↓
Commit
↓
Push
↓
Pull Request
↓
Revisión
↓
Merge
↓
Cerrar Issue
```

---

## Resumen

### Crear repositorio

Permite almacenar proyectos en GitHub.

---

### Fork

Copia un repositorio ajeno a tu cuenta.

---

### Pull Request

Solicita integrar cambios a otra rama o repositorio.

---

### Issue

Permite registrar errores, tareas o mejoras.

---

## PDT Personal

Piensa en GitHub como una oficina de trabajo colaborativo.

```text
Repositorio
↓
Proyecto

Issue
↓
Tarea pendiente

Branch
↓
Zona de trabajo

Pull Request
↓
Solicitud de revisión

Merge
↓
Cambios aprobados
```

Este flujo es utilizado diariamente por equipos de desarrollo en proyectos profesionales.
