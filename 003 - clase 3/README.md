# Encuentro 3 — Docker, Contenedores y Gemini API

**Python, Datos e Ingeniería de IA Aplicada — UTN Rosario · FRRO**  
Área de Extensión Universitaria · Matías Barreto, 2026

En esta clase damos el salto de los entornos locales a los entornos aislados: aprendemos Docker, entendemos por qué existe, y lo usamos para empaquetar una app Python con interfaz web. Al mismo tiempo, incorporamos la Gemini API como herramienta de pair programming.

---

## Cómo descargar esta carpeta

Esta es una subcarpeta dentro de un repositorio más grande. Para descargarla sola, sin clonar todo el repositorio, hay dos herramientas web gratuitas que no requieren registro:

### Opción 1 — Download Directory
Una de las opciones más limpias y directas:
1. Copiá el enlace completo de esta carpeta en GitHub.
2. Entrá en [download-directory.github.io](https://download-directory.github.io).
3. Pegá la URL en el cuadro de búsqueda y presioná **Enter**.
4. Se va a descargar automáticamente un archivo `.zip` con únicamente esta carpeta y todos sus archivos.

### Opción 2 — DownGit
Alternativa clásica y muy confiable:
1. Entrá en [downgit.github.io](https://downgit.github.io).
2. Pegá el enlace de la carpeta en el campo que dice **GitHub URL**.
3. Hacé clic en el botón **Download**.

---

## Contenido

| Material | Tema |
|---|---|
| `conceptos.md` | Mapa conceptual de Docker, comandos, variables de entorno, Dockerfile y Gemini como asistente |
| `001_entornos.ipynb` | Elección del entorno de desarrollo: local vs. aislado, herramientas y flujos de trabajo |
| `002_docker.ipynb` | Guía práctica: instalación, comandos, variables de entorno, Dockerfile, app Gradio en Docker |
| `003_gemini.ipynb` | Python + Gemini API: prompts dinámicos, funciones, listas, bucles, chatbot, visión multimodal |

---

## API utilizada

**Gemini API** — modelos de lenguaje e imagen de Google.

- Requiere API key gratuita (ver instrucciones abajo)
- Documentación: [ai.google.dev/gemini-api/docs](https://ai.google.dev/gemini-api/docs)
- Google AI Studio: [aistudio.google.com](https://aistudio.google.com)

---

## Cómo obtener la API key de Gemini

1. Entrar en [aistudio.google.com](https://aistudio.google.com)
2. Clic en **"Get API key"** → **"Create API key"**
3. Copiar la clave generada

---

## Configuración del entorno local

### Requisitos previos

- **Python 3.12 o superior** — [python.org/downloads](https://www.python.org/downloads/)
- **uv** — gestor de entornos virtuales ultrarrápido
- **Docker Desktop** — [docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

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

---

### Paso 2 — Crear el entorno virtual

Desde la carpeta `003 - clase 3/`:

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

---

### Paso 4 — Instalar las dependencias

```bash
uv pip install -r requirements.txt
```

---

### Paso 5 — Configurar la API key

```bash
# Copiar la plantilla:
cp .env.example .env

# Editar .env y pegar la clave de Gemini:
# GEMINI_API_KEY="tu_clave_aqui"
```

> ✦ El archivo `.env` está en `.gitignore` — no se sube al repositorio nunca.

---

### Paso 6 — Abrir los notebooks

```bash
jupyter lab
```

---

## Docker — inicio rápido

Con Docker instalado y la imagen construida:

```bash
# Construir la imagen de la app Gradio:
docker build -t app-gemini-gradio ./mi-app-gradio

# Correr el contenedor:
docker run --env-file .env -p 7860:7860 app-gemini-gradio

# Abrir en el navegador:
# http://localhost:7860
```

---

### Desactivar el entorno cuando terminan

```bash
deactivate
```
