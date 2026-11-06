# Actividad 2.10 — Clustering con K-means y jerárquico

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/h0ndv/lab-2.10-clustering/blob/main/lab_2_10_clustering.ipynb)

**Minería de Datos IEI097 · Unidad II · Laboratorio**  
**Estudiante:** Sebastián

## Descripción

Notebook de Google Colab con dos ejercicios de clustering:

- **K-means** sobre el dataset Mall Customers (`vjchoudhary7/customer-segmentation-tutorial-in-python`), con hipótesis inicial, EDA, estandarización, búsqueda de `k`, estabilidad, comparación con y sin escala, perfiles y acciones por segmento.
- **Clustering jerárquico** sobre Country Data (`rohan0301/unsupervised-learning-on-country-data`), con un subconjunto de 27 países que incluye Chile, dendrogramas con los enlaces `single`, `complete`, `average` y `ward`, corte justificado y comparación con K-means.

## Resultados principales

- K-means: `k = 5`, silueta 0,555; cinco segmentos con nombre y acción de comunicación.
- La partición fue idéntica con y sin estandarización (ARI = 1,0), porque las dos variables tienen rangos comparables.
- Jerárquico: 27 países, enlace `ward`, corte en 3 grupos.
- Chile se agrupa con Argentina, Brasil, Colombia, Costa Rica, Ecuador, Perú, Uruguay, Venezuela y China.
- K-means y Ward coinciden completamente en el subconjunto (ARI = 1,0).

## Cómo ejecutar

1. Abrir el notebook con el badge de Colab.
2. Agregar el token de Kaggle en **Secrets** con el nombre `KAGGLE_API_TOKEN`, o usar `KAGGLE_USERNAME` y `KAGGLE_KEY` con las credenciales clásicas.
3. Ejecutar `Runtime → Restart and run all`.

El token no se escribe en el código: se lee desde Colab Secrets. Si no hay Secrets, `kagglehub` usa el acceso anónimo a los datasets públicos.

## Datasets

- **Mall Customers:** 200 clientes, columnas `CustomerID`, `Gender`, `Age`, `Annual Income (k$)` y `Spending Score (1-100)`.
- **Country Data:** 167 países y 10 indicadores socioeconómicos y de salud.

## Reproducibilidad

El notebook fija `random_state = 42` y usa `n_init = 10` en K-means.

## Contenido

| Archivo | Descripción |
|---|---|
| `lab_2_10_clustering.ipynb` | Notebook ejecutado con las salidas y figuras |
| `README.md` | Este documento |
