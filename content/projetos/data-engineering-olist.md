---
title: "Olist Data Engineering Project"
date: 2026-04-19
description: "Pipeline de dados completo: Ingestão com Airflow, modelagem com dbt em Postgres e Dashboards no Power BI."
tags: ["Data Engineering", "Airflow", "dbt", "Docker", "PostgreSQL", "Power BI", "Python", "SQL"]
showToc: true
weight: 1
cover:
    image: "https://img.shields.io/badge/Stack-Airflow%20|%20dbt%20|%20Docker-blue?style=for-the-badge"
    alt: "Data Engineering Stack"
    relative: false
---

### 🛒 Visão Geral
Este projeto implementa um pipeline de dados ponta a ponta utilizando o dataset público da **Olist**. O objetivo é simular um ambiente real de engenharia de dados, transformando dados brutos em insights estratégicos.

### 🏗️ Arquitetura do Projeto
A solução foi desenhada para ser escalável e reprodutível, utilizando as seguintes etapas:

1.  **Extração e Carga (EL):** O **Apache Airflow** orquestra a captura dos arquivos CSV e realiza a ingestão no banco de dados **PostgreSQL**.
2.  **Transformação (T):** Utilização do **dbt** para criar camadas de dados (staging e marts).
3.  **Conteinerização:** Todo o ambiente (Airflow, Postgres) é gerenciado via **Docker Compose**, facilitando o deploy e a configuração.
4.  **Visualização:** Criação de Dashboards no **Power BI** consumindo as tabelas finais modeladas no dbt.

### 🚀 Principais diferenciais técnicos:
- **Orquestração:** Uso de DAGs no Airflow para gerenciar dependências.
- **Modelagem SQL:** Transformações e criação de tabelas fato/dimensão via dbt.
- **Infraestrutura como Código:** Configuração de ambiente com Docker.

---
[🔗 Confira o código completo no GitHub](https://github.com/cristianoreiss/data-engineering-olist)