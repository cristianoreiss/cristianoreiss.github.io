---
title: "Olist Data Engineering Project"
date: 2026-04-19
description: "Pipeline de dados completo: Ingestão com Airflow, modelagem com dbt em Postgres e Dashboards no Power BI."
tags: ["Data Engineering", "Airflow", "dbt", "Docker", "PostgreSQL", "Power BI", "Python", "SQL"]
showToc: true
weight: 1
cover:
    image: "https://img.shields.io/badge/Stack-Python%20|%20Airflow%20|%20dbt%20|%20Docker-blue?style=for-the-badge"
    alt: "Data Engineering Stack"
    relative: false
---

### 🛒 Visão Geral
Este projeto cria um fluxo de dados completo usando o dataset público da *Olist*. O objetivo é construir um pipeline que busca dados brutos, organiza tudo usando o Airflow e Postgres, tranasforma as informações com o dbt e exibe os resultados finais em dashboards no Power BI.

### 🏗️ Arquitetura do Projeto
![Fluxo de Dados Olist](/images/arquitetura-olist.png)
*O diagrama acima detalha a orquestração com Airflow e as camadas de transformação com o dbt.

1.  **Extração e Carga (EL):** O **Apache Airflow** orquestra a captura dos arquivos CSV e realiza a ingestão no banco de dados **PostgreSQL**.
2.  **Transformação (T):** Utilização do **dbt** para criar camadas de dados (staging e marts).
3.  **Conteinerização:** Todo o ambiente (Airflow, Postgres) é gerenciado via **Docker Compose**, facilitando o deploy e a configuração.
4.  **Visualização:** Criação de Dashboards no **Power BI** consumindo as tabelas finais modeladas no dbt.

### 🚀 Principais diferenciais técnicos:
- **Orquestração:** Uso de DAGs no Airflow para gerenciar dependências.
- **Modelagem SQL:** Transformações e criação de tabelas fato/dimensão via dbt.
- **Infraestrutura como Código:** Configuração de ambiente com Docker.

### 📊 Dashboard Interativo

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe 
    title="Dashboard Olist" 
    src="COLE_AQUI_O_SEU_LINK_DO_IFRAME" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
    allowFullScreen="true">
  </iframe>
</div>

---
[🔗 Confira o código completo no GitHub](https://github.com/cristianoreiss/data-engineering-olist)