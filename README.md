# olympics-datalake

# 🏅 Olimpíadas 1896-2024: Data Lake & Analytics

Este projeto implementa uma arquitetura de **Data Lake** para processar e analisar dados históricos das Olimpíadas, desde Atenas 1896 até Paris 2024.

## 🏗️ Estrutura do Data Lake

O projeto segue a arquitetura de medalhões para organização dos dados:

* **`raw/`**: Dados brutos no formato original (CSV) e seus metadados de origem.
* **`bronze/`**: Dados integrados e convertidos para **Apache Parquet**. Nesta camada, os dados são padronizados e os datasets (histórico + 2024) são unidos.
* **`gold/`**: Camada de consumo com análises refinadas, rankings e visualizações (PNG) prontas para tomada de decisão.

## 📂 Organização de Pastas
```text
├── raw/                      # Dados brutos (CSV)
├── bronze/                   # Dados integrados (Parquet/JSON)
├── gold/                     # Análises e Visualizações
│   ├── analise_medalhas/
│   ├── analise_modalidades/
│   └── analise_genero/
├── metadata_schema.json      # Definição do padrão de metadados
└── README.md                 # Documentação do projeto
