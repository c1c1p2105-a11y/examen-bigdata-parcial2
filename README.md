# Examen Práctico 2do Parcial — Tópicos de Big Data (Versión A)

**Alumno:** Cristiano Ronaldo Garnica Zúñiga · **Grupo:** 511 · **Fecha:** 26/10/2026

Clustering con **K-Means** de viajes de taxi de Nueva York pagados en efectivo (`Cash`), usando `trip_distance` y `trip_duration`.

## Estructura
```text
Examen_A/
├── notebooks/
│   └── Examen_A_Garnica_Zuniga_Cristiano_Ronaldo.ipynb
└── data/
    └── raw/
        ├── nyc_taxi_examen_csv.zip.001
        ├── nyc_taxi_examen_csv.zip.002
        └── nyc_taxi_examen_csv.zip.003   (partes del zip del dataset)
```

## Cómo ejecutar
El CSV pesa ~310 MB, por eso se incluye su `.zip` dividido en 3 partes de máx. 20 MB. Antes de ejecutar el notebook, únelas y descomprime en `Examen_A/data/raw/`:

- **Windows (CMD):**
```bat
cd Examen_A\data\raw
copy /b nyc_taxi_examen_csv.zip.001+nyc_taxi_examen_csv.zip.002+nyc_taxi_examen_csv.zip.003 nyc_taxi_examen_csv.zip
```
  Luego clic derecho en `nyc_taxi_examen_csv.zip` → *Extraer aquí*. (Con 7-Zip también basta abrir el `.001`.)
- **Linux / macOS:**
```bash
cd Examen_A/data/raw
cat nyc_taxi_examen_csv.zip.0* > nyc_taxi_examen_csv.zip && unzip nyc_taxi_examen_csv.zip
```

Después abre el notebook desde `Examen_A/notebooks/` y ejecuta todas las celdas (lee `../data/raw/nyc_taxi_examen.csv`).

Requisitos: Python 3, pandas, numpy, matplotlib, scikit-learn.

## Resultados (k = 3)
| Clúster | Tipo de viaje | Viajes | Distancia media (mi) | Duración media (min) |
|---|---|---|---|---|
| 2 | Cortos | 94,169 | 0.80 | 5.72 |
| 1 | Urbanos medianos | 125,521 | 2.30 | 15.43 |
| 0 | Largos / aeropuerto | 62,395 | 11.55 | 39.48 |
