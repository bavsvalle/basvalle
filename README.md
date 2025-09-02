# ETL Biodiesel - Brasil

Este projeto tem como objetivo analisar as **Matérias-Primas utilizadas na Produção de Biodiesel no Brasil**, a partir de dados abertos do [Governo Federal](https://dados.gov.br/home)

## 📊 Etapas do Projeto
1. **Coleta dos Dados**  
   - Fonte: [Painéis de Produção de Etanol e de Biodiesel](https://dados.gov.br/dados/conjuntos-dados/paineis-de-producao-de-etanol-e-de-biodiesel)
      - Arquivo: Matéria-Prima utilizadas na Produção de Biodiesel (CSV)
   
2. **Tratamento (ETL) com Python**  
   - Limpeza e padronização (remoção de acentos com *Unidecode*, ajuste de datas e nomes de colunas, entre outros) 
   - Manipulação e transformação de dados com **pandas**  
   - Uso do **Google Colab** para processamento

3. **Armazenamento em Banco de Dados (MySQL)**  
   - Criação de tabelas normalizadas
   - Importação dos dados tratados via scripts SQL

4. **Visualização** *(em progresso)*  
   - Gráficos e dashboards para explorar tendências de uso das matérias-primas

## 🗂️ Estrutura do Repositório

etl-biodiesel-python-mysql/
│
├── data/ # Arquivos de dados brutos (CSV, Excel, etc.)
│ └── biodiesel-materia-prima.csv
│
├── notebooks/ # Notebooks Jupyter para análise e testes
│ └── projeto_mp_biodiesel.ipynb
│
├── sql/ # Scripts SQL para criar e popular tabelas
│ ├── 01_create_tables.sql
│ ├── 02_insert_meses.sql
│ ├── 03_insert_anos.sql
│ ├── 04_insert_regioes.sql
│ ├── 05_insert_estados.sql
│ ├── 06_insert_produtos.sql
│ └── 07_insert_biocombustiveis.sql
│
└── README.md # Este arquivo
