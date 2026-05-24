
    Dia 1 - segunda etapa:
    - Descargamos el dataset de imagenes y lo descomprimimos dentro de 
    /data/raw/imgs/urban_flow_plates
    - Inicializamos dvc dentro del repositorio para hacer el traceo
    - Agregamos al traceo de dvc el directorio con las imagenes y hacemos el push
    - Configuramos el storage remoto de supabase creado para almacenar las 
    imagenes del proyecto
    - Agregamos la configuracion del cloud storage remoto para dvc a github
    
    Dia 2:
      - Separamos el dataset en completes y plates, contamos cuandas imagenes 
      hay en cada uno y calculamos la reoslucion promedio
      - Pasamos el dataset a formato json y lo agregamos al directorio
      - Desarrollamos la funcion solicitada para mostrar las imagenes

    Dia 3:
      - Convertimos las imagenes a escala de grises y las guardamos en el 
      directorio /imgs separadas en plates y completes
      - Convertimos las imagenes a blur y las guardamos en /imgs
      separadas en plates y completes
      - Convertimos las imagenes a canny y las guardamos en /imgs
      separadas en plates y completes

    Dia 4:
      - Por medio de opencv procesamos las imagenes para poder asilar las patentes
      - Procesamos las patentes aisladas y por medio de extraer_patente 
      con easyocr extraemos sus datos
      - Hacemos un match entre los datos extraidos y el dataframe  
      para identificar las patentes
      que se poseen multas activas, guardamos los datos en un nuevo 
      dataset dentro de /processed
    
    
    Dia 5:
    - Realizamos limpieza del colab y formateo segun pep 8 solicitado
    - Creamos las variables que muestran las metricas segun el enunciado

    Dia 6:
    - Completamos archivo Readme.md con conclusion del proyecto realizado

    
    