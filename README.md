# PROYECTO INDIVIDUAL DATA ANALITYCS
<p align="center">
  <img src="/data/portada.webp">
</p>

## Introducción

En el mundo de la aviación, la seguridad es un tema de importancia crítica. Los accidentes aéreos, eventos imprevistos y devastadores, han sido objeto de estudio y preocupación durante más de un siglo. Estos incidentes pueden involucrar a cualquier tipo de aeronave, desde aviones comerciales hasta helicópteros, y sus consecuencias pueden ser tanto humanas como económicas.

El objetivo principal de esta iniciativa es comprender y analizar exhaustivamente los datos relacionados con estos incidentes y proporcionar herramientas visuales, como un dashboard, que enriquezcan la comprensión de estos eventos. Para llevar a cabo este análisis, la OACI (La Organización de Aviación Civil Internaciona) cuenta con un valioso conjunto de datos sobre accidentes de aviones. Sin embargo, para lograr una comprensión más profunda y completa, se ha instado a una consultora de datos a que cruce esta información con otras fuentes de interés.

## Contexto

Imagina dar un paso atrás en el tiempo y explorar los cielos del pasado. Desde los primeros vuelos de la era pionera hasta las modernas aeronaves que surcan los cielos de hoy en día, la historia de la aviación está llena de momentos de triunfo y tragedia. Cada vuelo es una hazaña de ingeniería y destreza humana, pero, lamentablemente, no todos los viajes terminan de la misma manera.

Los accidentes aéreos son un recordatorio crudo de la fragilidad de la vida y la importancia de la seguridad en la aviación.

La Organización de Aviación Civil Internacional (OACI), como guardiana de la seguridad en la aviación, se ha embarcado en una tarea monumental. Su objetivo es investigar y comprender cada accidente aéreo registrado desde principios del siglo XX. En un mundo impulsado por datos, la OACI ha recurrido a la ciencia de datos para descubrir patrones y tendencias, para aprender de los errores del pasado y garantizar un futuro más seguro en los cielos.

Este proyecto es una ventana al pasado, un análisis minucioso de incidentes que han dejado huellas indelebles en la historia de la aviación. Pero no es solo un ejercicio de retrospectiva; es un paso hacia adelante. Al cruzar estos datos con otras fuentes y presentarlos de manera accesible en un dashboard, la OACI se esfuerza por empoderar a la comunidad de la aviación con información valiosa que pueda salvar vidas y proteger valiosos activos.

En cada punto de datos, en cada gráfico, se encuentra la promesa de un futuro más seguro en los cielos. A través de esta iniciativa, la OACI se embarca en un viaje para honrar el pasado, aprender del pasado y, en última instancia, mejorar el futuro de la aviación en todo el mundo.

## Datos
Este repositorio contiene un conjunto de datos que registra accidentes de aviones desde 1908 hasta 2021. El objetivo principal del proyecto, es analizar estos datos para evaluar y sacar conclusiones acerca de los KPIs planteados. A continuación, se detalla el contenido de cada archivo en este repositorio:

- `EDA.ipynb`: Este archivo contiene el analisis exploratorio (de manera detallada) acerca del dataset proporcionado para la realización del proyecto. 
- `AccidentesAviones.csv`: Este es el archivo preliminar. De este archivo extreremos toda la información que necesitamos y sacaremos nustras conclusiones sobre los KPIs planteados.

# Análisis de Accidentes Aéreos: Exploración y Transformación

### Librerias Utilizadas
- Pandas
- Matplotlib
- Seaborn

## Exploración de Datos


Comencé este análisis de accidentes aéreos explorando las columnas disponibles en los datos. Según mi analisis esta es mi conclusión respecto a las columnas del Dataset:

- **Fecha**: La fecha en que ocurrió el accidente.
- **Hora Declarada**: La hora del vuelo declarada.
- **Lugar del Accidente**: El lugar donde ocurrió el accidente, que se confirmó leyendo los resúmenes ('summary').
- **Tipo de Vuelo**: El tipo de vuelo.
- **Identificador del Vuelo**: El número de vuelo, que sirve como identificador único.
- **Recorrido**: La ruta del vuelo, que puede incluir el destino o el recorrido planeado.
- **Modelo del Aeronave**: El tipo o modelo de la aeronave.
- **Matrícula del Aeronave**: Un registro único para cada aeronave.
- **Número de Serie**: El número de serie o construcción de la aeronave, asignado en su fabricación.
- **Personas a Bordo**: La cantidad total de personas a bordo, incluyendo tripulantes y pasajeros.
- **Pasajeros a Bordo**: La cantidad de pasajeros a bordo.
- **Tripulantes a Bordo**: La cantidad de tripulantes a bordo.
- **Cantidad de Fallecidos**: La cantidad total de personas fallecidas en el accidente.
- **Pasajeros Fallecidos**: La cantidad de pasajeros fallecidos.
- **Tripulantes Fallecidos**: La cantidad de tripulantes fallecidos.
- **Personas Afectadas (No a Bordo)**: La cantidad de personas afectadas que no estaban a bordo.
- **Informe del Siniestro**: Un resumen de lo que sucedió.

