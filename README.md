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
<img width="638" height="590" alt="image" src="https://github.com/user-attachments/assets/7462b559-2f8c-4884-b6ca-db57d0a9ab37" />




## Recomendaciones Estratégicas
Propuestas basadas en los datos obtenidos...

## Tecnologías Utilizadas
* Python, Pandas, Seaborn.

## Autor
[Tu Nombre](Tu-Link)
