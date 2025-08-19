# Challenge_Alura_TelecomX_Latam_Parte-1: Telecom X - Análisis Exploratorio de Evasión de Clientes (Churn)
## Descripción del Proyecto

Telecom X es una empresa de telecomunicaciones que enfrenta un alto índice de evasión (churn) de clientes y aún no ha identificado claramente las razones de esta situación. Como analista de datos, se te ha contratado para realizar un análisis exploratorio de los datos proporcionados con el fin de descubrir posibles causas de la evasión y ofrecer insights que ayuden a la empresa a retener clientes.

El proyecto se centra en el análisis de un dataset con información demográfica, de servicios contratados y datos de facturación de clientes. El objetivo principal es entender qué factores están más relacionados con la evasión para apoyar la toma de decisiones estratégicas.

## Estructura del Proyecto

**Dependencias e Instalación**
El análisis fue desarrollado y probado en Google Colab, por lo que no se requiere instalación local si usas Colab. 
**¿Cómo Ejecutar el Análisis?**
Abre el notebook TelecomX_Churn_Analysis.ipynb en Google Colab.
Sube o monta el dataset original (si no está incluido).
Ejecuta las celdas en orden para reproducir todo el flujo:

## Limpieza y transformación de datos
- Se identificaron y trataron valores vacíos en las columnas `CargoTotal` y `Evasion`.
- Se corrigió el tipo de datos de `SeniorCitizen`, convirtiéndolo en booleano.
- Se eliminaron duplicados y se renombraron columnas para mayor claridad.
- Se creó la columna `Cuentas_Diarias` dividiendo el cargo mensual entre 30.

## Análisis descriptivo de variables cuantitativas y categóricas
- Tablas Resumenes, gráficos y tests estadísticos (chi-cuadrado)
- Interpretación de resultados y conclusiones preliminares

## Resumen de Insights 
- La mayoría de los clientes que cancelan tienen pocos meses de contrato (`MesesContrato`).
- Los clientes con contrato mensual tienen significativamente mayor propensión a la evasión que quienes tienen contratos a plazo fijo.
- Los clientes que tienen el método de pago "Electronic check" son más propensos a la evasión.
- Los cargos mensuales más altos también tienden a estar correlacionados con cancelaciones, lo cual podría indicar una baja satisfacción respecto a la relación del precio y las características del servicio adquirido.
- Los clientes sin servicios adicionales (como respaldo online y soporte técnico) presentan una mayor tasa de evasión.

## Conclusión
La evasión de clientes en TelecomX se podría explicar principalmente por una desatisfacción de los nuevos clientes con los servicios adquiridos o un descalze entre sus expectativas y la experiencia del servicio. Por ejemplo, los servicios asociados al acceso a Internet, como el servicio de fibra óptica, tienen una mayor tasa de evasión. Además, la experiencia del usuario también juego un rol importante, pues quienes si contaban con beneficios como un menor tiempor de espera en el servicio de Soporte Técnico estaban más fidelizados con la organización.

## Tests estadísticos:
- Chi-cuadrado para variables categóricas (tipo de contrato, método de pago, servicios adicionales) mostraron asociación significativa con evasión (p < 0.0001).
- Test de correlación de Pearson para variables numéricas.

## Notas Adicionales
- La limpieza de datos incluyó la revisión de valores faltantes, duplicados e inconsistencias.
- Se realizó la transformación de variables cualitativas para facilitar el análisis (p.ej., renombrado, binarización).
- Este análisis es exploratorio; para un modelo predictivo se recomienda profundizar en ingeniería de variables y modelado supervisado.
