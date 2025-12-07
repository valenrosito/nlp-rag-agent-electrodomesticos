# RAG Agent - Electrodomésticos

Agente conversacional basado en RAG (Retrieval-Augmented Generation) para responder consultas sobre electrodomésticos utilizando Google Generative AI.

## Descripción

Este proyecto implementa un sistema de recuperación de información mediante RAG que permite realizar consultas en lenguaje natural sobre electrodomésticos. 

El proyecto contiene dos implementaciones:
- **Problema 1 (`1.rag_flow.ipynb`)**: RAG con flujo simple utilizando búsqueda vectorial, tabular y de grafos con un enrutamiento
- **Problema 2 (`2.rag_agent.ipynb`)**: RAG con flujo agéntico que combina tres bases de datos (vectorial, tabular y grafos) con enrutamiento inteligente mediante Agente ReAct

## Estructura del Proyecto

```
nlp-rag-agent-electrodomesticos/
├── 1.rag_flow.ipynb  # Notebook con la implementacion del Problema 1
├── 2.rag_agent.ipynb  # Notebook con la implementacion del Problema 2
├── data/                                       # Directorio de datos
│   ├── raw/                                   # Datos originales
│   └── processed/                             # Datos procesados y embeddings
├── pyproject.toml                              # Configuración de dependencias
├── .env                                     
├── .gitignore                                  
└── README.md                                 
```

## Requisitos Previos

- Python version mayor o igual a 3.10 y menor o igual a 3.13.
- [uv](https://github.com/astral-sh/uv) - Gestor de paquetes Python
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

Para instalar Memgraph, debes ejecutar en la terminal con Docker corriendo:

```bash
docker run -p 7687:7687 memgraph/memgraph
```

**Comandos útiles de Docker:**
```bash
# Ver logs
docker logs memgraph

# Detener Memgraph
docker stop memgraph

# Iniciar Memgraph nuevamente
docker start memgraph

# Eliminar contenedor
docker rm memgraph
```

### 6. Configurar Variables de Entorno

Crear un archivo `.env` en la raíz del proyecto:

```bash
GOOGLE_API_KEY=tu_api_key_aqui
```
> Recomendación: Si activas por primera vez, te dan 300 dolares gratis de la API paga por 90 dias, esto aumenta el limite de request por minuto y disminuye el tiempo entre request minimo requerido

---

