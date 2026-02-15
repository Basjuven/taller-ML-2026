# Unidad 0 — Puente hacia Machine Learning (Pre-ML)

Esta unidad es un **puente** entre Python intermedio y Machine Learning.  
La meta es que todos los participantes tengan una base mínima sólida para:

- entender datasets como “tablas” (no como listas sueltas),
- manipular datos,
- reconocer conceptos típicos en ML (features, target, entrenamiento/validacion y prueba),
- Manejar Numpy y visualización.

---

## Objetivos de aprendizaje

Al terminar esta unidad podrán:

1. Diferenciar estructuras de datos clave en Python (listas vs diccionarios).
2. Escribir funciones simples para procesar datos.
3. Manipular tablas con Pandas (filtrar, seleccionar, describir).
4. Entender de forma básica qué es un `array` de Numpy y por qué ML lo usa.
5. Explicar el flujo general de un proyecto de ML (pipeline) sin entrar aún en modelos.

---

## 0.1 Repaso de Python esencial ([Data analysis](https://github.com/Basjuven/taller-ML-2026/blob/main/book/analisis_de_datos_taller.ipynb))

### Conceptos clave
- Tipos: `int`, `float`, `str`, `bool`
- Listas: indexación, slicing, métodos comunes (`append`, `sort`)
- Diccionarios: claves/valores (muy usados para representar registros)
- Bucles y condicionales aplicados a datos
- Funciones: `def ...` y `return` (fundamental para reutilizar código)
- Importación de bibliotecas: `import ... as ...`

### Mini-ejercicio (para notebook o demo rápida)
- Crear una lista de temperaturas y calcular el promedio.
- Crear un diccionario que represente un registro (por ejemplo: un producto o una medición).

---

## 0.2 Pensar en términos de datos (tablas y variables)

Machine Learning se alimenta de **datos**. La forma más común de trabajar datos es como tabla:

- **Fila**: una observación (un día, un sensor, un producto, un paciente, etc.)
- **Columna**: una variable (temperatura, ventas, edad, categoría, etc.)

### Tipos de variables (muy importante)
- **Numéricas**: se pueden operar (suma, promedio) → `float`, `int`
- **Categóricas**: etiquetas → “rojo”, “azul”, “norte”, “sur”
- **Booleanas**: verdadero/falso → `True`, `False`

> En ML llamamos **features** a las columnas que usamos para predecir y **target** a la columna que queremos predecir.

---

## 0.3 Pandas esencial para ML

Pandas te permite tratar datos como Excel, pero con el poder de Python.

### Lo mínimo que deben dominar
- Cargar datos (CSV) y ver estructura:
  - `df.head()`, `df.shape`, `df.info()`
- Estadísticas rápidas:
  - `df.describe()`
- Selección de columnas:
  - `df["columna"]`, `df[["col1","col2"]]`
- Filtrado con condiciones:
  - `df[df["col"] > valor]`
- Ordenar:
  - `df.sort_values("col")`

### Micro-actividad sugerida
Entregar un dataset pequeño (ventas, clima, sensores) y pedir:
1. Mostrar las primeras 5 filas (`head`)
2. Encontrar el promedio de una columna
3. Filtrar filas (ej. ventas > cierto valor)
4. Ordenar por una columna

---

## 0.4 Numpy básico

La mayoría de librerías de ML internamente trabajan con **vectores** y **matrices**.  
Numpy hace eso eficiente.

### Conceptos clave
- `np.array([...])`: convertir lista en array
- Operaciones rápidas (sin bucles):
  - sumar, multiplicar, promedio

### Intuición
- Un **vector** es como una lista numérica optimizada
- Una **matriz** es como una tabla numérica

---

## 0.5 Visualización mínima

Antes de ML, conviene aprender a ver tendencias:

- `scatter plot` (relación entre dos variables)
- `histograma` (distribución)
- `línea` (evolución temporal)

### Por qué importa
- Te ayuda a detectar errores
- Te ayuda a entender si hay relación entre variables
- Te prepara para interpretar predicciones luego

---

## 0.6 Flujo general de un proyecto de ML (pipeline mental)

Antes de entrenar modelos, es clave que el grupo tenga un mapa mental:

1. **Definir el problema** (¿qué quiero predecir o descubrir?)
2. **Conseguir/crear el dataset**
3. **Explorar y limpiar datos** (nulos, duplicados, tipos)
4. **Definir features (X) y target (y)**
5. **Dividir datos**: entrenamiento y prueba
6. **Entrenamiento de un modelo**
7. **Evaluación del modelo**
8. **Mejorar / repetir**
9. **Usar el modelo para predecir**



---

## Actividad final (10–15 min)

### “Checklist de preparación”
Antes de pasar a Machine Learning, cada docente debe poder responder:

- ¿Qué es una fila y qué es una columna?
- ¿Qué es una feature? ¿Qué es el target?
- ¿Cómo veo si un dataset tiene valores faltantes?
- ¿Cómo filtro un DataFrame?
- ¿Qué hace `train_test_split` (aunque aún no lo usemos a fondo)?

---

## Cierre y conexión con el curso

En el **Módulo 1** definiremos ML y los tipos de aprendizaje.  
En el **Módulo 2** practicaremos preparación de datos con más detalle.  
Luego iniciaremos el primer modelo real: **Regresión Lineal**.

✅ Si esta unidad queda clara, el resto del curso se siente mucho más fácil.
