---
title: Machine Learning Fundamentals
description: Fundamentos do aprendizado de máquina e tipos de algoritmos
duration: 60 min
difficulty: intermediate
showImages: true
showVideos: true
showReferences: true
videos:
  - title: "Machine Learning Explained"
    url: "https://www.youtube.com/watch?v=ukzFI9rgwfU"
  - title: "Supervised vs Unsupervised Learning"
    url: "https://www.youtube.com/watch?v=cfj6yaYE86U"
materials:
  - nome: "Guia Prático de ML"
    link: "../assets/pdfs/guia-ml.pdf"
  - nome: "Dataset Iris para Prática"
    link: "../assets/datasets/iris.csv"
  - nome: "Jupyter Notebook - Exemplos"
    link: "../assets/notebooks/ml-examples.ipynb"
  - nome: "Scikit-learn Documentation"
    link: "https://scikit-learn.org/stable/"
---

# Machine Learning Fundamentals

O **Machine Learning (ML)** é um subcampo da Inteligência Artificial que foca no desenvolvimento de algoritmos que podem aprender e fazer previsões ou decisões baseadas em dados, sem serem explicitamente programados para cada tarefa específica.

## O que é Machine Learning?

Tradicionalmente, na programação convencional, escrevemos regras específicas para resolver problemas. No Machine Learning, fornecemos dados e resultados esperados para que o algoritmo descubra as regras por si mesmo.

### Programação Tradicional vs Machine Learning

**Programação Tradicional:**
```
Dados + Programa → Resultado
```

**Machine Learning:**
```
Dados + Resultado → Programa (Modelo)
```

## Tipos de Machine Learning

### 1. Aprendizado Supervisionado (Supervised Learning)

No aprendizado supervisionado, o algoritmo aprende com dados rotulados - ou seja, temos tanto os dados de entrada quanto as respostas corretas.

#### Características:
- Dados de treinamento incluem **features** (características) e **labels** (rótulos)
- Objetivo: prever labels para novos dados
- Duas categorias principais: **Classificação** e **Regressão**

#### Exemplos de Algoritmos:
* **Regressão Linear**: Para prever valores contínuos
* **Árvores de Decisão**: Para classificação e regressão
* **Random Forest**: Conjunto de árvores de decisão
* **Support Vector Machines (SVM)**: Para classificação e regressão
* **Naive Bayes**: Para classificação probabilística

![Supervised Learning](../assets/imagens/img1.jpg)

### 2. Aprendizado Não Supervisionado (Unsupervised Learning)

No aprendizado não supervisionado, o algoritmo trabalha apenas com dados de entrada, sem rótulos ou respostas corretas conhecidas.

#### Características:
- Apenas dados de entrada, sem respostas esperadas
- Objetivo: descobrir padrões ocultos nos dados
- Principais tipos: **Clustering** e **Redução de Dimensionalidade**

#### Exemplos de Algoritmos:
* **K-Means**: Agrupamento em clusters
* **Hierarchical Clustering**: Clustering hierárquico
* **PCA (Principal Component Analysis)**: Redução de dimensionalidade
* **DBSCAN**: Clustering baseado em densidade

### 3. Aprendizado por Reforço (Reinforcement Learning)

No aprendizado por reforço, um agente aprende através de interações com um ambiente, recebendo recompensas ou punições por suas ações.

#### Características:
- Baseado em **tentativa e erro**
- Agente busca maximizar recompensas
- Não há dados de treinamento pré-definidos

#### Aplicações:
* Jogos (AlphaGo, xadrez)
* Robótica
* Carros autônomos
* Sistemas de recomendação

## Processo de Machine Learning

### 1. Coleta e Preparação dos Dados
- Coleta de dados relevantes
- Limpeza e tratamento de dados faltantes
- Normalização e transformação dos dados

### 2. Exploração dos Dados (EDA)
- Análise estatística descritiva
- Visualização dos dados
- Identificação de padrões e correlações

### 3. Seleção de Features
- Identificar características mais relevantes
- Reduzir dimensionalidade quando necessário
- Evitar overfitting

### 4. Escolha do Algoritmo
- Considerar o tipo de problema (classificação, regressão, clustering)
- Avaliar o tamanho e tipo dos dados
- Considerar requisitos de performance

### 5. Treinamento do Modelo
- Dividir dados em treino e teste
- Treinar o algoritmo com dados de treino
- Ajustar hiperparâmetros

