# Data Science 1 - Mateo Sapia

**Esta rama incluye la continuación completa. Ver [CONTINUACION.md](CONTINUACION.md) para las preentregas 4–9, el notebook final ejecutado, resultados y fechas.**

Las secciones siguientes documentan las primeras tres entregas, preservadas del trabajo previo.

Proyecto: clasificación retrospectiva de intención de compra en e-commerce.

## Entregas
- `Sapia_Mateo_Preentrega1.pdf`: contexto, pregunta, ficha y diccionario.
- `Sapia_Mateo_Preentrega2.ipynb`: ingesta, diagnóstico, def/lambda y outputs.
- `Sapia_Mateo_Checkpoint1.ipynb` y `.pdf`: notebook integral ejecutado y exportación con tres filtros y auditoría.

## Reproducir
Con Python 3.12: `pip install -r requirements.txt` y abrir los notebooks desde esta carpeta. Ejecutar todas las celdas en orden. También se pueden abrir en Google Colab: si falta el CSV, se descarga de UCI y se valida su SHA-256. Cada notebook es independiente.

## Datos y licencia
Fuente: https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset
Sakar, C. y Kastro, Y. (2018), DOI https://doi.org/10.24432/C5F88Q. Datos CC BY 4.0. Descarga: 2026-09-29.
CSV original: 12.330 filas, 18 columnas. SHA-256: `b3055ee355f59134d851d32641183cb4a8b45def7124d2f50442a042f358e0d9`.
`sesiones_saneadas.csv` es una adaptación: 38 filas excluidas por no visitar productos; se elimina PageValues. El CSV original se conserva sin modificaciones.

## Validación
Ambos notebooks ejecutados de principio a fin con nbclient. Las celdas verifican dimensiones, ausencia de nulos, reglas de negocio, conversión de unidades y reconciliación de filtros. No se entrenó un modelo en estas preentregas. No se interpreta el estudio como causal ni como medición actual.
