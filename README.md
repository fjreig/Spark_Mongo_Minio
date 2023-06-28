# Spark MongoDB Minio

### 0. Microservicios empleados

| Microservicio      | Descripcion |  GUI |
| :----:             |    :----:   |    :----:   |
| Spark Server    | Servidor con pyspark        | http://localhost:8080 |
| Jupyter Notebook   | Plataforma web para realizar pruebas del entorno pyspark        | http://localhost:8888 |
| MongoDB   | BBDD del tipo Mongo        | |
| Minio      | Almacenamiento del tipo S3        | http://localhost:9000 |

### 1. Levantar los contenedores
```docker compose up -d```

### 2. Accedemos a jupyter notebook

```http://localhost:8888```

### 3. Ejecutamos los siguientes Scripts

| Script      | Descripcion | 
| :----:             |    :----:   |
| InsertMongo    | El Script lee un fichero json con información de varios vuelos y lo almacena en MongoDB        | 
| QueryMongo   | Query mediante SparkSQL a la base de datos MongoDB y lo almacena en un fichero parquet        |
| InsertMinio   | Escritura mediante Spark en formato json en Minio        |
| ReadMinio     | Lectura mediante Spark de un fichero json en Minio       |

### 4. Visualizar documentos guardados en Minio

```http://localhost:9000```
