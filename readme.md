# Tutorial de Machine Learning

Este repositorio contiene un tutorial completo para aprender los fundamentos de Machine Learning, diseñado para estudiantes y profesionales que desean adentrarse en el mundo del aprendizaje automático.

## 📋 Tabla de Contenidos

- [Descripción](#descripción)
- [Requisitos Previos](#requisitos-previos)
- [Instalación](#instalación)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Temas Cubiertos](#temas-cubiertos)
- [Uso](#uso)
- [Ejemplos](#ejemplos)
- [Recursos Adicionales](#recursos-adicionales)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## 📖 Descripción

Este tutorial proporciona una introducción práctica a Machine Learning utilizando Python y las bibliotecas más populares del ecosistema de ciencia de datos. A través de ejemplos prácticos y ejercicios, aprenderás los conceptos fundamentales y técnicas esenciales.

## ✅ Requisitos Previos

- Conocimientos básicos de Python
- Conceptos fundamentales de matemáticas (álgebra lineal, estadística)
- Familiaridad con Jupyter Notebooks (recomendado)

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone <url-del-repositorio>
cd 20_ML_alum
```

### 2. Crear un entorno virtual

```bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### Dependencias principales:

- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- jupyter

## 📁 Estructura del Proyecto

```
20_ML_alum/
├── data/                  # Datasets utilizados
├── notebooks/             # Jupyter notebooks con tutoriales
│   ├── 01_introduccion.ipynb
│   ├── 02_preprocesamiento.ipynb
│   ├── 03_regresion.ipynb
│   ├── 04_clasificacion.ipynb
│   └── 05_evaluacion.ipynb
├── src/                   # Código fuente reutilizable
├── models/                # Modelos entrenados guardados
├── images/                # Gráficos y visualizaciones
├── requirements.txt       # Dependencias del proyecto
└── README.md
```

## 📚 Temas Cubiertos

1. **Introducción a Machine Learning**

   - Conceptos básicos
   - Tipos de aprendizaje (supervisado, no supervisado, por refuerzo)
   - Flujo de trabajo típico

2. **Preprocesamiento de Datos**

   - Limpieza de datos
   - Manejo de valores faltantes
   - Normalización y escalado
   - Codificación de variables categóricas

3. **Algoritmos de Regresión**

   - Regresión lineal
   - Regresión polinomial
   - Regresión Ridge y Lasso

4. **Algoritmos de Clasificación**

   - Regresión logística
   - K-Nearest Neighbors (KNN)
   - Árboles de decisión
   - Random Forest
   - Support Vector Machines (SVM)

5. **Evaluación de Modelos**
   - Métricas de rendimiento
   - Validación cruzada
   - Curvas ROC y AUC
   - Matriz de confusión

## 💻 Uso

### Ejecutar los notebooks

```bash
jupyter notebook
```

Navega a la carpeta `notebooks/` y abre cualquier notebook para comenzar el tutorial.

### Ejecutar scripts de Python

```bash
python src/ejemplo.py
```

## 🔍 Ejemplos

### Ejemplo de Regresión Lineal

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

# Cargar y dividir datos
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Crear y entrenar modelo
model = LinearRegression()
model.fit(X_train, y_train)

# Realizar predicciones
predictions = model.predict(X_test)
```

### Ejemplo de Clasificación

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score

# Crear y entrenar modelo
clf = RandomForestClassifier(n_estimators=100)
clf.fit(X_train, y_train)

# Evaluar modelo
y_pred = clf.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Precisión: {accuracy:.2f}")
```

## 📖 Recursos Adicionales

- [Documentación de Scikit-learn](https://scikit-learn.org/)
- [Kaggle - Competiciones y Datasets](https://www.kaggle.com/)
- [Curso de Machine Learning de Andrew Ng](https://www.coursera.org/learn/machine-learning)
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/NuevaCaracteristica`)
3. Commit tus cambios (`git commit -m 'Añadir nueva característica'`)
4. Push a la rama (`git push origin feature/NuevaCaracteristica`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👨‍🏫 Autor

Michel - UP2025

---

⭐ Si este tutorial te fue útil, no olvides darle una estrella al repositorio
