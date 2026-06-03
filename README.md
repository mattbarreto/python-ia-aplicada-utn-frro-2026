# Python, Datos e Ingeniería de IA Aplicada

**UTN Rosario — FRRO, Área de Extensión Universitaria**  
Matías Barreto · 2026

Curso profesional de 33 horas orientado al desarrollo de soluciones con Python e inteligencia artificial. Recorre el camino completo desde el entorno de trabajo hasta el prototipado y despliegue de sistemas con datos, modelos y APIs.

---

## Estructura del curso

| Carpeta | Encuentro | Tema | Estado |
|---|---|---|---|
| `001 - clase 1` | Encuentro 1 | Entorno profesional de desarrollo | ✓ Disponible |
| `002 - clase 2` | Encuentro 2 | Python aplicado para automatización y desarrollo | ✓ Disponible |
| `003 - clase 3` | Encuentro 3 | Reproducibilidad, Docker y pair programming con IA | En preparación |
| `004 - clase 4` | Encuentro 4 | Backend con FastAPI y Vibe Engineering | En preparación |
| `005 - clase 5` | Encuentro 5 | Análisis de datos con Python | En preparación |
| `006 - clase 6` | Encuentro 6 | Procesamiento de lenguaje natural y modelos de lenguaje | En preparación |
| `007 - clase 7` | Encuentro 7 | Computer Vision aplicada | En preparación |
| `008 - clase 8` | Encuentro 8 | Integración multimodal con VLMs, LLMs y RAG | En preparación |
| `009 - clase 9` | Encuentro 9 | Agentes de IA, MCP, Skills y prototipado | En preparación |
| `010 - clase 10` | Encuentro 10 | Fundamentos de nube y deploy inicial | En preparación |
| `011 - demo-day` | Encuentro 11 | Demo Day — presentación del proyecto integrador | En preparación |

---

## Pila tecnológica

| Área | Herramientas |
|---|---|
| Lenguaje y entorno | Python 3.12+, terminal, uv, venv, VS Code |
| Versionado | Git, GitHub |
| Backend y APIs | HTTP, JSON, FastAPI |
| Datos | Pandas, notebooks Jupyter |
| IA aplicada | LLMs, VLMs, embeddings, RAG, agentes |
| Interfaces y deploy | Gradio, Streamlit, Docker, servicios cloud |

---

## Cómo usar este repositorio

Cada carpeta de encuentro es autónoma: tiene su propio `README.md`, `requirements.txt` y notebooks listos para ejecutar.

### Flujo recomendado por encuentro

```bash
# 1. Clonar el repositorio del curso (una sola vez)
git clone https://github.com/tu-usuario/tu-repo-de-cursada.git
cd tu-repo-de-cursada

# 2. Entrar a la carpeta del encuentro
cd "001 - clase 1"

# 3. Crear el entorno virtual
uv venv .venv

# 4. Activarlo
source .venv/bin/activate          # Linux / macOS
.venv\Scripts\activate.bat         # Windows CMD
.venv\Scripts\Activate.ps1         # Windows PowerShell

# 5. Instalar dependencias del encuentro
uv pip install -r requirements.txt

# 6. Abrir los notebooks
jupyter lab
```

> ✦ Este curso usa `requirements.txt` en lugar de `pyproject.toml`.
> El comando de instalación es siempre `uv pip install -r requirements.txt`, no `uv sync`.

---

## Proyecto integrador

A lo largo de la cursada cada participante construye un proyecto integrador con criterios profesionales. Debe articular al menos:

- un backend funcional
- una fuente de datos o corpus de trabajo
- una capacidad de IA aplicada
- una interfaz de demostración

Los proyectos se presentan en el **Encuentro 11 — Demo Day**.

---

## Recursos generales

- [Documentación de Python 3.12](https://docs.python.org/3.12/)
- [uv — gestor de entornos](https://docs.astral.sh/uv/)
- [JupyterLab](https://jupyterlab.readthedocs.io/)
- [Git — referencia rápida](https://git-scm.com/docs)
- [FastAPI](https://fastapi.tiangolo.com/)
- [Open-Meteo API](https://open-meteo.com/en/docs)
