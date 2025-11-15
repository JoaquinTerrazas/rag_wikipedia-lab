# 🤖 rag_wikipedia-lab (Task 2)

Este proyecto es un sistema de **RAG (Generación Aumentada por Recuperación)**. El sistema consulta y resume artículos de Wikipedia utilizando un LLM 100% local y gratuito.

El pipeline completo está contenido en el notebook principal:
1.  Obtiene datos en vivo de la `wikipedia-api`.
2.  Trocea el texto con `LangChain TextSplitter`.
3.  Crea embeddings con `sentence-transformers`.
4.  Construye una base de datos `ChromaDB` desde cero.
5.  Utiliza el LLM `google/flan-t5-large` para responder preguntas y generar resúmenes.

---

## ✨ Características Principales

* **Entorno Estable:** Fija las versiones de `langchain==0.1.7` y `chromadb==0.4.14` para garantizar una reproducibilidad del 100% y evitar conflictos de dependencias.
* **LLM Rápido:** Utiliza `google/flan-t5-large`, un modelo eficiente y rápido que evita los timeouts y problemas de RAM de Google Colab.
* **Sin "Atajos":** Este notebook construye *todo* el pipeline desde cero.

---

## 🚀 Cómo Ejecutar (Google Colab)

1.  Abre el notebook `notebooks/rag_wikipedia.ipynb` en Google Colab.
2.  **IMPORTANTE:** Ve a **Entorno de ejecución** > **Cambiar tipo de entorno de ejecución** y selecciona **T4 GPU**.
3.  Ve a **Entorno de ejecución** > **Ejecutar todas**.
4.  El notebook instalará las dependencias, creará el dataset, construirá la base de datos y generará todos los entregables en las carpetas `data/` y `outputs/` del entorno de Colab.

---
