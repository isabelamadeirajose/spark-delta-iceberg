# Apache Spark com Delta Lake e Apache Iceberg

Projeto de pesquisa sobre Apache Spark com Delta Lake e Apache Iceberg, desenvolvido para a disciplina de Engenharia de Dados.

## 📚 Documentação

A documentação completa está disponível em:
👉 https://isabelamadeirajose.github.io/spark-delta-iceberg/

## 📋 Pré-requisitos

- [Docker](https://www.docker.com/) v29.4.1 ou superior
- [Git](https://git-scm.com/) v2.51.0 ou superior
- [Python](https://www.python.org/) 3.13 ou superior
- [Java](https://adoptium.net/) OpenJDK 17

## 🚀 Instalação e execução

### 1. Clone o repositório

```bash
git clone https://github.com/isabelamadeirajose/spark-delta-iceberg.git
cd spark-delta-iceberg
```

### 2. Suba o ambiente Docker

```bash
docker compose up -d
```

### 3. Acesse o JupyterLab

Abra o navegador em: http://localhost:8888

### 4. Execute os notebooks

Dentro do JupyterLab, navegue até `work/notebooks/` e execute:

- `delta_lake.ipynb` — demonstração do Delta Lake
- `iceberg.ipynb` — demonstração do Apache Iceberg

## 📁 Estrutura do Projeto

```
spark-delta-iceberg/
├── notebooks/
│   ├── delta_lake.ipynb     # Notebook Delta Lake
│   └── iceberg.ipynb        # Notebook Apache Iceberg
├── docs/                    # Documentação MkDocs
│   ├── index.md             # Contextualização
│   ├── spark.md             # Apache Spark
│   ├── delta.md             # Delta Lake
│   └── iceberg.md           # Apache Iceberg
├── data/                    # Dados gerados pelos notebooks
├── docker-compose.yml       # Configuração do ambiente Docker
├── mkdocs.yml               # Configuração da documentação
└── README.md                # Este arquivo
```

## 🛠️ Tecnologias

| Tecnologia | Versão |
|---|---|
| Apache Spark | 3.5.0 |
| Delta Lake | 3.2.0 |
| Apache Iceberg | 1.5.0 |
| PySpark | 3.5.0 |
| JupyterLab | 4.5.7 |
| Docker | 29.4.1 |

## 📖 Como executar os testes

Todos os notebooks podem ser executados do início ao fim com **Kernel > Restart Kernel and Run All Cells**.

## 🔗 Referências

- [Apache Spark](https://spark.apache.org/)
- [Delta Lake](https://delta.io/)
- [Apache Iceberg](https://iceberg.apache.org/)
- [Canal DataWay BR](https://www.youtube.com/@DataWayBR)