# Sistema Inteligente de Detección de Phishing en Correos Electrónicos

**Trabajo Fin de Grado — Grado en Ingeniería Informática**  
**Universidad de Alicante — Escuela Politécnica Superior**  
**Autor:** José Manuel Martínez Giganto  
**Tutora:** Patricia Compañ Rosique  
**Curso:** 2025-2026  

---

## Descripción

Sistema de detección de phishing en correos electrónicos basado en el ajuste fino 
(*fine-tuning*) de **DistilBERT Multilingual** sobre un corpus unificado de 38.630 
correos electrónicos, complementado con un módulo de explicabilidad **LIME** y una 
interfaz interactiva desarrollada con **Gradio**.

---

## Resultados principales

| Modelo | F1-score | ROC-AUC | FPR |
|--------|----------|---------|-----|
| Logistic Regression (baseline) | 0,9852 | 0,9986 | 0,0152 |
| Random Forest (baseline) | 0,9782 | 0,9978 | 0,0231 |
| XGBoost (baseline) | 0,9744 | 0,9973 | 0,0320 |
| **DistilBERT Multilingual** | **0,9850** | **0,9991** | **0,0058** |

---

## Contenido del repositorio

| Archivo | Descripción |
|---------|-------------|
| `TFG_Phishing_JoseManuel_Martinez_Giganto.ipynb` | Notebook principal: preprocesado, baseline, fine-tuning, LIME y demo |

---

## Datasets utilizados

Fuente: [Phishing Email Curated Datasets](https://zenodo.org/records/15882) 
(Champa et al., 2023), Zenodo.

| Dataset | Muestras | Legítimos | Phishing |
|---------|----------|-----------|----------|
| Enron.csv | 29.756 | 15.788 | 13.968 |
| SpamAssassin.csv | 5.809 | 4.091 | 1.718 |
| Nazario_5.csv | 3.065 | 1.500 | 1.565 |
| **Total** | **38.630** | **21.379** | **17.251** |

---

## Tecnologías

- Python 3.12 · PyTorch · Hugging Face Transformers
- DistilBERT Multilingual (`distilbert-base-multilingual-cased`)
- LIME · Gradio · scikit-learn · XGBoost
- Google Colab (GPU NVIDIA Tesla T4)

---

## Cómo ejecutar

1. Abre el notebook en Google Colab haciendo clic en el badge:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TU_USUARIO/TFG-Phishing-Detection/blob/main/TFG_Phishing_JoseManuel_Martinez_Giganto.ipynb)

2. Ejecuta las celdas en orden.
3. Los modelos entrenados se guardan automáticamente en Google Drive.
