# 📊 Desafio Técnico: Senior Analytics Engineer - Indicium AI

<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="PowerBI">
  <img src="https://img.shields.io/badge/Apache%20Parquet-632CA6?style=for-the-badge&logo=apache&logoColor=white" alt="Parquet">
</p>

## 📝 Descrição do Projeto
Este repositório contém a solução para o desafio técnico da **Indicium AI**, focado na transformação e modelagem de dados da base **Northwind** para a empresa *Northwind Traders*. O projeto visa transformar silos de dados brutos em uma estrutura analítica de alta performance.

---

## 📌 Visão Geral
O objetivo principal foi realizar o processamento de dados brutos (CSV), aplicando modelagem dimensional (Star Schema) e convertendo os dados para o formato **Parquet**, otimizando o consumo de memória e velocidade de processamento no **Power BI**.

## 🛠️ Stack Tecnológica
* **Linguagem:** ![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
* **Transformação:** ![Pandas](https://img.shields.io/badge/Pandas-ETL-150458?style=flat-square&logo=pandas)
* **Ambiente:** ![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?style=flat-square&logo=googlecolab)
* **Armazenamento:** ![Parquet](https://img.shields.io/badge/Storage-Apache%20Parquet-632CA6?style=flat-square)
* **BI:** ![Power BI](https://img.shields.io/badge/Visualization-Power%20BI-F2C811?style=flat-square&logo=powerbi)

---

## 📂 Estrutura Dimensional (Star Schema)

A arquitetura de dados foi desenhada para maximizar a performance analítica:

### 🔹 Tabelas Dimensão (`/data/dim_`)
* `dim_employees`: Cadastro e hierarquia de funcionários.
* `dim_customers`: Atributos detalhados dos clientes.
* `dim_products`: Catálogo com categorias e fornecedores integrados.
* `dim_states` & `dim_territories`: Dimensões geográficas.

### 🔸 Tabelas Fato (`/data/fact_`)
* `fact_sales_completed`: Transações de vendas, métricas de receita e volume.
* `fact_churn_analysis`: Modelagem preditiva/histórica de retenção de clientes.

---

## 🚀 Pipeline de Dados
1.  **Ingestão:** Extração de fontes `.csv`.
2.  **Transformação:** * Tratamento de tipos e valores nulos.
    * Criação de **Surrogate Keys**.
    * Lógica de negócio aplicada para análise de **Churn**.
3.  **Carga:** Escrita em `.parquet` com compressão *snappy*.

---

## 📁 Organização do Repositório
```bash
├── csv_files/          # Arquivos de ingestão (fonte em .csv)
├── parquet_files/      # Arquivos finais em formato Parquet
├── python_files/       # Scripts de ETL (Jupyter/Colab)
└── README.md           # Documentação
