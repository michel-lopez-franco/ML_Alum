# ¿Qué es One-Hot Encoding?

**One-Hot Encoding** es una técnica de preprocesamiento de datos utilizada en machine learning para convertir variables categóricas en un formato numérico que los algoritmos de machine learning puedan entender.

Las variables categóricas son aquellas que representan etiquetas o categorías, como "país" (México, Canadá, EUA) o "color" (Rojo, Verde, Azul). Los modelos de machine learning, en su mayoría, requieren que los datos de entrada sean numéricos.

## ¿Cómo funciona?

El proceso de One-Hot Encoding consiste en los siguientes pasos:

1.  **Crear una nueva columna binaria (0 o 1) para cada categoría única** en la variable original.
2.  Para cada fila de datos, **se asigna un `1` en la columna correspondiente a su categoría y un `0` en todas las demás columnas nuevas**.

## Ejemplo

Supongamos que tenemos un conjunto de datos con una variable categórica "Ciudad":

| Ciudad    |
| --------- |
| Madrid    |
| Barcelona |
| Valencia  |
| Madrid    |

Después de aplicar One-Hot Encoding, el resultado sería:

| Ciudad_Madrid | Ciudad_Barcelona | Ciudad_Valencia |
| ------------- | ---------------- | --------------- |
| 1             | 0                | 0               |
| 0             | 1                | 0               |
| 0             | 0                | 1               |
| 1             | 0                | 0               |

Cada ciudad tiene ahora su propia columna, y solo una de estas columnas puede ser "caliente" (hot), es decir, tener el valor `1` en cada fila.

## ¿Por qué usar One-Hot Encoding?

- **Evita la relación ordinal falsa:** Si simplemente asignáramos números a las categorías (ej. Madrid=1, Barcelona=2, Valencia=3), el modelo podría interpretar erróneamente que hay una relación de orden o jerarquía entre ellas (ej. que Valencia > Barcelona), lo cual no es cierto. One-Hot Encoding trata a todas las categorías por igual.
- **Compatibilidad con modelos:** Permite que los algoritmos que solo trabajan con datos numéricos puedan procesar variables categóricas.

## Desventajas

- **Maldición de la dimensionalidad (Curse of Dimensionality):** Si una variable categórica tiene muchas categorías únicas (por ejemplo, cientos de ciudades), se crearán muchas columnas nuevas, lo que puede hacer que el conjunto de datos sea muy grande y disperso (con muchos ceros). Esto puede afectar el rendimiento de algunos modelos.

En resumen, One-Hot Encoding es una técnica fundamental para manejar datos categóricos en la preparación de datos para modelos de machine learning.
