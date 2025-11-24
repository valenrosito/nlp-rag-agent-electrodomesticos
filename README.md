# RAG Agent - Electrodomésticos

Agente conversacional basado en RAG (Retrieval-Augmented Generation) para responder consultas sobre electrodomésticos utilizando Google Generative AI.

## Descripción

Este proyecto implementa un sistema de recuperación de información aumentada con generación (RAG) que permite realizar consultas en lenguaje natural sobre electrodomésticos. El sistema utiliza embeddings para buscar información relevante en una base de datos vectorial y genera respuestas coherentes utilizando modelos de Google AI (Gemini).

## Estructura del Proyecto

```
nlp-rag-agent-electrodomesticos/
├── TP_Final_NLP_RAG_Electrodomesticos.ipynb  # Notebook principal con toda la implementación
├── data/                                       # Directorio de datos
│   ├── raw/                                   # Datos originales
│   └── processed/                             # Datos procesados y embeddings
├── pyproject.toml                              # Configuración de dependencias
├── .env                                        # Variables de entorno (API keys)
├── .gitignore                                  # Archivos ignorados por git
└── README.md                                   # Este archivo
```

## Requisitos Previos

- Python 3.10 o superior
- [uv](https://github.com/astral-sh/uv) - Gestor de paquetes Python ultrarrápido
- API Key de Google AI Studio (obtener en [Google AI Studio](https://makersuite.google.com/app/apikey))

## Instalación

### 1. Instalar uv

Si aún no tienes uv instalado:

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# O con pip
pip install uv
```

### 2. Clonar o Descargar el Proyecto

```bash
cd /ruta/del/proyecto
```

### 3. Crear Entorno Virtual

```bash
uv venv
```

### 4. Activar el Entorno Virtual

```bash
# macOS/Linux
source .venv/bin/activate

# Windows
.venv\Scripts\activate
```

### 5. Instalar Dependencias

Usando el archivo `pyproject.toml`:

```bash
uv pip install -e .
```

### 6. Configurar Variables de Entorno

Crear un archivo `.env` en la raíz del proyecto:

```bash
GOOGLE_API_KEY=tu_api_key_aqui
```

---

