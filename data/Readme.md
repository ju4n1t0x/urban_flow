
      En a las imágenes, verificamos que si bien la mayoria cuenta con buena calidad,
      el hecho de contar con imágenes de la via pública, en donde el enfoque de las 
      mismas no se encuentra estandarizado debido a que se obtienen de diferentes 
      cámaras en distintas posiciones, y además en distintos momentos del día 
      (más luz, menos luz, etc), dificultan un poco mas la tarea de procesar las mismas.

      En cuanto a los datos, verificamos que el dataset que recibimos poseía muchas
      inconsistencias:
      - Columna patentes con datos faltantes.
      - Fechas con formatos diferentes. 
      - Horas con formatos diferentes.
      - Columna de velocidad_registra con datos faltantes.
      - Columna radar_id con datos faltantes
      - Columna estado de pago con estado declarado como ERROR

      Si bien aplicamos un proceso de limpieza y estandarización de los mismos,
      las inconsistencias en el dataset inicial, reducen la posibilidad de que
      las cantidades de imagenes con match sea superior a las obtenidas. 

      Una mejora en la obtención de las imágenes, y de los datos, ayudaría a que
      el resultado final sea más eficienciente y preciso.
     