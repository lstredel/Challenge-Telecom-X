# 📊 Análisis de Evasión de Clientes (Churn Analysis)

## 📑 Índice
1. [Descripción](#descripción)
2. [Objetivo](#objetivo)
3. [Principales Hallazgos](#principales-hallazgos)
4. [Tratamiento de Datos](#tratamiento-de-datos)
5. [Visualizaciones Clave](#visualizaciones-clave)
6. [Recomendaciones Estratégicas](#recomendaciones-estratégicas)
7. [Tecnologías Utilizadas](#tecnologías-utilizadas)
8. [Autor](#autor)

---

## Descripción
Challenger Telecom X - Análisis de Evasión de Clientes

He sido contratado como asistente de análisis de datos en Telecom X y formare parte del proyecto "Churn de Clientes". 

La empresa contratista enfrenta una alta tasa de cancelaciones y necesita comprender los factores que llevan a la pérdida de clientes.

Mi desafío será recopilar, procesar y analizar los datos, utilizando Python y sus principales bibliotecas para extraer información valiosa. 

A partir de mi análisis, el equipo de Data Science podrá avanzar en modelos predictivos y desarrollar estrategias para reducir la evasión.

¿Qué voy a practicar?

✅ Importar y manipular datos desde una API de manera eficiente.
✅ Aplicar los conceptos de ETL (Extracción, Transformación y Carga) en la preparación de los datos.
✅ Crear visualizaciones estratégicas para identificar patrones y tendencias.
✅ Realizar un Análisis Exploratorio de Datos (EDA) y generar un informe con insights relevantes.

¡Ahora es mi turno! de usar mis conocimientos obtendos a traves de los cursos de Alura para transformar datos en información estratégica y ayudar a Telecom X a retener más clientes.

## Objetivo

Mi objetivo central de este análisis es identificar los factores determinantes de la deserción de clientes, para transformar datos crudos en estrategias de retención accionables.

A través de este estudio buscamos:

Cuantificar el riesgo financiero: Determinar cuánto dinero pierde la compañía mensualmente por la desercion de clientes de alto valor.

Perfilamiento de Usuario: Clasificar a los clientes según su ecosistema de servicios (Internet, Streaming, Telefonía) para entender qué combinación es más propensa al abandono.

Detección de Anomalías de Precio: Identificar si existen rangos de facturación específicos donde la probabilidad de desercion se dispara.

Optimización de Contratos: Evaluar el impacto de la duración de los contratos en la lealtad del cliente para proponer cambios en la política comercial.

## Principales Hallazgos

Se detectó un patrón crítico de deserción temprana significativa antes de superar los primeros 10 meses de antigüedad.

El "Umbral Crítico" de Facturación: Se identificó un punto de fuga masivo en clientes que pagan entre $70 y $90 dólares mensuales. Específicamente, el 12.5% de la deserción total se concentra en usuarios con una facturación anual proyectada de $900 a $1000. Esto indica que los clientes de valor medio son los más sensibles al precio.

El análisis financiero proyectado a un año revela una pérdida total de $528,374 en ingresos brutos. Esta cifra no se distribuye de manera uniforme, sino que está fuertemente ligada al tipo de ecosistema de servicios contratado por el cliente, siendo los contratos de Solo Internet la de mayor impacto con 49,5% seguido del servicio de Ambos Streaming con 19,3%.

Correlación entre Costo y Abandono: A través de los diagramas de caja (Boxplots), confirmamos que la mediana de los cargos mensuales de los clientes que se van es significativamente más alta que la de los clientes que permanecen. El precio no es solo un factor, es el principal detonante de la fuga.

El Efecto "Ancla" de los Servicios Básicos: Los clientes con servicio de telefonía básica presentan los niveles de lealtad más altos. Esto sugiere que a mayor complejidad del paquete tecnológico (fibra óptica, múltiples streamings), mayor es la volatilidad del cliente.

Vulnerabilidad del Contrato Mensual: La gran mayoría de las bajas ocurren en el modelo de contrato "Month-to-month". Los clientes con contratos a 1 o 2 años muestran una resistencia casi total a la deserción, independientemente del precio que paguen, lo que resalta la importancia de la estructura del contrato sobre la satisfacción del servicio.

## Tratamiento de Datos
1. Estandarización de Variables Conversión de Tipos:
   Se transformaron variables categóricas críticas (como TotalCharges) a formato numérico, gestionando errores de datos faltantes o espacios en blanco que suelen sesgar los resultados.
   Proyección Financiera: Se creó la métrica "AnnualCharges" ($$MonthlyCharges \times 12$$) para cuantificar el impacto económico a largo plazo, permitiendo pasar de un análisis de "clientes perdidos" a uno de "capital fugado".

2. Segmentación de Perfiles de Servicio
   Para evitar un análisis genérico, se desarrolló una lógica de clasificación personalizada que agrupó a los clientes según su ecosistema tecnológico:
     Lógica de Agrupación: Se consolidaron las variables de StreamingTV e StreamingMovies junto con el tipo de conexión a internet.
     Perfiles Creados: * Sin Internet: Clientes tradicionales.Solo Internet: Usuarios de conectividad básica.Streaming TV / Movie: Usuarios de contenido específico.Ambos Streaming: Clientes de alto valor y alta demanda.

3. Tratamiento del Horizonte Temporal
   Métrica de Tenure: Se segmentó la antigüedad de los clientes para identificar el "Punto de Quiebre de los 10 Meses", permitiendo analizar la deserción no como un evento aislado, sino como un ciclo de vida con etapas de riesgo definidas.
   
## Visualizaciones Clave
<img width="990" height="848" alt="image" src="https://github.com/user-attachments/assets/0aa4d163-294a-43b6-9d6e-6cc402a1c5b1" />
<img width="1783" height="684" alt="image" src="https://github.com/user-attachments/assets/5a2ef5cd-4c6b-446c-869b-811089795ad9" />
<img width="1784" height="794" alt="image" src="https://github.com/user-attachments/assets/4f403940-6bf6-48b5-a06e-73926047b2f3" />
<img width="1384" height="684" alt="image" src="https://github.com/user-attachments/assets/672c8c88-e550-4492-b4e3-ccf24340259f" />
<img width="1184" height="684" alt="image" src="https://github.com/user-attachments/assets/088e03b3-d48d-422a-ab1f-692c04a796c5" />
<img width="982" height="899" alt="image" src="https://github.com/user-attachments/assets/f0df1f8c-b13e-4d1e-a697-55564d5a2140" />
<img width="1384" height="684" alt="image" src="https://github.com/user-attachments/assets/157664ca-b969-47d5-8c91-cd7746ce06f0" />
<img width="984" height="583" alt="image" src="https://github.com/user-attachments/assets/95640f6c-46a3-4831-a50a-1785b902243b" />












## Recomendaciones Estratégicas

1. Programa de Fidelización

Acción: Implementar una campaña de contacto proactivo y beneficios exclusivos en el mes 9 de antigüedad.

Objetivo: Romper la barrera de deserción de los 10 meses y asegurar la transición del cliente hacia el segmento de lealtad a largo plazo (donde la probabilidad de fuga cae un 40%).

2. Blindaje del Segmento de Alto Valor (Streaming)

Acción: Crear paquetes de retención específicos para el perfil "Ambos Streaming", quienes representan el 38% de la pérdida anual.

Objetivo: Ofrecer descuentos por permanencia o "upgrades" de servicio a este grupo, ya que recuperar a un solo cliente de este segmento tiene un impacto financiero 4 veces mayor que en los segmentos básicos.

3. Incentivos de Migración Contractual

Acción: Diseñar una estrategia de conversión con promociones de descuentos, para mover a los clientes con contratos "Mes a Mes" hacia contratos de 1 o 2 años.

Objetivo: Reducir la volatilidad. Los datos demuestran que el compromiso contractual es el predictor más fuerte de permanencia, independientemente del costo del servicio.

4. Rebalanceo de Precios en el Umbral Crítico

Acción: Revisar la oferta comercial para el rango de facturación de $70 - $90 mensuales.

Objetivo: Introducir servicios de valor agregado (sin costo adicional para la empresa) que aumenten la percepción de valor en este "punto de quiebre" donde el cliente se vuelve más sensible al precio

## Tecnologías Utilizadas

Python 3.x: Lenguaje base para el procesamiento de lógica y manipulación de datos.

Pandas: Biblioteca principal utilizada para la limpieza, transformación y creación de las métricas financieras (como la proyección anual de pérdidas).

NumPy: Utilizada para operaciones matemáticas eficientes y manejo de vectores en la segmentación de perfiles.

Matplotlib: Empleada para la creación de la arquitectura base de los gráficos y control detallado de los ejes de visualización.

Seaborn: Biblioteca de visualización estadística utilizada para generar los diagramas de caja (Boxplots) y los mapas de calor (Heatmaps) que revelaron la sensibilidad al precio.

Google Colab: Entornos de desarrollo interactivos que permitieron la experimentación rápida y la documentación del código paso a paso.

## Autor
Lisber Stredel
Contador Auditor y Proximo Data Science
https://www.linkedin.com/in/lisber-stredel-nu%C3%B1ez-67975715/