### 6. Avaliação do Modelo
- Testar com dados não vistos
- Calcular métricas de performance
- Validar generalização do modelo

### 7. Deploy e Monitoramento
- Colocar modelo em produção
- Monitorar performance ao longo do tempo
- Retreinar quando necessário

## Principais Métricas de Avaliação

### Para Classificação:
* **Acurácia**: Proporção de previsões corretas
* **Precisão**: Proporção de positivos verdadeiros entre previsões positivas
* **Recall**: Proporção de positivos verdadeiros identificados
* **F1-Score**: Média harmônica entre precisão e recall

### Para Regressão:
* **MSE (Mean Squared Error)**: Média dos erros quadráticos
* **RMSE (Root Mean Squared Error)**: Raiz quadrada do MSE
* **MAE (Mean Absolute Error)**: Média dos erros absolutos
* **R² (Coeficiente de Determinação)**: Proporção da variância explicada

## Problemas Comuns em ML

### Overfitting
O modelo "decora" os dados de treino mas não generaliza bem para novos dados.

**Soluções:**
- Usar mais dados de treinamento
- Aplicar regularização
- Usar validação cruzada
- Simplificar o modelo

### Underfitting
O modelo é muito simples e não consegue capturar os padrões dos dados.

**Soluções:**
- Usar modelos mais complexos
- Adicionar mais features
- Reduzir regularização

### Dados Insuficientes
Não há dados suficientes para treinar o modelo adequadamente.

**Soluções:**
- Coletar mais dados
- Data augmentation
- Transfer learning
- Usar modelos mais simples

## Bibliotecas Populares

### Python
* **Scikit-learn**: Biblioteca geral para ML
* **TensorFlow**: Framework para deep learning
* **PyTorch**: Framework para deep learning
* **Pandas**: Manipulação de dados
* **NumPy**: Computação numérica

### R
* **Caret**: Classificação e regressão
* **RandomForest**: Florestas aleatórias
* **e1071**: SVM e outras técnicas

## Exemplo Prático: Classificação de Flores

Vamos considerar o famoso dataset Iris, que contém medições de flores e suas espécies:

1. **Problema**: Classificar espécies de flores baseado em medições
2. **Dados**: 150 amostras com 4 características cada
3. **Algoritmo**: Árvore de Decisão
4. **Resultado**: Modelo capaz de classificar novas flores

Este exemplo demonstra um problema de classificação supervisionada típico.

## Considerações Éticas em ML

* **Viés nos Dados**: Dados podem refletir preconceitos sociais
* **Transparência**: Modelos complexos podem ser "caixas-pretas"
* **Responsabilidade**: Quem é responsável pelas decisões do modelo?
* **Privacidade**: Como proteger dados sensíveis dos usuários?

> "Machine Learning é como uma receita de bolo: você precisa dos ingredientes certos (dados), seguir o processo correto (algoritmo) e ter a experiência para ajustar quando necessário." - Anonymous Data Scientist

## Resumo dos Conceitos-Chave

- **Supervised Learning**: Aprende com dados rotulados
- **Unsupervised Learning**: Descobre padrões em dados sem rótulos
- **Reinforcement Learning**: Aprende através de recompensas e punições
- **Overfitting**: Modelo muito complexo que não generaliza
- **Cross-validation**: Técnica para avaliar generalização do modelo
- **Feature Engineering**: Processo de criar e selecionar características relevantes

## Próximos Passos

No próximo módulo, mergulharemos no **Deep Learning e Redes Neurais**, explorando como essas técnicas revolucionaram o campo da IA e permitiram avanços impressionantes em áreas como visão computacional e processamento de linguagem natural.

## Referências

- James, G.; Witten, D.; Hastie, T.; Tibshirani, R. (2021). *An Introduction to Statistical Learning with Applications in R*. 2ª edição. Springer.
- Hastie, T.; Tibshirani, R.; Friedman, J. (2017). *The Elements of Statistical Learning*. 2ª edição. Springer.
- Géron, A. (2019). *Hands-On Machine Learning with Scikit-Learn and TensorFlow*. 2ª edição. O'Reilly Media.
- Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*. Springer.
- Pedregosa, F. et al. (2011). "Scikit-learn: Machine Learning in Python". *Journal of Machine Learning Research*, 12, 2825-2830.