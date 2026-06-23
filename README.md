# 🌳 Semana 11 – Árvores de Decisão vs Random Forest

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-green.svg)](https://scikit-learn.org/)

## 📋 Sobre o Projeto

Este notebook faz parte do curso de **Machine Learning** e tem como objetivo comparar o desempenho de dois modelos de classificação:

- **Árvore de Decisão** (`DecisionTreeClassifier`)
- **Random Forest** (`RandomForestClassifier`)

O dataset utilizado contém informações de **clientes** (idade, renda, histórico de compras, tempo desde a última compra) e o objetivo é prever se um cliente vai **comprar** ou **não comprar** um produto.

---

## 🎯 Resultados Principais

| Modelo | Melhor Acurácia |
|--------|-----------------|
| Árvore de Decisão | **87.50%** (max_depth=5) |
| Random Forest | **92.50%** (n_estimators=25) |

### 📊 Evolução da Árvore por Profundidade

| max_depth | Acurácia |
|-----------|----------|
| 2 | 77.00% |
| 3 | 86.00% |
| **5** | **87.50%** |
| 10 | 86.00% |
| 15 | 86.50% |
| 20 | 86.50% |
| Sem limite | 86.50% |

### 📊 Evolução da Random Forest por Número de Árvores

| n_estimators | Acurácia |
|--------------|----------|
| 10 | 91.00% |
| **25** | **92.50%** |
| 50 | 92.00% |
| 100 | 91.50% |
| 200 | 91.50% |
| 500 | 91.50% |

---

## Conclusão

Para este problema de previsão de compra de clientes, **a Random Forest teve um desempenho superior**, com uma diferença de **5 pontos percentuais** em relação à árvore individual.

### Motivos para escolher a Random Forest:
1. Melhor acurácia (92.50%)
2. Maior estabilidade
3. Baixo custo computacional com 25 árvores
4. Permite análise de importância das variáveis

> 💡 Se a interpretabilidade for mais importante que a acurácia, a Árvore de Decisão com max_depth=5 é uma boa alternativa.

---

## Tecnologias Utilizadas

- **Python 3.8+**
- **Jupyter Notebook**
- **Pandas** – Manipulação de dados
- **NumPy** – Operações matemáticas
- **Scikit-learn** – Modelos de Machine Learning
- **Matplotlib** – Visualização de dados

---

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/semana11-arvores-vs-random-forest.git
cd semana11-arvores-vs-random-forest
```

### 2. Crie um ambiente virtual (opcional, mas recomendado)
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate     # Windows
```

### 3. Instale as dependências
```bash
pip install -r requirements.txt
```

### 4. Execute o Jupyter Notebook
```bash
jupyter notebook arvores.ipynb
```

## 📊 Visualizações Geradas
O notebook gera automaticamente os seguintes gráficos:

1. Evolução da Acurácia da Árvore de Decisão por profundidade
2. Evolução da Acurácia da Random Forest por número de árvores
3. Importância das Variáveis para o modelo Random Forest

## 📚 Aprendizados
- Árvores de Decisão são intuitivas e interpretáveis, mas podem sofrer com overfitting
- Random Forest combina múltiplas árvores para reduzir overfitting e melhorar a acurácia
- O número de árvores na floresta tem um ponto de retorno decrescente
- A profundidade da árvore deve ser controlada para evitar overfitting
- A importância das variáveis ajuda a entender quais fatores mais influenciam a decisão de compra

## 📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## 👩‍💻 Autora
Kailayni Janez
