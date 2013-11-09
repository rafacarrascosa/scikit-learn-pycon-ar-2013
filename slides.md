# **`scikit-learn`**

---

# Esta charla

- Título: Aprendizaje automático con `scikit-learn`

- Todo el material de la charla esta en github: `https://github.com/rafacarrascosa/scikit-learn-pycon-ar-2013`

- Quien soy?
    - Rafael Carrascosa.
    - Soy programador.
    - Me especializo en PLN y ML.
    - Trabajo para Machinalis.
    - También trabajo de docente.

---

# Outline

- Introducción

- Clasificación
    - Superficies de decisión (iuju!)

- Clustering

- Regression

- Cierre

---


# Qué es scikit-learn?

 - Aprendizaje automático (Machine Learning) en python

 - Open source (BSD)

 - ~3 años de edad (de 2007 a 2010 no era público)

 - ~1800 stars en github (django ~7800, numpy ~1000)

---

# Qué es Machine Learnig?

- Al `ML` le conciernen algoritmos para aprender **funciones** a partir
  de **ejemplos**.

- Un algoritmo de `ML` es una *factory* de funciones: Toma ejemplos y produce
  una función.
    - Por ejemplo: Un detector de spam toma ejemplos de spam y produce una
      función que puede decidir si algo es spam o no.

- Todo trabajo con `ML` tiene una etapa de **entramiento**.

- Todo trabajo con `ML` tiene una etapa de **evaluación**.

---

# Clasificación

En el contexto de `scikit-learn`, clasificación es la tarea de aprender
a partir de **ejemplos** una función de la pinta:


$$
  f: \mathbb{R}^n \mapsto Category
$$

Donde $Category \hspace{5px}$ es un conjunto de labels, tipicamente no muy grande (menos de 20).

A cada dimension de $\mathbb{R}^n$ se la llama **feature** o **atributo**.


# Aplicaciones:

 - Detección de spam, ejemplo: $Category = \lbrace {spam}, {nospam} \rbrace$
 - OCRs, ejemplo: $Category = \lbrace a, b, c \dots , 0, 1, 2, \dots \rbrace$
 - Procesamiento del Lenguage Natural, ejemplo $Category = \lbrace {verbo}, {sustantivo}, {adjetivo}, \dots \rbrace$
 - Un largo laaaargo etc.

---



# Un problema concreto

Determinar el sexo de una persona (masculino o femenino) en base a su altura y a su peso.
El problema sería aprender:

$$
f: {Peso} \times {Altura} \mapsto  \lbrace M, F \rbrace
$$

Donde ${Peso}, {Altura} \subseteq \mathbb{R}$.

Se esperaría que:

$$ 
f(85, 1.80) = M \hspace{50px} \text{ese soy yo}
$$
$$ 
f(65, 1.70) = F \hspace{50px} \text{esta es mi novia}
$$

---

# Hands on the mass now

---

# Clustering

En el contexto de `scikit-learn`, clustering es la tarea de agrupar
automáticamente datos que son similares entre si. Es decir, aprender
automáticamente una función:

$$
  f: \mathbb{R}^n \mapsto \mathbb{N}
$$

Donde los datos que terminan agrupados juntos son mapeados por $f$ al mismo
número.

Notar que el dataset no necesita tener una atributo *target*.

# Aplicaciones:

- Biología: inferencia de comunidades, agrupación de genomas humanos
- Investigación de mercado: Grupos de consumidores
- Análisis de redes sociales: Grupos de personas
- Etc.

---

# Un problema sintético


---

# Otros métodos de clustering

- Hierarchical (WARD).

- Affinity propagation

- Mean shift

- Spectral clusterin

---

# Regresión:

En el contexto de `scikit-learn`, regresión es la tarea de aprender
a partir de **ejemplos** una función de la pinta:

$$
  f: \mathbb{R}^n \mapsto \mathbb{R}
$$

# Aplicaciones:
- Inumerables aplicaciones en economía, p.ej. Tendencias en la bolsa de valores
- Establecer relaciones causa-efecto en varias áreas de la ciencia
- Ey! es $\mathbb{R}^n$ a $\mathbb{R}$, la imaginación es el límite!

---

# Problema del peaje de Avellaneda

Determinar la cantidad de autos que van a pasar por un peaje a lo largo del día
en base a los autos que pasaron a las 3am.

$$
f: {Tresam} \times {Hora} \mapsto {Autos}
$$

Donde ${Tresam}, {Hora}, {Autos} \subseteq \mathbb{R}$.

---

# Otros métodos de regresión

- Ordinary least squared
- Ridge regression
- Lasso
- Elastic net
- Least Angle Regression
- Bayesian Regression
- Perceptron
- Support Vector Regression
- Algunos ensemble methods
- Etc...


---

# Qué más hay en `scikit-learn`?

 - Preproceso de datos:
    - Scaling, Normalizacion, Binarizacion
    - Label handling, Data imputation
    - Feature extractors (p.ej: tf-idf)
 - Reduccion de dimensionalidad:
    - PCA
    - SVD
    - Non-negative matrix factorization
 - Evaluación y model selection:
    - Evaluacion: precision, recall, accuracy, cross validation, etc.
    - Grid Search
    - Metricas para clusters.

---

# Y en la vida real?

 - Dimensiones altas!

 - Caso de uso: **Yalign**

---

# Fin! Ahora comentarios y preguntas
