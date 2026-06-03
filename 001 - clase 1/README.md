# Encuentro 1 — Entorno profesional de desarrollo

**Python, Datos e Ingeniería de IA Aplicada — UTN Rosario · FRRO**  
Área de Extensión Universitaria · Matías Barreto, 2026

Configuración del entorno de trabajo profesional con Git, GitHub y Python. Primer contacto con el lenguaje: tipos de datos, estructuras, bucles y funciones.

---

## Contenido

| Notebook | Tema |
|---|---|
| `001_git` | Git y GitHub: repositorio personal, nomenclatura, flujo de trabajo y troubleshooting |
| `002_python` | Primer contacto con Python: variables, strings, listas, diccionarios, condicionales, bucles y funciones |

---

## Cómo descargar esta carpeta

Esta es una subcarpeta dentro de un repositorio más grande. Para descargarla sola sin clonar todo el repositorio, hay dos herramientas web gratuitas que no requieren registro:

### Opción 1 — Download Directory

1. Copiá el enlace completo de esta carpeta en GitHub.
2. Entrá en **[download-directory.github.io](https://download-directory.github.io)**.
3. Pegá la URL en el cuadro de búsqueda y presioná Enter.
4. Se descarga automáticamente un `.zip` con únicamente esta carpeta.

### Opción 2 — DownGit

1. Entrá en **[downgit.github.io](https://downgit.github.io)**.
2. Pegá el enlace de la carpeta en el campo *GitHub URL*.
3. Hacé clic en **Download**.

---

## Configuración del entorno local

### Requisitos previos

- **Python 3.12 o superior** — [python.org/downloads](https://www.python.org/downloads/)
- **uv** — gestor de entornos virtuales ultrarrápido

> ✦ Este encuentro usa únicamente la biblioteca estándar de Python.
> La única dependencia externa es JupyterLab para ejecutar los notebooks.

---

### Paso 1 — Instalar uv

**Linux / macOS:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell):**
```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**Alternativa universal** (si ya tenés pip):
```bash
pip install uv
```

Verificá la instalación:
```bash
uv --version
```

---

### Paso 2 — Crear el entorno virtual

Desde la carpeta `001 - clase 1/`:

```bash
uv venv .venv
```

---

### Paso 3 — Activar el entorno

**Linux / macOS:**
```bash
source .venv/bin/activate
```

**Windows (CMD):**
```cmd
.venv\Scripts\activate.bat
```

**Windows (PowerShell):**
```powershell
.venv\Scripts\Activate.ps1
```

El prompt de la terminal va a mostrar `(.venv)` cuando el entorno esté activo.

---

### Paso 4 — Instalar las dependencias

Este proyecto usa `requirements.txt` directamente, **sin `pyproject.toml`**.  
El comando de instalación con uv es:

```bash
uv pip install -r requirements.txt
```

> ✦ Diferencia clave con otros proyectos:
> - Con `pyproject.toml` se usa `uv sync`
> - Con `requirements.txt` se usa `uv pip install -r requirements.txt`
>
> Ambos crean el mismo entorno aislado — solo cambia el origen de la lista de dependencias.

---

### Paso 5 — Abrir los notebooks

```bash
jupyter lab
```

O si preferís la interfaz clásica:
```bash
jupyter notebook
```

---

### Desactivar el entorno cuando terminás

```bash
deactivate
```
