# Reporte de Análisis del Trastorno del Sueño

## Introducción
Este reporte presenta un análisis exhaustivo de los trastornos del sueño utilizando un conjunto de datos de 374 pacientes. El objetivo principal es identificar los factores que influyen en el desarrollo de trastornos del sueño y crear un modelo predictivo para apoyar el diagnóstico.

## Metodología
El análisis se realizó utilizando Python con las siguientes bibliotecas principales:
- Pandas y NumPy para manipulación de datos
- Matplotlib, Seaborn y Plotly para visualización
- Scikit-learn para modelado predictivo

## Análisis Exploratorio de Datos

### Distribución de Trastornos por Género
![Distribución por género](https://github.com/tu_usuario/tu_repositorio/raw/main/images/gender_distribution.png)

**Hallazgos:**
- 185 mujeres y 189 hombres en el dataset
- Mayor prevalencia de apnea en mujeres (36.2% vs 5.8% en hombres)
- 72.5% de hombres sin trastorno vs 44.3% en mujeres

### Distribución por Ocupación
![Distribución por ocupación](https://github.com/tu_usuario/tu_repositorio/raw/main/images/occupation_distribution.png)

**Hallazgos:**
- Enfermeras/os: grupo más numeroso (73 casos)
- Mayor prevalencia de apnea en enfermería
- Profesores (40) y contadores (37) con patrones distintos

### Relación Edad-BMI
![Relación Edad-BMI](https://github.com/tu_usuario/tu_repositorio/raw/main/images/age_bmi_relation.png)

**Hallazgos:**
- Obesidad (BMI ≥ 30) asociada con apnea del sueño
- Insomnio más frecuente en sobrepeso
- Casos sin trastorno predominan en peso normal

### Pasos Diarios por Ocupación
![Pasos diarios](https://github.com/tu_usuario/tu_repositorio/raw/main/images/steps_heatmap.png)

**Hallazgos:**
- Enfermeras con apnea: mayor promedio de pasos (8264)
- Ingenieros de software con insomnio: menor promedio (3000)
- Relación no clara entre pasos y trastornos

## Modelo Predictivo
**Variables consideradas:**
```python
Variables numéricas:
- Edad, Duración del sueño, Calidad del sueño
- Actividad física, Estrés, Frecuencia cardíaca, Pasos diarios

Variables categóricas:
- Género, Ocupación, Categoría de BMI
```

**Resultados del modelo (Random Forest):**

| Métrica    | Valor |
|------------|-------|
| Precisión  | 92%   |
| Recall     | 89%   |
| F1-score   | 90%   |

## Conclusiones
1. El sobrepeso y obesidad son factores de riesgo significativos para apnea del sueño
2. Las ocupaciones sedentarias tienen mayor prevalencia de insomnio
3. Mayor susceptibilidad en género femenino
4. Random Forest demostró alta efectividad (90% F1-score)

## Recomendaciones
- Programas de control de peso para prevenir apnea
- Fomentar actividad física en trabajos sedentarios
- Usar modelo como herramienta de screening inicial

## Estructura del Repositorio
```
/project-root
│── /data
│   └── Sleep_health_and_lifestyle_dataset.csv
│── /notebooks
│   └── Analisis_del_Trastorno_del_sueno.ipynb
│── /images
│   ├── gender_distribution.png
│   ├── occupation_distribution.png
│   ├── age_bmi_relation.png
│   └── steps_heatmap.png
└── README.md
```

## Cómo reproducir el análisis
```bash
git clone https://github.com/tu_usuario/tu_repositorio.git
cd tu_repositorio
jupyter notebook notebooks/Analisis_del_Trastorno_del_sueno.ipynb
```

## Requisitos
- Python 3.8+
- Jupyter Notebook
- Bibliotecas: pandas, numpy, matplotlib, seaborn, plotly, scikit-learn
