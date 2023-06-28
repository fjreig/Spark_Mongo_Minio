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

| Microservicio      | Descripcion |  GUI |
| :----:             |    :----:   |    :----:   |
| InsertMongo    | Servidor Kafka donde se guardan los datos        | |
| QueryMongo   | Plataforma web para monitorizar el servidor Kafka        | http://localhost:8080 |
| InsertMinio   | Servidor de connectores sink y source        | |
| ReadMinio     | BBDD donde se almacenan los datos para representarlos en Kibana        | http://localhost:5601 |
