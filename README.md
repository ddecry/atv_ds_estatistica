# Atividade 2 – Compreensão Aprofundada dos Dados

**Bacharelado em Engenharia de Software**  
**Disciplina:** Ciência de Dados  
**Base de Dados:** Board Games Dataset Complete Features

## Objetivo
Explorar e analisar dados do dataset de jogos de tabuleiro, aplicando estatística descritiva, tratamento de dados ausentes e outliers, visualizações, análise de correlação e estudo temporal.

## Etapas Realizadas

### A. Estatística Descritiva e Exploração Inicial
- Carregado o dataset `boardgame-geek-dataset_organized.csv` em um DataFrame do Pandas.
- Verificadas as 5 primeiras linhas e os tipos de dados de cada coluna com `info()`.
- Geradas estatísticas descritivas com `describe()` para colunas numéricas como `average_rating` e `playing_time`.
- **Resultados:**
  - Nota média de um jogo: **aproximadamente 6.22**.
  - Tempo médio de jogo: **~88 minutos**, desvio padrão: **~77 minutos**.
  - Algumas colunas possuem valores nulos, destacando `average_rating`, que poderia impactar análises futuras.

### B. Tratamento de Dados Ausentes e Outliers
- Valores nulos na coluna `average_rating` foram preenchidos com a **mediana**, pois a mediana é menos sensível a valores extremos do que a média.
- Boxplot criado para visualizar `playing_time` e identificar outliers.
- Cálculo do IQR mostrou a quantidade de jogos com tempos atípicos de jogo.

### C. Visualização e Transformação de Dados
- Criado histograma para `average_rating` mostrando distribuição **assimétrica à direita**.
- Aplicada transformação logarítmica em `playing_time` para reduzir assimetria e facilitar análise.
- Comparação entre histogramas mostrou que a transformação logarítmica suaviza a cauda longa dos tempos de jogo.

### D. Análise da Relação entre Variáveis
- Scatter plot de `min_players` x `max_players` mostrou tendência positiva: jogos com mais jogadores mínimos tendem a ter mais jogadores máximos.
- Matriz de correlação e heatmap revelaram:
  - **Maior correlação positiva:** `min_players` x `max_players`.
  - **Correlação mais próxima de zero:** `average_rating` x `playing_time`.

### E. Análise Temporal
- Criada coluna `Decada` para agrupar jogos por década de publicação.
- Contagem de jogos por década mostrou tendência de aumento de lançamentos ao longo do tempo.
- **Década com mais lançamentos:** 2010, com **1.245 jogos** lançados.

## Ferramentas Utilizadas
- Python 3
- Pandas, Numpy
- Matplotlib, Seaborn

## Conclusão
A análise permitiu compreender melhor as características do dataset de jogos de tabuleiro, identificar padrões, tratar dados ausentes e outliers, visualizar relações entre variáveis e analisar tendências temporais de lançamentos.
