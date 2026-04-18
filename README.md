# ProjetoChurn

# Projeto de Previsão de Churn - Telco Customer

Este repositório contém a Parte 1 do projeto final da disciplina de Introdução ao Aprendizado de Máquina (CMPINAM). O objetivo desta etapa é realizar uma Análise Exploratória de Dados (EDA) profunda sobre o cancelamento de clientes em uma empresa de telecomunicações.

## Integrante
* Natasha Sales Ferreira Pinto (CP3025799)

## Problema
O Churn (taxa de rotatividade) é uma métrica crítica que indica a perda de clientes. Neste projeto, foi analisado o comportamento de clientes da empresa Telco para identificar padrões que levam ao cancelamento do serviço, permitindo ações preventivas de retenção.

## Dataset
Os dados foram obtidos originalmente na plataforma [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). 
A base contém 7.032 registros e 20 atributos após a limpeza inicial, cobrindo dados demográficos, serviços contratados e informações financeiras.

## Principais Achados da EDA
A análise revelou pontos cruciais sobre a evasão de clientes:
1. **Contratos:** Clientes com contratos mensais ("Month-to-month") representam a vasta maioria do churn.
2. **Tempo de Casa:** O risco de cancelamento é crítico nos primeiros 12 meses de contrato.
3. **Fatura Mensal:** Clientes com cobranças entre $70 e $100 tendem a sair mais do que clientes de faixas menores.
4. **Tecnologia:** Notou-se um índice de churn elevado em usuários de Fibra Óptica em comparação ao DSL.
5. **Serviços Adicionais:** A ausência de suporte técnico está fortemente correlacionada ao cancelamento.

## Como Executar o Notebook
1. Abra o arquivo `.ipynb` e importe no [Google Colab](https://colab.research.google.com/).
2. Certifique-se de que o arquivo `.csv` está na mesma pasta que o notebook antes de rodar as células.
