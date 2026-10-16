# Notebooks Resueltos — Clase IA

Carpeta con los notebooks organizados por lecture, con las secciones de
instrucciones / ejercicios completadas.

## Estructura

```
Notebooks_Resueltos/
├── Lecture_4_MDP/                 (Value/Policy Iteration + lab Warehouse)
├── Lecture_5_Q_Learning/          (CheeseWorld, FrozenLake, Taxi)
├── Lecture_6_ML_Pipeline/         (pipeline de clasificación de vinos)
├── Lecture_7_Keras_NN/            (redes densas con Keras 3)
├── Lecture_8_Transfer_Learning/   (transfer learning con EfficientNetB0)
└── Lecture_10_LLM_RAG/            (prompt engineering + RAG con NVIDIA NIM)
```

## Lecture 10 — Prompt engineering y RAG (NVIDIA NIM)

A diferencia de las lectures 4–8, los notebooks de la 10 **no tenían huecos
`TODO`/`NotImplementedError`**: todo el código ya venía escrito. Lo que piden son
**ejercicios de variación y preguntas de observación** dentro de cada sección.

### `00_prompt_engineering_nvidia_nim.ipynb`
Se resolvieron los ejercicios añadiendo, tras cada uno, una celda de código con la
variación pedida y una celda markdown con la respuesta:

- **Ej. 1 (tokens):** compara chars/token en inglés, español, código y emojis, y
  explica por qué la razón es solo aproximada.
- **Ej. 3 (alucinaciones):** añade la instrucción de admitir lo ficticio y discute
  por qué la temperatura no sustituye verificar con fuentes.
- **Ej. 4 (instrucción vs contenido):** reutiliza el mismo texto para doctorado,
  tweet y bullets.
- **Ej. 5 (system + multi-turno):** cambia el system a comentarista deportivo, añade
  turnos y muestra qué se pierde sin historial.
- **Ej. 6 (few-shot):** añade un tercer ejemplo (NEUTRAL) y compara con zero-shot.
- **Ej. 7 (respuesta verificable):** compara con/sin estructura y prueba un segundo
  problema aritmético.
- **Ej. 8 (formato de salida):** pide YAML y añade un campo `confidence` 0–1.
- Los ejercicios 2 y 9/9b/9c ya estaban resueltos en el notebook original.

### `01_rag_nvidia_nim.ipynb` y `02_rag_langchain_nvidia_nim.ipynb`
Son notebooks **demostrativos y ya completos** (pipeline RAG completo desde cero y
con LangChain). No tienen ejercicios por rellenar; las preguntas de observación ya
venían respondidas en el propio notebook. Se incluyen tal cual para mantener la
colección completa.

## Notas de ejecución

- Toda la Lecture 10 requiere una **API key de NVIDIA** (`NVIDIA_API_KEY`, gratis en
  https://build.nvidia.com/) y librerías (`openai`, `qdrant-client`, `faiss-cpu`,
  `deepeval`, `langchain-*`, `pydantic-ai`) que no están instaladas en este entorno,
  por lo que **las celdas no se pudieron ejecutar aquí**. El código añadido sigue
  exactamente los mismos patrones que las celdas ya resueltas del notebook y su
  sintaxis Python fue validada.
- Para correrlos: Google Colab → crear el Secret `NVIDIA_API_KEY` → "Ejecutar todo".
