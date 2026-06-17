# ProjetoChurn

# Projeto de Previsão de Churn - Telco Customer

Este repositório contém o projeto final da disciplina de Introdução ao Aprendizado de Máquina (CMPINAM). O objetivo é analisar o comportamento dos clientes de uma empresa de telecomunicações e desenvolver modelos capazes de prever o cancelamento dos serviços (Churn), permitindo ações preventivas de retenção.

## Integrante
* Natasha Sales Ferreira Pinto (CP3025799)

## Problema
O Churn (taxa de rotatividade) é uma métrica crítica que representa a perda de clientes. Neste projeto, foi analisado o comportamento dos clientes da empresa Telco para identificar fatores associados ao cancelamento e construir modelos preditivos capazes de antecipar esse evento.

## Dataset
Os dados foram obtidos originalmente na plataforma [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). 
A base contém 7.032 registros e 20 atributos após a limpeza inicial, cobrindo dados demográficos, serviços contratados e informações financeiras.

## Parte 1 - Análise Exploratória de Dados (EDA)
**Principais Achados da EDA**
**Contratos:** Clientes com contratos mensais ("Month-to-month") representam a maioria dos casos de churn.
**Tempo de Casa:** O risco de cancelamento é mais elevado nos primeiros 12 meses.
**Fatura Mensal:** Clientes com cobranças entre US$70 e US$100 apresentam maior tendência ao cancelamento.
**Tecnologia:** Usuários de Fibra Óptica possuem maior índice de churn em comparação aos clientes de DSL.
**Serviços Adicionais:** A ausência de suporte técnico está fortemente associada ao cancelamento.

## Parte 2 - Modelagem e Avaliação
**Objetivo:** Desenvolver modelos de classificação supervisionada capazes de prever se um cliente irá cancelar os serviços da empresa, permitindo ações proativas de retenção.

**Preparação dos Dados:**
1. Divisão dos dados em treino (80%) e teste (20%);
2. Separação estratificada da variável-alvo;
3. Aplicação de One-Hot Encoding para variáveis categóricas;
4. Padronização das variáveis numéricas com StandardScaler;
5. Balanceamento das classes utilizando SMOTE;
6. Cuidados para evitar Data Leakage.
   
**Modelos Utilizados**
**Regressão Logística (Baseline):** Modelo linear utilizado como referência inicial, oferecendo alta interpretabilidade e rapidez no treinamento.

**Árvore de Decisão:** Capaz de capturar relações não lineares entre as variáveis e fornecer regras de decisão facilmente interpretáveis.

**Random Forest (Ensemble):** Modelo baseado em múltiplas árvores de decisão, proporcionando maior robustez e melhor capacidade de generalização.

**Métricas Avaliadas:**
- Acurácia
- Precisão
- Recall (Sensibilidade)
- F1-Score
- Matriz de Confusão

**Principais Resultados:**
- A Regressão Logística apresentou alto recall, identificando boa parte dos clientes propensos ao cancelamento, porém com maior quantidade de falsos positivos.
- A Árvore de Decisão obteve desempenho intermediário.
- O Random Forest apresentou o melhor equilíbrio entre Precisão e Recall, obtendo o maior F1-Score e sendo considerado o modelo mais adequado para aplicação prática.
  
**Possíveis Melhorias Futuras:**
- Otimização de hiperparâmetros utilizando GridSearchCV ou RandomizedSearchCV;
- Engenharia de atributos (Feature Engineering);
- Inclusão de variáveis comportamentais, como histórico de reclamações, consumo de serviços e qualidade da conexão.


## Como Executar o Notebook
1. Abra o arquivo `.ipynb` e importe no [Google Colab](https://colab.research.google.com/).
2. Certifique-se de que o arquivo `.csv` está na mesma pasta que o notebook antes de rodar as células.

