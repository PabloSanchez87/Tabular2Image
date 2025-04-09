
# Tabular2Image: Transformando Datos Tabulares en Imágenes para Deep Learning Visual

¿Y si los modelos de visión por computador pudieran ayudarte a resolver problemas con datos tabulares?

Este repositorio explora una idea tan simple como poderosa: **convertir datos tabulares en imágenes sintéticas**, para luego procesarlas con modelos de deep learning especializados en visión, como **CNNs** o **Vision Transformers (ViT)**.

Inspirado por la librería [TINTOlib](https://tintolib.readthedocs.io/en/latest/), este proyecto investiga cómo estas transformaciones pueden mejorar el rendimiento de modelos en tareas clásicas con datos estructurados, y cómo combinarlas con arquitecturas tradicionales en modelos híbridos.

---

## 🚀 Motivación

Aunque las redes neuronales profundas brillan en imágenes y texto, su rendimiento en datos tabulares suele estar por detrás de modelos clásicos como:

- `XGBoost`
- `LightGBM`
- `Random Forest`

Estos modelos manejan muy bien columnas heterogéneas, valores categóricos y relaciones no lineales.

Pero… ¿y si pudiéramos **representar las tablas como imágenes** y aprovechar lo mejor de ambos mundos?

---

## 🧠 ¿Cómo funciona?

1. **Cada fila del dataset se transforma en una imagen.**
2. **Los valores de las variables se codifican como píxeles.**
3. **La posición de cada píxel se basa en relaciones estadísticas**, como:
   - Correlación
   - Distancia euclídea
   - Proyecciones tipo t-SNE o PCA

---


## 🔀 Modelos híbridos

Combinamos lo mejor de ambos mundos:

- **Rama visual:** procesamos la imagen con una CNN o ViT.
- **Rama tabular:** procesamos directamente los valores con un MLP (red densa).
- **Fusión:** combinamos ambas salidas para realizar la predicción.

### Métodos de fusión implementados:

- Concatenación simple
- Concatenación + atención
- Attention fusion (aprende qué rama es más relevante)
- Transformer encoder fusion

---

## 🧪 Resultados esperados

- No se garantiza que supere a modelos tradicionales en todos los casos.
- Pero en problemas donde **las representaciones visuales capturan relaciones útiles**, los resultados pueden ser **competitivos o incluso superiores**.
- El enfoque **brilla especialmente en contextos donde queremos mezclar la visión global y el detalle variable a variable**.

---

## 📚 Recursos recomendados

- [Curso gratuito en Udemy (por el creador de TINTOlib):](https://www.udemy.com/course/tintolib-deep-learning-tabutar-data-con-imagenes-sinteticas/)
- [Crash Course en GitHub: ](https://github.com/oeg-upm/TINTOlib-Crash_Course)
- [Documentación oficial de TINTOlib:](https://tintolib.readthedocs.io/en/latest/)

---

## 📦 Requisitos

```bash
pip install -r requirements.txt
```

Principales dependencias:

- `tintolib`
- `tensorflow` / `torch`
- `scikit-learn`
- `matplotlib`, `seaborn`

---


## 🧭 Filosofía

> A veces, la clave no está en la técnica más compleja, sino en **cómo representamos los datos**.  
> Y quizás, transformar una tabla en una imagen sea justo lo que tu red necesitaba ver 👀

