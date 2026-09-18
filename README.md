# ✈️ Global Flight Data Analytics | Power BI Portfolio

<div align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-207245?style=for-the-badge&logo=microsoft&logoColor=white)
![Star Schema](https://img.shields.io/badge/Architecture-Star%20Schema-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

</div>

---

## 📌 Sobre o Projeto
O **Global Flight Data Analytics** é uma solução completa de inteligência de negócios projetada para monitorar e analisar o desempenho de vendas de passagens aéreas globais. O projeto simula um ambiente corporativo real, respondendo a perguntas cruciais de negócio como: *Qual o faturamento por rota e companhia aérea? Quais são os produtos mais rentáveis? Qual o comportamento do ticket médio e o volume de vendas ao longo do tempo?*

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Power BI & Power Query (Linguagem M):** Extração, transformação de dados (ETL), limpeza e tratamento de tipos.
* **Modelagem Dimensional (Star Schema):** Organização estruturada em tabelas Fato e Dimensões para garantir alta performance e escalabilidade de consultas.
* **DAX Avançado (Data Analysis Expressions):** Criação de medidas calculadas dinâmicas para análise de faturamento, bilhetes vendidos, ticket médio e indicadores de variação percentual.
* **Figma / UI Design:** Criação de um layout e background customizados e profissionais, focados em *Data Storytelling* e experiência do usuário (UX).

---

## 📐 Arquitetura de Dados & Modelagem
O projeto segue rigorosamente as boas práticas de modelagem dimensional de Kimball:
1. **Tabela Fato (`Fato_Vendas`):** Contém as transações detalhadas de vendas, chaves estrangeiras e métricas quantitativas.
2. **Tabelas de Dimensão (`Dim_Produtos`, `Dim_Companhias`, `Dim_Rotas`, `Dim_Clientes`):** Contextualizam os dados transacionais (classes de voos, alianças aéreas, origens/destinos IATA e perfis de clientes).
3. **Tabela Calendário Dinâmica:** Desenvolvida via Power Query com atualização automática baseada na data atual do sistema, garantindo suporte completo a inteligência de tempo (*Time Intelligence*).

---

## 📈 Principais Indicadores e Métricas (KPIs)
O painel principal centraliza os seguintes KPIs estratégicos:
* **Faturamento Total (BRL):** Receita bruta acumulada das operações.
* **Volume de Vendas & Bilhetes:** Quantidade total de transações e assentos comercializados.
* **Ticket Médio:** Valor médio gerado por bilhete/transação.
* **Indicadores de Variação (Growth MoM/YoY):** Análise comparativa de crescimento dos principais indicadores de negócio.

---

## 🖼️ Pré-visualização do Dashboard e Arquitetura dos Dados
<img width="949" height="532" alt="image" src="https://github.com/user-attachments/assets/c5292e9b-11de-48a7-a23e-149ade5217a6" />
<img width="954" height="536" alt="image" src="https://github.com/user-attachments/assets/cc2ef123-7841-4b3e-bda3-cea1fe043856" />
<img width="957" height="534" alt="image" src="https://github.com/user-attachments/assets/8f92df93-4f05-4f1e-b334-f6fbeea1161d" />
<img width="952" height="538" alt="image" src="https://github.com/user-attachments/assets/d4c0f0a9-71c3-41fa-bd75-315cb2160c68" />



```text

🚀 Como Executar o Projeto:

1. Certifique-se de ter o Microsoft Power BI Desktop instalado em sua máquina.
2. Clone este repositório ou faça o download do arquivo Global Flight Data BI.pbix.
3. Abra o arquivo no Power BI Desktop e explore as páginas, filtros interativos e códigos DAX na aba de modelagem.
