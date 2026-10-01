# Continuación del proyecto de Data Science 1

Mateo Sapia, comisión 102390. Archivos preparados el 30/09–01/10/2026, antes de la apertura del campus. **No están entregados**: los formularios de estas instancias aún no están habilitados.

| Entrega | Archivo | Apertura indicada en campus |
|---|---|---|
| 4: EDA visual | `Sapia_Mateo_Preentrega4_EDA_Visual.pdf` | 14/10, 09:30 |
| 5: TechWorld | `Sapia_Mateo_Preentrega5_TechWorld.pdf` | 21/10, 09:30 |
| 6: Oportunidad ML | `Sapia_Mateo_Preentrega6_OportunidadML.pdf` | 28/10, 09:30 |
| 7: Comparación | `Sapia_Mateo_Preentrega7_Evaluacion.pdf` | 04/11, 09:30 |
| 8: Clustering | `Sapia_Mateo_Preentrega8_Clustering.pdf` | 11/11, 09:30 |
| 9: Solución ML | `Sapia_Mateo_Preentrega9_SolucionML.pdf` | 18/11, 09:30 |
| Final | `Sapia_Mateo_Final.ipynb` | 18/11, 10:00 |

Horarios tal como aparecen en la sesión del campus. Las consignas 5, 6, 8 y 9 son ejercicios conceptuales; no se inventaron datos ni ejecuciones. Las preentregas 4 y 7 usan cálculos reales del notebook final.

## Reproducir

Clonar la rama `continuacion-proyecto`, crear un entorno con Python 3.12 e instalar `requirements.txt`. Abrir el notebook desde esta carpeta y ejecutar todas las celdas en orden. Las dependencias de análisis están fijadas; instalar `jupyterlab` adicionalmente si se desea ese editor. Ejecución por terminal:

```bash
python -m jupyter nbconvert --execute --to notebook --inplace Sapia_Mateo_Final.ipynb --ExecutePreprocessor.timeout=600
```

El notebook se ejecutó de principio a fin: 14 celdas de código sin errores, 8 figuras y resultados guardados. Incluye descarga de respaldo de UCI con comprobación SHA-256. `Sapia_Mateo_Final.html` es una vista estática con los outputs; la entrega final corresponde al enlace del `.ipynb`.

## Decisiones y evidencia

- EDA: 12.292 sesiones saneadas, 1.902 compras, como en el checkpoint anterior.
- Modelado: se retiran 125 filas exactamente repetidas; quedan 12.167 patrones. No se afirma que fueran eventos duplicados reales.
- 9.733 filas de entrenamiento y 2.434 de test, con 381 compras en test. Predictores idénticos nunca se reparten entre particiones ni entre folds.
- Imputación, escalado y codificación se ajustan en el pipeline dentro de cada fold. PageValues queda excluida.
- Random Forest fue elegido por AP media de CV (0,377 vs 0,322). En test: AP 0,378, AUC 0,778 y F1 0,429. No se promete utilidad operativa ni impacto causal.
- `resultados_final.json` y `metricas_test.csv` contienen valores exactos; las matrices de confusión reconcilian con el total de test.
- Los seis PDF se renderizaron y revisaron página por página. El HTML del notebook se inspeccionó en Chrome; tablas, resumen y figuras están presentes.

Las versiones previamente entregadas permanecen en `main`. Fuente y licencia del dataset: UCI, Sakar y Kastro (2018), DOI 10.24432/C5F88Q, CC BY 4.0.
