# 📊 Análise de Desempenho e Eficiência - Rede Alura Store

![Status](https://img.shields.io/badge/Status-Concluído-2e8b57) ![Python](https://img.shields.io/badge/Python-3.10+-blue) ![Libs](https://img.shields.io/badge/Libs-Pandas%20|%20Matplotlib-orange)

## 💼 Contexto do Negócio
O Senhor João, proprietário da rede **Alura Store**, planeja vender uma de suas 4 filiais para financiar um novo empreendimento.

**O Desafio:** Analisar os dados históricos de 9.435 vendas para identificar a loja com a **menor eficiência operacional e financeira**, fornecendo uma recomendação estratégica baseada em dados sobre qual unidade deve ser vendida.

---

## 🛠️ Metodologia e Ferramentas
O projeto foi estruturado em um pipeline linear de Ciência de Dados:
1.  **Coleta e Tratamento:** Importação de múltiplos CSVs, limpeza de dados, conversão de tipos (`datetime`, `float`) e tratamento de nulos.
2.  **Feature Engineering:** Criação de métricas derivadas como `Faturamento` (Preço + Frete) e `Mês/Ano`.
3.  **Análise Exploratória (EDA):** Estudo profundo de 5 dimensões (Faturamento, Volume, Categorias, Avaliação, Logística).
4.  **Síntese de KPIs:** Consolidação dos indicadores para comparação direta.

---

## 🔎 Análise de Desempenho (Insights Chave)

### 1. Faturamento: Quem traz mais dinheiro?
A **Loja 1** é a líder indiscutível em receita, enquanto a **Loja 4** apresenta o pior desempenho financeiro da rede.

![Faturamento Total por Loja](images/faturamento_total_loja.png)

> 📉 **Insight:** A diferença de faturamento entre a melhor (Loja 1) e a pior (Loja 4) é de aproximadamente **R$ 150.000,00**.

### 2. Onde ganhamos dinheiro? (Mix de Produtos)
Apesar de "Móveis" ter um alto volume de vendas, a categoria **Eletrônicos** é a verdadeira máquina de dinheiro, representando a maior fatia da receita.

![Faturamento por Categoria](images/faturamento_por_categoria.png)

### 3. Satisfação do Cliente e Eficiência Logística
* **Qualidade:** A **Loja 3** tem a melhor avaliação média (4.05⭐). A Loja 1, apesar de faturar muito, tem a pior nota (3.98⭐), indicando possíveis dores de crescimento.
* **Custo:** A **Loja 4** tem o frete mais barato da rede, o que sugere que seu baixo faturamento não é culpa da logística, mas sim de uma baixa conversão ou ticket médio.

<div style="display: flex; gap: 10px;">
  <img src="images/avaliacao_media_loja.png" width="48%" />
  <img src="images/frete_medio_loja.png" width="48%" />
</div>

---

## 📊 Tabela Resumo de KPIs (O "Raio-X" das Lojas)

Consolidando todas as métricas, temos o cenário completo para a tomada de decisão:

| Loja | Faturamento Total | Vendas (Qtd) | Ticket Médio | Avaliação | Frete Médio |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Loja 1** | 🥇 **R$ 1.616.347,09** | 2.359 | R$ 685,18 | 3.98 (Pior) | R$ 34,69 (Maior) |
| **Loja 2** | 🥈 R$ 1.567.773,22 | 2.359 | R$ 664,59 | 4.04 | R$ 33,62 |
| **Loja 3** | 🥉 R$ 1.542.047,69 | 2.359 | R$ 653,69 | **4.05 (Melhor)** | R$ 33,07 |
| **Loja 4** | 🔻 **R$ 1.458.253,46** | 2.358 | **R$ 618,43** | 4.00 | **R$ 31,28 (Menor)** |

---

## 🎯 Recomendação Final

Com base na análise dos KPIs, a recomendação estratégica para o Sr. João é:

### **➡️ Vender a Loja 4**

#### Por que essa decisão? (Justificativa Baseada em Dados)

1.  **Menor Impacto Financeiro:** A Loja 4 é a que menos contribui para o caixa da empresa. Sua venda representa a menor perda de receita possível.
2.  **Baixa Eficiência de Venda (O Problema Oculto):**
    * A Loja 4 tem praticamente o **mesmo número de clientes** (vendas) que as outras lojas.
    * Ela tem o **frete mais barato** (o que deveria ajudar a vender mais caro).
    * Mesmo assim, ela tem o **Pior Ticket Médio**. Isso indica que ela falha em vender produtos de maior valor agregado (como Eletrônicos), operando de forma ineficiente.
3.  **Proteção dos Ativos Principais:**
    * Vender a Loja 1 seria um erro gravíssimo: ela é a "vaca leiteira" da rede. Seus problemas (frete alto e nota baixa) são operacionais e podem ser corrigidos, mas sua capacidade de gerar receita é insubstituível.

---

## 🚀 Como reproduzir este projeto

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/SEU-USUARIO/NOME-DO-REPO.git](https://github.com/SEU-USUARIO/NOME-DO-REPO.git)
    ```
2.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Execute o Notebook:**
    Abra o arquivo `notebooks/AluraStoreBrasil.ipynb` no Jupyter ou VS Code.

---
*Projeto desenvolvido como parte do portfólio de Data Science.*
