# Apache Iceberg

## O que é o Apache Iceberg?

Apache Iceberg é um formato de tabela open source de alto desempenho para grandes conjuntos de dados analíticos. Foi criado pela Netflix em 2017 e doado à Apache Software Foundation.

## Principais características

- **Transações ACID:** operações seguras e consistentes
- **Versionamento por snapshots:** cada operação gera um novo snapshot
- **SQL padrão:** suporte completo a UPDATE e DELETE via SQL
- **Compatibilidade:** funciona com Spark, Flink, Trino, Hive e outros engines
- **Evolução de schema:** permite adicionar, renomear e remover colunas sem reescrever dados
- **Partition evolution:** permite mudar o particionamento sem reescrever dados

## Como funciona

O Iceberg mantém um conjunto de **snapshots** — cada operação (INSERT, UPDATE, DELETE) gera um novo snapshot, permitindo consultar qualquer versão anterior dos dados.

## Configuração no Spark

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Iceberg Demo") \
    .config("spark.jars.packages", "org.apache.iceberg:iceberg-spark-runtime-3.5_2.12:1.5.0") \
    .config("spark.sql.extensions", "org.apache.iceberg.spark.extensions.IcebergSparkSessionExtensions") \
    .config("spark.sql.catalog.local", "org.apache.iceberg.spark.SparkCatalog") \
    .config("spark.sql.catalog.local.type", "hadoop") \
    .config("spark.sql.catalog.local.warehouse", "/home/jovyan/work/data/iceberg_warehouse") \
    .getOrCreate()
```

## Operações demonstradas

| Operação | Descrição |
|---|---|
| INSERT | Criação da tabela e inserção dos dados iniciais |
| UPDATE | Atualização de cidade e valor de compra de um cliente |
| DELETE | Remoção de um cliente da tabela |
| SNAPSHOTS | Consulta do histórico de snapshots da tabela |

## Diferença entre Delta Lake e Iceberg

| Característica | Delta Lake | Apache Iceberg |
|---|---|---|
| Criado por | Databricks | Netflix |
| Ano | 2019 | 2017 |
| Formato de log | Transaction log | Snapshots |
| Compatibilidade | Principalmente Spark | Multi-engine |

## Versão utilizada neste projeto

- Apache Iceberg **1.5.0**
- Compatível com Apache Spark **3.5.0**