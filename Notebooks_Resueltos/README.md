# Notebooks Resueltos — Clase IA

Carpeta con los notebooks organizados por lecture (4–8), con todas las secciones de
instrucciones (`TODO`, `raise NotImplementedError`, preguntas abiertas) completadas.

## Estructura

```
Notebooks_Resueltos/
├── Lecture_4_MDP/
│   ├── 01_value_iteration_gridworld.ipynb        (ya estaba completo)
│   ├── 02_policy_iteration_gridworld.ipynb        (ya estaba completo)
│   └── 03_lab_warehouse_mdp_estudiantes.ipynb     ✅ RESUELTO
├── Lecture_5_Q_Learning/
│   ├── 01_cheeseworld_q_learning.ipynb            (ya estaba completo)
│   ├── 02_qlearning_frozenlake.ipynb              (ya estaba completo)
│   └── 03_qlearning_taxi.ipynb                     ✅ RESUELTO
├── Lecture_6_ML_Pipeline/
│   ├── 01_data_challenge.ipynb                     ✅ RESUELTO
│   ├── 02_training_challenge.ipynb                 ✅ RESUELTO
│   └── 03_evaluation_deployment_challenge.ipynb   ✅ RESUELTO
├── Lecture_7_Keras_NN/
│   ├── YourFirstDeepNN_FashionMNIST_Keras3.ipynb  (ya estaba completo)
│   ├── Challenge_Keras3_CIFAR10_Grayscale.ipynb   ✅ RESUELTO
│   └── Challenge_Keras3_OlivettiFaces.ipynb       ✅ RESUELTO
└── Lecture_8_Transfer_Learning/
    └── taller_transfer_learning_datos_propios_keras3.ipynb  ✅ RESUELTO
```

## Qué se resolvió en cada notebook

### Lecture 4 — `03_lab_warehouse_mdp_estudiantes.ipynb`
- Clase `WarehouseMDP` completa (estados, paredes, pisos resbalosos, terminales,
  peligros, `R(s)` y función de transición `T(s,a,s')` con probabilidades dependientes
  del tipo de piso).
- `value_iteration`, `extract_policy`.
- `policy_evaluation`, `policy_improvement`, `policy_iteration`.
- Respuestas a las preguntas de interpretación (Parte 5).
- **Verificado:** las distribuciones de transición suman 1, y Value Iteration y
  Policy Iteration convergen a la misma política óptima.

### Lecture 5 — `03_qlearning_taxi.ipynb`
- `choose_action` (ε-greedy), `update_q` (regla de Q-Learning), `train_q_learning`.
- Respuestas a las 7 preguntas + experimento de hiperparámetro (ε).
- Nota: se usa el entorno `Taxi-v3` de Gymnasium (el id `Taxi-v4` del enunciado no
  existe en Gymnasium).

### Lecture 6 — Pipeline de clasificación de vinos
- `01_data_challenge`: carga, profiling, split estratificado, EDA y persistencia
  (`train.csv`, `test.csv`, `data_contract.json`). Incluye una celda que genera
  `data/raw/wine.csv` desde scikit-learn si no existe.
- `02_training_challenge`: preprocesadores en pipelines, modelos candidatos
  (DecisionTree, LogisticRegression, KNN), comparación con CV, GridSearchCV y
  persistencia del campeón.
- `03_evaluation_deployment_challenge`: evaluación en test, función `predict` con
  validación de esquema, predicción por lotes y reporte de métricas.

### Lecture 7 — Redes neuronales con Keras 3
- `Challenge_Keras3_CIFAR10_Grayscale`: normalización, arquitectura
  (Flatten → Dense(128) ReLU → Dense(10)), compile, fit, evaluate, Softmax/argmax y
  respuestas a las 10 preguntas.
- `Challenge_Keras3_OlivettiFaces`: arquitectura (Flatten → Dense(64) ReLU →
  Dense(40)), compile, fit, evaluate, Softmax/argmax y respuestas a las preguntas.

### Lecture 8 — `taller_transfer_learning_datos_propios_keras3.ipynb`
- TODO 1: problema de ejemplo (bus/motorcycle/bicycle) con términos de búsqueda.
- TODO 3: compile + EarlyStopping + fit de la cabeza con backbone congelado.
- Curvas de aprendizaje (accuracy y loss).
- TODO 5: `N_UNFROZEN=20`, recompilación y fine-tuning con `lr=1e-5`.
- TODO 4 y TODO 6: interpretación de la evaluación, tabla de análisis de errores,
  conclusiones y cierre conceptual (feature extraction vs fine-tuning vs entrenar
  desde cero).

## Notas sobre ejecución

- Los notebooks de **Lecture 5, 7 y 8** requieren librerías externas
  (`gymnasium`, `keras`/`tensorflow`, `scikit-learn`, `ddgs`) que no están instaladas
  en este entorno sandbox de solo lectura, por lo que no se pudieron ejecutar aquí.
  El código fue completado siguiendo exactamente la "receta" indicada en cada enunciado.
- El notebook de **Lecture 4** sí fue ejecutado y verificado (solo usa Python puro).
- El pipeline de **Lecture 6** usa `scikit-learn` estándar y el dataset Wine público.
