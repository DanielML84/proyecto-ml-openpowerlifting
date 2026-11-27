# Predicción del total levantado en powerlifting (OpenPowerlifting)

Proyecto completo de Machine Learning del Máster de FP en Inteligencia Artificial y Big Data (CPIFP Alan Turing).

**Autor:** Daniel Meléndez Loreto

## De qué trata

El powerlifting es un deporte de fuerza en el que cada persona hace tres levantamientos: sentadilla, press de banca y peso muerto. En cada uno cuenta su mejor intento, y la suma de los tres da el **total** (`TotalKg`).

El proyecto intenta responder a una pregunta: **¿se puede predecir el total que va a levantar una persona usando solo datos que se conocen antes de competir?** (sexo, edad, peso corporal, equipación, federación, país, año y control antidopaje).

## Datos

[OpenPowerlifting](https://www.openpowerlifting.org): dataset público con unas 4 millones de filas de resultados reales de competiciones y 42 columnas (CSV del 2026-11-07). Se trabaja con 2.716.528 filas: las competiciones de tres levantamientos con total válido.

El dataset no está en este repositorio por su tamaño.

## Contenido del cuaderno

1. Obtención de los datos
2. Descripción de los atributos
3. Exploración y visualización (nulos, correlaciones, gráficos)
4. Objetivo y variable a predecir
5. Preparación de los datos (edades, reparto por levantador, escalado y codificación)
6. Entrenamiento y evaluación de modelos (línea base, regresión lineal, árbol, random forest y gradient boosting; validación cruzada y ajuste de hiperparámetros)
7. Conclusiones

## Resultados

Error en kilos (RMSE) en el conjunto de prueba, separado por levantador:

- Predecir la media (línea base): 168,3 kg
- Regresión lineal: 96,0 kg
- Árbol de decisión limitado: 86,0 kg
- Random forest: 83,0 kg
- **Gradient boosting ajustado: 79,5 kg (R² 0,777)**

El modelo reduce el error un 53 % frente a predecir la media y capta bien las tendencias generales, pero con estos datos no es lo bastante preciso para predecir a una persona concreta.

## Enlaces

- Cuaderno en Colab: (https://colab.research.google.com/drive/1de1dRxjK4BGV53r3mOWJIzdXAtAlEMRn)
- Vídeo explicativo:  https://youtu.be/gDZUEGEjIj8

## Nota

El cuaderno se ve con todas las salidas ya guardadas. Si se quiere ejecutar, las rutas apuntan a una carpeta de Google Drive propia y habría que cambiarlas.
