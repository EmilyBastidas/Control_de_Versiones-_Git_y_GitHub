# Fundamentos

## ¿Qué es Git?

Git es un sistema de control de versiones distribuido que permite registrar y gestionar los cambios realizados en un proyecto a lo largo del tiempo.

Con Git es posible:

- Guardar versiones del proyecto.
- Recuperar versiones anteriores.
- Trabajar en equipo.
- Crear ramas para desarrollar nuevas funcionalidades.
- Mantener un historial completo de cambios.

### PDT

Git trabaja de forma local en tu computadora.

---

## ¿Qué es GitHub?

GitHub es una plataforma en la nube que permite almacenar y compartir repositorios Git.

GitHub facilita:

- Guardar proyectos online.
- Colaborar con otros desarrolladores.
- Gestionar cambios mediante Pull Requests.
- Mantener respaldo del código.
- Mostrar proyectos en un portafolio profesional.

### PDT

Git y GitHub no son lo mismo.

```text
Git
↓
Herramienta de control de versiones

GitHub
↓
Plataforma donde se almacenan repositorios Git
```

---

## ¿Qué es un repositorio?

Un repositorio es el lugar donde Git almacena todos los archivos, cambios e historial de un proyecto.

Puede ser:

### Local

Existe únicamente en tu computadora.

```bash
git init
```

---

### Remoto

Está alojado en plataformas como GitHub.

```bash
git push
```

---

### PDT

Un repositorio contiene:

- Archivos del proyecto.
- Historial de cambios.
- Configuración de Git.
- Ramas.

---

## ¿Qué es un commit?

Un commit es una captura o punto de guardado del proyecto en un momento específico.

Cada commit registra:

- Los cambios realizados.
- El autor.
- La fecha.
- Un mensaje descriptivo.

Ejemplo:

```bash
git commit -m "Agrega validación de formulario"
```

### PDT

Piensa en un commit como una partida guardada de un videojuego.

Puedes volver a ese punto cuando lo necesites.

---

## ¿Qué es una rama?

Una rama (branch) es una línea de trabajo independiente dentro de un repositorio.

Permite desarrollar nuevas funcionalidades sin afectar la versión principal del proyecto.

Por defecto existe la rama:

```text
main
```

Ejemplo:

```text
main
│
├── login
│
├── dashboard
│
└── tareas
```

Cada funcionalidad puede desarrollarse en una rama diferente.

---

### Crear una rama

```bash
git branch nueva-funcionalidad
```

---

### Cambiar de rama

```bash
git switch nueva-funcionalidad
```

---

### Fusionar una rama

```bash
git merge nueva-funcionalidad
```

---

### PDT

Las ramas permiten experimentar sin romper el proyecto principal.

Primero se trabaja en una rama y luego se integra a `main`.
