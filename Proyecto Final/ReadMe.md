## Análisis de la política de "Pico y Género" y su relación con la evolución de los accidentes de tránsito en Bogotá  

#### 29-05-2020
#### Juan Diego Castro Rodríguez

![NA5RR5ImnVG49QqY_QZqZQeMMzmFtCQ1CR9wvUWbrn0.png](attachment:NA5RR5ImnVG49QqY_QZqZQeMMzmFtCQ1CR9wvUWbrn0.png)

## Descripción y Motivación
En el contexto de la pandemia producto del Covid-19, los países del mundo se han visto en la obligación de aislar a sus ciudadanos para evitar el aumento de la cadena de contagios.  Distintas estrategias han sido utilizadas hasta la fecha con el fin de evadir las aglomeraciones masivas cambiando así del día a día de las personas.

Siendo una conducta natural de hombres y mujeres la movilidad surge la motivación de investigar un apartado específico de este fenómeno: los accidentes de tránsito. Para poder ilustrar las dinámicas de género al interior de los accidentes de tránsito se plantea la pregunta de investigación ¿tiene una política de confinamiento basada en el género un efecto sobre los accidentes de tráfico?

A la vez, otras dudas que motivan este estudio son:

-¿Cual es el tipo de accidente más común?

-¿Qué localidades concentran la mayor cantidad de accidentes?

-¿Cómo evolucionan los accidentes ante restricciones de movilidad?

-¿Existen momentos del año donde los accidentes tienden a aumentar?

-¿Estas tendencias se mantienen en otras ciudades de Colombia?

## Objetivo
El presenten trabajo se plantea la meta de analizar el efecto que tuvo la política de aislamiento preventido obligatorio "pico y género" en los accidentes de tránsito en la ciudad de Bogotá-Colombia. Dicha política pública tuvo una duración de 28 días. Durante el 13 de abril hasta el 10 de mayo del 2020, los residentes de Bogotá solo podían salir durante días impares las mujeres y durante días pares los hombres (las personas transgenero de acuerdo al auto reconocimiento de su identidad de género). Para fines de académicos se tomo a la ciudad de Medellín como punto de comparación.


## Métodos:
1. Extraer y limpiar datos:

    *Con las bases de datos abiertos de la Secretaría de Movilidad sobre accidentes de tránsito durante el 2020 para Bogotá http://datos-abiertos-sdm-movilidadbogota.hub.arcgis.com/datasets/b16a3f69814c40ffae63a037b8f0cbf3_0.csv?outSR={%22latestWkid%22:4686,%22wkid%22:4686 y Medellín https://opendata.arcgis.com/datasets/f3e14868231f4bbd825968203de64e48_24.csv 
    
    *Se construyeron funciones auxiliares utilizando las librerias "os" y "requests" para acceder a dichas bases de datos, descargarlas y guardarlas bajo un nombre dado por el usuario en la carpeta de trabajo
    
    *Con la ayuda de la librería Pandas se limpiaron los datos referentes a la fecha de ocurrencia de los accidentes
    
    
2. Análisis y gráficos:

    *Para desarrollar el análisis se construyeron los periodos de tiempo de interés y se filtraron las bases de datos utilizando el método 'loc' de 'Pandas' y expresiones regulares
    
    *Con 'Pandas' se crearon Dataframes para ambas bases de datos dependiendo del periodo a analizar
    
    *Para observar las variaciones por día, se utilizó el método de 'Pandas' 'groupby' y 'agg' para agregar un contador por accidente
    
    *Con la ayuda de la librería 'Matplotlib' se crearon gráficos de barra y circulares para cada periodo en Bogotá y Medellín según la localidad o comuna donde se dió el accidente (retoman los métodos 'groupby' y 'agg')
    
    
3. Otros prográmas:

    *Se construyeron gráficos en Tableau para ilustrar la evolución de los accidentes de tránsito en ambas ciudades, los cuales se pueden encontrar aquí: https://public.tableau.com/views/Picoygnero/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link , https://public.tableau.com/app/profile/juan.diego.castro3168/viz/EvolucindeaccidentesenBogot/Hoja1 , https://public.tableau.com/app/profile/juan.diego.castro3168/viz/AccidentesMed/Hoja1
    
    *Del mismo modo se utilizó el programa QGIS para construir un mapa que ilustre la ubicación de los accidentes resaltando aquellos que presentaron muertos en Bogotá. Para ello se utilizaron los shapes de las UPZ de Bogotá (https://sites.google.com/site/seriescol/shapes) y la Malla Vial Integral de Bogotá (https://www.ideca.gov.co/recursos/mapas/malla-vial-integral-bogota-dc)
    



Jupyter Notebook con el código completo : [Aquí](./Pico_y_género.ipynb).

## Hallazgos 

-El tipo de accidente más común son los choques sin heridos

-Para Bogotá los accidentes se concentran principalmente en Kennedy, Engativa y Suba

-Para Medellín los accidentes se concentran en La Candelaria, Castilla y Laureles

-Existe una tendencia al aumento de los accidentes de tránsito durante el paso del tiempo (marzo-abril-mayo-julio) independiente de la presencia de una política de restricción de movilidad.

-Las tendencias de Bogotá varían al compararlas con el comportamiento de los accidentes de tránsito en Medellín

![Accidentes_Bogot%C3%A1_tratamiento.png](attachment:Accidentes_Bogot%C3%A1_tratamiento.png)

![Accidentes_Medell%C3%ADn_tratamiento.png](attachment:Accidentes_Medell%C3%ADn_tratamiento.png)

![Accidentes_Loc_Bogot%C3%A1_tratamiento.png](attachment:Accidentes_Loc_Bogot%C3%A1_tratamiento.png)

![Accidentes_Com_Medell%C3%ADn_t_tratamiento.png](attachment:Accidentes_Com_Medell%C3%ADn_t_tratamiento.png)

![Evoluci%C3%B3n_accidentes_bogot%C3%A1.png](attachment:Evoluci%C3%B3n_accidentes_bogot%C3%A1.png)

![Evoluci%C3%B3n_accidentes_Medell%C3%ADn.png](attachment:Evoluci%C3%B3n_accidentes_Medell%C3%ADn.png)

![Mapa%20Accidentes%20con%20convenciones.png](attachment:Mapa%20Accidentes%20con%20convenciones.png)
