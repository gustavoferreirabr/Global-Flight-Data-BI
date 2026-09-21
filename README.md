# ✈️ Global Flight Data BI

### Dashboard de Vendas Aéreas desenvolvido com Power BI

Projeto de **Business Intelligence** desenvolvido para transformar dados de vendas de passagens aéreas em informações visuais para análise de desempenho e apoio à tomada de decisão.

O projeto foi desenvolvido do zero, aplicando conceitos de **modelagem dimensional, Star Schema, Power Query, DAX, indicadores de desempenho, análise temporal e visualização de dados**.

> 🔗 **[Acessar Dashboard Online](https://app.powerbi.com/view?r=eyJrIjoiYWU5MDQ0ODctYWE2Yy00NTI3LTg4OGEtMDRhOWM5ODQ0NjgzIiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**

---

## 📊 Dashboard

<p align="center">
<img width="863" height="482" alt="image" src="https://github.com/user-attachments/assets/989b1ba8-b343-4189-a807-abe42ac6fb59" />
<img width="865" height="477" alt="image" src="https://github.com/user-attachments/assets/09743534-4165-48e5-bcee-ed02d095f2f8" />
<img width="866" height="481" alt="image" src="https://github.com/user-attachments/assets/3dcd4cac-41e5-4efb-905b-6fcb5cb57306" />
<img width="862" height="485" alt="image" src="https://github.com/user-attachments/assets/a252c813-42e1-4cca-ae22-9f4778a0eda3" />

</p>

> *Imagem ilustrativa do dashboard. Os arquivos das páginas podem ser encontrados na pasta **`assets`** do projeto.*

---

## 🎯 Objetivo

O objetivo do projeto é utilizar dados de vendas aéreas para responder perguntas de negócio relacionadas a **faturamento, vendas, ticket médio, rotas, companhias aéreas e classes de passagem**.

### Business Questions

* Qual é o faturamento total e como ele evolui ao longo do período?
* Qual é o ticket médio das vendas?
* Quais rotas apresentam maior volume de vendas?
* Quais companhias aéreas concentram maior faturamento?
* Como o faturamento se distribui entre as diferentes classes?
* Como os principais indicadores se comportam em comparação ao período anterior?
* Quais rotas e companhias apresentam maior participação nas vendas?

---

## 🏗️ Arquitetura do projeto

O projeto foi estruturado em diferentes camadas, separando o tratamento dos dados, o modelo semântico, as regras de negócio e a visualização.

```text
Fonte de dados
      ↓
Power Query
      ↓
Modelo Dimensional
(Star Schema)
      ↓
Medidas DAX
      ↓
Dashboard / Visualização
```

### Camadas

| Camada               | Aplicação                                                            |
| -------------------- | -------------------------------------------------------------------- |
| **Fonte de dados**   | Dados de vendas de passagens, clientes, companhias, rotas e produtos |
| **Tratamento**       | Limpeza, transformação e padronização utilizando Power Query         |
| **Modelo semântico** | Estrutura dimensional baseada em Star Schema                         |
| **Medidas**          | Regras de negócio e indicadores desenvolvidos em DAX                 |
| **Visualização**     | Dashboard interativo com KPIs, filtros e análises comparativas       |

---

## ⭐ Modelo de dados — Star Schema

O modelo utiliza uma estrutura de **Star Schema**, com uma tabela fato central relacionada a dimensões descritivas.

Essa estrutura favorece a organização do modelo, a previsibilidade dos filtros e a criação de medidas DAX mais simples e reutilizáveis.

### Estrutura

| Tipo            | Tabela           | Descrição                                        |
| --------------- | ---------------- | ------------------------------------------------ |
| 🟢 **Fato**     | `Fato_Vendas`    | Transações de venda de passagens                 |
| 🔵 **Dimensão** | `Dim_Clientes`   | Informações dos clientes                         |
| 🔵 **Dimensão** | `Dim_Companhias` | Companhias aéreas                                |
| 🔵 **Dimensão** | `Dim_Produtos`   | Produtos e classes das passagens                 |
| 🔵 **Dimensão** | `Dim_Rotas`      | Rotas e informações relacionadas                 |
| 🔵 **Dimensão** | `Calendario`     | Estrutura para análises temporais                |
| ⚙️ **Suporte**  | `Medidas`        | Tabela dedicada ao armazenamento das medidas DAX |

### Diagrama

<p align="center">
<img width="1073" height="480" alt="image" src="https://github.com/user-attachments/assets/bd44eb40-01ea-474a-9a5d-3c36cf928f87" />

</p>

---

## 📐 Medidas DAX

As medidas foram centralizadas em uma tabela específica chamada `Medidas`, separando as regras de negócio das tabelas de dados.

### Indicadores principais

* `Faturamento Total (BRL)`
* `Qntd de Vendas`
* `Qntd de Bilhetes Vendidos`
* `Ticket Medio`

### Comparativos de período

* `Resultado Variação Faturamento`
* `Resultado Variação Qntd Vendas`
* `Resultado Variação Qnt de Bilhetes Vendidos`
* `Resultado Variação Ticket Medio`

### Rankings

* `Rota Mais Vendida`
* `Rota Mais Vendida TOP 1`
* `Companhia Mais Vendida`
* `Companhia TOP 1`

---

## 📊 Páginas do Dashboard

### 🏠 Overview

Página inicial utilizada como capa e ponto de navegação entre as análises.

### 📈 Visão Geral

Apresenta os principais indicadores do negócio:

* Faturamento
* Quantidade de vendas
* Quantidade de bilhetes vendidos
* Ticket médio
* Comparação com período anterior
* Evolução mensal do faturamento
* Faturamento por rota
* Faturamento por classe
* Evolução do ticket médio
* Participação por companhia aérea

### 🛫 Rotas

Análise do desempenho das rotas, incluindo:

* Rota mais vendida
* Faturamento por rota
* Quantidade de vendas
* Evolução mensal das vendas
* Comparação entre diferentes rotas

### ✈️ Companhias Aéreas

Análise do desempenho das companhias:

* Companhia líder em vendas
* Faturamento por companhia
* Evolução do ticket médio
* Comparação de desempenho entre companhias

---

## 🎛️ Interatividade

O dashboard possui recursos de interação para facilitar a exploração dos dados:

* Segmentação por **Data**
* Segmentação por **Companhia**
* Segmentação por **Rota**
* Navegação entre páginas
* Botões de navegação
* Interação entre visuais
* KPIs comparativos
* Filtros dinâmicos

---

## 💡 O que este projeto demonstra

Este projeto demonstra conhecimentos práticos em:

* **Power BI**
* **DAX**
* **Power Query**
* **Modelagem dimensional**
* **Star Schema**
* **Análise temporal**
* **Time Intelligence**
* **Criação de KPIs**
* **Data Visualization**
* **Business Intelligence**
* **Storytelling com dados**
* **Análise de indicadores**
* **Construção de dashboards interativos**

---

## 🛠️ Tecnologias e ferramentas

| Tecnologia           | Aplicação                                       |
| -------------------- | ----------------------------------------------- |
| **Power BI Desktop** | Desenvolvimento do modelo e dashboard           |
| **Power BI Service** | Publicação e disponibilização do dashboard      |
| **DAX**              | Desenvolvimento das medidas e regras de negócio |
| **Power Query**      | Tratamento e transformação dos dados            |
| **Star Schema**      | Modelagem dimensional                           |
| **IA Generativa**    | Apoio na concepção da identidade visual         |

---

## 🎨 Design

A identidade visual do projeto foi desenvolvida com foco em **clareza, consistência e facilidade de leitura dos indicadores**.

A concepção visual contou com apoio de **IA generativa**, utilizada para auxiliar na criação dos backgrounds em SVG utilizados nas páginas do dashboard.

### Características do design

* Paleta sóbria e consistente
* Sidebar de navegação lateral
* Cards de KPI padronizados
* Hierarquia visual dos indicadores
* Layout baseado em resolução **1920 × 1080**
* Tipografia **Segoe UI**
* Tema visual inspirado no **Fluent Design**

### Paleta

| Elemento | Cor       |
| -------- | --------- |
| Grafite  | `#222220` |
| Bege     | `#E9E7E2` |
| Verde    | `#3D6B58` |

---

## 📂 Estrutura do repositório

```text
Global-Flight-Data-BI/
│
├── assets/
│   ├── background-cia-aerea.svg
│   ├── background-rotas.svg
│   ├── background-visao-geral-aerea.svg
│   ├── capa-dashboard-bi.svg
│
├── Global_Flight_Data_BI.pbix
│
└── README.md
```

---

## 🚀 Como utilizar

### Opção 1 — Dashboard online

Acesse diretamente o projeto publicado no Power BI Service:

**[Abrir Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYWU5MDQ0ODctYWE2Yy00NTI3LTg4OGEtMDRhOWM5ODQ0NjgzIiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**

### Opção 2 — Power BI Desktop

1. Clone ou baixe este repositório.
2. Abra o arquivo `Global_Flight_Data_BI.pbix` no **Power BI Desktop**.
3. Explore o modelo de dados.
4. Consulte as medidas DAX.
5. Navegue pelas páginas do dashboard.
6. Utilize os filtros e interações para explorar os dados.

---

## 👤 Autor

### Gustavo Ferreira

**Data Analytics | Business Intelligence**

Profissional em transição e desenvolvimento de carreira na área de **Dados e Business Intelligence**, com experiência prática em análise de dados, indicadores, dashboards, SQL, automação e soluções orientadas a dados.

📧 **E-mail:** [gustavoferreirabarbosa13@gmail.com](mailto:gustavoferreirabarbosa13@gmail.com)

💼 **LinkedIn:** [linkedin.com/in/gustavo-ferreira-barbosa-16aaab229](https://www.linkedin.com/in/gustavo-ferreira-barbosa-16aaab229)

🐙 **GitHub:** [@gustavoferreirabr](https://github.com/gustavoferreirabr)

---

## 📚 Sobre o projeto

Este projeto foi desenvolvido para fins de **estudo, prática e construção de portfólio profissional**, com foco no desenvolvimento de competências aplicadas a **Business Intelligence, análise de dados e visualização de informações**.

O objetivo é demonstrar, por meio de um projeto prático, a aplicação de conceitos de **modelagem de dados, tratamento, análise, DAX e visualização no Power BI**.
