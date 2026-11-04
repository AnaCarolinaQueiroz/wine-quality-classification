# Wine Quality Classification

Classificação da qualidade de vinhos com Machine Learning a partir de características físico-químicas.

> **Status:** em andamento. As seções de resultados e entregáveis serão atualizadas conforme o projeto avança.

## Contexto e Objetivo

A avaliação da qualidade de vinhos é tradicionalmente realizada por especialistas por meio de análises sensoriais, um processo que pode ser subjetivo, demorado e dependente da experiência dos avaliadores. Com o auxílio de técnicas de Ciência de Dados e Machine Learning, é possível utilizar características físico-químicas medidas durante a produção para prever a qualidade final do vinho e apoiar a tomada de decisão no processo produtivo.

**Objetivo:** construir e comparar modelos de classificação binária capazes de categorizar vinhos em:

- **Alta Qualidade:** nota de qualidade maior ou igual a 7
- **Baixa/Média Qualidade:** nota de qualidade menor que 7

**Pergunta que orienta a análise:**

É possível prever, a partir de características físico-químicas, se um vinho será de alta qualidade, e quais dessas características mais influenciam essa classificação?

## Dataset

- **Fonte:** [Wine Quality Dataset (Kaggle)](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)
- **Variável alvo:** `quality`, transformada em classe binária (1 para alta qualidade, 0 para baixa/média qualidade)

| Variável | Descrição |
|---|---|
| `fixed acidity` | Acidez fixa |
| `volatile acidity` | Acidez volátil |
| `citric acid` | Ácido cítrico |
| `residual sugar` | Açúcar residual |
| `chlorides` | Cloretos |
| `free sulfur dioxide` | Dióxido de enxofre livre |
| `total sulfur dioxide` | Dióxido de enxofre total |
| `density` | Densidade |
| `pH` | Nível de acidez ou basicidade |
| `sulphates` | Sulfatos |
| `alcohol` | Teor alcoólico |
| `quality` | Nota de qualidade atribuída por especialistas |

## Estrutura do Projeto

```text
wine-quality-classification/
│
├── data/            Base de dados utilizada
├── notebooks/       Notebook com a análise exploratória e a modelagem
├── src/             Scripts auxiliares (pré-processamento e modelagem)
├── results/         Gráficos e métricas dos modelos
├── requirements.txt Bibliotecas utilizadas
└── README.md        Descrição do projeto
```

## Metodologia

1. **Compreensão do problema:** interpretação do contexto, definição da variável alvo e transformação da nota de qualidade em classificação binária.
2. **Análise exploratória dos dados (EDA):** distribuição das variáveis, correlações, detecção de outliers e análise do balanceamento das classes.
3. **Pré-processamento:** tratamento de dados faltantes, padronização das variáveis numéricas e engenharia de atributos.
4. **Modelagem:** treinamento e comparação de ao menos dois modelos de classificação, com divisão estratificada entre treino e teste para preservar a proporção das classes.
5. **Avaliação:** comparação dos modelos com métricas adequadas a classes desbalanceadas (precisão, recall, F1-score e ROC-AUC), e não apenas acurácia.
6. **Interpretação:** identificação das variáveis de maior influência na qualidade e discussão das implicações para o processo de produção.

## Tecnologias Utilizadas

- **Linguagem:** Python
- **Manipulação de dados:** Pandas, NumPy
- **Visualização:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn
- **Ambiente:** Jupyter Notebook

Os modelos de classificação serão definidos ao longo do desenvolvimento.

## Resultados

Em andamento. Esta seção apresentará os principais insights da análise exploratória, a comparação de desempenho entre os modelos e as variáveis mais influentes na qualidade dos vinhos.

## Como Executar

### 1. Clonar o repositório

```bash
git clone https://github.com/AnaCarolinaQueiroz/wine-quality-classification.git
cd wine-quality-classification
```

### 2. Criar e ativar um ambiente virtual (recomendado)

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/macOS
source .venv/bin/activate
```

### 3. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 4. Executar os notebooks

Certifique-se de que a base de dados está na pasta `data/` e abra os notebooks disponíveis na pasta `notebooks/`.

```bash
jupyter notebook notebooks/
```
