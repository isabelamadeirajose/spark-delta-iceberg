# Delta Lake

## O que é o Delta Lake?

Delta Lake é um framework open source que adiciona uma camada de confiabilidade ao Data Lake, trazendo transações ACID, versionamento de dados e operações de UPDATE e DELETE para arquivos no formato Parquet.

## Principais características

- **Transações ACID:** garante atomicidade, consistência, isolamento e durabilidade
- **Time Travel:** acesso a versões anteriores dos dados
- **UPDATE e DELETE:** operações não disponíveis no Parquet comum
- **Histórico de operações:** registro completo de todas as alterações
- **Compatibilidade:** totalmente compatível com Apache Spark

## Como funciona

O Delta Lake armazena os dados em arquivos Parquet e mantém um **transaction log** (pasta `_delta_log`) que registra cada operação realizada na tabela.

## Configuração no Spark

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Delta Lake Demo") \
    .config("spark.jars.packages", "io.delta:delta-spark_2.12:3.2.0") \
    .config("spark.sql.extensions", "io.delta.sql.DeltaSparkSessionExtension") \
    .config("spark.sql.catalog.spark_catalog", "org.apache.spark.sql.delta.catalog.DeltaCatalog") \
    .getOrCreate()
```

## Operações demonstradas

| Operação | Descrição |
|---|---|
| INSERT | Criação da tabela e inserção dos dados iniciais |
| UPDATE | Atualização de cidade e valor de compra de um cliente |
| DELETE | Remoção de um cliente da tabela |
| TIME TRAVEL | Consulta de versões anteriores da tabela |

## Versão utilizada neste projeto

- Delta Lake **3.2.0**
- Compatível com Apache Spark **3.5.0**