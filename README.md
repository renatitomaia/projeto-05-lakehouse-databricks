# 🏅 Lakehouse Medallion Architecture: Databricks & PySpark

## 📌 Sobre o Projeto
Projeto de Engenharia de Dados focado no processamento de grandes volumes de informação (Big Data) utilizando a arquitetura **Lakehouse**. O pipeline foi totalmente desenvolvido em **PySpark** dentro do ambiente **Databricks**, estruturando os dados nas três camadas corporativas da arquitetura Medallion (Bronze, Silver e Gold) em formato **Delta Lake**.

## 🏗️ Estrutura das Camadas (Medallion)
1. **🥉 Camada Bronze (Raw):** Ingestão dos dados transacionais brutos simulados, mantendo o histórico e a imutabilidade da fonte.
2. **🥈 Camada Silver (Cleansed):** Aplicação de filtros de qualidade (remoção de transações pendentes/canceladas), padronização de strings e adição de metadados de auditoria (timestamps).
3. **🥇 Camada Gold (Business Aggregations):** Transformação focada no negócio, com cálculos de receita e volume de vendas agrupados por categoria e produto, otimizados para consumo em dashboards executivos.

## 🛠️ Stack Tecnológica
* **Plataforma:** Databricks
* **Processamento:** Apache Spark (PySpark)
* **Armazenamento:** Delta Lake (DBFS)
* **Linguagem:** Python

## 🚀 Como Visualizar
* O código completo com as transformações PySpark está disponível no notebook `01_ingestao_bronze.ipynb`.
* Para reproduzir, basta importar o notebook para um workspace do Databricks (Community Edition ou Cloud) e executar as células num cluster compatível.