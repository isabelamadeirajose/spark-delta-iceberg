# Apache Spark (PySpark)

## O que é o Apache Spark?

Apache Spark é um engine de processamento de dados distribuído, open source, criado para processar grandes volumes de dados de forma rápida e eficiente. Suporta processamento em batch e streaming.

## PySpark

PySpark é a API Python do Apache Spark, permitindo escrever aplicações Spark usando Python.

## Principais características

- **Velocidade:** processa dados em memória, até 100x mais rápido que Hadoop MapReduce
- **Facilidade:** API em Python, Scala, Java e R
- **Versatilidade:** batch, streaming, SQL, machine learning e grafos
- **Escalabilidade:** roda de um laptop a milhares de servidores

## SparkSession

O ponto de entrada de qualquer aplicação PySpark:

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Minha Aplicação") \
    .getOrCreate()
```

## Versão utilizada neste projeto

- Apache Spark **3.5.0**
- Scala **2.12**
- OpenJDK **17**