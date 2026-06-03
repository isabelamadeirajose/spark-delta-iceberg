# Apache Spark com Delta Lake e Apache Iceberg

Projeto de pesquisa sobre **Apache Spark** com **Delta Lake** e **Apache Iceberg**, desenvolvido para a disciplina de Engenharia de Dados do curso de Engenharia de Software (5ª fase).

## Sobre o Projeto

Este projeto explora o uso do Apache Spark integrado ao Delta Lake e ao Apache Iceberg — dois dos principais formatos de tabela open source para arquitetura **Data Lakehouse**. O objetivo é demonstrar como essas tecnologias adicionam transações ACID, versionamento de dados e operações de UPDATE e DELETE a um Data Lake.

## Documentação

A documentação completa, incluindo instruções de instalação, configuração do ambiente e como executar os notebooks, está disponível em:

👉 **[https://isabelamadeirajose.github.io/spark-delta-iceberg/](https://isabelamadeirajose.github.io/spark-delta-iceberg/)**

## Estrutura do Projeto

```
spark-delta-iceberg/
├── notebooks/
│   ├── delta_lake.ipynb     # Notebook com demonstração do Delta Lake
│   └── iceberg.ipynb        # Notebook com demonstração do Apache Iceberg
├── docs/                    # Documentação MkDocs
│   ├── index.md             # Contextualização
│   ├── spark.md             # Apache Spark
│   ├── delta.md             # Delta Lake
│   └── iceberg.md           # Apache Iceberg
├── assets/                  # Imagens e diagramas
├── data/                    # Dados gerados pelos notebooks
├── docker-compose.yml       # Configuração do ambiente Docker
├── pyproject.toml           # Configuração do projeto (padrão UV)
└── mkdocs.yml               # Configuração da documentação
```

## Tecnologias

| Tecnologia | Versão |
|---|---|
| Apache Spark | 3.5.0 |
| Delta Lake | 3.2.0 |
| Apache Iceberg | 1.5.0 |
| PySpark | 3.5.0 |
| JupyterLab | 4.5.7 |
| Docker | 29.4.1 |

## Referências

- [Apache Spark](https://spark.apache.org/)
- [Delta Lake](https://delta.io/)
- [Apache Iceberg](https://iceberg.apache.org/)
- [Canal DataWay BR](https://www.youtube.com/@DataWayBR)
- [spark-delta - Prof. Jorge Silva](https://github.com/jlsilva01/spark-delta)
- [spark-iceberg - Prof. Jorge Silva](https://github.com/jlsilva01/spark-iceberg)
