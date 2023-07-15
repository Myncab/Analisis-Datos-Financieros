# Análisis-Datos-Financieros-Edutek

Fuentes de Datos utilizados:
- JSON ( GASTOS DE VENTA )
- SQL ( VENTAS ) [dbo].[PJ_MYNORC]
- SNOSFLAKE ( GASTOS OPERATIVOS )
- EXCEL (POWER QUERY)

Resumen:
El objetivo de este proyecto es aprovechar el poder del análisis de datos para mejorar la eficiencia operativa y respaldar la toma de decisiones estratégicas en la empresa el pato azul. Mediante el análisis de conjuntos de datos internos financieros relevantes, se busca identificar patrones, tendencias y relaciones ocultas que puedan proporcionar información valiosa para mejorar la eficiencia, optimizar los procesos y brindar una ventaja competitiva.

Objetivos del Proyecto:

1.	Recopilar, limpiar y estructurar los datos relevantes disponibles en la empresa, incluyendo fuentes internas y externas pertinentes.
2.	Realizar un análisis exploratorio de los datos para identificar patrones, correlaciones y tendencias significativas.
3.	Diseñar paneles interactivos y visualizaciones claras para presentar los resultados del análisis de manera comprensible y accesible para los diferentes equipos y niveles de la organización.
4.	Realizar el estado de resultados financieros del 01 de enero al 31 de diciembre del 2020
5.	Proponer recomendaciones concretas basadas en los resultados del análisis para mejorar la eficiencia operativa, reducir costos, optimizar los recursos y respaldar la toma de decisiones estratégicas.

Entregables Esperados:

1.	Un conjunto de datos limpios, estructurados y preparados para el análisis en excel.
2.	Informes y visualizaciones que presenten los hallazgos y recomendaciones de manera clara y concisa que respondan las siguientes preguntas;
a.	El top 5 de costos de venta más elevados
    2	Bonificaciones de ventas	2,083.00	31/01/2020
    9	Bonificaciones de ventas	2,083.00	28/01/2020
    16	Bonificaciones de ventas	2,083.00	31/03/2020
    23	Bonificaciones de ventas	2,083.00	30/04/2020
    30	Bonificaciones de ventas	2,083.00	31/05/2020
b.	Top 10 de gastos Operativos 
    6	Gastos de tecnología y comunicación incluyendo servicios de Internet telefonía y software	120000
    12	Gastos de almacenamiento y logística	110000
    1	Salarios y beneficios de los empleados	85000
    15	Depreciación de activos fijos	75000
    2	Alquiler o arrendamiento de espacio comercial u oficinas	65000
    4	Gastos de mantenimiento y reparaciones de instalaciones	50000
    8	Honorarios profesionales como asesores legales y contables	50000
    5	Suministros de oficina y consumibles	40000
    14	Gastos de mantenimiento y reparación de equipos	35000
    10	Costos de seguros como seguros generales o de responsabilidad civil	25000
c.	Que 5 meses son en los que más se vendieron. 
    4	197,747.32
    7	190,748.21
    3	160,428.57
    1	158,694.64
    9	147,217.86
 
d.	Que 2 meses son en los que menos se vendieron.
    5	91,202.68
    12	1,760.71
 
3.	Estado de resultados.
4.	Recomendaciones concretas y accionables para mejorar la eficiencia operativa y respaldar la toma de decisiones.
    Se tiene que hacer promociones para que los meses mas bajos que son mayo y diciembre pueda vender mas y rotar así el inventario.

Para elaborar el estado de resultado necesitamos poder llegar a obtener la utilidad neta sin llegar a algo mas detallado guiarse por el siguiente cuadro

VENTAS	SUM(VENTAS)	1,543,405.36
COSTO VENTAS	SUM(COSTO VENTAS)	132,972.00
UTILIDAD BRUTA	VENTAS-COSTO DE VENTAS	1,410,433.36
GASTOS OPERATIVOS	SUM(GASTOS OPERATIVOS)	734,000.00
UTILIDAD OPERACIONAL	UTILIDAD BRUTA - GASTOS OPERATIVOS	676,433.36
ISR 1 TRIMESTRE	SUM(ENE,FEB,MAR) *0.28	122,716.75
ISR 2 TRIMESTRE	SUM(ABR,MAY,JUN) *0.28	111,562.50
ISR 3 TRIMESTRE	SUM(JUL,AGO,SEP) *0.28	127,438.25
ISR 4 TRIMESTRE	SUM(OCT,NOV,DIC) *0.28	70,436.00
UTILIDAD NETA	UTILIDAD OPERACIONAL - ISR TRIMESTRE 1,2,3,4	244,279.86

 
Para la parte de los datos transaccionales el caso del archivo en classroom llamado PJ utilizar el usuario analista de datos cargado tambien en classrrom para poder carga ese archivo plano en sql favor de llamar a su tabla PJ_(PRIMER NOMBRE)(LETRA INICIAL DE PRIMER APELLIDO) ejemplo PJ_EDERC PJ_MYNORC

Notas importantes:

En caso de encontrar outliers en los datos, aislarlos y presentar sus interpretaciones de porque se pudieron generar esos datados
Las fechas no son válidas para estos registros:

no_factura	Nombre_del_cliente	Dirección	Total_con_iva	Tienda	Fecha
A17867	Mary Davis	456 Elm Avenue	50.00	Tienda B	35/5/2020
A17868	Christopher Brown	789 Oak Lane	75.00	Tienda A	37/3/2020
A17919	Ava Wilson	249 Walnut Street	146.00	Tienda B	30/2/2020
A17945	Jennifer Lee	789 Oak Lane	34.00	Tienda B	31/11/2020
A18083	Ava Wilson	249 Walnut Street	426.00	Tienda B	31/4/2020
A18213	Ava Wilson	249 Walnut Street	14,139.00	Tienda B	31/4/2020
