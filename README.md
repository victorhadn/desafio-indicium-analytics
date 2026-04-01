# desafio-indicium-analytics

Desafio Técnico: Indicium Analytics (Senior Analytics Engineer)

• Este repositório contém a solução para o desafio técnico da Indicium AI, focado na transformação e modelagem de dados da base Northwind para fins de Business Intelligence.


📌 Visão Geral

O objetivo deste projeto foi processar dados brutos (CSV), aplicar técnicas de modelagem dimensional e disponibilizar os arquivos em um formato otimizado para consumo em ferramentas de BI, como o Power BI.


🛠️ Tecnologias Utilizadas

• Python: Linguagem principal para manipulação de dados.

• Pandas: Biblioteca utilizada para limpeza e transformação.

• Google Colab: Ambiente de desenvolvimento para os scripts de ETL.

• Apache Parquet: Formato de armazenamento colunar escolhido pela alta performance e compressão.

• Power BI: Camada de visualização de dados (consumindo os arquivos .parquet).



📂 Estrutura de Dados (Star Schema)

A modelagem foi estruturada seguindo os princípios de Star Schema, facilitando a performance em consultas analíticas:

Tabelas Dimensão (dim_)

• dim_employees: Informações cadastrais dos funcionários.

• dim_customers: Dados detalhados dos clientes.

• dim_products: Catálogo de produtos, categorias e fornecedores.

• dim_states & dim_territories: Dimensões geográficas para análise regional.


Tabelas Fato (fact_)

• fact_sales_completed: Registros de vendas finalizadas, métricas de valor e quantidade.

• fact_churn_analysis: Modelagem específica para análise de retenção e perda de clientes.



🚀 Fluxo de Trabalho (Pipeline)

• Ingestão: Leitura dos arquivos originais em formato .csv.

• Transformação: * Tratamento de valores ausentes e normalização de tipos.

• Criação de chaves substitutas (surrogate keys) onde necessário.

• Filtragem e agregação para a criação das tabelas fato.

• Carga: Exportação dos DataFrames para o formato .parquet, garantindo que o esquema de dados seja preservado e o arquivo final seja leve.



🔧 Como Executar

• Acesse o notebook desafio_tecnico_northwind.ipynb no Google Colab ou ambiente Jupyter local.

• Certifique-se de que os arquivos CSV de origem estejam no diretório correto.

• Execute as células para gerar os arquivos .parquet listados no repositório.

• Importe os arquivos .parquet no Power BI através do conector nativo de pastas ou arquivos.