## Transformación de Datos

Realicé varias transformaciones en los datos para hacerlos más coherentes y comprensibles:

1. **Nombres de Columnas en Español**: Renombré las columnas en español para facilitar la lectura y comprensión de los datos. Aquí tienes los nuevos nombres de las columnas:

   - Fecha del Accidente
   - Hora Declarada
   - Lugar del Accidente
   - Tipo de Vuelo
   - Identificador del Vuelo
   - Recorrido
   - Modelo del Aeronave
   - Matrícula del Aeronave
   - Número de Serie
   - Personas a Bordo
   - Pasajeros a Bordo
   - Tripulantes a Bordo
   - Cantidad de Fallecidos
   - Pasajeros Fallecidos
   - Tripulantes Fallecidos
   - Personas Afectadas (No a Bordo)
   - Informe del Siniestro

2. **Manejo de Valores Nulos**: Identifiqué y manejé los valores nulos que estaban representados en el dataset. Tuve que hacerles transformaciones ya que estos valores 'nulos' no estaban representados como 'None' o 'Null', si no que tenian un string.

3. **Corrección de Errores Tipográficos**: Corregí errores tipográficos en las columnas, lo que mejoró la legibilidad y la coherencia de los datos.

4. **Extracción de Países**: Extraje información sobre los países de las ubicaciones proporcionadas. Esto fue esencial porque muchas ubicaciones no incluían el país (por ejemplo, solo los estados en el caso de Estados Unidos).


## Tendencias y Conclusiones

- **Tendencia a la Baja**: Grafiqué la cantidad de muertes en accidentes aéreos a lo largo de los años. Desde el pico de muertes en 1972, se observa una tendencia a la baja. Esto se debe a mejoras en la industria de la aviación, avances tecnológicos, regulaciones de seguridad, gestión del tráfico aéreo, entrenamiento de la tripulación y mantenimiento de aeronaves.

- **Correlación Positiva Fuerte**: Se destacó una correlación positiva fuerte entre la cantidad de tripulantes a bordo y la cantidad de vuelos por año. Esto subraya la importancia de la seguridad en la aviación.

- **Baja Probabilidad de Sobrevivir**: Calculé la probabilidad de sobrevivir a un accidente aéreo siendo tripulante, que resultó extremadamente baja (0.226%). Esto enfatiza la alta tasa de mortalidad en accidentes aéreos y la necesidad de reducir la cantidad de estos eventos.

- **Análisis de Outliers**: Realicé un análisis de outliers en todo el conjunto de datos y me centré en outliers específicos entre dos décadas distintas. Esto permitió explorar incidentes particulares, como atentados terroristas, errores humanos y problemas de mantenimiento.

# KPIs

### Análisis de KPI - Tasa de Fatalidad de la Tripulación

El KPI principal establecido es evaluar la disminución de un 10% en la tasa de fatalidad de la tripulación en los últimos 10 años, en comparación con la década anterior. Este KPI es fundamental para medir el progreso en la seguridad de la aviación y asegurar que los accidentes aéreos continúen disminuyendo.

### KPI Adicional 1:

**Tasa de Fatalidad de Pasajeros**: Evaluar la disminución de un 10% en la tasa de fatalidad de los pasajeros en los últimos 10 años, comparado con la década anterior. Este KPI se enfoca en la seguridad de los pasajeros.

### KPI Adicional 2:

**Tasa de Supervivencia:** Evaluar el aumento del 10% en la tasa de supervivencia respecto al año anterior. Este KPI mide la mejora en la tasa de supervivencia en accidentes aéreos y refleja directamente la seguridad en la aviación.

Estos KPIs nos permitirán evaluar de manera efectiva la evolución en la aviación.

## Material de origen

Este proyecto de análisis de accidentes aéreos se ha desarrollado con fines educativos y ha sido proporcionado por [Henry](https://www.soyhenry.com) academia virtual de carreras tecnológicas. El objetivo de este proyecto es explorar datos históricos de accidentes aéreos y aplicar técnicas de análisis de datos para obtener información valiosa sobre la la evolución en la aviación.

* Puedes acceder al repositorio donde estan las consignas haciendo click [aquí](https://github.com/soyHenry/PI_DA/tree/Full_Time)

Quiero agradecer a Henry por proporcionar este proyecto educativo y alentar a los estudiantes y entusiastas de la tecnología a explorar y aprender de estos datos. Juntos, podemos contribuir a un futuro más seguro en los cielos.

¡Disfruta explorando y analizando los datos de accidentes aéreos!

## Contacto
- LinkedIn : [Lucas Santos Oliveira](www.linkedin.com/in/lucas-santosoliveira10)
- Correo electronico : lucas-santosoliveira@hotmail.com
