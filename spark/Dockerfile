FROM bde2020/spark-master:3.2.1-hadoop3.2

COPY ./jars/ /spark/jars
COPY spark_job.py /stocks/spark_job.py

RUN mkdir -p /stocks
RUN pip3 install install delta-spark==1.2.0

# USER root
# # needed so that thrift server can create the megastore_db directory
# RUN chmod g+w /opt/bitnami/spark

# USER 1001
# CMD ["/bin/bash", "-c","/opt/bitnami/spark/bin/spark-submit --class org.apache.spark.sql.hive.thriftserver.HiveThriftServer2"]
