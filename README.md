## MVP da Disciplina Machine Learning &amp; Analytics - PUC Rio

**Aluno:** Leandro Ribeiro de Castro

**Data:** 20/09/2025

**Matrícula:** 4052025000159


**Projeto de Classificação de Inadimplência de Clientes de Cartão de Crédito**

**Resumo**

Este projeto de Machine Learning visa construir e avaliar modelos capazes de prever se um cliente de cartão de crédito irá se tornar inadimplente no próximo mês. Utilizando o dataset "Default of Credit Card Clients" do UCI Machine Learning Repository, o projeto aborda um problema de classificação binária, com foco em identificar clientes de risco para auxiliar em medidas preventivas.

**Metodologia**

O projeto seguiu as seguintes etapas:

**Carga e Exploração de Dados**

Carregamento do dataset e análise exploratória para compreender a estrutura, distribuição das variáveis e, crucialmente, o forte desbalanceamento da variável-alvo (inadimplência).

**Pré-processamento e Engenharia de Atributos**

Mapeamento de variáveis categóricas, criação de novas features a partir do histórico de pagamentos, faturas e pagamentos (ex: `atrasos_recorrente`, `media_atraso`, `media_faturas`, `media_pagamentos`). Padronização de variáveis numéricas e codificação One-Hot para categóricas.

Divisão do dataset em treino e teste de forma estratificada para preservar a proporção das classes.

**Modelagem e Treinamento**

Implementação de pipelines para Regressão Logística (baseline) e Random Forest Classifier.

**Otimização de Hiperparâmetros**

Utilização do GridSearchCV para ajustar os hiperparâmetros do Random Forest, visando maximizar o desempenho no conjunto de treino com validação cruzada (métrica ROC AUC).

**Avaliação e Análise de Resultados**

Métricas utilizadas: ROC AUC, Precisão, Recall e F1-Score (com foco na classe minoritária) e Matriz de Confusão, devido ao desbalanceamento.

Comparação de desempenho entre modelos padrão e otimizado no conjunto de teste.

**Principais Resultados**

O Random Forest otimizado apresentou o melhor desempenho em termos de ROC AUC (0.7667) e Precisão (0.6310) para a classe de inadimplentes. No entanto, o Recall para a classe minoritária permaneceu baixo (0.3157), indicando que o modelo ainda tem dificuldade em identificar uma parcela significativa dos clientes que inadimplirão.

**Conclusão**

O projeto demonstrou a viabilidade da previsão de inadimplência, com a Random Forest otimizada sendo a melhor solução encontrada até o momento. O desbalanceamento da classe minoritária é o principal desafio identificado, limitando o Recall. Futuras melhorias devem focar em técnicas para lidar com dados desbalanceados (como reamostragem ou ajuste de peso das classes) e na exploração de outros algoritmos para aumentar a capacidade de detecção de inadimplentes e, consequentemente, o valor para o negócio através da redução de perdas financeiras.

### Dados Complementares

Uma cópia do notebook do Google Colab e do dataset (Default of Credit Card Clients), em formato csv, encontram-se anexados a este repositório.

Link para o dataset utilizado: https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

Link para o notebook no Google Colab: https://colab.research.google.com/drive/1qlXzwmZ_pQY0ccNBps69e_9ACwF_3O__#
