# CHANGELOG

- Día 1:

En el primer día de trabajo hemos implementado el ejercicio 1, en donde realizamos la estructura base del proyecto y la sincronización con el repositorio remoto en github, además de la creación de la rama Sprint_1 sobre la cual iremos trabajando.

Como parte de esta solución se decidió implementar dentro de las variables del entorno de sistema de colab un TOKEN_GIT el cual utilizaremos importando user.data desde google.colab para no exponer tokens key publicamente en el repositorio.

Además hemos creado el archivo README.md en donde se encuentra toda la descripción y ejercicios del Sprint_1. Y el archivo CHANGELOG.md en donde se dejara constancia de todos los cambios realizados día a día en el Sprint_1.

También avanzamos con el ejercicio 2 en el cual se nos pedía descargar el dataset "speeding_fines", realizamos el análisis exploratorio planteado en el Sprint_1. Verificamos la estructura y los datos que contiene el dataset, además de crear la variable speeding_fines con la cual lo manipularemos a través del colab. Y contamos también los valores nulos.


- Día 2:

En el segundo día de trabajo implementamos el ejercicio 3, enfocado en la limpieza y normalización del dataset "speeding_fines".

Se realizaron las siguientes tareas:
- Normalización de fechas al formato YYYY-MM-DD.
- Normalización de horas al formato 24hs.
- Limpieza de ubicaciones (sin caracteres especiales y en mayúsculas).
- Limpieza de patentes y manejo de valores inválidos con NA.
- Eliminación de registros con valores nulos en columnas relevantes.
- Detección y tratamiento de outliers (IQR).
- Creación de columnas exceso_velocidad_real y exceso_velocidad.
- Filtrado de infracciones reales (exceso_velocidad > 0).
- Guardado del dataset limpio.

- Día 3:

  En este dia de trabajo realizamos la implementacion de ejercicio 4 del Sprint_1. Se realizaron las siguientes tareas:

  - Definir una clase FineAnalyzer que cumpla con las siguientes funcionalidades:

    - Reciba el DataFrame limpio como argumento de inicialización.

    - Encapsule correctamente los datos.

    - Implemente métodos para:
      - Ranking de las patentes mas multadas (top 5).
      - Ranking de los horarios donde se producen mas multas (top 5).
      - Exceso promedio de velocidad.
      - Exceso real promedio de velocidad .
      - Contabilizar la cantidad de multas por cada  ubicación.
  
    En este dia de trabajo realizamos la implementacion de ejercicio 5 del Sprint_1. Se realizaron las siguientes tareas:

    - Ranking de las 10 patentes más reincidentes ordenadas de mayor a menor.
    - Mostrar el porcentaje de infracciones por hora en un gráfico de torta.
    - Mostrar la cantidad de infracciones por mes en un gráfico de barras horizontal ordenado de mayor a menor.
    - Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la hora 00:00.
    - Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la fecha 1932-01-01.
    
    Ademas realizamos una correccion en la limpieza de la columna fecha en data/interim/speeding_fines.csv, debido a que estabamos persitiendo un error de formato.
    
    - Dia 4:
    En este dia de trabajo realizamos la implementacion de ejercicio 5 del Sprint_1. Se realizaron las siguientes tareas:

    - Ranking de las 10 patentes más reincidentes ordenadas de mayor a menor.
    - Mostrar el porcentaje de infracciones por hora en un gráfico de torta.
    - Mostrar la cantidad de infracciones por mes en un gráfico de barras horizontal ordenado de mayor a menor.
    - Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la hora 00:00.
    - Mostrar en un gráfico de líneas de los excesos de velocidad agrupados por la fecha 1932-01-01.
    
    Ademas realizamos una correccion en la limpieza de la columna fecha en data/interim/speeding_fines.csv, debido a que estabamos persitiendo un error de formato.
    
      Dia 5:

      - En este dia de trabajo realizamos la implementacion de ejercicio 6 del Sprint_1. Se realizaron las siguientes tareas:

      - Mostrar el porcentaje de infracción que se produjeron en la fecha 1932-01-01.
      - Mostrar el porcentaje de infracción que se produjeron en la hora 00:00.

      Tomamos como decisión ademas utilizar gráficos de torta para hacer una presentación visual de las variabes calculadas
      