# Trabajo practico - Herramientas de Desarrollo para Análisis de Datos
Objetivo
El objetivo principal de este proyecto es aplicar los conocimientos adquiridos en para el versionado de código, la organización, limpieza del código y la utilización de pandas.

## ***Sprint_1***

La localidad llamada Vaalserberg de Bélgica se encuentra en la zona fronteriza y limita con los paises de Países Bajos y Alemania.
Esta localidad cuenta con un sistema de radares urbanos para la detección de infracciones por exceso de velocidad. Los registros históricos provienen de sistemas heredados,
el cuál presenta errores de formato, faltante de datos generando registros inconsistentes en el nuevo sistema.

Debemos analizar y depurar los datos de viejo sistema para obtener información relevante sobre las infracciones y de está forma en el futuro poder incorporar los datos
al nuevo sistema sin inconsistencias.

Descargar el dataset speeding fines https://raw.githubusercontent.com/HAD141/datasets/refs/heads/main/TrabajosPracticos/urban_flow/speeding_fines.csv

El dataset contiene información histórica de multas por exceso de velocidad y presenta errores que deberán ser tratados para evitar inconsistencias.

## ***Ejercicios:***


### Ejercicio 1.

> Puntos: 1

Inicialización y configuración de la herramienta de versionado. Vamos a trabajar sobre la rama llamada "Sprint_1".

La estructura de directorios es:

```
├── urban_flow
│   ├── data
│   │   ├── interim (almacena dataset procesados de pasos intermedios)
│   │   │   ├── plots
│   │   ├── processed (almacena dataset procesados finales para entregar a otra aplicación)
│   │   ├── raw (almacena los dataset en crudo, sin procesar)
```


### Ejercicio 2.

> Puntos: 1

Los desarrollos que deben realizar son:

- Descargar el dataset raw original y almacenarlo en `urban_flow/data/raw`.

- Mostrar las 5 primeras filas.

- Analizar tipos de datos

- Contar los valores nulos.


### Ejercicio 3.

> Puntos: 2

Utilizando Pandas:

- Normalizar las de fechas con el formato 'YYYY-MM-DD', en caso de fechas inválidas completar con la fecha `1932-01-01`. Mostrar las 10 primeras fechas.

- Normalizar los horas al formato de 24hs, las horas inválidas se procesaran como `00:00`. Mostrar las 10 primeras horas.

- Normalizar las ubicaciones. Quitar caracteres especiales y pasar todo a mayúsculas. Mostrar las 10 primeras ubicaciones.

- Limpiar y normalizar las patentes, en caso de error completar con pd.NA (no disponible/not available). Quitar caracteres especiales y pasar todo a mayúsculas. Mostrar las 10 últimas patentes.

- Eliminar las filas que posean valores relevantes para las multas y que se encuentren vacios. Mostrar la cantidad de registros eliminados y cuales son las columnas que se observaron utilizando la leyenda
```
Se eliminaron X filas.
Las columnas observadas son:
 - XXX
 - XXX
 - ...
```

- Detectar y eliminar los outliers. Mostrar la cantidad de registros eliminados y cuales son las columnas que se observaron utilizando la leyenda
```
Se eliminaron X filas.
Las columnas observadas son:
 - XXX
 - XXX
 - ...
```

- Crear la columna `exceso_velocidad_real` y calcularla. El exceso de velocidad real es la diferencia entre velocidad_registrada y la velocidad_maxima. Mostrar las primeras 10 patentes y su exceso de velocidad real.

- Crear la columna `exceso_velocidad` y calcularla. El exceso de velocidad es la diferencia entre velocidad_registrada y la velocidad_maxima más un 5 porciento de la velocidad máxima. Mostrar las primeras 10 patentes y su exceso de velocidad.

- Eliminar las filas que no cometieron infracciones según el exceso de velocidad.Mostrar cuantas filas se eliminaron con la leyenda
```
Se eliminaron X filas.
```

- Guardar el dataset limpio en `urban_flow/data/interim/speeding_fines.csv`


### Ejercicio 4.

> Puntos: 2

Definir una clase FineAnalyzer que cumpla con las siguientes funcionalidades:

- Reciba el DataFrame limpio como argumento de inicialización.

- Encapsule correctamente los datos.

- Implemente métodos para:

  - Ranking de las patentes más multadas (top 5). Debe retornar un DataFrame ordenado de mayor a menor y el índice debe comenzar desde 1, con las columnas de patentes y cantidad..

  - Ranking de los horarios donde se producen más multas (top 5). Debe retornar un DataFrame ordenado de mayor a menor y el índice debe comenzar desde 1, con las columnas de hora y cantidad.


  - Exceso promedio de velocidad. Debe retorna un flotante.

  - Exceso real promedio de velocidad . Debe retorna un flotante.

  - Contabilizar la cantidad de multas por cada  ubicación. Debe retornar un DataFrame ordenado por ubicación mostrando la ubicación y la cantidad.

- Crear el objecto e invocar cada uno de los métodos en celdas separadas.


### Ejercicio 5.

> Puntos: 2

Responder a cada punto con un gráfico.

- Ranking de las 10 patentes más reincidentes ordenadas de mayor a menor. Exportar el gráfico con el nombre `ubran_flow/data/interim/plots/fines.jpg`


- Mostrar el porcentaje de infracciones por hora en un gráfico de torta. Exportar el gráfico con el nombre `ubran_flow/data/interim/plots/hours.jpg`

- Mostrar la cantidad de infracciones por mes en un gráfico de barras horizontal ordenado de mayor a menor. Exportar el gráfico con el nombre `ubran_flow/data/interim/plots/months.jpg`

- Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la hora 00:00. Exportar el gráfico con el nombre `ubran_flow/data/interim/plots/hour.jpg`

- Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la fecha 1932-01-01. Exportar el gráfico con el nombre `ubran_flow/data/interim/plots/date.jpg`


### Ejercicio 6.

> Puntos: 1

- Mostrar el porcentaje de infracción que se produjeron en la fecha 1932-01-01.

```
El porcentaje de infracciones en la fecha 1932-01-01 es XX.XX%
```

- Mostrar el porcentaje de infracción que se produjeron en la hora 00:00.
```
El porcentaje de infracciones a la hora 00:00 es XX.XX%
```


## Ejercicio 07

> Puntos: 1

Redactar una conclusión acerca de los datos que contiene el dataset.

