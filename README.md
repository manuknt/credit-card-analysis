# Análise de Aprovação de Cartão de Crédito

## Sobre o projeto

Este projeto tem como objetivo analisar os fatores associados à aprovação de solicitações de cartão de crédito e desenvolver modelos de classificação capazes de prever a aprovação com base nas características dos solicitantes.

O trabalho foi desenvolvido com Python, utilizando análise exploratória de dados, preparação de variáveis e algoritmos de aprendizado de máquina.

## Objetivos

- Explorar o perfil dos solicitantes.
- Investigar relações entre características financeiras e aprovação.
- Preparar os dados para modelagem.
- Treinar e comparar modelos de classificação.
- Avaliar o desempenho dos modelos utilizando métricas apropriadas.

## Estrutura do projeto

```text
credit-card-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_exploracao.ipynb
│   ├── 02_limpeza_preparacao.ipynb
│   └── 03_modelagem.ipynb
│
├── Dashboard/
├── sql/
├── README.md
└── requirements.txt
```

## Etapas desenvolvidas

### 1. Análise exploratória

- Análise da distribuição de aprovações e reprovações.
- Investigação de variáveis financeiras e características dos solicitantes.
- Identificação de padrões e possíveis relações com a aprovação.

### 2. Limpeza e preparação

- Verificação de valores ausentes e registros duplicados.
- Análise de redundância entre variáveis.
- Seleção de seis variáveis preditoras.
- Separação da variável-alvo.
- Preparação da base para modelagem.

### 3. Modelagem preditiva

Foram utilizados dois algoritmos:

- Regressão Logística.
- Árvore de Decisão.

A divisão dos dados foi realizada em treinamento (80%) e teste (20%), utilizando estratificação da variável-alvo.

## Resultados dos modelos

| Métrica | Regressão Logística | Árvore de Decisão |
|---|---:|---:|
| Acurácia | 0.7852 | 0.7481 |
| Precisão | 0.8261 | 0.7907 |
| Recall | 0.6441 | 0.5763 |
| F1-Score | 0.7238 | 0.6667 |
| ROC-AUC | 0.8182 | 0.8015 |

A Regressão Logística apresentou os melhores resultados nas cinco métricas avaliadas, demonstrando desempenho superior à Árvore de Decisão neste experimento.

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Limitações e considerações

- O conjunto de dados possui 672 registros, sendo relativamente pequeno.
- Não há documentação completa para interpretar todos os códigos das variáveis categóricas.
- Algumas variáveis foram excluídas por redundância, falta de documentação ou necessidade de cuidados relacionados à privacidade e à equidade.
- Os resultados representam um experimento exploratório e não devem ser utilizados diretamente para decisões reais de concessão de crédito.
- O desempenho foi avaliado em uma única divisão entre treinamento e teste.

## Conclusão

A análise permitiu identificar associações entre características financeiras dos solicitantes e a aprovação de crédito.

Entre os modelos avaliados, a Regressão Logística apresentou melhor desempenho geral, alcançando acurácia de 78,52% e ROC-AUC de 0,8182.

O projeto demonstra um fluxo completo de análise de dados, desde a exploração e preparação até a construção e avaliação de modelos preditivos.

## Autor

Projeto desenvolvido para fins de estudo e construção de portfólio em Ciência de Dados e Machine Learning.
