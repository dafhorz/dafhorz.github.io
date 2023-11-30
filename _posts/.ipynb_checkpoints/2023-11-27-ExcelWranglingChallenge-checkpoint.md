---
layout: post
title:  "Data Wrangling Challenge in Excel: Salary Survey 2021"
date:   2023-02-12 00:33:33 -0600
categories: Wrangling
tags:
  - Excel
  - Wrangling
  - Cleaning
permalink: /ExcelWranglingChallenge
image: 
  path: /assets/images/excel.jpg
  thumbnail: /assets/images/excel-400x200.jpg
---
## Summary
This is a challenge I took part in. I handled an eccentric Excel Salary Survey dataset, transforming complex characters and data into usable information. I cleaned up and organized the information, using different tools to find patterns. This challenge provided an opportunity to test my efficiency working in Excel. In this post, I will describe my process."

# **Important**
**In order not to give away the solution for anybody who is attempting the same challenge, I will not make it public, but I will describe vaguely procedure.**

Here's two screenshots for you to get an idea of how the challenge looks:

<figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Excel_Wrangling_Challenge/before.jpg" alt=""></a>
  <figcaption>Dataset before.</figcaption>
</figure> 

<figure class="align-center">
  <a href="#"><img src="{{ site.url }}{{ site.baseurl }}/assets/images/Excel_Wrangling_Challenge/after.jpg" alt=""></a>
  <figcaption>Dataset after.</figcaption>
</figure> 

## Procedure
This is what I wrote in the file I sent. I hope it doesn't cause any inconvenience that it's in Spanish.

"La solución está dividida en tres pasos que quise destacar para mejor comprensión del proceso. El resultado de cada paso se encuentra en su respectiva pestaña.

### 1 RemoveAccent
Los acentos y demás caracteres externos al inglés fueron eliminados mediante la implementación de una función (VBA). La idea es relacionar a cada caracter con su versión estandarizada y sin acento; para cada celda se reemplazará cada caracter. El resultado puede obervarse en la pestaña correspondiente.

### 2 Formulas
Para limpiar cada una de las columnas, hubo que hacer una exploración de qué tipo de errores se podían localizar. En su mayoría destacan:
- Eliminar caracteres fuera de lugar, por ejemplo ""="",
- Eliminar espacios innecesarios,
- Conversión de minúscula a mayúsculas,
- Conversión de números (strings) a valores,
- Llenar celdas nulas en donde hacía sentido y no complicaría su localización (por ejemplo, en celdas numéricas, asumiendo que no fueron llenadas por no tener un valor nulo: 0).

Además de esto, se separó la columna TIMESTAMP en dos: fecha y hora. Cada una de estas se separó en más partes (MES, DÍA, AÑO, DÍA=DÍA ANTERIOR?) y (HORA, MINUTOS&SEGUNDOS, P.M.?) respectivamente. La finalidad de esto es procesar cada una por separado para después concatenarlas. 
Nota: Dichas columnas se encuentran ocultas para evitar ver más información de la necesaria; si se desea, siéntase libre de exponerlas y visualizarlas.

***********************

### 3 PROCESAMIENTO DE LA HORA
El algoritmo para procesar HORA es sencillo y funciona de la siguiente manera: 
VARIABLES
1. HORA - Se extrae únicamente la hora. Puede modificar su valor.
2. MINUTOS&SEGUNDOS - se quedará fija, 
3. P.M.? - adquiere el valor TRUE <-> La hora tiene el sufijo P.M. al final.

#### ALGORITMO
Si P.M. tiene valor TRUE (es la tarde) y la HORA es menor que 12, se le suman 12 horas.

FIN DEL ALGORITMO

Nótese que si la hora tiene el sufijo A.M. o simplemente no tiene sufijo, entonces no hay necesidad de modificarla.

***********************
### 4 PROCESAMIENTO DE LA FECHA
Tuve problema para procesar la fecha, sobre todo cuando el valor del día y del mes eran ambos menor a 12 y debido al cambio de formato de fecha, era complicado detectar cuál hacía referencia al mes y cuál al día. Al final opté por la siguiente idea:

#### Algoritmo
1. El primer valor de la tabla es introducido manualmente para indicar cuál es el mes y cuál es el día.
2. Aprovechando que las entradas están ordenadas cronológicamente, se comparan los posibles DÍA y MES (aún sin saber cuál es cuál) con el DÍA y MES anterior; si los valores coinciden, DÍA=DÍA ANTERIOR? obtiene el valor TRUE.
3. Si, efectivamente, es el mismo día (DÍA=DÍA ANTERIOR? es TRUE): acomoda los valores en el mismo orden que el día anterior.
4. Si no es el mismo día, pero es el mismo mes: coloca el mes en donde mismo que el día anterior, el otro valor debe ser el día. Regresa a paso 3.
5. Si no es el mismo día, no el mismo mes, pero sí el mismo año: aumenta el número de mes en uno e intenta de nuevo. Regresa a paso 3.
6. Si no es ni el mismo día, ni el mismo mes, ni el mismo año: aumenta el año en uno e introduce el valor manualmente para conocer el día y mes inicial. Regresa a paso 3.

**********************

### 5 Find&Replace
Una vez estandarizados los valores por medio de fórmulas se simplifica la tarea de encontrar errores de dedo, distintas abreviaciones para referirse al mismo lugar, es más fácil entender algunas respuetas, etc. 
Se concatenan las columnas que conforman la FECHA y HORA.
Se simplificaron los títulos de los encabezados para cada columna.

Cabe destacar el hecho de intervenir en algunas respuestas para facilitar su procesamiento en el análisis. Por ejemplo, la pregunta ""What Country do you work in?"" tenía respuetas del estilo: Trabajo desde Canadá para una compañía Alemana. Como la pregunta se refiere al lugar desde donde trabajan, es decir, el lugar físico en donde se encuentra el trabajador haciendo su labor, sin importar el origen de la empresa, se tomó la decisión de intervenir y colocar el lugar correspondiente (cuando fue especificado); en el ejemplo: ""Canadá"".

Finalmente, para estandarizar el uso de monedas, se incluyeron dos columnas ( ANNUAL SALARY (USD) y ADDITIONAL MONETARY COMPENSATION (USD) ), estas toman las cantidades y monedas proporcionadas y las convierte en dólares estadounidenses (XLOOKUP) siempre y cuando no se haya indicado OTHER en la columna CURRENCY. Esta información se encuentra en la pestaña CurrencyRates, la cual no es necesario consultar.

Gracias por su tiempo y dedicación para la revisión de estos archivos.
Cualquier pregunta, no dude en contactarme.

¡Lindo día!"																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
																			
