# 📊 Análisis de Evasión de Clientes (Churn Analysis)

## 📑 Índice
1. [📖 descripción](#1-descripción)
2. [🎯 Objetivo](#2-objetivo)
3. [📊 Principales Hallazgos](#3-principales-hallazgos)
4. [🛠️ Tratamiento de Datos](#4-tratamiento-de-datos)
5. [📈 Visualizaciones Clave](#5-visualizaciones-clave)
6. [💡 Recomendaciones Estratégicas](#6-recomendaciones-estratégicas)
7. [🚀 Tecnologías Utilizadas](#7-tecnologías-utilizadas)
8. [✨ Autor](#8-autor)

---

## ## 1. 📖 Descripción
Este proyecto realiza un análisis exploratorio y estadístico sobre la pérdida de clientes en una empresa de servicios. Utilizando Python, se han identificado patrones de comportamiento, perfiles de servicio y el impacto financiero que representa la deserción para la organización.

## ## 2. 🎯 Objetivo
Identificar los factores determinantes que llevan a un cliente a cancelar su servicio y cuantificar el valor económico de dicha pérdida para priorizar estrategias de retención.

## ## 3. 📊 Principales Hallazgos
* **Sensibilidad al Precio:** Los clientes que abandonan la empresa tienen cargos mensuales significativamente más altos que los clientes leales.
* **Segmento Crítico:** Existe una fuga de valor concentrada (12.5%) en el rango de facturación de $900 - $1000 anuales.
* **Anclas de Lealtad:** Los clientes con servicios básicos (sin internet) y contratos de 2 años muestran la mayor tasa de permanencia.

## ## 4. 🛠️ Tratamiento de Datos
El análisis incluyó procesos avanzados de ingeniería de características:
* **Clasificación Desagregada:** Segmentación de usuarios en perfiles como *Solo Internet*, *Streaming TV*, *Streaming Movie* y *Ambos Streaming*.
* **Proyección Financiera:** Cálculo de la métrica `AnnualCharges` ($$Cargos\_Mensuales \times 12$$).
* **Limpieza:** Tratamiento de nulos y estandarización de variables categóricas.

## ## 5. 📈 Visualizaciones Clave

### ### Distribución de Facturación Anual

*Este gráfico muestra cómo los clientes en fuga se desplazan hacia rangos de precios más elevados.*

### ### Permanencia por Perfil de Servicio

*Comparativa de cuántos meses duran los clientes antes de irse según los servicios contratados.*

## ## 6. 💡 Recomendaciones Estratégicas
* **Fidelización Preventiva:** Crear alertas para clientes con facturaciones superiores a la mediana que no tengan servicios de streaming.
* **Promociones Dirigidas:** Enfocar campañas de retención en el segmento de valor medio ($900 anuales).
* **Estrategia de Contratos:** Incentivar el paso de contratos "Mes a mes" a contratos de "2 años" mediante bonificaciones en servicios de valor agregado.

## ## 7. 🚀 Tecnologías Utilizadas
* **Python** (Pandas, NumPy)
* **Visualización:** Matplotlib y Seaborn
* **Entorno:** Jupyter Notebook / Google Colab

## ## 8. ✨ Autor
**Tu Nombre** [LinkedIn](TU_URL_DE_LINKEDIN) | [GitHub](TU_URL_DE_GITHUB)
