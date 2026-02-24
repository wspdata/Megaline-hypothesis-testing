# Megaline — Análise de Planos e Teste de Hipóteses

## Descrição do Projeto
Projeto de análise de dados aplicado à empresa de telecomunicações Megaline. A empresa oferece dois planos pré-pagos — **Surf** e **Ultimate** — e o objetivo foi determinar qual plano gera mais receita para orientar o orçamento de publicidade. A análise foi realizada com base em dados de 500 clientes ao longo de 2018, cobrindo chamadas, mensagens e consumo de internet.

---

## Metodologia
1. **Pré-processamento dos dados**
   - Tratamento de tipos de dados (conversão de datas para datetime, correção de variáveis numéricas) e enriquecimento das tabelas com colunas derivadas (mês de referência, conversão de MB para GB).
2. **Agregação por usuário**
   - Consolidação das tabelas de chamadas, mensagens e internet em um único DataFrame por usuário e por mês, incluindo as condições de cada plano.
3. **Cálculo de receita**
   - Desenvolvimento de função personalizada para calcular a receita mensal de cada usuário, considerando o pacote incluso e as cobranças por excedente (minutos, mensagens e dados).
4. **Análise Exploratória de Dados (EDA)**
   - Análise do comportamento dos usuários por plano: consumo de minutos, mensagens e internet — com estatísticas descritivas, histogramas, gráficos de barras e boxplots.
5. **Teste de hipóteses estatísticas**
   - Teste t de Welch (bicaudal) com valor alfa de 0,05 para duas hipóteses: diferença de receita entre os planos e diferença de receita entre usuários da região NY-NJ e demais regiões.

---

## Principais Insights

- **Comportamento de uso semelhante entre planos**
  Os usuários de ambos os planos apresentam padrões de consumo parecidos em chamadas, mensagens e internet — sem diferenças expressivas no volume de uso.

- **Plano Ultimate gera mais receita por cliente**
  Apesar de o plano Surf concentrar mais usuários, a receita média por cliente é maior no plano Ultimate. O teste de hipótese confirmou diferença estatisticamente significativa na receita média entre os dois planos (*p-valor < 0,05*), levando à rejeição da hipótese nula.
  *Recomendação:* Direcionar maior investimento em publicidade para o plano Ultimate pode ser a estratégia mais eficiente para maximizar receita.

- **Receita menor na região NY-NJ**
  O segundo teste de hipótese identificou diferença estatisticamente significativa (*p-valor < 0,05*) entre a receita dos clientes de NY-NJ e das demais regiões — com NY-NJ gerando, em média, menos receita.

---

## 📂 Conteúdo do Repositório

- **Notebook (.ipynb):** análise completa, incluindo pré-processamento, EDA, cálculo de receita, testes de hipótese e conclusões
- **README (.md):** Este arquivo.

---

## Tecnologias e Bibliotecas
- Linguagem: **Python**
- Bibliotecas: **pandas**, **numpy**, **matplotlib**, **seaborn**, **scipy**
- Notebook: **Jupyter Notebook**

---

## Contato

Willian De Souza Pereira — ws13292@gmail.com

LinkedIn: https://linkedin.com/in/willian-de-souza-pereira-b69109202

## Licença

Este repositório está disponível para estudo e demonstração. Sinta-se à vontade para clonar, adaptar e abrir *issues* com dúvidas ou sugestões.
