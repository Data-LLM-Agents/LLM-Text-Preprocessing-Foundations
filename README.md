# LLM Text Preprocessing Foundations (Embeddings)

**Estudiante:** Juan Pablo Nieto Cortes  
**Materia:** AREP (Arquitecturas Empresariales)  
**Fecha:** Febrero 2026

## Descripción del Proyecto
Este repositorio contiene la solución para el laboratorio de preprocesamiento de texto para LLMs, basado en el Capítulo 2 del libro *"Build a Large Language Model From Scratch"* de Sebastian Raschka.

El objetivo es entender y reproducir los pasos fundamentales para preparar texto antes de ser procesado por un modelo de lenguaje (LLM), específicamente enfocándose en **Embeddings**.

## Contenido

### Archivos
- **`embeddings.ipynb`**: Notebook principal que contiene todo el código, explicaciones y experimentos.
- **`the-verdict.txt`**: Corpus de texto utilizado ("The Verdict" de Edith Wharton).
- **`libro.ipynb`**: Notebook de referencia original del autor (para consulta).

### Actividades Realizadas
1.  **Carga de Datos**: Lectura y procesamiento del archivo de texto.
2.  **Tokenización**: Implementación de un tokenizador utilizando BPE (Byte Pair Encoding) con la librería `tiktoken` (modelo gpt2).
3.  **Data Loader**: Creación de un `DataLoader` personalizado (`GPTDatasetV1`) que genera pares de entrada-salida (targets desplazados) utilizando una ventana deslizante.
4.  **Embeddings**: Implementación de las capas fundamentales:
    - **Token Embeddings**: Representación vectorial de cada token.
    - **Positional Embeddings**: Vectores que codifican la posición del token en la secuencia.
    - **Input Embeddings**: Suma de ambas representaciones.
5.  **Experimentación**: Análisis del impacto de los parámetros `max_length` y `stride` en la cantidad de datos de entrenamiento generados (Data Augmentation).

## Cómo Ejecutar
1.  Clonar el repositorio.
2.  Abrir el archivo `embeddings.ipynb` en Jupyter Notebook o VS Code.
3.  Ejecutar la primera celda para instalar las dependencias necesarias:
    ```python
    !pip install torch tiktoken
    ```
4.  Ejecutar el resto de las celdas para ver el paso a paso y los resultados del experimento.