# 🧠 NLP_TrabajoFinal

## 🎯 Objetivo

El objetivo principal de este proyecto es **comprobar la consistencia de noticias relacionadas con mercados financieros**, para su **posterior análisis de sentimiento y traducción al inglés**.  
Con ello buscamos desarrollar una herramienta capaz de **filtrar las fake news** y ofrecer una **aproximación del estado del mercado**.  
La **traducción al inglés** es un requisito imprescindible para **estandarizar el idioma** de todas las noticias antes de su análisis.

---

## 🧩 Tareas de NLP

### 1. Normalización lingüística
- Uso de un **modelo NMT o LLM** (aún por especificar) para traducir las noticias al inglés.
- La traducción permite unificar el idioma de las fuentes para el análisis posterior.

### 2. Detección de consistencia interna
- Implementación de un **modelo NLI (Natural Language Inference)**.
- Su objetivo es **detectar si la noticia es coherente** o si contiene fragmentos inconexos o contradictorios.

### 3. Análisis de sentimiento
- Uso de un **transformer preentrenado BERT** como modelo base.
- Realizaremos **fine-tuning específico para el dominio financiero**.
- Clasificación del sentimiento de las noticias en tres categorías:
  - Positivo  
  - Negativo  
  - Neutral

---

## 🧪 Evaluación

### Normalización lingüística
- Se empleará la métrica **COMET**, una métrica neuronal moderna que **correlaciona bien con el juicio humano**.  
- Dado que disponemos de las noticias en su idioma original y traducidas, podremos **evaluar directamente la calidad de la traducción**.

### Detección de consistencia interna y análisis de sentimiento
- Como ambos son **problemas de clasificación**, se utilizarán métricas estándar de *Machine Learning*:
  - **Accuracy**
  - **F1-score**
  - **Matriz de confusión** (para visualizar errores sistemáticos)

---

## ⚙️ Resumen del pipeline

1. **Entrada:** Noticias financieras (texto libre, distintos idiomas).  
2. **Traducción al inglés:** Modelo NMT/LLM → evaluación con COMET.  
3. **Verificación de consistencia:** Modelo NLI → métrica F1/Accuracy.  
4. **Análisis de sentimiento:** Fine-tuned BERT → tres clases (Positivo, Negativo, Neutral).  
5. **Salida:** Noticia clasificada y validada en inglés, lista para análisis cuantitativo.

---

## 📚 Tecnologías previstas

- Python  
- Transformers (Hugging Face)  
- PyTorch / TensorFlow  
- COMET (para evaluación de traducción)  
- Herramientas de preprocesamiento NLP (spaCy, NLTK, etc.)

---

## 👥 Autores
Proyecto desarrollado en el marco de la asignatura **Procesamiento del Lenguaje Natural (NLP)**.
